# VALORES, TIPOS Y OPERADORES

Toda la información guardada en una computadora se conoce como datos. Estos datos pueden ser creados, modificados o eliminados y son almaenados como largas secuencias de 'bits'.
 Un bit es cualquier cosa que úeda representarse con '0' y '1' (binario). Estos dígitos toman forma de cargas eléctricas (altas o bajas), a señales (fuerte o débil) o puntos brillantes. Cualquier tipo de información discreta es posible convertirla a un sistema binario.

<br>

## VALORES

Al tener una computadora la capacidad de almacenar y procesar billones de bits, *JavaScript* los separa en porciones a las que llama ***VALORES***. Si bien todos los valores están hechos de bits, *Javascript* tiene un rol determinado.

Estos valores se utilizan únicamente **declarándolos** (es decir, nombrándolos), sin la necesidad de declarar un espacio en memoria o el largo del mismo, además de tener la particularidad de disipar su espacio en memoria si no está en uso, permitiendo usar los bits que se les había asignado para otros usos.

<br>

### Números
Los valores ***number*** son aquellos que contienen números como contenido. Estos se escriben de la siguiente manera:

```
13
```
A los números enteros los vamos a denominar como **Integers**.

Javascript utiliza **64 bits de memoria para crear un solo número** , por ende, la cantidad de datos *number* que pueden almacenarse en memoria está limitada a la capacidad de almacenamiento de nuestra computadora.

Otro tipo de valor numérico que puede almacenar son los fraccionarios o decimales que se escriben de esta forma:

```
9.81
```

Además, podemos crear numeros con exponentes (mayores o menores) que también son considerados del tipo numérico, para ello, escribimos el valor, seguido de la letra *e* (de exponente) y el número por el cuál será elevado:

```
2.998e8 
```
Valor equivalente a 2.998 x 10(8) = 299,800,00

<br>

#### Aritmética
Es sumamente común realizar operaciones aritméticas como la suma, la resta, la multiplicación o la división para generar un nuevo valor a raíz de otros. En *JavaScript* lo podemos representar de la siguiente manera:

```
100 + 4 * 11
```
Recordemos que existen jerarquias en los operadores, en este caso, se realiza primero la multiplicación y luego la suma. Sin embargo, es posible realizar la suma primero **siempre y cuándo se englobe entre paréntesis**:

```
(100 + 4) * 11
```

<br>

##### Operadores lógicos y su uso

       || * = Multipliación
       || / = División
       || % = Residuo
        | + = Suma
        | - = resta
       
La jerarquía al realizar una operación determina que multiplicación y división tienen la misma prioridad mayor que la suma y la resta. Si tenemos dos operadores con la misma prioridad juntos el orden será de izquierda a derecha:

```
1 - 2 + 1
```
En este ejemplo, como la suma (+) y la resta (-) tienen el mismo nivel de prioridad se comienza a leer de izquierda a derecha y primero se realiza la resta para posteriormente seguir con la suma.

<br>

#### Números especiales

Existen 3 valores especiales en Javascript que son considerados números pero no se comportan como tal.

Los primeros dos son `Infinity` e `-Infinity` que representan números infinitos tanto positivos como negativos. No es recomendado utilizar estos valores por su amplitud y muy seguramente terminen en el siguiente tipo: `NaN`.

`NaN` (del inglés ***Not a Number** / No rd un número), es considerado un valor numérico pero únicamente será devuelto cuando alguna operación aritmética nos devuelva valores no significativos como dividir 0/0.

<br>
<br>

### Strings