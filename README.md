[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/753uUyVk)

Juan Sebastian Rojas y Santiago Becerra

Respuestas Preguntas

1. ¿Por qué arreglo se pasa como const?

Cuando pasamos un arreglo como parámetro en C++, en realidad pasamos un puntero al primer elemento del arreglo.
Si no se especifica const, dentro de la función sería posible modificar los elementos del arreglo, aunque la intención sea solo consultarlos (por ejemplo, al calcular el promedio).

Al usar const double arreglo[] , se garantiza que los valores no podrán modificarse dentro de la función, lo que protege la integridad de los datos e indica claramente que la función solo va a leer el arreglo, no cambiarlo. Esto es una buena práctica para evitar errores y dejar claro el propósito del parámetro.

2. ¿Por qué es necesario pasar tamaño como un parámetro separado?

En C++ los arreglos no guardan información de su tamaño cuando se pasan como parámetros a una función.

Ejemplo: void funcion(double arreglo[]);

Aquí, dentro de funcion, el parámetro arreglo se convierte en un puntero (double*), y el compilador ya no sabe cuántos elementos contiene.

Por eso es necesario pasar el número de elementos (tamano) como un argumento adicional, para que la función sepa hasta dónde debe recorrer el arreglo sin salirse de sus límites.

