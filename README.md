# Proyecto-Integrador-Data-Science-UTN
Segmentación RFM y sistema de recomendación de productos para e-commerce utilizando Python y Machine Learning.
Descripción del proyecto

Este proyecto analiza datos transaccionales de una empresa de comercio electrónico con el objetivo de identificar diferentes perfiles de clientes y evaluar sistemas de recomendación de productos.

El propósito es aportar herramientas analíticas que permitan diseñar estrategias de marketing más personalizadas y mejorar la toma de decisiones comerciales.

Dataset utilizado

Se utiliza el conjunto de datos Online Retail, que contiene información sobre transacciones comerciales.

El análisis incluye procesos de limpieza, tratamiento de registros inválidos e ingeniería de variables.

Metodología

El proyecto sigue un enfoque basado en CRISP-DM e incluye:

Comprensión del problema de negocio.

Exploración y preparación de datos.

Segmentación de clientes mediante RFM y K-Means.

Desarrollo de sistemas de recomendación.

Evaluación y comparación de modelos.

Interpretación de resultados y recomendaciones comerciales.

Modelos evaluados

Se comparan tres estrategias de recomendación:

Top-Sellers (productos más vendidos).

Filtrado colaborativo Usuario-Usuario.

Filtrado colaborativo Ítem-Ítem.

Resultados principales

El modelo Usuario-Usuario obtuvo el mejor desempeño global en el conjunto de prueba:

Precision@5: 0,0515

Recall@5: 0,0078

HitRate@5: 0,1874

Estos resultados corresponden a la evaluación global y no implican que el mismo modelo sea superior en todos los segmentos de clientes.

Tecnologías utilizadas

Python

Pandas y NumPy

Scikit-learn

Matplotlib

Jupyter Notebook / Google Colab

Cómo ejecutar el proyecto

Abrir el archivo Proyecto_Integrador_EntregaFinal.ipynb en Google Colab o Jupyter Notebook.

Verificar que estén instaladas las bibliotecas necesarias.

Comprobar que el conjunto de datos esté accesible desde la fuente indicada en el notebook.

Ejecutar todas las celdas en orden.

Revisar los resultados de segmentación y evaluación de los modelos.

Limitaciones

Los resultados se obtuvieron a partir de un conjunto de datos histórico. Las métricas de recomendación representan una evaluación offline y no garantizan incrementos reales de ventas.

Para validar el impacto comercial sería necesario realizar pruebas adicionales en un entorno de negocio.

Proyecto académico

Trabajo Integrador Final de la Diplomatura en Ciencia de Datos – UTN.
