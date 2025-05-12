# Proyecto_Demanda_Farmacia
Crear un modelo con la capacidad de predecir la cantidad de medicamentos que se van a vender con el fin de optimizar la gestión del inventario.

# Ruta del proyecto

## 1. Definición del problema
Objetivo: Predecir cuántas unidades de cada medicamento del laboratorio Kern hay que comprar mensualmente.

Datos: Ventas mensuales por producto (2020–2024).

Salida esperada: Tabla con predicción de ventas futuras (por ejemplo, para 2025), por medicamento.

## 2. Exploración y preparación de los datos
Cargar y concatenar los datos históricos (una fila por producto, columnas por mes).

Validar tipos de datos, valores nulos, outliers.

Convertir a formato long: ['Producto', 'Fecha', 'Unidades'].

## 3. Análisis exploratorio
Evolución de ventas por medicamento y en total.

Estacionalidad: meses con más o menos ventas.

Tendencia a lo largo de los años.

## 4. Modelado (series temporales)
Opción 1: Prophet (recomendado si el dataset es pequeño)
Modelo de Facebook, muy bueno para datos con estacionalidad y festivos.

Entrenar un modelo por medicamento.

Opción 2: LSTM/GRU (Deep Learning)
Requiere secuencias y más datos por serie. Mejor para patrones complejos.

Mayor carga computacional.

Opción 3: ETS / ARIMA / SARIMA
Modelos clásicos, útiles para series con tendencias claras y datos suficientes.

## 5. Evaluación del modelo
División entrenamiento/test (por años).

Métricas: RMSE, MAE, MAPE.

Visualizar predicciones vs. ventas reales.

## 6. Optimización con descuentos por escalado
Agregar lógica que, dado el precio y descuentos por volumen, recomiende:

Cuánto pedir

En qué momento del mes pedirlo

Para maximizar beneficio o minimizar coste

## 7. Visualizaciones para portfolio
Gráficos claros: evolución, predicción, errores, comparación modelos.

Dashboard si lo deseas (con Streamlit, por ejemplo).

## 8. Documentación y entrega
README con objetivo, metodología, resultados.

Código limpio y estructurado (Notebook o script).

Dataset de ejemplo incluido (no confidencial).

