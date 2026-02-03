
#####2026-01-29: Práctica 1

cd .. -> para ir al directorio anterior
Por ejemplo en 4º tengo dos opciones, entonces, pongo una S + Tab y me lleva a la carpeta 4º SEGUNDO CUATRI

cd ~ -> para volver al inicial
cd $HOME

mv ~/Downloads/epe ~/Documents/ mover el archivo epe de Downloads a Documents luego ya meterlo donde quiera. 

cp ../../.. para subir varios niveles
 ls -1 -> ver que hay en el directorio donde estas

> sirve para dirigir un output a un archivo

#####2026-02-02 TEORÍA: presentación de alineamientos

Explicación de lo que es el alineamiento. Hay alineamientos globales y locales.

El algoritmos de Needleman-Wunsch nos proporciona el mejor alineamiento posible. La idea de las tablas de puntuación es comparar los residuos de una secuencia y de la otra, si es el mismo suma x puntos, pero si no es el mismo se resta x puntos, porque sería equivalente a una mutación.
Hay diferentes esquemas de puntuación depende en cada caso. 

PAM250 sería la matriz entre cambios esperados en secuencias que han acumulado 250 mutaciones por cada 100 aminoácidos. Siguen siendo esquemas de puntuación, que nos ayuda a linear proteínas, la cosa es que no es lo mismo intentar alinear 2 proteínas que se midieron hace pocos años, que otras que se recogieron muestras hace millones de años.

Las BLOSUM, en la actualidad, son más usadas que las PAM. 
BLOSUM90, matriz construido con los datos observados entre bloques de proteínas que comparten el 90% de los residuos. 

Alineamiento local:
El algoritmo de Smith-Waterman es de alineamiento local y las puntuación no depende de la proteína tal, empieza en una región y acaba en otra, busca regiones de homología máxima.

Alineamiento múltiple: 
Alineamiento de más de dos secuencias, hoy en día miles de secuencias. Se usa el algoritmo CLUSTAL. Cuando se alinean múltiples secuencias el resultado no tiene porque ser el óptimo. Se hace un alineamiento progresivo, empieza con las más semejantes y mediante un árbol guía determina el orden de incorporación de secuencias en el alineamiento.
Dependiendo del árbol guía se llegan a conclusiones diferentes.

Al autor de MUSCLE no le mola esa aleatoriedad, por así decirlo, entonces proporciona una estrategia para poder hacer alineamientos con diferentes árboles guía para saber si las conclusiones corresponden con el alineamiento y si los resultados finales son coherentes. 
Repetir en bucle el esquema de MUSCLE hasta encontrar el alineamiento bueno. 
Affine gap: pide la penalización por abrir un gap y otra por extenderlo, por abril es más grave que por extenderlo. 

#####2026-02-03: Práctica 2











