---
"pnpm": patch
---

`pnpm clean`: renamed the `--lockfile` flag to `--include-lockfile` (short alias `-l`). The previous flag name collided with the global `lockfile` setting (which controls whether a lockfile is created during install, default `true`). When that setting was present in `pnpm-workspace.yaml` or `.npmrc`, `pnpm clean` would unintentionally delete `pnpm-lock.yaml` even without the flag being passed [#11420](https://github.com/pnpm/pnpm/issues/11420).
