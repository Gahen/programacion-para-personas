## Consideraciones preliminares

Tal vez por colonización cultural - o simplemente por arbitrariedad histórica - el inglés se estableció como el idioma de los conceptos de la programación. Por ello, algunas palabras no las traduciremos ya que las tomaremos como conceptos del arte en si mismos, de la misma manera que en la música no se traduce "presto" a "lento" y en la danza clásica se nombran las posturas en francés.


Algunas palabras se usarán sin explicarlas en el sentido entendido comunmente, por ejemplo "archivo", "ejecutar un programa".

Sin embargo, siempre que sea posible las traduciremos y pueden preguntar cualquier palabra o concepto que necesite una mejor aclaración.

## ¿Qué es programar?

De manera simple, podríamos decir que **programar** es "la acción de decirle qué tareas realizar a una computadora". Un **programa informático** es, a su vez, una serie de instrucciones que la computadora ejecuta. Por **computadora** nos referimos a cualquier dispositivo capaz de procesar **código**, como tablets, celulares y notebooks.

## Código

Llamamos así al objeto que moldeamos al programar, lo que constituirá, una vez terminado, el programa informático que será procesado en la computadora. Siempre se lo llama en singular, no tiene sentido hablar de "los códigos".

<!-- aclarar -->
## Lenguaje natural de las computadoras

Los equipos electrónicos se comunican en un lenguaje binario, la mínima unidad de información (bit) solo tiene 2 valores posibles, usualmente los representamos como 0 (apagado) o 1 (encendido). Así se encuentra la información almacenada en discos rígidos, unidades de memoria.

Si quisieramos comunicarnos directamente con una computadora, deberíamos poner en ciertas partes de la memoria ciertos bits en 0 y otros en 1 y luego esperar a que los procese. No sería agradable, eficiente, ni claro.

## Lenguajes de programación

Desde el comienzo de la informática, este problema fue evidente y se empezaron a crear diversos lenguajes que nos permitieran interactuar con computadoras de una manera fácilmente comprensible para alguien nuevo al código y que nos permitiera modelar programas complejos sin tener que dar vuelta cientos de miles de bits individualmente.
<!-- fin aclarar -->

## Intérpretes y compiladores

Para que sean útiles, los lenguajes de programación necesitan otros programas que los conviertan al lenguaje de la computadora. A estos programas los llamaremos **intérpretes** y **compiladores**.

Un intérprete es un programa que toma lo que escribimos en nuestro lenguaje amigable y expresivo (eficiente, en términos de escribir poco y decir mucho) , lo traduce a binario para que la computadora lo ejecute y lo ejecuta inmediatamente. Seguirá ejecutándose hasta terminar o encontrar un error.

Un compilador hace algo similar al intérprete, pero se diferencia en que no ejecuta el código compilado de manera inmediata, sino que nos genera un archivo binario (el **programa** propiamente dicho) que luego podremos ejecutar cuando querramos. Terminará al procesar todo el código que le pedimos o al encontrar un error. En el último caso, no generará un archivo ejecutable.

Al terminar de correr todas las instrucciones - o al encontrar un error - el programa se cerrará. Mientras esté en ejecución, nuestro programa (binario o interpretado) reservará parte de los recursos físicos de la computadora: memoria, espacio en disco, capacidad de procesamiento. Al terminar, todos estos recursos vuelven a estar disponibles para los demás programas.

Actualmente, es común referirse a estos archivos compilados como **Apps**.

## ¿Qué lenguaje aprender primero?

<!-- revisar  -->
Python es el lenguaje más usado para aprender a programar. Si buscamos algo orientado al desarrollo web, se puede empezar por **Javascript**. Para lo demás también se usa mucho **Ruby**. Los tres son lenguajes interpretados, y por lo tanto amigables para empezar a aprender, ya que facilitan la experimentación ayudando a un rápido aprendizaje.
<!-- fin revisar  -->

Los lenguajes interpretados suelen tener un **Command Line Interface** - o CLI interactivo - que permite probar rápidamente las expresiones que construyamos. Al ejectuarlo, veremos un **prompt** con un cursor parpadeante, y allí podremos introducir lo que queramos y evaluarlo apretando **enter**

```
$_
```

Los interpretes son programas, y por lo tanto es recomendable bajarse alguno de ellos y jugar un poco. Descargando el intérprete de python desde [el sitio oficial](http://python.org), se puede acceder al CLI ejecutando una terminal y escribiendo `python`. Para abrir una terminal en windows buscar la app `powershell` y en Mac la app `Terminal`

Un ejemplo de lo que haría en mi terminal de MacOS

```
micompu:ejemplo gahen$ python
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

Llamaremos así a las palabras que usaremos para identificar conceptos creados por programadoras: nosotres mismes o que vengan de **Libraries** (bibliotecas) externas. 

### Libraries y Frameworks

Una **Library** agrupa un conjunto de funcionalidad para que una programadora la reuse en su programa. Por ejemplo una biblioteca llamada "Math" de javascript nos permite hacer fácilmente (en términos de tiempo de la programadora) la raiz cuadrada de 5 escribiendo `Math.sqrt(5)`.

Llamamos **framework** a una biblioteca que nos provee bastante funcionalidad y además nos sugiere una manera de estructurar el código, con el fin de ahorrar tiempo de desarrollo y tener un resultado más claro y mantenible. Como hay muchas opiniones diferentes de qué es "claro", "mantenible" y si nos interesa o no la funcionalidad que un framework nos da, hay numerosos frameworks populares en cada lenguaje de programación.

### Keywords

Traducido usualmente como **palabras reservadas**, serán todas aquellas que tienen un significado estructural en el código fuente. Dependerán del lenguaje que estemos usando. En general los caracteres no alfabéticos son palabras reservadas y tienen significados especiales. Por ejemplo: `[] {} , . ; () ! "" ''` y todos los símbolos matemáticos `+ - * / = < >`.

Las palabras reservadas ocupan el mismo espacio conceptual que los identificadores, por ejemplo `string` es una palabra reservada de Java, nadie puede crear un identificador con ese nombre.

### Variables

Las variables son simplemente lugares de la memoria a los que les ponemos un nombre y donde guardamos cosas. A veces es útil guardar datos en el código de manera que podamos volver a accederlos y reusarlos. Debemos ponerles nombre para poder accederlos nuevamente.

```python
palabras_escritas = 12345
```

### Constants

Las constantes guardan valores que no cambiaran a través del tiempo. Al igual que las variables debemos ponerle un nombre (convencionalmente en mayúsculas). Algunos lenguajes tienen formas de crear constantes, otros no.

```python
const NOMBRE_CHARLA = 'Introducción a la programación'
```

### Literals

Son valores que escribimos en el código como expresiones literales. En los ejemplos anteriores estuvimos usandolo, `12345` es un valor literal que representa al numero 12345, mientras que `'Introducción a la programación'` representa al texto "Introducción a la programación". Parece medio extraño decirlo así ya que estamos haciendo una **abstracción** entre lo que escribimos y lo que las cosas representan, estos casos parecen obvios pero no siempre será evidente la relación entre lo escrito y lo representado.

### Operators

Es el propósito de cualquier lenguaje de programación permitirnos **hacer** operaciones con datos, sorprendemente llamamos a los elementos que nos permiten hacerlas "operadores". En general tenemos las siguientes categorías:

- Aritméticos: para operaciones aritméticas. Algunos ejemplos: `+ - * /`
- De asignación: para determinar valores a variables y constantes, el `=` de los ejemplos anteriores. No confundir su significado con "igual a".
- Relacionales: para comparar valores. Ejemplos `a < b` compararía el valor de `a` y `b` y sería verdadero solo si `b` es mayor.
- Lógicos: para trabajar con lógica, escencialmente establecer condiciones respecto a valores que sabemos verdaderos o falsos. Ejemplo: `a && b` representa la afirmación "a y b" y será verdadero solo si ambos son verdaderos.

### Comentarios

Que el código fuente sea claro es muy importante, así alguna programadora distinta podrá entender como funciona sin dedicarle muchísimo esfuerzo. Esto se logra escribiendo una buena **documentación** y una manera de lograr eso es añadiendo **comentarios** en las partes más importantes o que puedan ser confusas. Los intérpretes y compiladores ignoran los comentarios, es decir que el resultado final será igual sin importar cuantos añadamos, son solamente para los ojos de la siguiente programadora.

```python
# Esta variable siempre tendrá el número de palabras escritas actualizado
palabras_escritas = 12345
```

## Tipos de datos

Para poder guardar información en la memoria, por ejemplo usando los **literals** que vimos antes, el programa necesita saber el contenido y también el tipo de información que estamos guardando. De esta manera `'hola'` sería de tipo `string` (cadena de texto) y `12345` sería de algún tipo numérico `number`. Cada lenguaje tiene sus tipos asociados, aunque encontramos similitudes entre todos.

### Básicos

Estos son los tipos que estaremos usando sin ni siquiera pensar en ellos, además de `string` y `number` podríamos mencionar `boolean` para valores verdadero o falso y `char` para representar un solo caracter o letra.

### Complejos

Los tipos complejos representan conceptos más avanzados de los lenguajes. Entre los más comunes que nos encontraremos podemos mencionar al tipo `Array` que representará una lista de valores o al tipo `Dictionary` que representaría a un diccionario de palabras con deficiones asociadas.

## Debugging

Hablamos brevemente de los errores que podemos tener al intentar compilar o ejecutar un programa. A estos errores se los llama popularmente **bugs** (y en español "errores" jamás "bichos") y deshacerse de ellos muchas veces requiere de un arte especialmente dedicada a la tarea.

### Syntax errors

Este es el tipo de bug más simple de resolver. Ocurre en lo que llamamos "tiempo de compilación": el momento en que ejecutamos el compilador o el interprete. Como el nombre lo indica lo que tenemos es un problema de sintaxis, el lenguaje que estamos usando exige que cumplamos ciertas reglas de estructura del contenido y no lo estamos haciendo.

De la misma manera que en español siempre estará mal poner dos artículos seguidos, i.e. "el la cosa", en general cualquier lenguaje nos dirá que está mal usar dos operadores seguidos, i.e. `const CONSTANTE = = 'algo'`. `= =` es una sintaxis inválida en js, cambiarlo a `const CONSTANTE = 'algo'` lo soluciona.

### Semantic errors

Estos errores refieren a la semántica de lo que estamos escribiendo, no a la forma, por lo que son más problematicos de descubrir. El programa no detectará estos errores porque no puede saber si el significado (semántica) de lo que estamos haciendo es correcto y solo el usuario, o una persona que lea muy atentamente el código, podrá detectarlo.

```python
1 + 2 * 3
# tal vez esperáramos ver 9 pero vemos 7 ya que primero se resuelve el producto y luego la suma => 1 + 6
(1 + 2) * 3
# ahora sí vale 9
```

### Runtime errors

Estos errores ocurren cuando durante la ejecución del programa se intenta hacer alguna operación imposible, como podría ser dividir por 0 o alguna otra operación que no esté permitida en el lenguaje pero que no sea un error de sintaxis. A diferencia de los errores semánticos este si será detectado por la computadora: el intérprete nos avisará del error o la aplicación se cerrará y el sistema operativo nos avisará que algo falló.

También pueden haber errores en tiempo de ejecución por operaciones invalidas respecto a los recursos del sistema, como querer usar un parte de memoria que no existe.

### Debugging

Es la actividad encontrar, entender y corregir los bugs. Hay varias herramientas que nos ayudan a encontrar los errores:

- Linters: son programas que revisan el código fuente y nos avisan si lo que escribimos no cumple con cierto estándares que hayamos definido. Algo que podría detectar un linter sería una expresión ambigua en su significado pero correcta en sus sintaxis, como por ejemplo podríamos decirle que en las operaciones aritméticas siempre se usen paréntesis y nos avise si no es así.

- IDEs: IDE significa Integrated Development Environment, es el nombre que le damos a los editores de texto que usaremos para programar. Además de permitirnos edición simple de texto suelen tener linters y autocompletado, lo que nos ayuda a escribir más rápido y con menos errores.

- Leer el código en voz alta: seguir paso a paso lo que escribimos puede exponernos rápidamente a encontrar donde lo escrito se aleja de lo que queríamos escribir.

- **Logs** de errores: cuando un programa corriendo termina abruptamente o muestra algún error recobrarle suele dejar algún texto expresando lo que pasó, a ellos los llamamos "logs". Revisarlos en muchos casos nos permite saber instantáneamente qué salió mal, pero incluso si no es así igualmente nos da una buena guía para saber por donde empezar a investigar.

## Estructura de un programa

### Lineas de código, expressions y statements

La línea de código es la unidad mínima para pensar el código fuente, el programa mínimo tendrá al menos una.

```python
area_triangular = base * altura / 2
```

En este ejemplo hay una sola linea de código y varias expresiones. Una expresión es una combinación de operadores y operandos; dado que hay 3 operadores `= * /` podríamos hablar de 3 expresiones. Llamaremos **statement** a una unidad sintáctica del programa, podríamos pensarlo como una "oración". En este caso, y en muchos otros, el statement es la linea de código completa, pero no es una correspondencia necesaria.

Así como este artículo es una secuencia de oraciones, podemos pensar un programa como una secuencia de statements. Para poder hablar de ellos de manera simbólica usaremos la letra **S** y el enésimo statement lo representaremos como **Sn**.

No siempre los statements se ejecutarán de manera secuencial, pasaremos a hablar de los 3 flujos básicos de ejecución:

### Ejecución secuencial

(En los próximos ejemplos dejaremos python para escribir "pseudo código" en ningún lenguaje en particular)

Este es el más básico, es el flujo que rige los ejemplos de múltiples líneas que mostramos. Podríamos representarlo de manera simbólica como

```
S1 S2 S3 ... Sn
```

### Ejecución condicional

En este tipo de flujo el statement se ejecutará solo si se cumple alguna condición específica. Usaremos las palabras claves  `if` y `then` de la siguiente manera

```
if (condición) then:
  S1
```

En este ejemplo S1 solo se ejecutará si `condición` tiene un valor verdadero como podría ser el valor booleano `True`.

```
if (condición) then: 
  S1 S2 
else: 
  S3 S4
```

En este otro ejemplo introducimos la palabra clave `else` que nos permite hacer algo si la condición **no** se cumple. También vemos que no estamos limitados a ejecutar un solo statement por condicional.

### Ejecución repetida: bucles, iteración y repetición

Este tipo de flujo repetirá una serie de statements mientras que cierta condicion se cumpla y dejará de ejecutarlos cuando deje de ser verdadera

```
while (condición):
  S1 S2 S3
```

En el ejemplo anterior los statements se pueden ejecutar 1 vez, muchas veces o ninguna, si el valor de la condición era falso al comienzo.


Si por ejemplo se repitiera 2 veces tendríamos la siguiente secuencia de statements:

```
S1 S2 S3 S1 S2 S3
```

¡Termina siendo una serie secuencial! Siempre un programa se puede representar como una ejecución secuencial de statements.

## Conclusión

### El arte de programar

Habiendo definido la programación como instruir a una computadora sobre qué tareas debe realizar, implíciamente asumimos que tenemos algún objetivo finla en nuestra tarea. De ahí que podríamos decir que programar es también "resolver problemas por medio de una computadora", a veces serán problemas inacibles e integrados a soluciones no informáticas como "desarrollar una app que me permita conseguir estacionamiento fácil y barato" pero usualmente los descompondremos en problemas solubles solo con código como "dada una representación de un mapa con estacionamientos y mi posición, quiero obtener el más cercano y barato a la posición dada".

La persona programadora es entonces una persona más o menos apasionada en resolver problemas y desafíos de manera cotidiana. Otra cosa implícita en la definición anterior es que no existe **una** solución única a un problema así que también podemos inferir que programar exige un esfuerzo creativo y educado, debemos encontrar una solución y aquella debe ser aceptable, entre otras cosas, en términos de eficiencia. Si la aplicación que le preguntamos donde estacionar nos response 3 horas después habiendo gastado toda la batería del celular no es válida para nuestro caso de uso. Hacer un programa aceptable requiere, entonces, de conocer de programación y también del contexto de nuestros usuarios.

Finalmente mencionaré que la programadora también tiene que tener presente a sus colegas del futuro siendo ordenado y claro en la solución que escriba. Es muy usual encontrar soluciones breves a problemas complejos que solo el que las escribió entiende, algo que en general no es deseable ni aceptable profesionalmente.

## Saber más

- Existen compiladores híbridos que pasan de código fuente a un **bytecode** o "código precompilado", Java hace esto y el resultado es interpretaado por otro programa, la **Java Virtual Machine** o JVM. También existen lenguajes cuya finalidad es ser compilados (**transpiled**) a otros, como Typescript a Javascript, esto es común en la web ya que los navegadores solo ejecutan Javascript.

- Hay quien dice que las programadoras solo copiamos y pegámos código de Internet. Tal vez no sea cierto, pero esta guía fue escrita tomando como base https://www.freecodecamp.org/news/a-gentler-introduction-to-programming-1f57383a1b2c 

- Permalink al texto de esta charla: [link](https://github.com/Gahen/programacion-para-personas)
