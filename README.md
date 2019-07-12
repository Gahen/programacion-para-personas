## Consideraciones preliminares

Tal vez por colonización cultural - o simplemente por arbitrariedad histórica - el inglés se estableció como el idioma de los conceptos de la programación. Por ello, algunas palabras no las traduciremos ya que las tomaremos como conceptos del arte en si mismos, de la misma manera que en la música no se traduce "presto" a "lento" y en la danza clásica se nombran las posturas en francés.


Algunas palabras se usarán sin explicarlas en el sentido entendido comunmente, por ejemplo "archivo", "ejecutar un programa".

Sin embargo, siempre que sea posible las traduciremos y pueden preguntar cualquier palabra o concepto que necesite una mejor aclaración.

## ¿Qué es programar?

De manera simple, podríamos decir que **programar** es "la acción de decirle qué tareas realizar a una computadora". Un **programa informático** es, a su vez, una serie de instrucciones que la computadora ejecuta. Por **computadora** nos referimos a cualquier dispositivo capaz de procesar **código**, como tablets, celulares y notebooks.

## Código

Llamamos así al objeto que moldeamos al programar, lo que constituirá, una vez terminado, el programa informático que será procesado en la computadora. Siempre se lo llama en singular, no tiene sentido hablar de "los códigos".

/////////////////
//aclarar
## Lenguaje natural de las computadoras

Los equipos electrónicos se comunican en un lenguaje binario, la mínima unidad de información (bit) solo tiene 2 valores posibles, usualmente los representamos como 0 (apagado) o 1 (encendido). Así se encuentra la información almacenada en discos rígidos, unidades de memoria.

Si quisieramos comunicarnos directamente con una computadora, deberíamos poner en ciertas partes de la memoria ciertos bits en 0 y otros en 1 y luego esperar a que los procese. No sería agradable, eficiente, ni claro.

## Lenguajes de programación

Desde el comienzo de la informática, este problema fue evidente y se empezaron a crear diversos lenguajes que nos permitieran interactuar con computadoras de una manera que fácilmente comprensible para alguien nuevo al código y que nos permitiera modelar programas complejos sin tener que dar vuelta cientos de miles de bits individualmente.
///////////////////////

## Intérpretes y compiladores

Para que sean útiles, los lenguajes de programación necesitan otros programas que los conviertan al lenguaje de la computadora. A estos programas los llamaremos **intérpretes** y **compiladores**.

Un intérprete es un programa que toma lo que escribimos en nuestro lenguaje amigable y expresivo (eficiente, en términos de escribir poco y decir mucho) , lo traduce a binario para que la computadora lo ejecute y lo ejecuta inmediatamente. Seguirá ejecutándose hasta terminar o encontrar un error.

Un compilador hace algo similar al intérprete, pero se diferencia en que no ejecuta el código compilado de manera inmediata, sino que nos genera un archivo binario (el **programa** propiamente dicho) que luego podremos ejecutar cuando querramos. Terminará al procesar todo el código que le pedimos o al encontrar un error. En el último caso, no generará un archivo ejecutable.

Al terminar de correr todas las instrucciones - o al encontrar un error - el programa se cerrará. Mientras esté en ejecución, nuestro programa (binario o interpretado) reservará parte de los recursos físicos de la computadora: memoria, espacio en disco, capacidad de procesamiento. Al terminar, todos estos recursos vuelven a estar disponibles para los demás programas.

Actualmente, es común referirse a estos archivos compilados como **Apps**.

## ¿Qué lenguaje aprender primero?

//revisar
Python es el lenguaje más usado para aprender a programar. Si buscamos algo orientado al desarrollo web, se puede empezar por **Javascript**. Para lo demás también se usa mucho **Ruby**. Los tres son lenguajes interpretados, y por lo tanto amigables para empezar a aprender, ya que facilitan la experimentación ayudando a un rápido aprendizaje.
//

Los lenguajes interpretados suelen tener un **Command Line Interface** - o CLI interactivo - que permite probar rápidamente las expresiones que construyamos. Al ejectuarlo, veremos un **prompt** con un cursor parpadeante, y allí podremos introducir lo que queramos y evaluarlo apretando **enter**

```
$_
```

Los interpretes son programas, y por lo tanto es recomendable bajarse alguno de ellos y jugar un poco. Descargando el intérprete de python desde [el sitio oficial](http://python.org), se puede acceder al CLI ejecutando una terminal y escribiendo `python`. Para abrir una terminal en windows buscar la app `powershell` y en Mac la app `Terminal`

Un ejemplo de lo que haría en mi terminal de MacOS

```
micompu:ejemplo tumasj$ python
Python 2.7.16 (default, Mar  4 2019, 09:02:19)
[GCC 4.2.1 Compatible Apple LLVM 9.0.0 (clang-900.0.39.2)] on darwin
Type "help", "copyright", "credits" or "license" for more information.
>>>
```

y ya puedo ejecutar código Python:

```
>>> 2 + 2
4
>>>
```

## Código fuente

Llamaremos así al conjunto de archivos escritos en un **lenguaje de programación** que constituirán nuestro programa. Estos archivos estarán en texto plano y solo se diferenciarán de otros archivos de texto por su extensión y contenido. Los archivos de Python tendrán la extensión `.py`, los de Javascript `.js`, etc.

<!-- # META: Ejemplo corriendo un Hello World en Python -->

### Identificadores

Llamaremos así a las palabras que usaremos para identificar conceptos creados por programadores, nosotros mismos o que vengan de **Libraries** (bibliotecas) externas. Una **Library** agrupa un conjunto de funcionalidades para que un programador la reuse en su programa. Por ejemplo, una librería llamada "Math" de javascript nos permite hacer fácilmente (en términos de tiempo del programador) la raiz cuadrada de 5 escribiendo `Math.sqrt(5)`.

Llamamos **framework** a una librería que nos provee muchas funcionalidades y además nos sugiere una manera de estructurar el código, con el fin de ahorrar tiempo de desarrollo y tener un resultado más claro y mantenible. Como hay muchas opiniones diferentes de qué es "claro", "mantenible" - y si nos interesa o no la funcionalidad que un framework nos da, hay numerosos frameworks populares en cada lenguaje de programación.

### Keywords

Traducido usualmente como **palabras reservadas**, serán todas aquellas que tienen un significado estructural en el código fuente. Dependerán del lenguaje que estemos usando. En general los caracteres no alfabéticos son palabras reservadas y tienen significados especiales, por ejemplo: `[] {} , . ; () ! "" ''` y todos los símbolos matemáticos `+ - * / = < >`.

Las palabras reservadas ocupan el mismo espacio conceptual que los identificadores. Por ejemplo, `string` es una palabra reservada de Java, nadie puede crear un identificador con ese nombre.

### Variables

Las variables son lugares de la memoria a los que les ponemos un nombre y en donde guardamos información. Las variables son útiles para almacenar datos en el código, para que podamos volver a accederlos y usarlos cuando necesario. 

```python
palabras_escritas = 12345
```

### Constants

Las constantes guardan valores que no cambiarán a través del tiempo. Al igual que las variables debemos ponerle un nombre (por convención, en mayúsculas). No todos los lenguajes soportan la creación y uso de constantes.

```python
const NOMBRE_CHARLA = 'Introducción a la programación'
```

### Literals

Son valores que escribimos en el código como expresiones literales. En los ejemplos anteriores los estuvimos usando: `12345` es un valor literal que representa al numero 12345, bien como `'Introducción a la programación'`, que representa el texto "Introducción a la programación".

### Operators

**Hacer** operaciones con datos es el propósito de cualquier lenguaje de programación. Sorprendemente, llamamos a los elementos que nos permiten hacerlas "operadores". En general, tenemos las siguientes categorías:

- Aritméticos: para operaciones aritméticas. Algunos ejemplos: `+ - * /`
- De asignación: para determinar valores a variables y constantes, el `=` de los ejemplos anteriores. No confundir su significado con "igual a".
- Relacionales: para comparar valores. Ejemplos `a < b` compararía el valor de `a` y `b` y sería verdadero solo si `b` es mayor.
- Lógicos: para trabajar con lógica, escencialmente establecer condiciones respecto a valores que sabemos verdaderos o falsos. Ejemplo: `a && b` representa la afirmación "a y b" y será verdadero solo si ambos son verdaderos.

### Comentarios

Es muy importante que el código fuente sea claro - por ejemplo, para que alguien nuevo pueda entender como funciona la aplicaciòn. Para que eso sea posible, es esencial que haya una buena **documentación**. Una manera de lograrlo es añadiendo **comentarios** en las partes más importantes o que puedan ser confusas. Los intérpretes y compiladores ignoran los comentarios.

```python
# Esta variable siempre tendrá el número de palabras escritas actualizado
palabras_escritas = 12345
```

## Tipos de datos

Para poder guardar información en la memoria, por ejemplo usando los **literals** que vimos antes, el programa necesita saber el contenido y también el tipo de información que estamos guardando. De esta manera, `'hola'` sería de tipo `string` (cadena de texto) y `12345` sería de algún tipo numérico `number`. Cada lenguaje tiene sus tipos asociados, aunque encontramos similitudes entre todos.

# TODO: buscar el tipo numérico de python y ponerlo arriba y abajo

### Básicos

Estos son los tipos que estaremos usando sin ni siquiera pensar en ellos. Además de `string` y `number`, podríamos mencionar `boolean` para valores verdaderos o falsos y `char` para representar un solo caracter o letra.

### Complejos

Los tipos complejos representan conceptos más avanzados de los lenguajes. Entre los más comunes que nos encontraremos, podemos mencionar el tipo `Array`, que representará una lista de valores, o al tipo `Dictionary` que representaría un diccionario de palabras con deficiones asociadas.

## Debugging

Hablamos brevemente de los errores que podemos tener al intentar compilar o ejecutar un programa. A estos errores se los llama popularmente **bugs** (y en español "errores", jamás "bichos"), y deshacerse de ellos muchas veces requiere de un arte especialmente dedicada a la tarea.

### Syntax errors

Este es el tipo de bug más simple de resolver. Ocurre en lo que llamamos "tiempo de compilación", es decir, inmediatamente al ejeutar el compilador o el intérprete. Como el nombre lo indica, tenemos un problema de sintaxis - el lenguaje que estamos usando exige que cumplamos ciertas reglas y no lo estamos haciendo.

De la misma manera que en español siempre estará mal poner dos artículos seguidos, i.e. "el la cosa", cualquier lenguaje nos dirá que está mal usar dos operadores seguidos, i.e. `const CONSTANTE = = 'algo'`.

### Semantic errors

Estos errores refieren a la semántica de lo que estamos escribiendo, no a la forma. Por lo tanto, suelen ser más problematicos de descubrir. El programa no detectará estos errores, ya que no puede saber si el significado de lo que estamos haciendo es correcto. Solo el usuario, o una persona que lea muy atentamente el código, podrá detectarlo.

```python
1 + 2 * 3
# tal vez esperáramos ver 9 pero vemos 7 ya que primero se resuelve el producto y luego la suma => 1 + 6
(1 + 2) * 3
# ahora sí vale 9
```

### Runtime errors

Estos errores ocurren cuando, en la ejecución, se intenta hacer alguna operación imposible, como dividir por 0 - o alguna otra operación que no esté permitida en el lenguaje, pero que no sea un error de sintaxis. A diferencia de los errores semánticos, este sí será detectado por la computadora: el intérprete nos avisará del error o la aplicación se cerrará y el sistema operativo nos avisará que algo falló.

También pueden haber errores en tiempo de ejecución por operaciones inválidas respecto a los recursos del sistema, como querer usar una parte de la memoria que no existe.

### Debugging

Es la actividad de encontrar la explicación y corregir los bugs. Hay varias herramientas que nos ayudan a encontrar los errores, algunas analizando el código fuente, antes de que el programa se ejecute.

- Linters: son programas que revisan el código fuente y nos avisan si lo que escribimos no cumple con ciertos estándares que hayamos definido. Por ejemplo, nos alertan si escribimos algo que es correcto, pero que podría ser ambiguo.

- IDEs: IDE significa Integrated Development Environment, y es el nombre que le damos a los editores de texto que usaremos para programar. Además de permitirnos edición básica, suelen tener linters y autocompletado, lo que nos ayuda a escribir más rápido y con menos errores.

- Leer el código en voz alta: seguir paso a paso lo que escribimos puede exponernos rápidamente a encontrar donde lo escrito se aleja de lo que queríamos escribir.

- **Logs** de errores: cuando un programa corriendo muere o tira algún error, recobrarle suele dejar algún texto expresando lo que pasó. Revisarlo, en muchos casos, nos permite saber instantáneamente qué salió mal, y en otros casos nos puede dar una buena guía de por donde empezar a investigar.

## Estructura de un programa

### Lineas de código y expressions y statements

La línea de código es la unidad mínima para pensar el código fuente, el programa mínimo tendrá al menos una.

```python
area_triangular = base * altura / 2
```

En este ejemplo, hay una sola linea de código y varias expresiones. Una expresión es una combinación de operadores y operandos - dado que hay 3 operadores `= * /`, podríamos hablar de 3 expresiones. Llamaremos **statement** a una unidad sintáctica del programa - podríamos pensarlo como una "oración". En este caso, y en muchos otros, el statement es la linea de código completa, pero no es una correspondencia necesaria.

Así como este artículo es una secuencia de oraciones, podemos pensar un programa como una secuencia de statements. Para poder hablar de ellos de manera simbólica, usaremos la letra **S** y el enésimo statement lo representaremos como **Sn**.

No siempre los statements se ejecutarán de manera secuencial. Pasaremos a hablar de los 3 flujos básicos de ejecución:

### Ejecución secuencial

(En los próximos ejemplos dejaremos python para escribir "pseudo código" en ningún lenguaje en particular)

Este es el más básico flujo de ejecución. Es el flujo que rige los ejemplos de múltiples líneas que mostramos. Podríamos representarlo de manera simbólica como

```
S1 S2 S3 ... Sn
```

### Ejecución condicional

En este tipo de flujo, el statement se ejecutará solo si se cumple alguna condición específica. Usaremos las palabras clave  `if` y `then` de la siguiente manera

```
if (condición) then:
  S1
```

En este ejemplo, S1 solo se ejecutará si `condición` tiene un valor verdadero - como el valor booleano `True`.

```
if (condición) then: 
  S1 S2 
else: 
  S3 S4
```

En este otro ejemplo, introducimos la palabra clave `else` que nos permite hacer algo si la condición **no** se cumple. También vemos que no estamos limitados a ejecutar un solo statement por condicional.

### Ejecución repetida: bucles, iteración y repetición

Este tipo de flujo repetirá una serie de statements mientras que cierta condicion se cumpla y dejará de ejecutarlos cuando deje de ser verdadera:

```
while (condición):
  S1 S2 S3
```

En el ejemplo anterior, los statements se pueden ejecutar 1 vez, muchas veces o ninguna, si el valor de la condición era falso al comienzo.


Si, por ejemplo, se repitiera dos veces, tendríamos la siguiente secuencia de statements:

```
S1 S2 S3 S1 S2 S3
```

¡Termina siendo una serie secuencial! Siempre un programa se puede representar como una ejecución secuencial de statements.

## Conclusión

### El arte de programar

Habiendo definido la programación como instruir a una computadora sobre qué tareas debe realizar, implíciamente asumimos que tenemos algún objetivo final en nuestra tarea. De ahí, podríamos decir que programar es también "resolver problemas por medio de una computadora". A veces serán problemas integrados a soluciones no informáticas - como "desarrollar una app que me permita conseguir estacionamiento fácil y barato", pero normalmente los descompondremos en problemas solubles solo con código, por ejemplo: "dada una representación de un mapa con estacionamientos y mi posición, quiero obtener el más cercano y barato a la posición dada".

El programador es, entonces, una persona más o menos apasionada por resolver problemas y desafíos de manera cotidiana. Otra cosa implícita en la definición anterior es que no existe **una** solución única a un problema - así que también podemos inferir que programar exige un esfuerzo creativo y educado. Debemos encontrar una solución y debe ser aceptable, entre otras cosas, en términos de eficiencia. Una aplicación a la que le pidamos donde estacionar y nos responda 3 horas después habiendo gastado toda la batería del celular no es válida para nuestro contexto de uso. Esto requiere conocer de programación y también del contexto de nuestros usuarios.

Finalmente, mencionaré que el programador también tiene que tener presente a sus colegas del futuro, siendo ordenado y claro en la solución que escriba. Es muy común encontrar soluciones breves a problemas complejos que solo el que las escribió entiende - y esto no es deseable ni aceptable.

## Saber más

- Existen compiladores híbridos que pasan de código fuente a un **bytecode** o "código precompilado". Java hace esto y el resultado es interpretado por otro programa, la **Java Virtual Machine** o JVM. También existen lenguajes cuya finalidad es ser compilados (**transpiled**) a otros, como Typescript a Javascript - esto es común en la web, ya que los navegadores solo ejecutan Javascript.

- Hay quien dice que los programadores solo copiamos y pegámos código de Internet. Tal vez no sea cierto, pero esta guía fue escrita tomando como guía https://www.freecodecamp.org/news/a-gentler-introduction-to-programming-1f57383a1b2c 

> NOTE: I don’t recommend over-reading on the same topic. I believe in acting on the little you’ve learned, that is, practicing. This is why I’m not dumping too many links here for your learning. Feel free to google up or find others based on what you already know if you are not a first-timer.

- Permalink al texto de esta charla: [link](http://some-url.com.ar)
