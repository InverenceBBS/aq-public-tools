# aq-public-tools
Herramientas públicas en forma de imágenes o documentación

## Este repositorio es público y producción lo enlaza en caliente

- Es un repositorio **público** de GitHub (`InverenceBBS/aq-public-tools`, GPLv3). No subir nunca
  nada privado: credenciales, datos de clientes, informes internos ni material sin publicar.
- Los dashboards y los informes de producción cargan sus ficheros **directamente** (sin copia), así
  que mover, renombrar o borrar una ruta enlazada, o reescribir la historia, rompe los logos, el pie
  de página y las imágenes del manual de usuario en los sitios en producción.
- Trabajar siempre en `main` (sin ramas de desarrollo): los enlaces del dashboard siguen `refs/heads/main`.

## Rutas enlazadas desde producción

| Ruta | Enlazada desde | Cómo |
|---|---|---|
| `img/Logo-Inverence-N_T-Ajustado.webp` | `aq-shiny-report/aq_dashboard/aq_dashboard_ui.R`, `aq_dashboard_server_init.R` (pie de página) | `raw.githubusercontent.com/.../refs/heads/main/` |
| `img/llull-environment/llull_environment_verde.png` | `aq-shiny-report/aq_dashboard/aq_dashboard_server_init.R` (logo de cabecera) | `github.com/.../blob/main/...?raw=true` |
| `img/llull-environment/*.png`, `*.gif` e `img/socaire/*` | `aq-shiny-report/aq_dashboard/user-manual-llull-environment.md`, `user-manual-socaire.md` | `github.com/.../blob/main/...?raw=true` |
| `img/llull-environment/cities/*` | `config.def_city_eea.tx_url_img1` / `tx_url_img2` (logos por ciudad, p. ej. Vilnius) | `raw.githubusercontent.com/.../<commit>/...` (fijado a un commit) |
| `img/aq-report-forecast-dygraph-legend.png` | `aq-shiny-report/aq_session_report-*.Rmd` | copia local `/code/aq/aq-public-tools/` |

Antes de borrar o renombrar un fichero, buscarlo en `aq-shiny-report` y en `config.def_city_eea`
(`tx_url_img1`, `tx_url_img2`, `tx_url_ref1`, `tx_url_ref2`, `tx_url_footer`).
