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
Los valores *string* son utilizados para representar **textos**. Su contenido esencerrado en comillas, ya sean simples, dobles o invertidas siempre y cuando coincidan al inicio y al cierre del string:

```
`Debajo en el mar`
"Descansa en el océano"
'Flota en el océano'
```

También es posible agregar saltos de línea o *Newlines* a un string utilizando una barra o diagonal invertida (Este caracter le indica al programa que será seguida por otro caracter que tendrá un valor especial). Si queremos dar un espacio utilizamos la combinación **\n**, si quisieramos tabular usamos la combinación **\t** y si dentro de un texto encapsulado en un string queremos agregar otras comillas usamos **\ (la comilla que queremos agregar)**. Por ejemplo:

```
ESCRITURA DEL STRING: 
"Esta es la primera línea\nY esta es la segunda "


RESULTADO FINAL:
Esta es la primera linea
Y esta es la segunda
```

Si quisieramos hacer que una barra invertida o \ aparezca en nuestro string debe ser precedida por otra barra similar, Por ejemplo;

```
ESCRITURA DEL STRING: 
"Un caracter de salto de línea es ecrito así: \"\\n\"."


RESULTADO FINAL:
Un caracter de salto de línea es escrito así: "\n".
```

Al igual que los valores *number*, los Strings son modelados como una serie de bits. Este modelado se basa en el estándar **Unicode**, el cuál asigna un valor numérico a todo caracter existente, incluidos en Griego, Árabe, Japones, Armenio, etc. por ende, podemos decir que un String es una secuencia de números.

No es posible realizar operaciones aritméticas con los strings, sin embargo, utilizamos el operador **+** para agregar cadenas de strings seguidas unas de otras. A este proceso de le conoce como ***Concatenar***

```
ESCRITURA DEL STRING: 
"con" + "ca" + "te" + "nar"

RESULTADO FINAL:
concatenar
```

##### Comillas invertidas o plantillas literales:

Al usar comillas invertidas, simples o dobles notamos que no nos generará ningún problema, sin embargo, sí pueden tener funcionalidades diferentes.

Al usar comillas invertidas para englobar un string podemos utilizar `${}` para realizar una operación aritmética dentro de un string y devolver el resultado como un string:

```
ESCRITURA DEL STRING: 
`La mitad de 100 es ${100 / 2}`

RESULTADO FINAL:
La mitad de 100 es 50
```

<br>
<br>

### Operadores

<br>

#### Operadores unitarios y binarios

Anteriormente vimos que a los signos que usamos para realizar operaciones les llamamos *operadores*, sin embargo, no todos son signos.

Existen operadores que se escriben con palabras como `typeof` que produce un string con el tipo de valor que le demos:

```
console.log(typeof 4.5)
--> number

console.log(typeof "x")
--> String
```

Como podemos darnos cuenta, `typeof` funciona con un solo valor a diferencia de los anteriores operadores que necesitan por lo menos dos. A aquellos operadores que funcionan con un solo valor se les llama ***unitarios*** y a los que requieren dos se les llama ***binarios***. Existe un operador que puede ser unitario y binario al mismo tiempo y ese es el signo menor (-): 

```
console.log(-(10-2))
--> -8

```