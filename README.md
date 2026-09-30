# Análisis de series de tiempo: ventas diarias

Exploración de una serie temporal de ventas diarias para entender su tendencia y preparar un modelo de pronóstico.

**Stack:** Python · pandas · statsmodels · matplotlib · seaborn

## Problema
Pronosticar la demanda permite planificar inventario y compras. El primer paso es entender el comportamiento de la serie.

## Datos
Ventas diarias a partir de septiembre de 2022 (columnas `date` y `sales`), con frecuencia diaria (`D`) verificada con `pd.infer_freq`.

## Enfoque
1. Conversión de fechas e indexación temporal.
2. Visualización de la serie y de la tendencia con media móvil de 12 periodos.
3. Prueba de estacionariedad de Dickey-Fuller aumentada (ADF).

## Resultados

| Prueba | Valor |
|---|---|
| Estadístico ADF | 0.545 |
| p-value | 0.986 |

Con un p-value de 0.986 **no se rechaza la hipótesis nula**: la serie **no es estacionaria** y muestra una tendencia creciente clara.

## Próximos pasos
- Diferenciar la serie y repetir la prueba ADF.
- Ajustar un modelo ARIMA (con `auto_arima`) y evaluar el pronóstico con MAE/RMSE.

## Estructura
```
├── src/explore.ipynb   # Análisis
└── requirements.txt
```
