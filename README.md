# **Salto de lo clásico a lo cuántico**

Para iniciar y comprender el salto de lo clásico a lo cuantico lo ejemplificamos con un experimento o "juego de las piquis".

Entender la teoría de grafos facilita entender este salto.

## ¿En qué consiste este juego?

Ubicamos diversas "cajas" en las que colocaremos una cantidad de "piquis", que cada cierta cantidad de tiempo se moveran entre "cajas".

La cantidad que se mueve entre cada caja es establecida previamente, se pueden dirigir a varias o tan solo a una, así mismo, no recibir de ninguna.

Plantearemos el siguiente ejemplo:

- Definiremos 6 cajas, nombradas con las letras de la A a la F

- La cantidad que se mueven entre ellas serán las siguientes:
  
  - De A la totalidad se dirigirá a B.
  
  - De B la totalidad se dirigirá a C.
  
  - De C la totalidad se dirigirá a E.
  
  - De D la totalidad se dirigirá a B.
  
  - De E la mitad se dirigirá a D, la otra mitad a F.

## ¿Cómo lo extrapolamos a Grafos?

Consideramos cada caja como un nodo del grafo, las dirección a donde se mueven las piquis son los arcos, y la cantidad de la misma que se mueve es el peso del arco. Por lo que el resultante del experimentado planteado previamente es:

![](https://github.com/NicolasPrieto12/cnyt2-T/blob/main/Grafos.png)

Ahora, al relacionarlo con el mundo cuántico, se agregan unas ciertas normas a estos grafos:

- Los pesos de los arcos son el porcentaje del movimiento de un nodo a otro, por lo que la suma de estos debe ser igual a 1, no más, no menos.

- La única excepción a la regla anterior es en que no se presente movimiento que tenga como origen al nodo.

- La suma de la cantidad de "piquis" o particulas, según el sistema, siempre debe de ser el mismo, no pueden desaparecer del sistema ni provenir de alguna otra forma.

Así mismo, este grafo se puede representar en una matriz, del caso que estamos llevando, es la siguiente:

![](https://github.com/NicolasPrieto12/cnyt2-T/blob/main/Matriz.png)

Para poder inicializar el sistema, se debe de definir un estado inicial, que debe de ser un vector, de dimensión igual a la cantidad de filas de la matriz del sistema.

Este puede tener las cantidades iniciales de piquis deseada en las posiciones deseadas:

![](https://github.com/NicolasPrieto12/cnyt2-T/blob/main/Vector.png)

## ¿Cómo se simula el paso del tiempo en el sistema?

Aquí entramos ya en consideraciones de la librería, pues aunque el procedimiento es el mismo en todos los casos, se puede manejar y abarcar de diversas formas.

Consideramos a una matriz, un vector, y un entero.

Por lo que el funcionamiento principal lo llevará a cabo la función ``` SistemaProbabilistico(mat,vec,times) ``` en donde:

- mat := Matriz representante del sistema.

- vec := Vector representante del estado inicial del sistema.

- times := Entero representando el paso del tiempo o clics, indicando este el movimiento de las piquis.



### Ejecutar Test.

- Clonar repositorio ``` git clone  ```

- Cambiar directorio ``` cd Segundo Corte/ClassicToQuantum ```

- Ejecutar .py correspondiente ``` py TestClassicToQuantum.py ```

### ¿Salta un error indicando que faltan librerías?

Es un error común considerando que usamos librerías como numpy, scipy y matplotlib, se __deben__ seguir los pasos indicados en el [siguiente video]( https://www.youtube.com/watch?v=oE4KeuVNqcQ&list=LLwZJu6f8CavefyakHGC1HEw).
