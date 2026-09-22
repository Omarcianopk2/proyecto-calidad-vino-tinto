# Proyecto 1: Predicción de la calidad del vino tinto

Laboratorio de Aprendizaje Estadístico, ITESO. Omar Mendoza (757806) y Carlos Nieves (758210).

- `proyecto_calidad_vino_tinto.ipynb`: notebook con el reporte completo y el código.
- `winequality-red.csv`: dataset (Wine Quality, UCI Machine Learning Repository).
- `Presentación calidad del vino.pdf`: presentación tal como se expuso.
- `Presentación con correcciones.pdf`: misma presentación con dos precisiones que surgieron durante la exposición, ya corregidas (slide 16).

## Correcciones después de la presentación

1. **Qué explica el R².** Se dijo que el modelo "explica el 40 % de la calidad". Lo correcto: el R² es la proporción de la **varianza** de la calidad que explica el modelo. El modelo 2 explica el 41.6 % de la varianza de la calidad en prueba.

2. **Sesgo.** A la pregunta sobre el sesgo se respondió con el sesgo (asimetría) de las variables, que fue lo que motivó la transformación logarítmica (chlorides 5.5, residual sugar 4.6, sulphates 2.4, total y free SO₂ 1.5 y 1.2). Lo que se preguntaba era el sesgo del modelo en el intercambio sesgo–varianza: la regularización agrega un poco de sesgo a cambio de reducir varianza. En el modelo 1 se ve directamente: con Lasso el R² de entrenamiento baja de 0.3582 a 0.3554 (sesgo agregado) y el de prueba sube de 0.3921 a 0.3982 (varianza reducida). OLS sin penalización es el estimador insesgado, por eso la significancia se evalúa ahí.
