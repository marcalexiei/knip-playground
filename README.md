# knip-playground

Minimal pnpm monorepo reproducing a knip bug (knip 6.32.2, pnpm 11.21.0):
valid pnpm subcommands are reported as unlisted binaries.

```sh
pnpm install
pnpm exec knip
```

Expected no findings, got:

```text
Unlisted binaries (3)
create  .github/actions/nested/action.yml
info    .github/workflows/ci.yml
view    packages/a/package.json
```
