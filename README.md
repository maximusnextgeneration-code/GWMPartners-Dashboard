# GWM Partners — Investment Dashboard

Dashboard mensual de los portafolios modelo de **GWM Partners** (Global Wealth Management),
elaborado por **LATAM ConsultUs**.

🔗 **Link para el cliente (siempre el mismo):**
<https://maximusnextgeneration-code.github.io/GWMPartners-Dashboard/>

La página de inicio muestra **siempre el mes más reciente**. El cliente solo tiene que refrescar.

## Contenido

- `index.html` — dashboard del mes vigente (se reemplaza en cada actualización).
- `meses/MM-YYYY/index.html` — archivo histórico de cada mes publicado.

El HTML es **autocontenido** (fuentes, logo y datos embebidos): no depende de internet ni de otros archivos.

## Cómo se actualiza cada mes

1. Dejar los inputs del mes en `…/CLIENTES/DASHBOARDS/GWM/MM-YYYY/inputs/`.
2. Generar el dashboard:
   ```
   python _build/extract_gwm.py MM-YYYY
   python _build/build_gwm.py   MM-YYYY
   python _build/compliance_check.py MM-YYYY
   ```
3. Publicar:
   ```
   python _build/publish.py MM-YYYY
   ```
   (copia el HTML a este repo, commitea y hace push; GitHub Pages lo sirve en 1-2 minutos)

## Meses publicados

- 09-2026 — septiembre 2026 *(vigente)*
- 08-2026 — agosto 2026
- 07-2026 — julio 2026
