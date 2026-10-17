# Ficha del artículo

Completa esta ficha al crear el repositorio y mantenla al día. Es el único
lugar con datos propios del artículo; el README es igual en todos los
repositorios.

## Identificación

- **Título:** Revisitando el aborto: ¿qué piensan los ecuatorianos?
- **Descripción del repositorio:** Repositorio del artículo Revisitando el aborto: ¿qué piensan los ecuatorianos? por Joyce Sarmiento.
- **Autoría:** Joyce Sarmiento
- **Fecha de publicación:** 2023-05-02
- **Artículo publicado:** https://elquantificador.org/post/valores/2023-05-02-revisitando-el-aborto-que-piensan-los-ecuatorianos-en-2023/
- **Categoría:** Valores y comportamiento
- **Edición:** Febrero - Agosto 2023

## Estado

Publicado el 2023-05-02.

## Pregunta y alcance

El artículo pregunta qué piensan los ecuatorianos sobre el aborto y compara la
opinión de 2013 con la de 2018, tras la despenalización del aborto por
violación. Usa las rondas de 2013 y 2018 de la Encuesta Mundial de Valores
(WVS) para Ecuador, con cobertura nacional y personas encuestadas como unidad de
análisis. Para 2018 desagrega la no justificación del aborto por sexo, nivel
educativo, grupo de edad y religión.

## Requisitos

- R: no documentada en el repositorio.
- Paquetes de R: ggplot2, knitr (para renderizar el `.Rmd`), patchwork,
  readxl, tidyverse.

## Fuentes de datos

| Fuente | Institución | Periodo | Acceso | Script |
|---|---|---|---|---|
| Encuesta Mundial de Valores (WVS), ronda 6, Ecuador | World Values Survey Association | 2013 | Descarga automática de un `.zip` con exportaciones en Excel alojado en el repositorio de GitHub de la autora (`joyceliss/LIDE_ESPOL_Joyce_Sarmiento`) | `code/analisis-aborto-2023.R` |
| Encuesta Mundial de Valores (WVS), ronda 7, Ecuador | World Values Survey Association | 2018 | Misma descarga automática del `.zip` anterior | `code/analisis-aborto-2023.R` |

El script descarga las dos bases desde ese `.zip` alojado por la autora, no
desde el sitio oficial de la WVS (https://www.worldvaluessurvey.org/, enlace
general que ni el repositorio ni el artículo citan). El `.zip` no forma parte de
este repositorio. Se descomprime en una carpeta temporal, así que no hay que
colocar archivos en `data/raw/`.

## Salidas

- `images/fig1.png`: justificación y no justificación del aborto en Ecuador,
  WVS 2013 y 2018.
- `images/fig2.png`: no justificación del aborto por sexo de la persona
  encuestada, WVS 2018.
- `images/fig3.png`: no justificación del aborto por nivel educativo y sexo,
  WVS 2018.
- `images/fig4.png`: no justificación del aborto por grupo de edad y sexo,
  WVS 2018.
- `images/fig5.png`: no justificación del aborto por religión y sexo, WVS 2018.
- `report/aborto-2023.docx` y `report/aborto-2023.html`: versiones renderizadas
  de `report/aborto-2023.Rmd`.

## Cómo replicar en este repositorio

Este repositorio no tiene `MASTER.R`. El orden surge del README anterior y de
los scripts:

1. Clona o descarga el repositorio y ábrelo con `aborto2023.Rproj`, de modo que
   la raíz del proyecto sea el directorio de trabajo (el script guarda en
   `images/fig1.png` y siguientes con rutas relativas a esa raíz).
2. Ejecuta `code/analisis-aborto-2023.R`. Instala los paquetes que falten,
   descarga y lee las bases de la WVS 2013 y 2018, construye la variable
   "Justifica" / "No justifica" (respuestas 1 a 6 y 7 a 10) y guarda las cinco
   figuras en `images/`. Requiere conexión a internet.
3. Renderiza `report/aborto-2023.Rmd` para regenerar el texto del artículo
   (Word y HTML). El `.Rmd` solo inserta las figuras de `images/`, así que
   depende del paso 2. Para compilar en PDF hace falta LaTeX, opcional según el
   README anterior.

## README anterior

Texto del README de este repositorio antes de adoptar el README estándar,
conservado sin cambios de contenido para no perder información.

### Revisitando el aborto: ¿qué piensan los ecuatorianos?

Repositorio del artículo *Revisitando el aborto: ¿qué piensan los ecuatorianos?* por [Joyce Sarmiento](https://github.com/joyceliss) en [El Quantificador](https://elquantificador.org/). Repositorio preliminar en el [perfil](https://github.com/joyceliss) de la autora.

#### Requisitos
- R (se recomienda usar RStudio).
- Paquetes de R que se instalarán automáticamente al ejecutar los scripts.
- Opcionalmente LaTeX para compilar el artículo en PDF.

#### Cómo reproducir el análisis
1. Clona o descarga este repositorio.
2. Ejecuta `analisis-aborto-2023.R` para replicar el análisis del artículo.
3. En `aborto-2023.Rmd`, encontrarás el texto del artículo, en caso de querer replicarlo por completo.
