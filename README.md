# Proyecto analítica Black-Friday

## Introducción

Nuestro caso de Estudio fue el análisis de ventas en período de Black Friday para la cadena de supermercados/e-commerce Walmart

## Recordamos brevemente nuestros objetivos:
- Analizar las ventas de Black Friday en el período 2014-2017, determinado por nuestro dataset
- Determinar los productos más vendidos
- Predecir las ventas para 2018


## EDA

Para comenzar el análisis, creamos nuevos data sets con las variables a estudiar. 
Como nuestro objetivo era analizar las ventas de Black Friday en los años que nos daba el data set, lo filtramos por año, mes y días exactos en el que cayó esta fecha. También filtramos por categoría para ver cuáles fueron las que más se vendieron. Llegamos a nuestro data set final, con una menor cantidad de valores que el original.

Con el fin de visualizar los resultados obtenidos de los diferentes data sets que creamos, usamos barplots, plots y boxplots.

### Conclusiones que sacamos del análisis de los gráficos:

 1.	Sales and Category: La categoría que más se vendió fue Technology, seguida de Furniture. La que menos se vendió fue Office Supplies.

2.	Sales and Year: a medida que pasan los años van aumentando las ventas de cada año. Leve disminución en 2015, pero luego siguen aumentando.

3.	Sales by Year and Month: menos en 2015, podemos ver que los meses en los que más se vende son noviembre y diciembre. Puede explicarse por fechas como cyber monday, black friday y además las fiestas.

4.	Sales by Category and Year: Menos en 2015, la categoría más vendida es siempre Technology (en 2015 la más vendida es Furniture). Menos en 2017, office supplies es la categoría menos vendida (en 2017 la menos vendida es furniture)


## Correlación

Al llegar al análisis de la correlación, nos dimos cuenta de que en nuestro EDA faltaban datos, por lo que tuvimos que profundizar un poco más en lo que fue la limpieza de los datos, eliminando filas innecesarias y creando algunos más pequeños para ver con mayor claridad lo que queríamos.

Usando el corr_matrix, calculamos el coeficiente de correlación de Pearson.
Sabemos que, mientras más cercano a uno es el valor del CP, más alta es la correlación/asociación entre variables.

### Observamos que:

1.	La mayor correlación se da entre Sales y Year. Hay una relación entre la cantidad de ventas y el año. Recordemos lo observado en las gráficas.

2.	Luego, dentro de las categorías, la mayor correlación se da entre sales y Technology (coincide con lo que observamos en los gráficos), lo sigue furniture y por último office supplies.

3.	A pesar de esto, los coeficientes obtenidos no son tan cercanos a 1 e incluso hay resultados negativos, lo que indica que la relación entre las variables no es tan cercana.

## Modelos
Para el modelo de una variable, relacionamos Sales and Year. Hicimos 3 modelos para comparar y ver cuál se ajusta mejor a los puntos obtenidos en cada uno.

1.	Polinomio de grado 1: El ajuste es bastante bueno. Si miramos el R^2 es 0.86, se acerca bastante a 1. Sin embargo, viendo la gráfica, hay puntos como el de 2015 que se aleja bastante de la recta.

2.	Polinomio de grado 2: El ajuste es mejor. Si miramos el R^2, es 0.96 y se acerca aún más a 1 que el primer modelo. Viendo la gráfica, los puntos se acercan de manera más uniforme a la curva.

3.	Polinomio de grado 5: Aunque el R^2 es 0.99, no sería correcto utilizar este modelo, ya que estaríamos forzando al mismo a ajustarse a todos los puntos.

Elegimos el polinomio de grado 2 ya que es el que mejor se ajusta.

## Predicción
Luego de haber seleccionado el modelo, hicimos la predicción de ventas para el año 2018 el cual era uno de nuestros objetivos. De acuerdo al resultado obtenido, vemos que es mayor a las ventas del 2017 mostradas en la diapositiva. Acá también se ve reflejada la tendencia al aumento de las ventas a medida que pasan los años, la cual se puede explicar por:

1.	Mejora de las plataformas (las compras por internet son más rápidas y seguras)

2.	Ventajas para los usuarios (Comodidad que ofrece la compra online, no hay necesidad de ir hasta una tienda y menos pérdida de tiempo)

3.	Mayor cantidad de usuarios en internet a medida que pasan los años.

## Conclusión

A pesar de haber tenido inconvenientes para encontrar el data set y luego en la limpieza de datos, creemos que supimos superar las dificultades que fueron surgiendo a lo largo del análisis, llegamos a sacar conclusiones coherentes a los resultados obtenidos y también a la realidad y aprendimos no solo a entender el negocio sino también a trabajar en equipo.





