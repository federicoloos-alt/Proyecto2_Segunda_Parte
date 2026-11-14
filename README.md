# Proyecto2_Segunda_Parte
Descripción
Modelo de Regresión Lineal Múltiple que predice la tasa de natalidad en 2024 
(nacimientos por cada 1.000 personas) a partir de la natalidad en 1960, 1980 y 2000.

Conclusiones

¿Cuál fue el desempeño del modelo?
Fue bueno. En Test el R2 fue de 0,895: el modelo explica casi el 90 % de las variaciones de la natalidad en 2024. 
El error promedio (MAE) fue de 2,2 nacimientos por cada 1.000 personas y el RMSE de 3,2. 
Como la natalidad promedio en 2024 es de unos 17 y varía mucho entre países (desde 4 hasta 46), ese error es chico.

¿Qué variable fue la más influyente según los coeficientes del modelo?
La natalidad del año 2000 (coeficiente 0,81), muy por encima de las otras dos (1980: 0,06 y 1960: −0,12). 
Se pueden comparar los coeficientes directamente porque las tres variables están en la misma unidad. 
Cuanto más cerca en el tiempo, más parecida es la natalidad a la actual. 
El coeficiente negativo de 1960 no quiere decir que más natalidad en 1960 baje la de hoy: 
las tres variables están muy relacionadas entre sí y el modelo reparte el peso entre ellas.

¿Las features extraídas del dataset fueron buenas predictoras? ¿Sugieren otras?
Sí, sobre todo la de 2000 (correlación de 0,95 con 2024). La de 1960 aporta poco (correlación de 0,68). 
Aun así, usar la natalidad de otros años es una solución limitada, porque solo mira el pasado de la misma variable 
y no explica por qué cambia la natalidad. Variables que podrían mejorar el modelo: 
PBI per cápita, nivel de educación, mortalidad infantil, porcentaje de población urbana 
y acceso a métodos anticonceptivos.

Comparativa de resultados con datos de Entrenamiento y de Test

| Métrica | Entrenamiento | Test |
|---|---|---|
| R2 | 0,917 | 0,895 |
| MAE | 1,987 | 2,217 |
| RMSE | 2,672 | 3,204 |

Los resultados en Test son un poco peores que en Entrenamiento (el R2 baja de 0,917 a 0,895 y
los errores suben un poco). Esa diferencia es chica, así que no hay sobreajuste, 
el modelo no memorizó los datos, sino que aprendió una relación que también funciona con datos nuevos.
