# Anteproyecto de Maestría

Repositorio del anteproyecto titulado "Mecanismo de detección automática de deriva arquitectónica mediante el uso de Fitness Functions y análisis estático de grafos de dependencia: un enfoque de gobernanza continua para PyMES de software".

## Propósito

Este repositorio contiene la fuente en LaTeX del anteproyecto de trabajo de grado para la Maestría en Ingeniería de Software de la Pontificia Universidad Javeriana Cali.

El proyecto propone un mecanismo automatizado para detectar deriva arquitectónica a partir del código fuente, utilizando análisis estático, grafos de dependencia y reglas expresadas como Fitness Functions. El objetivo es apoyar la gobernanza continua de arquitectura en PyMES de software sin depender de documentación arquitectónica externa y desactualizada.

## Resumen

La deriva arquitectónica representa una de las principales causas del deterioro estructural del software en PyMES, debido a que las decisiones de diseño se desalinean progresivamente de la implementación real sin que existan mecanismos continuos de verificación. Este anteproyecto propone desarrollar un mecanismo automatizado de detección de deriva arquitectónica basado en análisis estático de código, construcción de grafos de dependencia y ejecución de Fitness Functions, con el fin de apoyar la gobernanza técnica sin depender de documentación arquitectónica externa. El trabajo se enfocará en un único ecosistema tecnológico y evaluará tres dimensiones concretas de conformidad: integridad de capas, ausencia de ciclos de dependencia y cumplimiento de convenciones de nomenclatura arquitectónica. A partir de estas reglas, el mecanismo generará una representación estructural del sistema y calculará una Tasa de Conformidad (CR) que permita identificar desviaciones relevantes de manera temprana. Se espera como resultado un prototipo funcional, un conjunto de reglas preconfiguradas y evidencia sobre la utilidad del enfoque para apoyar decisiones de mantenimiento y refactorización en contextos de desarrollo ágil.

## Abstract

Architectural drift is one of the main causes of structural software deterioration in SMEs, since design decisions progressively diverge from the actual implementation without continuous verification mechanisms. This proposal aims to develop an automated mechanism for detecting architectural drift based on static code analysis, dependency graph construction, and the execution of Fitness Functions, in order to support technical governance without relying on external architectural documentation. The work will be limited to a single technological ecosystem and will evaluate three specific conformance dimensions: layer integrity, absence of dependency cycles, and compliance with architectural naming conventions. From these rules, the mechanism will generate a structural representation of the system and calculate a Conformance Rate (CR) to identify relevant deviations at an early stage. The expected outcomes include a functional prototype, a set of preconfigured rules, and evidence of the usefulness of the approach to support maintenance and refactoring decisions in agile development environments.

## Estructura del repositorio

- `main.tex`: documento principal que integra todas las secciones.
- `src/`: capítulos y secciones del anteproyecto.
- `img/`: imágenes y recursos gráficos.
- `bibfile.bib`: base bibliográfica utilizada por el documento.
- `out/`: carpeta de salida para artefactos generados durante la compilación.

## Compilación

### Opción 1: latexmk

Si tienes `latexmk` disponible:

```bash
latexmk -pdf -interaction=nonstopmode -outdir=out main.tex
```

### Opción 2: pdflatex + biber

Si compilas manualmente:

```bash
pdflatex -output-directory=out main.tex
biber out/main
pdflatex -output-directory=out main.tex
pdflatex -output-directory=out main.tex
```

## Requisitos sugeridos

- Una distribución LaTeX como TeX Live o MiKTeX.
- `biber` para procesar la bibliografía.
- Soporte para codificación UTF-8.

## Estado del documento

El repositorio contiene la versión de trabajo del anteproyecto. Algunas secciones aún pueden estar en ajuste editorial o metodológico antes de la entrega final.

## Licencia

El contenido de este repositorio se distribuye bajo la licencia Creative Commons Attribution 4.0 International (CC BY 4.0). Consulta el archivo `LICENSE` para el texto aplicable.