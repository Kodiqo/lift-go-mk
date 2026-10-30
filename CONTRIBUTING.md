# Contributing

1. Fork or branch from `main`.
2. Install with `npm ci` and run `npm run dev`.
3. Before opening a pull request run `npm run lint`, `npm run format:check` and
   `npm run build` (content validation, type check and static build).
4. For layout changes run the checks in `scripts/` (`npm run test:responsive`,
   `npm run test:seo`, etc.; Python 3 required for most of them).
5. Site copy is Macedonian and lives in `src/content/site.json`.

Commit messages: short imperative summary, e.g. `Fix iPhone image loading`.
