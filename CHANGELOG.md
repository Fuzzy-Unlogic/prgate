# Changelog

## 1.1.2

### Dependencies
- Bump `minimatch` from 10.2.6 to 11.0.9 (includes the fix for GHSA-cf2h-pxjq-68xw). Matching behaviour for the `dot: true` globs prgate uses is unchanged.
- Bump dev dependencies: `@biomejs/biome` 2.6.2 → 2.6.8, `vitest` 5.0.5 → 5.1.1, `vite` 8.3.5 → 8.3.8.

## 1.1.0

### Security
- On `pull_request` events the guardrails config is now loaded from the PR base sha through the GitHub API instead of the checked-out tree, closing a self-bypass where a PR could empty `protected` in its own config. An `actions/checkout` step is no longer required.
