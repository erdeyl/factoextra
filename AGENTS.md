# Codex Repo Guidance

This CRAN-style R package repo can invoke the global skill library in `/Users/erdeylaszlo/.codex/skills`.

## Prefer these global skills

- `$stat-dev` for R package code, roxygen comments, tests, examples, vignettes, dependency issues, and cross-package compatibility work.
- `$audit` / `$update` for whole-repo review and fixes.
- `$audit-pr` / `$update-pr` for pull request review and remediation.
- `$gh-fix-ci`, `$gh-address-comments`, and `$tidy-up` for GitHub workflow tasks.
- `$long-document-context` for large `README.Rmd`, NEWS files, or long R sources.
- `$doc` and `$pdf` only when the task is specifically about rendered documentation artifacts.

## Repo notes

- Preserve CRAN-style package structure: `DESCRIPTION`, `NAMESPACE`, `R/`, `man/`, and tests must remain consistent.
- Prefer editing source files such as `README.Rmd` and roxygen comments rather than generated outputs when the repo already follows that pattern.
