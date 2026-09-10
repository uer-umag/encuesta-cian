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
```

Sin dependencias ni build. La única carga externa es la tipografía **Asap** (oficial UMAG)
desde Google Fonts; sin conexión la página cae a una tipografía de sistema y sigue siendo
legible.

Paleta tomada de los propios logotipos institucionales: azul OLN `#3C6CB4`, celeste
`#30A8D8` y navy `#242454`; magenta `#E4186C`, teal `#0C9C90` y amarillo `#FCC018` de la
marca municipal. El violeta UMAG `#593D80` queda reservado a la mención de la UER.

## Trabajar en el sitio

```bash
open index.html          # ver los cambios localmente
git add -A && git commit -m "…"
git push                 # GitHub Pages republica solo, en ~1 minuto
```

## Origen del contenido

El texto se deriva de los documentos de trabajo del proyecto, que viven en la carpeta
compartida de Drive `UMAG/01_Proyectos/OLN-Natales/`:

| Sección | Fuente |
| --- | --- |
| De dónde viene, actores, marco legal, hitos | `CLAUDE.md` |
| Módulos M0–M4 y pregunta de cierre | `Cuestionario_Final/CLAUDE.md` |
| Objetivo general y específicos, tramos y versiones | `Presentacion_EncuestaCIAN.pptx` |
| 16 instrumentos revisados (7 chilenos, 9 internacionales) | `Presentacion_EncuestaCIAN.pptx` |
| Qué es la OLN, qué es el CIAN, contacto y ubicación | portal.muninatales.cl/oln/ |
| Cómo se responde | `metodo_cuestionario.md` §§2, 5 |
| Tus derechos | `metodo_cuestionario.md` §4 y `manual_supervisor.md` |

## Duración declarada

La página declara **10 a 15 minutos**, cifra acordada el 2026-09-09 y aplicada también a
la pantalla de presentación del cuestionario (DOCX, XLSForm y Markdown) y al guion del
manual del supervisor. Los tres artefactos de comunicación dicen ahora lo mismo.

Queda una brecha abierta con la estimación técnica: `metodo_cuestionario.md` §3 estima
15–20 min para el tramo 10–13 y 25–30 min para el 14–17, y el instrumento vigente presenta
24 preguntas a ambos tramos porque la ramificación por `tramo` no está implementada
(pendientes 1 y 2 de `Cuestionario_Final/CLAUDE.md`). Se cierra reduciendo preguntas para
el tramo menor, no estirando el tiempo. El piloto con 5–10 NNA confirma la cifra final; si
supera los 15 minutos, hay que corregir esta página, el cuestionario y el manual.
