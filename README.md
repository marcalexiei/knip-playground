# knip-playground

Minimal pnpm monorepo reproducing a knip false positive (knip 6.48.0, sass
1.108.2): stylesheets and packages loaded with Sass `meta.load-css()` are
reported as unused.

```sh
pnpm install
pnpm build
pnpm exec knip
```

`pnpm build` shows that Sass loads both stylesheets from
`packages/app/src/main.scss`.

Expected no findings, got:

```text
Unused files (1)
packages/app/src/_partial.scss
Unused dependencies (1)
@playground/styles  packages/app/package.json:10:6
```
