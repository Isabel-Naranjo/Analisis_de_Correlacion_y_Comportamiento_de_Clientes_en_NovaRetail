# Análisis de Factores de Comportamiento y Retención en NovaRetail+

## Objetivo del proyecto
En este proyecto analicé los datos de NovaRetail+ para entender qué factores del comportamiento de los clientes están más relacionados con el ingreso anual generado en la plataforma durante 2024. El objetivo principal fue realizar un análisis exploratorio y correlacional (recordando que la correlación no implica causalidad), identificando patrones clave mediante visualizaciones y coeficientes estadísticos para entregar recomendaciones responsables al equipo de Crecimiento y Retención.

## Principales hallazgos
Durante la exploración y el análisis descubrí varias cosas interesantes:

- **La relación clave y colinealidad:** Encontré una correlación altísima (0.97) entre las compras mensuales y el ingreso anual. Aunque los clientes que compran más generan más ingresos, esta relación tan fuerte advierte sobre un problema de **colinealidad**, lo que significa que ambas variables están muy relacionadas y aportan información muy similar.
- **Impacto de la publicidad:** El gasto en publicidad dirigida muestra una relación positiva moderada con las visitas mensuales, lo que indica que ayuda a atraer tráfico a la plataforma.
- **Variables categóricas:** Al aplicar la prueba **V de Cramér** (que mide la asociación entre variables categóricas), noté que la región o el dispositivo no tienen una asociación real con el abandono de los usuarios.

## Pasos del análisis
1. **Carga y exploración:** Cargué el dataset de 15,000 registros, revisé su estructura y corregí el tipo de dato de la columna `edad` a entero (`int64`).
2. **Preparación y supuestos:** Definí los métodos estadísticos adecuados según el tipo de variable: Pearson y Spearman para relaciones numéricas, **punto-biserial** para evaluar variables binarias (como miembro premium o abandono) frente a numéricas, y V de Cramér para las categóricas.
3. **Visualización:** Generé un mapa de calor (*heatmap*) para ver el panorama general y diagramas de dispersión (*scatterplots*) para analizar a fondo los pares de variables más importantes.
4. **Cálculo de correlaciones:** Cuantifiqué la fuerza de las relaciones e identifiqué el riesgo de alta colinealidad entre el volumen de compras y los ingresos.
5. **Interpretación y negocio:** Organicé los hallazgos con evidencia visual y numérica, detallando las implicaciones prácticas para el negocio.
6. **Limitaciones y próximos pasos:** Concluí el reporte analizando el alcance transversal de los datos y proponiendo segmentaciones adicionales junto con la evaluación del impacto de las campañas publicitarias.

## Archivos utilizados
Para este análisis utilicé un archivo principal de datos:
- `novaretail_comportamiento_clientes_2024.csv`: Contiene la información de 15,000 clientes con variables clave de la plataforma.

## Herramientas que usé
- **Lenguaje:** Python
- **Librerías:** pandas, numpy, matplotlib, seaborn y scipy.stats

## Cómo ver este proyecto
Puedes leer todo el análisis, revisar el código paso a paso y ver los gráficos abriendo el archivo [analisis_comportamiento_novaretail.ipynb](analisis_comportamiento_novaretail.ipynb) aquí mismo en GitHub.

*Nota sobre los datos:* El archivo CSV no está incluido en este repositorio. Sin embargo, el notebook muestra el análisis completo con los resultados y gráficos ya ejecutados, por lo que puedes revisarlo sin necesidad de descargar nada adicional.
