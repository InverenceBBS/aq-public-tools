# aq-public-tools
Public tools as images or documentation

## This repository is public and hot-linked from production

- It is a **public** GitHub repository (`InverenceBBS/aq-public-tools`, GPLv3). Never commit
  anything private: credentials, client data, internal reports or unpublished material.
- The production dashboards and reports load files from it **directly** (no copy), so moving,
  renaming or deleting a linked path, or rewriting history, breaks logos, the footer and the user
  manual images on the live sites.
- Always work on `main` (no feature branches): the dashboard links follow `refs/heads/main`.

## Paths linked from production

| Path | Linked from | How |
|---|---|---|
| `img/Logo-Inverence-N_T-Ajustado.webp` | `aq-shiny-report/aq_dashboard/aq_dashboard_ui.R`, `aq_dashboard_server_init.R` (footer) | `raw.githubusercontent.com/.../refs/heads/main/` |
| `img/llull-environment/llull_environment_verde.png` | `aq-shiny-report/aq_dashboard/aq_dashboard_server_init.R` (header logo) | `github.com/.../blob/main/...?raw=true` |
| `img/llull-environment/*.png`, `*.gif` and `img/socaire/*` | `aq-shiny-report/aq_dashboard/user-manual-llull-environment.md`, `user-manual-socaire.md` | `github.com/.../blob/main/...?raw=true` |
| `img/llull-environment/cities/*` | `config.def_city_eea.tx_url_img1` / `tx_url_img2` (per-city logos, e.g. Vilnius) | `raw.githubusercontent.com/.../<commit>/...` (pinned to a commit) |
| `img/aq-report-forecast-dygraph-legend.png` | `aq-shiny-report/aq_session_report-*.Rmd` | local checkout `/code/aq/aq-public-tools/` |

Before removing or renaming any file, search for it in `aq-shiny-report` and in
`config.def_city_eea` (`tx_url_img1`, `tx_url_img2`, `tx_url_ref1`, `tx_url_ref2`, `tx_url_footer`).
