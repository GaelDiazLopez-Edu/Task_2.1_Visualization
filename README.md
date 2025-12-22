# Task_2.1_Visualization

Este proyecto consiste en un análisis exploratorio de datos utilizando Python. El objetivo principal es visualizar cómo se distribuyen las medidas físicas (altura y peso) de una población y entender cómo el género influye en estas distribuciones y en la detección de valores atípicos.

## El flujo de trabajo se divide en cuatro etapas principales:

Preparación de Datos: Importamos las librerías necesarias (Pandas, Matplotlib, Seaborn) y cargamos un dataset con registros de miles de personas.

Transformación de Unidades: Convertimos las medidas del sistema imperial (pulgadas y libras) al sistema internacional (centímetros y kilogramos) para facilitar la interpretación.

Visualización de Distribuciones: Generamos histogramas con curvas de densidad (KDE) para observar la "forma" de los datos.

Análisis de Outliers: Utilizamos diagramas de caja (Boxplots) para identificar valores extremos, primero de forma global y luego segmentando por género.

## Funcionamiento del Código
El código utiliza principalmente la librería Seaborn para la creación de gráficos estadísticos complejos con pocas líneas de código.

### Lógica de los Gráficos de Caja (Boxplots):

El funcionamiento clave para entender los resultados es cómo el gráfico identifica los valores atípicos:

La Caja: Representa el 50% central de los datos (el rango intercuartílico).

Los Bigotes: Se extienden hasta 1.5 veces el rango de la caja.

Puntos (Outliers): Cualquier dato que quede fuera de los bigotes se marca como un punto individual.

### Segmentación por Género (hue)

Una parte fundamental del notebook es el uso del parámetro hue. Al separar los datos por género:

El algoritmo calcula las estadísticas (media, desviación, bigotes) de forma independiente para hombres y para mujeres.

Esto evita que una persona sea marcada como "atípica" simplemente por pertenecer a un grupo con una media diferente (por ejemplo, una mujer alta comparada con la media global de hombres y mujeres).

## Cómo usar
Asegúrate de tener instalado Python y las librerías: pip install pandas matplotlib seaborn.

Ejecuta las celdas en orden secuencial o aprentando "ejecutar todo".

Observa las gráficas generadas para interpretar cómo la segmentación de datos cambia nuestra percepción de lo que es un "valor normal".