---
"@pnpm/installing.deps-installer": patch
"pnpm": patch
---

Running `pnpm install` with `--ignore-pnpmfile` no longer removes `pnpmfileChecksum` from the lockfile or triggers a full resolution. The flag is meant to temporarily skip the pnpmfile (e.g. for tools like Renovate that combine it with `--ignore-scripts`) and shouldn't mutate the lockfile's recorded pnpmfile state [#10944](https://github.com/pnpm/pnpm/issues/10944).
