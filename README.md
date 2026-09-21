# Análisis y Evolución de la Tasa de Interés Real Ex Ante mediante Homología Persistente

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python 3.10+](https://img.shields.io/badge/python-3.10+-blue.svg)](https://www.python.org/downloads/)
[![Giotto-TDA](https://img.shields.io/badge/Library-Giotto--TDA-orange)](https://giotto-ai.github.io/gtda-documentation/)

Este repositorio contiene el desarrollo del código, datos y reporte de investigación enfocado en el modelado y pronóstico de la tasa de interés real ex ante en México, integrando Análisis Topológico de Datos y algoritmos de Machine Learning.

📄 **[Leer el artículo de investigación completo (PDF)](./docs/Análisis y predicción de la tasa de interés real ex ante mediante homología persistente.pdf)**

---

## 📌 Descripción del Proyecto

Se presenta un análisis de la evolución mensual de la tasa de interés real ex ante de México, Estados Unidos, Chile y Colombia en los últimos 22 años, haciendo uso del análisis topológico de datos, en particular, el cálculo de características topológicas mediante la homología persistente. A su vez se presenta una predicción de esta para el caso particular de México con el uso de árboles de decisión.

Metodología Clave:
1. Incrustación Espacial: Reconstrucción del espacio de fases mediante `SlidingWindow` y `TakensEmbedding`.
2. Filtraciones Topológicas: Cálculo de homología persistente usando complejos de Vietoris-Rips (`VietorisRipsPersistence`) en dimensiones H_0, H_1 y $H_2$.
3. Extracción de Invariantes: Vectorización de diagramas mediante métricas de amplitud topológica (`Amplitude`).
4. Modelado y Pronóstico: Ajuste con `RandomForestRegressor` / modelos lineales y evaluación del rendimiento tanto dentro (*In-Sample*) como fuera de muestra (*Out-of-Sample*).

---

## 📁 Estructura del Repositorio

```text
├── docs/
│   └── Articulo_Homologia_Persistente.pdf   # Reporte escrito y artículo académico
├── notebooks/
│   └── 01_pipeline_tda_forecasting.ipynb   # Código del proyecto en Jupyter Notebook
├── data/
│   └── tasa_interes_mexico.csv              # Serie histórica de datos de Banxico
├── LICENSE                                  # Licencia MIT
└── README.md                                # Documentación principal
```

---

## 🚀 Instalación y Requisitos

Para clonar este repositorio y ejecutar el código localmente:

```bash
# Clonar el repositorio (reemplaza 'tu-usuario' por tu nombre de usuario real en GitHub)
git clone https://github.com/tu-usuario/tasa-interes-homologia-persistente.git

# Entrar al directorio
cd tasa-interes-homologia-persistente

# Instalar dependencias necesarias
pip install numpy pandas matplotlib scikit-learn giotto-tda
```
