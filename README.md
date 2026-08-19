# Análisis de Accidentes de Tránsito en Carreteras del Perú — SUTRAN 2020–2021

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-orange)
![NumPy](https://img.shields.io/badge/NumPy-Data%20Processing-blue)
![Seaborn](https://img.shields.io/badge/Seaborn-Data%20Visualization-green)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange)
![Google Colab](https://img.shields.io/badge/Google%20Colab-Environment-yellow)

## Descripción

Proyecto de **Análisis Exploratorio de Datos (EDA)** desarrollado a partir del conjunto de datos oficial de accidentes de tránsito registrados por la **Superintendencia de Transporte Terrestre de Personas, Carga y Mercancías (SUTRAN)** en las carreteras del Perú durante los años **2020 y 2021**.

El proyecto aborda las principales etapas de un flujo de trabajo de **Data Science**, desde la exploración y limpieza de datos hasta la generación de nuevas variables y el análisis de patrones temporales, geográficos y de gravedad de los accidentes.

### Objetivos

- Explorar y comprender la estructura y calidad del conjunto de datos.
- Identificar y tratar valores nulos, duplicados e inconsistencias.
- Analizar la distribución temporal de los accidentes.
- Evaluar la ocurrencia y gravedad de los accidentes según sus víctimas.
- Identificar patrones geográficos mediante la agrupación de departamentos en macro-regiones.
- Detectar posibles valores atípicos en la cantidad mensual de accidentes.
- Generar variables derivadas que faciliten el análisis estadístico y la visualización.

---

## Flujo de Trabajo

### 1. Exploración Inicial

Se realizó una exploración del dataset original para conocer su estructura, tipos de datos y calidad.

- **8,155 registros**
- **9 variables**
- Lectura del archivo con codificación `latin-1`.
- Revisión de tipos de datos.
- Identificación de valores nulos y registros duplicados.
- Análisis inicial de las principales variables.

### 2. Limpieza y Preparación de Datos

Se aplicaron técnicas de **Data Cleaning** para mejorar la calidad y consistencia del conjunto de datos:

- Eliminación de la columna redundante `FECHA_CORTE`.
- Identificación y eliminación de registros duplicados.
- Estandarización de etiquetas sin información (`N.I.`, `N. I.`).
- Conversión de valores sin información a `NaN`.
- Tratamiento de valores faltantes mediante imputación o eliminación, según la variable.
- Verificación de la consistencia de los datos después de la limpieza.

### 3. Feature Engineering

Se generaron nuevas variables para facilitar el análisis temporal y de siniestralidad.

#### Variables temporales

- `AÑO`: año de ocurrencia del accidente.
- `MES`: mes de ocurrencia.
- `HORA_NUM`: hora numérica del accidente.

#### Variables relacionadas con víctimas

- `TOTAL_VICTIMAS`: suma de fallecidos y heridos.
- `CON_VICTIMAS`: indicador binario que identifica si el accidente registró víctimas.
- `GRAVEDAD`: clasificación del accidente en:
  - **Fatal**
  - **Con heridos**
  - **Sin víctimas**

### 4. Categorización Geográfica

Para facilitar el análisis espacial, los departamentos fueron agrupados en **9 macro-regiones**.

Esta transformación permite analizar la distribución de los accidentes a un nivel geográfico agregado e identificar diferencias en los patrones de siniestralidad entre regiones del país.

### 5. Análisis de Valores Atípicos

Se utilizaron **boxplots** para explorar la distribución mensual de accidentes por macro-región.

El análisis permitió identificar meses con valores potencialmente atípicos respecto al comportamiento habitual de cada región y generar hipótesis para posteriores análisis.

---

## Análisis Realizado

El proyecto permite explorar preguntas como:

- ¿Cómo se distribuyen los accidentes a lo largo del tiempo?
- ¿Qué meses presentan mayor cantidad de accidentes?
- ¿Qué macro-regiones concentran una mayor cantidad de siniestros?
- ¿Qué proporción de accidentes registra víctimas?
- ¿Cómo se distribuye la gravedad de los accidentes?
- ¿Existen diferencias en los patrones de siniestralidad entre macro-regiones?
- ¿Qué meses presentan comportamientos atípicos?

---

## Tecnologías y Herramientas

| Área | Tecnologías |
|---|---|
| Lenguaje | Python |
| Manipulación de datos | Pandas, NumPy |
| Visualización | Matplotlib, Seaborn |
| Análisis estadístico | SciPy |
| Entorno | Google Colab, Jupyter Notebook |
| Control de versiones | Git, GitHub |

---

## Estructura del Repositorio

```text
├── data/
│   └── Accidentes de tránsito en carreteras-2020-2021-Sutran.csv
│
├── notebooks/
│   └── Entregable1_DS_SUTRAN.ipynb
│
├── README.md
│
└── requirements.txt
```

**AUTOR**

**Davila Ponce Rosa**
