## Test environments

* macOS (latest) — R release
* Windows (latest) — R release
* Ubuntu 22.04 — R release, R devel

All checks run via GitHub Actions.

## R CMD check results

0 errors | 0 warnings | 1 note

## Additional local pre-submission checks (March 13, 2026)

* macOS Tahoe 26.3.1 — R 4.5.3
* `devtools::run_examples(run_donttest = TRUE)`: clean after refreshing examples and manuals
* `R CMD check factoextra_2.0.0.999.tar.gz`: 0 errors | 0 warnings | 0 notes
* `R CMD check --as-cran factoextra_2.0.0.999.tar.gz`: 0 errors | 0 warnings | 1 note

The remaining `--as-cran` note is environment-specific:

* `unable to verify current time`

## Major version bump

This is a major update (1.0.7 → 2.0.0). The last CRAN release was in April 2020. Key changes include:

* Replaced deprecated tidyr internals with base R (`stats::reshape()`)
* Updated Hopkins statistic to use corrected formula (Wright 2022)
* Added parallel analysis support in `fviz_eig()`
* Replaced deprecated ggplot2 functions (`aes_string()`, `stat()`, `guide_legend(override.aes)`)
* Added comprehensive test suite (113 tests via testthat)
* Fixed documentation issues (lost braces, bare URLs, missing `\value` tags)
* Raised the plotting-stack support floor to `R >= 4.5.0`,
  `ggplot2 >= 4.0.0`, and `ggrepel >= 0.9.7`

## Resubmission

This is a resubmission. In this version I have:

* Added a note about `datanovia.com` URLs returning HTTP 503 to automated
  crawlers. The URLs are valid and accessible in a browser; the server
  returns 503 to automated crawlers. This affects URLs in DESCRIPTION,
  README.md, and man/*.Rd files.
* Removed the Ubuntu `oldrel-1` CI workaround that pinned `ggrepel` to
  `0.9.5`, because the current development baseline now requires
  `R >= 4.5.0`.

## Downstream dependencies

Checked reverse dependencies. All packages that could be installed passed R CMD check.
