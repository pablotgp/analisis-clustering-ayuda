# 🌍 Análisis de Clustering para Estrategia de Ayuda Humanitaria

![Python](https://img.shields.io/badge/Python-3.9+-blue.svg)
![Libraries](https://img.shields.io/badge/Librerías-Scikit--learn%2C%20Pandas%2C%20Plotly-orange.svg)
![License](https://img.shields.io/badge/Licencia-MIT-green.svg)

## 🎯 Descripción del Proyecto

Este proyecto aborda un desafío real: **¿Cómo puede una ONG asignar sus recursos limitados para maximizar el impacto humanitario?**

Utilizando un conjunto de datos socioeconómicos y de salud de 167 países, se desarrolla un modelo de clustering (K-Means) para segmentar las naciones en grupos homogéneos. El análisis no solo construye un modelo robusto, sino que se enfoca en la **interpretación de los clústeres** para definir perfiles de vulnerabilidad claros. El resultado es una guía estratégica y visual que permite a "Ayuda Internacional" tomar decisiones basadas en datos para dirigir sus esfuerzos a las regiones más necesitadas del mundo.

## 💡 Hallazgos Principales

El análisis revela una clara división global, donde el nivel de desarrollo de un país determina su perfil de necesidad:

1️⃣ **Países de Alta Prioridad (Nivel de Ayuda 2):** Un grupo de naciones, principalmente en **África Subsahariana**, sufre de una combinación crítica de **muy alta mortalidad infantil** y **muy bajos ingresos**. Son, sin duda, los candidatos urgentes para la ayuda.

2️⃣ **Países en Desarrollo (Nivel de Ayuda 1):** Este clúster intermedio, que incluye a la mayoría de **América del Sur y Asia**, presenta desafíos significativos pero con indicadores menos extremos que el primer grupo. Representan una oportunidad para la ayuda de consolidación.

3️⃣ **Países Desarrollados (Nivel de Ayuda 0):** Naciones de **Norteamérica, Europa Occidental y Oceanía** con ingresos altos y sistemas de salud robustos. No requieren ayuda, pero pueden ser considerados socios estratégicos.

## 📈 Visualizaciones Destacadas

#### Mapa Mundial de Necesidad de Ayuda
Esta visualización es la conclusión principal del proyecto. Muestra geográficamente los tres clústeres, coloreando cada país según su nivel de necesidad. Los "puntos calientes" (amarillo) en África son evidentes.

![Mapa Mundial](mapa_ayuda_corregido.png)

#### Perfil de los Clústeres por Ingreso y Mortalidad
Estos diagramas de caja demuestran las diferencias drásticas entre los tres grupos. El clúster de "Ayuda Urgente" (etiquetado como 0 en el gráfico original) tiene la mortalidad infantil más alta y los ingresos más bajos.

![Boxplots de Ingreso y Mortalidad](boxplots.png)

## ⚙️ Características Técnicas

*   **Modelo de Clustering:** Implementación de un clasificador no supervisado `KMeans` de Scikit-learn.
*   **Selección de K:** Proceso riguroso para determinar el número óptimo de clústeres (K=3) utilizando tres métodos: **Método del Codo**, **Puntuación de Silueta** y **Gap Statistic**.
*   **Ingeniería de Características:** Creación de 3 indicadores agregados (Salud, Comercio, Finanzas) a partir de 9 variables originales para reducir la dimensionalidad y mejorar la interpretabilidad del modelo.
*   **Preprocesamiento de Datos:** Aplicación de `StandardScaler` y `MinMaxScaler` para estandarizar y normalizar las características antes del modelado.
*   **Análisis Interpretativo:** Caracterización de cada clúster mediante el análisis de variables clave y su representación en visualizaciones 2D y 3D interactivas.
*   **Informe Completo:** El proyecto está documentado en un **informe técnico de 9 páginas** en formato LaTeX que detalla la metodología, el análisis y las conclusiones.

## 💻 Tecnologías Utilizadas

*   **Lenguaje:** Python 3
*   **Librerías Principales:**
    *   Pandas & NumPy (Manipulación de datos)
    *   Scikit-learn (Clustering y preprocesamiento)
    *   Matplotlib & Seaborn (Visualización estática)
    *   Plotly & Kaleido (Visualización interactiva y exportación)
*   **Entorno:** Jupyter Notebook
*   **Documentación:** LaTeX

## 📂 Estructura del Repositorio

.
├── Feedback_Clustering_Pablo_Garcia.ipynb # 📓 Notebook con el código completo del análisis.
├── Reporte_Clustering_Ayuda_Humanitaria.pdf # 📄 Informe técnico detallado del proyecto en PDF.
├── Reporte_Clustering_Ayuda_Humanitaria.tex # ✍️ Código fuente del informe en LaTeX.
├── requirements.txt # 📋 Dependencias para replicar el entorno.
└── README.md # ℹ️ Este archivo.

## 🚀 Cómo Replicar el Análisis

Para ejecutar este proyecto en tu máquina local, sigue estos pasos:

1.  **Clona el repositorio:**
    ```bash
    git clone https://github.com/TU_USUARIO/TU_REPOSITORIO.git
    cd TU_REPOSITORIO
    ```

2.  **Crea un entorno virtual (recomendado):**
    ```bash
    python -m venv venv
    source venv/bin/activate  # En Windows usa `venv\Scripts\activate`
    ```

3.  **Instala las dependencias:**
    ```bash
    pip install -r requirements.txt
    ```

4.  **Inicia Jupyter Notebook:**
    ```bash
    jupyter notebook
    ```
    Abre el archivo `Feedback_Clustering_Pablo_Garcia.ipynb` y ejecuta las celdas.

## 👨‍💻 Autor

*   **Pablo García**
*   [LinkedIn](URL_DE_TU_LINKEDIN)
*   [Correo Electrónico](mailto:TU_CORREO@gmail.com)
