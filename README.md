# 🚗 Análisis de Accidentes de Tránsito en Carreteras del Perú (SUTRAN 2020 - 2021)

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-orange.svg)
![Seaborn](https://img.shields.io/badge/Seaborn-Data%20Viz-green.svg)
![Jupyter](https://img.shields.io/badge/Jupyter-Colab-yellow.svg)

## 📌 Descripción del Proyecto
Este proyecto realiza un análisis exploratorio de datos (EDA), limpieza, estandarización e ingeniería de características (*feature engineering*) sobre el conjunto de datos oficial de **accidentes de tránsito registrados por la SUTRAN** en las carreteras del Perú durante los años **2020 y 2021**.

El objetivo principal es identificar patrones espaciales y temporales en la siniestralidad vial, evaluar la gravedad de los accidentes y categorizar el impacto a nivel macro-regional.

---

## 📊 Estructura y Flujo de Trabajo

El procesamiento de datos se realizó siguiendo los siguientes pasos:

1. **Carga y Exploración Inicial:** 
   - Lectura del dataset original de **8,155 filas y 9 columnas** con codificación `latin-1`.
2. **Depuración y Limpieza de Datos:**
   - Eliminación de columnas redundantes (`FECHA_CORTE`).
   - Identificación y remoción de filas duplicadas.
   - Reemplazo de etiquetas sin información (`'N.I.'`, `'N. I.'`) por valores nulos `NaN`.
   - Tratamiento e imputación/eliminación de valores nulos (< 1.1% del total).
3. **Ingeniería de Características (*Feature Engineering*):**
   - Extracción de dimensiones temporales: `AÑO`, `MES` y `HORA_NUM`.
   - Creación de métricas asociadas a víctimas:
     - `TOTAL_VICTIMAS` (Fallecidos + Heridos)
     - `CON_VICTIMAS` (Flag binario: 0 / 1)
     - `GRAVEDAD` (Categorías: *Fatal*, *Con heridos*, *Sin víctimas*)
4. **Categorización Geográfica:**
   - Mapeo de departamentos a **9 Macro-Regiones** (Costa Norte, Sierra Centro, Costa Sur, Selva Norte, etc.) para análisis espacial agregado.
5. **Análisis de Outliers (Valores Atípicos):**
   - Generación de diagramas de caja (*Boxplots*) para identificar meses atípicos con alta siniestralidad por macro-región.

---

## 🛠️ Tecnologías y Librerías Utilizadas

- **Lenguaje:** Python 3.x
- **Manipulación de Datos:** `pandas`, `numpy`
- **Visualización:** `matplotlib`, `seaborn`
- **Análisis Estadístico:** `scipy`
- **Entorno de Desarrollo:** Google Colab / Jupyter Notebook

---

## 📁 Estructura del Repositorio

```text
├── data/
│   └── Accidentes de tránsito en carreteras-2020-2021-Sutran.csv
├── notebooks/
│   └── Entregable1_DS_SUTRAN.ipynb
├── README.md
└── requirements.txt
