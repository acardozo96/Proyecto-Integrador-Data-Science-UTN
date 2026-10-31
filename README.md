# Proyecto-Integrador-Data-Science-UTN
Segmentación RFM y sistema de recomendación de productos para e-commerce utilizando Python y Machine Learning.
Descripción del proyecto
Este proyecto analiza datos transaccionales de una empresa de comercio electrónico con el objetivo de identificar diferentes perfiles de clientes y evaluar sistemas de recomendación de productos mediante técnicas de ciencia de datos y aprendizaje automático.

El propósito es proporcionar herramientas analíticas que permitan diseñar estrategias de marketing personalizadas, mejorar la experiencia de compra y contribuir a la toma de decisiones comerciales.

2. Objetivos del proyecto

Objetivo general:

Desarrollar una solución analítica que combine segmentación de clientes y sistemas de recomendación de productos para apoyar las estrategias comerciales de una empresa de e-commerce.

Objetivos específicos:

Explorar y preparar los datos transaccionales.

Identificar patrones de compra y comportamiento de los clientes.

Segmentar clientes mediante el análisis RFM y el algoritmo K-Means.

Implementar y comparar diferentes sistemas de recomendación.

Evaluar el desempeño mediante métricas cuantitativas.

Proponer estrategias comerciales basadas en los resultados obtenidos.

3. Conjunto de datos utilizado

Se utiliza el conjunto de datos Online Retail, que contiene información histórica de transacciones comerciales.

Características principales:

Registros originales: 541.909.

Registros después de la limpieza: 397.884.

Clientes identificados: 4.338.

Productos identificados: 3.665.

Variables principales:

InvoiceNo: identificador de factura.

StockCode: identificador de producto.

Description: descripción del producto.

Quantity: cantidad adquirida.

InvoiceDate: fecha de transacción.

UnitPrice: precio unitario.

CustomerID: identificador del cliente.

Country: país de la transacción.

Durante la preparación de los datos se aplicaron procedimientos de limpieza, tratamiento de registros inválidos e ingeniería de variables.

4. Metodología

El proyecto sigue un enfoque basado en CRISP-DM, organizado en las siguientes etapas:

Comprensión del problema de negocio.

Comprensión y exploración de los datos.

Preparación y limpieza del conjunto de datos.

Modelado mediante segmentación y recomendadores.

Evaluación y comparación de resultados.

Interpretación comercial y recomendaciones futuras.

5. Segmentación de clientes mediante RFM

Se utiliza el análisis RFM para estudiar tres dimensiones del comportamiento de compra:

Recency: tiempo transcurrido desde la última compra.

Frequency: frecuencia de compra.

Monetary: valor monetario de las compras.

Posteriormente, se aplica el algoritmo K-Means para identificar cuatro segmentos comerciales:

VIP / Alto valor: clientes con mayor frecuencia y gasto.

Leales / Frecuentes: clientes con compras recurrentes.

Nuevos / Prometedores: clientes recientes con potencial de desarrollo.

En riesgo / Inactivos: clientes con mayor tiempo desde su última compra.

Se evaluaron distintas cantidades de clústeres mediante la métrica Silhouette. Aunque K=2 presentó un valor superior al de K=4, se seleccionaron cuatro segmentos por su mayor utilidad e interpretabilidad comercial.

6. Sistemas de recomendación evaluados

Se implementaron tres estrategias:

6.1. Top-Sellers

Modelo de referencia que recomienda productos populares a partir del historial de compras.

6.2. Filtrado colaborativo Usuario-Usuario

Identifica similitudes entre clientes y genera recomendaciones basadas en los comportamientos de compra de usuarios semejantes.

6.3. Filtrado colaborativo Ítem-Ítem

Analiza relaciones de similitud entre productos para recomendar artículos relacionados con las compras anteriores.

7. Evaluación de los modelos

Para evaluar los recomendadores se utilizó una separación temporal de los datos en entrenamiento, validación y prueba.

Las principales métricas utilizadas fueron:

Precision@5: proporción de recomendaciones acertadas entre los cinco productos sugeridos.

Recall@5: proporción de productos relevantes recuperados.

HitRate@5: proporción de clientes que recibieron al menos una recomendación acertada.

Resultados en el conjunto de prueba

Modelo

Precision@5

Recall@5

HitRate@5

Top-Sellers

0,0375

0,0052

0,1624

Usuario-Usuario

0,0515

0,0078

0,1874

Ítem-Ítem

0,0438

0,0065

0,1666

Resultado principal:

El modelo Usuario-Usuario obtuvo el mejor desempeño global y fue seleccionado previamente utilizando el conjunto de validación.

Sin embargo, su superioridad global no implica que sea el modelo más efectivo en todos los segmentos RFM. En el segmento VIP / Alto valor, por ejemplo, el modelo Ítem-Ítem obtuvo una Precision@5 superior en el conjunto de prueba.

8. Impacto esperado en el negocio

Los resultados permiten identificar oportunidades para:

Personalizar las recomendaciones de productos.

Diseñar campañas comerciales diferenciadas por segmento.

Mejorar la relevancia de las ofertas dirigidas a los clientes.

Apoyar estrategias de fidelización y reactivación.

Orientar futuras pruebas de personalización comercial.

Los beneficios económicos planteados en el informe corresponden a escenarios hipotéticos y no representan incrementos de ventas comprobados experimentalmente.

9. Tecnologías utilizadas

Python.

Pandas.

NumPy.

Scikit-learn.

Matplotlib.

SciPy.

Jupyter Notebook.

Google Colab.

10. Estructura del repositorio

El repositorio contiene el notebook principal del proyecto, el presente archivo README y los demás documentos de entrega incorporados.

Archivo principal de código:

Proyecto_Integrador_EntregaFinal.ipynb

11. Instrucciones para ejecutar el proyecto

Opción A: Google Colab

Ingresar a https://colab.research.google.com/

Seleccionar la opción para abrir un notebook desde GitHub.

Buscar este repositorio y seleccionar Proyecto_Integrador_EntregaFinal.ipynb.

Conectar el entorno de ejecución de Python.

Verificar la disponibilidad de las bibliotecas utilizadas y el acceso al dataset.

Ejecutar todas las celdas en orden.

Revisar las tablas, gráficos, segmentos RFM y métricas de evaluación.

Opción B: Ejecución local

Descargar o clonar el repositorio.

Abrir el archivo .ipynb mediante Jupyter Notebook o Visual Studio Code.

Configurar un entorno de Python con las dependencias necesarias.

Verificar la ruta o URL del conjunto de datos.

Ejecutar las celdas secuencialmente.

La reproducción de los resultados requiere utilizar los mismos datos, procedimientos y parámetros definidos en el notebook.

12. Riesgos y limitaciones

Los resultados corresponden a una evaluación offline realizada sobre datos históricos.

El desempeño predictivo no garantiza automáticamente un incremento de ventas.

Las preferencias y hábitos de compra pueden cambiar con el tiempo.

Los segmentos RFM representan perfiles analíticos y no categorías permanentes.

Las recomendaciones requieren validación adicional mediante experimentos comerciales.

En una implementación real se deben considerar medidas de protección de datos, privacidad y uso responsable de la información de clientes.

13. Conclusiones

La combinación del análisis RFM, el algoritmo K-Means y los sistemas de recomendación permitió identificar perfiles comerciales y comparar alternativas de personalización de productos.

El modelo Usuario-Usuario presentó el mejor desempeño global en la evaluación realizada, mientras que el análisis por segmentos mostró diferencias relevantes entre estrategias.

Como siguiente etapa, se recomienda validar los resultados en un entorno comercial, analizar el comportamiento por segmento y medir el impacto real sobre indicadores de negocio.

Proyecto Integrador Final – Diplomatura en Ciencia de Datos – UTN
