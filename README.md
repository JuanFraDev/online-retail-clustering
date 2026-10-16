# Segmentación de clientes mediante Machine Learning

Proyecto de aprendizaje automático no supervisado que utiliza técnicas de clustering para identificar patrones de comportamiento en clientes de comercio electrónico.

## Dataset

Se utiliza **Online Retail**, disponible en UCI Machine Learning Repository, con 541.909 registros de transacciones comerciales realizadas entre 2010 y 2011.

Fuente: https://doi.org/10.24432/C5BW33

## Metodología

El proyecto comprende análisis exploratorio de datos, limpieza de transacciones, construcción de características RFM, selección de características por correlación, transformación logarítmica y estandarización.

Se implementan K-Means y Gaussian Mixture Models mediante pipelines de scikit-learn, optimización de hiperparámetros con Repeated K-Fold, comparación estadística exploratoria con Wilcoxon, curvas de aprendizaje y visualización con t-SNE.

## Resultados

K-Means fue seleccionado como modelo final, obteniendo un Silhouette Score de **0,41** sobre el conjunto de reserva.

Se identificaron dos segmentos entre 4.317 clientes:

- Clientes ocasionales o de menor actividad: 59,74 % de los clientes y 14,65 % del gasto neto.
- Clientes frecuentes de alto valor: 40,26 % de los clientes y 85,35 % del gasto neto.

## Reproducibilidad

1. Clonar este repositorio.
2. Crear un entorno virtual de Python 3.12.
3. Instalar las dependencias con `pip install -r requirements.txt`.
4. Descargar `Online Retail.xlsx` desde UCI y colocarlo en `data/raw/`.
5. Abrir el notebook ubicado en `notebooks/` utilizando VS Code, Jupyter o Google Colab.
6. Ejecutar las celdas secuencialmente.

El archivo original del dataset no se incluye en este repositorio; puede descargarse desde su fuente oficial.

## Limitaciones

Las agrupaciones representan patrones históricos de compra y no necesariamente predicen abandono, rentabilidad o respuesta a campañas. Los resultados estadísticos sobre particiones repetidas se interpretan de forma exploratoria.

## Tecnologías

Python, Pandas, NumPy, Matplotlib, Seaborn, scikit-learn, SciPy, Jupyter y VS Code.