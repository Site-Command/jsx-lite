# JSX-Lite CLI

A CLI for jsx-lite.

## Installation

```bash
npm install -g @jsx-lite/cli
```

## Usage

```bash
jsx-lite --to=<format> < <input-file>
cat my-file.tsx | jsx-lite -t=<format>
jsx-lite -t=<format> <input-file>
```

Check the output from `jsx-lite --help`.

**Examples**

```bash
jsx-lite -t react component.tsx
jsx-lite -t react < component.tsx
cat component.tsx | jsx-lite -t html -
jsx-lite -t react --out-dir build -- src/**/*.tsx
```

## Options

Supported formats for `--to` are:

- `reactNative`
- `solid`
- `vue`
- `react`
- `template`
- `html`
- `customElement`
- `jsxLite`
- `builder`
- `swift`
- `svelte`
- `liquid`
- `angular`

## Known issues

- Running `jsx-lite` from the root of this repository breaks due to some
  dynamic babel configuration look up
- Files that are created as the result of `--out-dir=<dir>` maintain the original
  file extension of the input file, which doesn't make any sense in the case of
  an html output.
- `--out=<file>` does not support concatenating multiple files together.

## Manual installation

```bash
git clone git@github.com:BuilderIO/jsx-lite.git
cd jsx-lite/packages/cli
npm install
npm run build
npm link
```
# License

MIT - see LICENSE
