# Encuesta CIAN — sitio web

Página pública de la **Encuesta CIAN**, dirigida a niños, niñas y adolescentes de 10 a 17
años de Puerto Natales. Explica qué es la encuesta, qué pregunta, cómo se responde y
cuáles son los derechos de quien la contesta.

**Sitio publicado:** https://uer-umag.github.io/encuesta-cian

## Quiénes

| Actor | Rol |
| --- | --- |
| **CIAN** — Consejo Consultivo Comunal de Infancia y Adolescencia de Natales | Levantó la necesidad de la encuesta y define las temáticas. |
| **OLN Natales** — Oficina Local de la Niñez, I. Municipalidad de Natales | Conduce la iniciativa. Formalizó la solicitud de apoyo técnico (Oficio ORD. N° 14, 24 de abril de 2026) y coordina con los establecimientos. |
| **UER — UMAG** — Unidad de Estudios Regionales, Universidad de Magallanes | Acompañamiento metodológico: cómo preguntar, no qué preguntar. |

El protagonismo visual de la página corresponde a la **OLN** y al **CIAN**. La UER aparece
en el pie, identificada por su rol de acompañamiento.

**Contacto de la OLN** (fuente: <https://portal.muninatales.cl/oln/>): Angamos 650,
Puerto Natales, Pueblo Artesanal, Edificio OMIL · +56 9 3463 8651 (también WhatsApp) ·
oln@muninatales.cl · lunes a jueves 8:00–17:00 continuado, viernes 8:00–16:00.

Marco normativo: Ley N° 21.430 de Garantías y Protección Integral de los Derechos de la
Niñez y Adolescencia, y Decreto N° 12.

## Estructura

```
index.html      # la página completa, con el CSS embebido
assets/         # logos OLN, I. Municipalidad de Natales, UER y UMAG
.nojekyll       # sirve los archivos tal cual, sin procesamiento Jekyll
README.md       # este archivo
```

Sin dependencias ni build. La única carga externa es la tipografía **Asap** (oficial UMAG)
desde Google Fonts; sin conexión la página cae a una tipografía de sistema y sigue siendo
legible.

Paleta tomada de los propios logotipos institucionales: azul OLN `#3C6CB4`, celeste
`#30A8D8` y navy `#242454`; magenta `#E4186C`, teal `#0C9C90` y amarillo `#FCC018` de la
marca municipal. El violeta UMAG `#593D80` queda reservado a la mención de la UER.

## Trabajar en el sitio

El repositorio es a la vez la carpeta de trabajo: se edita y se publica en el mismo
lugar, sin build ni servidor.

```bash
open index.html          # revisar los cambios localmente, antes de publicar
git add -A && git commit -m "…"
git push                 # GitHub Pages republica solo, en ~1 minuto
```

La revisión se hace siempre sobre el archivo local. La URL publicada muestra la última
versión difundida, no el trabajo en curso.

## Origen del contenido

El texto se deriva de los documentos de trabajo del proyecto, que viven en la carpeta
compartida de Drive `UMAG/01_Proyectos/OLN-Natales/`:

| Sección | Fuente |
| --- | --- |
| De dónde viene, actores, marco legal, hitos | `CLAUDE.md` |
| Módulos M0–M4 y pregunta de cierre | `Cuestionario_CIAN/Cuestionario_Final/Cuestionario_CIAN_final.md` |
| Objetivo general y específicos, tramos y versiones | `informes_presentaciones/Presentacion_cuestionario_v263107.md` |
| 16 instrumentos revisados | `Referencias/estudios_referencia.md` |
| Qué es la OLN, qué es el CIAN, contacto y ubicación | portal.muninatales.cl/oln/ |
| Cómo se responde | `Cuestionario_CIAN/metodo_cuestionario.md` §§2, 5 |
| Tus derechos | `metodo_cuestionario.md` §4 y `manual_supervisor.md` |

La ficha de referencias tiene 17 entradas numeradas, pero la 4 y la 16 son dos ediciones
del mismo Barómetro de UNICEF España: **son 16 instrumentos distintos**, que es la cifra
que muestra la página.

## Estado del proyecto

Al **10 de septiembre de 2026**, el cuestionario está en revisión por el CIAN y la OLN.
El calendario acordado es:

| Etapa | Cuándo |
| --- | --- |
| Cierre del instrumento y piloto con 5–10 NNA | Septiembre 2026 |
| Aplicación en los establecimientos | Septiembre–octubre 2026 |
| Análisis de resultados | Octubre–noviembre 2026 |
| Presentación y discusión con el CIAN | Noviembre 2026 |

Las fechas de aplicación las coordina la OLN con cada establecimiento; mientras no estén
confirmadas, la página no las anuncia.
