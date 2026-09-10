# Encuesta CIAN — sitio web

Página pública de la **Encuesta CIAN**, dirigida a niños, niñas y adolescentes de 10 a 17
años de Puerto Natales. Explica qué es la encuesta, qué pregunta, cómo se responde y
cuáles son los derechos de quien la contesta.

**Sitio publicado:** https://uer-umag.github.io/encuesta-cian

## Quiénes

| Actor | Rol |
| --- | --- |
| **CIAN** — Consejo Consultivo Comunal de Niños, Niñas y Adolescentes de Natales | Levantó la necesidad de la encuesta y define las temáticas. |
| **OLN Natales** — Oficina Local de la Niñez, I. Municipalidad de Natales | Solicitante (Oficio ORD. N° 14, 24 de abril de 2026). Coordina la articulación territorial. |
| **UER — UMAG** — Unidad de Estudios Regionales, Universidad de Magallanes | Apoyo técnico-metodológico. |

Marco normativo: Ley N° 21.430 de Garantías y Protección Integral de los Derechos de la
Niñez y Adolescencia, y Decreto N° 12.

## Estructura

```
index.html      # la página completa, con el CSS embebido
assets/         # logos UER y UMAG (versiones color y blanco)
.nojekyll       # sirve los archivos tal cual, sin procesamiento Jekyll
```

Sin dependencias ni build. La única carga externa es la tipografía **Asap** (oficial UMAG)
desde Google Fonts; sin conexión la página cae a una tipografía de sistema y sigue siendo
legible.

Paleta según el *Breve Manual de Normas Gráficas UMAG*: azul `#4A5CAB`, violeta `#593D80`,
con el naranja `#E69055` de la UER como acento.

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
| Cómo se responde | `metodo_cuestionario.md` §§2, 5 |
| Tus derechos | `metodo_cuestionario.md` §4 y `manual_supervisor.md` |

## Pendiente antes de difundir

La página declara que la encuesta **toma unos 10 minutos**, cifra que **no coincide** con la
documentación metodológica: `metodo_cuestionario.md` §3 estima 15–20 min para el tramo
10–13 y 25–30 min para el 14–17, y el instrumento vigente tiene 24 preguntas que hoy ven
ambos tramos, porque la ramificación por `tramo` aún no está implementada.

Hay que alinear las tres cifras que circulan (esta página, el guion del manual del
supervisor y la metodología) antes de que el sitio se difunda a los establecimientos.
Se resuelve acortando el instrumento para el tramo menor o ajustando la cifra tras el
piloto de 5–10 NNA.
