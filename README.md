# Parcial-ALSE-T1

## Descripción
Este programa en C++ permite trabajar con puntos en un plano 2D.
Dado un conjunto de puntos y un punto de referencia ingresado por el usuario, el programa determina cuál de los puntos se encuentra más cerca del punto de referencia.
El cálculo se realiza utilizando la distancia entre puntos en el plano, comparando cada punto del conjunto hasta encontrar el más cercano.

## Función Implementada
La función principal del parcial:
- Recibe un arreglo de puntos.
- Recibe la cantidad total de puntos.
- Recibe un punto de referencia.
- Recibe una variable donde se almacenará la posición del punto más cercano.

La función realiza los siguientes pasos:
1. Verifica que exista al menos un punto en el arreglo.
2. Calcula la distancia entre el punto de referencia y cada punto del conjunto.
3. Compara todas las distancias.
4. Identifica la menor distancia.
5. Guarda el índice del punto más cercano.
6. Retorna la distancia mínima encontrada.

## Uso
Para utilizar la función correctamente:
- Definir un conjunto de puntos.
- Indicar cuántos puntos contiene el arreglo.
- Definir el punto de referencia.
- Llamar a la función pasando estos valores.

La función devolverá la distancia mínima y almacenará la posición del punto más cercano.
