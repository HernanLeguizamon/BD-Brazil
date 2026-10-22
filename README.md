# Predicción de Ocurrencia y Severidad de Accidentes de Tránsito en Brasil (2017–2023)

## 1. Descripción del proyecto

Este repositorio contiene el código fuente desarrollado para una investigación académica enfocada en el análisis y la predicción de accidentes de tránsito en Brasil durante el período 2017–2023.

El proyecto utiliza técnicas de aprendizaje automático (*Machine Learning*) para estudiar dos problemas de clasificación:

* **Predicción de ocurrencia:** análisis y clasificación de la ocurrencia de accidentes de tránsito a partir de las variables disponibles en el conjunto de datos.
* **Predicción de severidad:** clasificación de los accidentes según su nivel de gravedad, considerando las categorías leve, grave y fatal.

Para el desarrollo de los modelos se utilizaron los algoritmos XGBoost y LightGBM.

Asimismo, se incorporaron técnicas de inteligencia artificial explicable mediante SHAP (*SHapley Additive exPlanations*) para analizar la contribución de las variables utilizadas en las predicciones.

## 2. Conjunto de datos

La investigación utiliza registros de accidentes de tránsito ocurridos en Brasil entre los años 2017 y 2023.

**Archivo utilizado:**

`accidents_2017_to_2023_english.csv`

Los datos corresponden a registros de accidentes de tránsito de la Policía Rodoviária Federal (PRF) de Brasil.

El conjunto de datos incluye información relacionada con:

* Fecha y hora de los accidentes.
* Ubicación geográfica.
* Condiciones meteorológicas.
* Características de las vías.
* Causas y tipos de accidentes.
* Personas involucradas.
* Víctimas y consecuencias de los accidentes.
* Vehículos involucrados.

Durante el preprocesamiento se realizaron operaciones de limpieza, selección de variables, transformación de datos y preparación de los conjuntos de entrenamiento y prueba.

## 3. Estructura del repositorio

El repositorio contiene los siguientes archivos principales:

**BD_Brazil_Ocurrencia_Accidentes.ipynb**

Cuaderno de Jupyter Notebook destinado al análisis de ocurrencia de accidentes de tránsito.

Incluye:

* Exploración y limpieza de datos.
* Transformación y preparación de variables.
* División de datos para entrenamiento y evaluación.
* Implementación de modelos XGBoost y LightGBM.
* Experimentos con diferentes configuraciones de los modelos.
* Evaluación mediante métricas de clasificación.
* Generación de matrices de confusión y curvas ROC.
* Interpretación de resultados mediante SHAP.
* Comparación de resultados experimentales.

**BD_Brazil_Severidad_Accidentes.ipynb**

Cuaderno de Jupyter Notebook destinado a la clasificación de severidad de accidentes de tránsito.

Incluye:

* Limpieza y preparación de datos.
* Definición de las categorías de severidad.
* Transformación de variables.
* División de datos para entrenamiento y prueba.
* Implementación de modelos XGBoost y LightGBM.
* Evaluación del rendimiento mediante métricas de clasificación.
* Generación y visualización de matrices de confusión.
* Análisis de importancia de variables mediante SHAP.
* Visualizaciones estadísticas y geográficas.

## 4. Tecnologías utilizadas

**Lenguaje de programación:**

* Python.

**Entorno de desarrollo:**

* Jupyter Notebook.

**Bibliotecas principales:**

* Pandas: manipulación y análisis de datos.
* NumPy: operaciones numéricas.
* Scikit-learn: preparación de datos y evaluación de modelos.
* XGBoost: implementación de modelos de aprendizaje automático.
* LightGBM: implementación de modelos de aprendizaje automático.
* SHAP: interpretación de las predicciones.
* Matplotlib: generación de gráficos.
* Seaborn: visualización estadística.
* Folium: visualización geográfica.

## 5. Metodología

El desarrollo experimental comprende las siguientes etapas:

**Etapa 1. Exploración de datos**

Análisis inicial del conjunto de datos para identificar sus características, variables y distribución.

**Etapa 2. Preprocesamiento**

Aplicación de procedimientos de limpieza, transformación, selección y codificación de variables.

**Etapa 3. Preparación de datos**

Construcción de los conjuntos de entrenamiento y prueba para los experimentos de clasificación.

**Etapa 4. Entrenamiento de modelos**

Implementación y entrenamiento de los algoritmos XGBoost y LightGBM para los problemas de ocurrencia y severidad.

**Etapa 5. Evaluación**

Análisis del rendimiento de los modelos mediante métricas de clasificación, matrices de confusión y otras visualizaciones de evaluación.

**Etapa 6. Interpretabilidad**

Aplicación de SHAP para identificar las variables que influyen en las predicciones y analizar su contribución a los resultados.

## 6. Requisitos para la ejecución

Para ejecutar los cuadernos se requiere una instalación de Python compatible con las bibliotecas utilizadas y un entorno Jupyter Notebook.

Las dependencias principales pueden instalarse mediante el siguiente comando:

```bash
pip install notebook pandas numpy scikit-learn xgboost lightgbm shap matplotlib seaborn folium
```

También es necesario disponer del conjunto de datos utilizado durante la investigación.

## 7. Instrucciones de ejecución

**Paso 1. Obtener el repositorio**

Clonar o descargar el repositorio desde GitHub.

**Paso 2. Instalar las dependencias**

Instalar las bibliotecas indicadas en la sección de requisitos.

**Paso 3. Preparar el conjunto de datos**

Disponer del archivo:

`accidents_2017_to_2023_english.csv`

Los notebooks originales utilizan una ruta local de Windows para cargar este archivo. Por lo tanto, es necesario modificar la ruta en la instrucción `pd.read_csv()` para que coincida con la ubicación del archivo en el equipo donde se ejecutarán los experimentos.

**Paso 4. Iniciar Jupyter Notebook**

Ejecutar el siguiente comando:

```bash
jupyter notebook
```

**Paso 5. Abrir los cuadernos**

Seleccionar uno de los siguientes archivos:

* `BD_Brazil_Ocurrencia_Accidentes.ipynb`
* `BD_Brazil_Severidad_Accidentes.ipynb`

**Paso 6. Ejecutar los experimentos**

Ejecutar las celdas correspondientes en el orden establecido y revisar los resultados generados.

Los cuadernos incluyen diferentes pruebas y configuraciones experimentales. Para reproducir un experimento específico, deben ejecutarse las celdas correspondientes y verificarse las dependencias entre variables y modelos.

## 8. Resultados y visualizaciones

Los cuadernos permiten generar y analizar:

* Métricas de clasificación.
* Matrices de confusión.
* Curvas ROC para los experimentos correspondientes.
* Gráficos de importancia de variables.
* Visualizaciones SHAP de importancia global.
* Gráficos SHAP tipo beeswarm.
* Gráficos de dependencia de variables.
* Explicaciones individuales mediante gráficos waterfall.
* Visualizaciones estadísticas y geográficas.

Estos resultados permiten comparar el comportamiento de XGBoost y LightGBM y examinar los factores que influyen en las predicciones.

## 9. Consideraciones sobre reproducibilidad

Los cuadernos contienen pruebas exploratorias, simulaciones y experimentos utilizados durante el desarrollo de la investigación.

Para reproducir los resultados es necesario utilizar el mismo conjunto de datos, conservar las configuraciones de entrenamiento y respetar los procedimientos de preprocesamiento y evaluación implementados.

Las versiones exactas de las bibliotecas no se encuentran documentadas de manera completa en los cuadernos proporcionados.

Por este motivo, la reproducción exacta de todos los resultados no está garantizada en entornos con versiones diferentes de las dependencias.

## 10. Finalidad académica

Este repositorio tiene fines exclusivamente académicos y forma parte de una investigación sobre la aplicación de técnicas de aprendizaje automático para la predicción de ocurrencia y severidad de accidentes de tránsito.

El código fuente se proporciona como material complementario para facilitar la consulta de la metodología, los experimentos y los resultados desarrollados durante la investigación.
