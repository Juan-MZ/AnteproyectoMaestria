# Insumo para diligenciar la Plantilla de Correcciones — Primera Entrega

## Instrucción para Claude

Con el contenido de este archivo, por favor diligencia la **Tabla de Control de Cambios** del formato "Formato de Corrección de Anteproyecto — Primera Entrega" de la Pontificia Universidad Javeriana Cali, Facultad de Ingeniería y Ciencias, Maestría en Ingeniería.

La tabla tiene cuatro columnas: **Ítem**, **Correcciones solicitadas**, **Ajustes solicitados para atender las correcciones** y **Sección**. A continuación se provee el contenido fila a fila.

---

## Ítem 1

### Corrección solicitada
Revisar el objetivo específico 1 (OBJ1) con la taxonomía de Bloom para asegurar que el verbo empleado refleja el nivel cognitivo adecuado para un trabajo de maestría.

### Contenido original (OBJ1)
> "Definir un catálogo acotado de *Fitness Functions* para tres familias de deriva arquitectónica relevantes en PyMES: violaciones de capas, ciclos de dependencia y concentración excesiva de dependencias salientes, dejando explícita la racionalidad de cada regla, su evidencia esperada y su criterio de incumplimiento."

### Análisis realizado
El verbo "**definir**" se ubica en el nivel 1–2 de la taxonomía de Bloom (Recordar / Comprender). Para un objetivo de maestría que implica construir un artefacto original, justificado y documentado con criterios explícitos de aceptación, el verbo adecuado pertenece al nivel 6 (Crear).

### Ajuste aplicado
Se reemplaza "Definir" por "**Formular**" (nivel 6 — Crear), que expresa la construcción deliberada de un catálogo con estructura, fundamentos teóricos, evidencia esperada y criterios de incumplimiento.

### Texto corregido (OBJ1)
> "Formular un catálogo acotado de *Fitness Functions* para tres familias de deriva arquitectónica relevantes en PyMES: violaciones de capas, ciclos de dependencia y concentración excesiva de dependencias salientes, dejando explícita la racionalidad de cada regla, su evidencia esperada y su criterio de incumplimiento."

### Sección del documento
`src/2-objetivos.tex` — Sección 2: Objetivos específicos, ítem 1.

---

## Ítem 2

### Corrección solicitada
En el objetivo específico 4 (OBJ4), eliminar la conjunción "y" y conservar únicamente el verbo de mayor nivel taxonómico. El evaluador sugiere el verbo "**ejecutar**".

### Contenido original (OBJ4)
> "**Diseñar y ejecutar** un experimento controlado sobre un caso de estudio, comparando una versión base con versiones que contengan derivas introducidas deliberadamente, para medir la capacidad del mecanismo de detectar desviaciones, clasificar correctamente el estado arquitectónico y generar evidencia útil para la toma de decisiones."

### Análisis realizado
El objetivo usa dos verbos en par ("diseñar" y "ejecutar"). Mantener dos verbos en un solo objetivo puede dificultar su evaluación independiente. El evaluador indica conservar "**ejecutar**", que en el contexto metodológico de Design Science Research representa la fase de demostración experimental, núcleo de la contribución empírica del trabajo.

### Ajuste aplicado
Se elimina "Diseñar y" y el objetivo queda encabezado por "**Ejecutar**", conservando íntegro el resto del enunciado.

### Texto corregido (OBJ4)
> "Ejecutar un experimento controlado sobre un caso de estudio, comparando una versión base con versiones que contengan derivas introducidas deliberadamente, para medir la capacidad del mecanismo de detectar desviaciones, clasificar correctamente el estado arquitectónico y generar evidencia útil para la toma de decisiones."

### Sección del documento
`src/2-objetivos.tex` — Sección 2: Objetivos específicos, ítem 4.

---

## Ítem 3

### Corrección solicitada
La sección de antecedentes debe finalizar con una tabla comparativa (por ejemplo, formato PROS vs. CONTRA o ventajas/limitaciones) que permita identificar **brechas** en el estado del arte. Esas brechas son las que justifican la ejecución del presente trabajo.

### Contenido original (cierre de Antecedentes)
La sección actualmente concluye con un párrafo de síntesis que enuncia en prosa la diferenciación del proyecto frente a los antecedentes.

> "En síntesis, los antecedentes confirman que el problema existe, que la automatización es viable y que las reglas ejecutables aportan valor. Lo que diferencia a este proyecto es su foco en PyMES, su dependencia exclusiva del código fuente como evidencia viva, su uso combinado de grafo estructural y *Fitness Functions*, y la incorporación de un experimento controlado con criterios explícitos para determinar si el mecanismo realmente ayuda a distinguir entre una arquitectura aceptable y una arquitectura problemática."

### Ajuste aplicado
Se mantiene el párrafo de síntesis y se agrega, a continuación, una tabla comparativa con los antecedentes revisados. La tabla organiza, por cada antecedente, sus **aportes al campo** (fortalezas) y sus **limitaciones o brechas** respecto al problema de este trabajo. La última fila consolida la brecha acumulada que motiva y diferencia el proyecto propuesto.

### Tabla sugerida para incluir al final de la subsección Antecedentes

| Antecedente | Aportes al campo | Limitaciones / Brechas frente al presente trabajo |
|---|---|---|
| **ArchUnit** | Valida que las reglas arquitectónicas pueden expresarse como verificaciones ejecutables sobre código Java. | Limitado a una única biblioteca y a un lenguaje; no produce clasificación por umbrales ni experimento controlado; no está orientado a PyMES. |
| **ArchSync** | Confirma la sincronización arquitectura-código como problema real; usa trazas y heurísticas de comportamiento. | Requiere instrumentación del sistema en ejecución; mayor complejidad de adopción para equipos pequeños; no usa análisis estático puro. |
| **Gestión de ATD en PyMES (Hamed et al., 2023)** | Evidencia que las PyMES necesitan mecanismos ligeros y automatizados; fundamenta el contexto del trabajo. | No proporciona un artefacto técnico; no define reglas ejecutables ni métricas de conformidad estructural. |
| **ATDI / Smells con ML (Sas & Avgeriou)** | Muestra que la deuda arquitectónica puede resumirse en un indicador interpretable; usa aprendizaje automático. | Modelo complejo y de caja negra; baja trazabilidad de las decisiones; difícil adopción inicial en PyMES sin experiencia en ML. |
| **Conformidad en CI/CD (Klein et al., 2022)** | Muestra valor de la verificación continua cerca del flujo de desarrollo; referencia práctica. | Centrado en integración a pipelines maduros; no propone experimento controlado para validar detección; asume contextos con mayor gobernanza. |
| **Modelos de reflexión (Murphy et al., 2001)** | Base formal para comparar modelo extraído con modelo esperado; fundamenta el motor de validación. | Propuesta formal sin operacionalización para conjuntos acotados de reglas ejecutables ni clasificación por umbrales comprensibles. |
| **Brecha consolidada** | — | Ningún antecedente combina: (1) análisis estático exclusivo del código fuente, (2) grafo de dependencia + *Fitness Functions*, (3) clasificación por Tasa de Conformidad (CR), (4) experimento controlado con criterios explícitos, y (5) orientación específica a PyMES sin documentación arquitectónica externa. Esta brecha justifica el presente trabajo. |

### Sección del documento
`src/5-marco.tex` — Subsección Antecedentes (al final, antes del cierre o reemplazando el párrafo de síntesis por la tabla seguida del párrafo).

---

## Ítem 4

### Corrección solicitada
Relacionar los **resultados esperados** con cada uno de los **objetivos específicos**, de manera que quede explícita la trazabilidad entre lo que se propone lograr y los productos que se entregarán.

### Contenido original (Resultados esperados)
Los resultados esperados se enuncian como lista de productos sin referencia explícita a los objetivos que los originan.

```
- Un prototipo funcional capaz de extraer dependencias estructurales...
- Un catálogo documentado de Fitness Functions...
- Una matriz de validación y un conjunto de reportes que permitan observar la CR...
- Evidencia experimental obtenida al comparar una línea base con versiones alteradas...
- Un documento final de investigación...
```

### Ajuste aplicado
Se agrega una **tabla de trazabilidad** que relaciona explícitamente cada resultado esperado con el objetivo específico que lo genera, permitiendo verificar cobertura y coherencia interna del anteproyecto.

### Tabla de trazabilidad sugerida

| Objetivo específico | Resultado esperado asociado |
|---|---|
| **OBJ1 — Formular el catálogo de *Fitness Functions*** | Catálogo documentado de *Fitness Functions* para las tres familias de deriva seleccionadas, con racionalidad, evidencia esperada y criterio de incumplimiento para cada regla. |
| **OBJ2 — Implementar el componente de análisis estático** | Componente de software funcional que extrae dependencias estructurales desde el código fuente y genera el grafo de dependencia del sistema evaluado. |
| **OBJ3 — Construir el motor de validación con CR** | Motor de validación que compara el grafo con las reglas definidas, calcula la Tasa de Conformidad (CR) y clasifica el estado arquitectónico (aceptable / en observación / no conforme). Incluye la matriz de validación y los reportes de salida. |
| **OBJ4 — Ejecutar el experimento controlado** | Evidencia experimental: reportes comparativos entre la versión base y las versiones con derivas deliberadas, que muestran la capacidad del mecanismo de detectar desviaciones, variar la CR y clasificar correctamente el estado arquitectónico. |
| **Trabajo integrador (todos los objetivos)** | Documento final de investigación que sistematiza el problema, la solución construida, el proceso metodológico y los hallazgos derivados de la evaluación experimental. |

### Sección del documento
`src/6-metodologia.tex` — Subsección "Resultados esperados" (se agrega la tabla de trazabilidad a continuación de la lista existente o en reemplazo de ella).

---

## Otros comentarios para el evaluador

No aplica. Todas las observaciones fueron atendidas en los ítems anteriores con acuerdo del director de trabajo de grado.
