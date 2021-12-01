### Seminario de Sistemas de Recuperación de Información

##### Integrantes

- Daniel de la Cruz CXXX

- Mauricio Mahmud Sánchez C312

---



# Características del NLP

El **procesamiento de lenguaje natural**, abreviado **NLP** por sus siglas en inglés, es un campo de las ciencias de la computación, de la inteligencia artificial y de la lingüística que estudia las interacciones entre las computadoras y el lenguaje humano. Se ocupa de la formulación e investigación de mecanismos eficaces computacionalmente para la comunicación entre personas y máquinas por medio del lenguaje natural, es decir, de las lenguas del mundo.  Los modelos aplicados se enfocan no solo a la comprensión del lenguaje de por sí, sino a aspectos generales cognitivos humanos y a la organización de la memoria.



#### Características más comunes

...

# Dificultades de Procesamiento

#### Ambigüedad

Las lenguas naturales son inherentemente ambiguas en diferentes niveles:

- En el nivel léxico, una misma palabra puede tener varios significados, y la selección del apropiado se debe deducir a partir del contexto oracional o conocimiento básico. Muchas investigaciones en el campo del procesamiento de lenguajes naturales han estudiado métodos de resolver las ambigüedades léxicas mediante diccionarios, gramáticas, bases de conocimiento y correlaciones estadísticas.
- A nivel referencial, la resolución de anáforas y catáforas implica determinar la entidad lingüística previa o posterior a que hacen referencia.
- En el nivel estructural, se requiere de la semántica para desambiguar la dependencia de los sintagmas preposicionales que conducen a la construcción de distintos árboles sintácticos. Por ejemplo, en la frase *Rompió el dibujo de un ataque de nervios*.

Para resolver estos tipos de ambigüedades y otros, el problema central en el NLP es la traducción de entradas en lenguas naturales a una representación interna sin ambigüedad, como árboles de análisis.

#### Detección de separación entre las palabras

En la lengua hablada no se suelen hacer pausas entre palabra y palabra. El lugar en el que se deben separar las palabras a menudo depende de cuál es la posibilidad de que mantenga un sentido lógico tanto gramatical como contextual. En la lengua escrita, lenguas como el chino mandarín tampoco tienen separaciones entre las palabras.

#### Recepción imperfecta de datos

Acentos extranjeros, regionalismos o dificultades en la producción del habla, errores de mecanografiado o expresiones no gramaticales, errores en la lectura de textos mediante reconocimiento óptico de caracteres.

# Reconocimiento de Entidades Nombradas

## Definición 

El Reconocimiento de entidades nombradas (NER por sus siglas en inglés) (también conocido como extracción de entidades) es una tarea de extracción de información que busca localizar y clasificar en categorías predefinidas, como personas, organizaciones, lugares, expresiones de tiempo y cantidades, las entidades nombradas encontradas en un texto.

En la expresión entidad nombrada, la palabra nombrada restringe la tarea a aquellas entidades para las cuales existe uno o más de un designador rígido (un designador rígido es una expresión que designa o refiera una misma entidad en todos los mundos posibles en los que esa entidad existe, y no designa nada en aquellos mundos en los que no existe). Por ejemplo, la compañía automotriz creada por Henry Ford en 1903 está relacionada con los designadores *Ford* o *Ford Motor Company*. Los designadores rígidos incluyen tanto nombres propios como términos para ciertas especies biológicas y sustancias.

Las expresiones temporales y algunas expresiones numéricas (dinero, porcentajes, etc.) también pueden ser considerados entidades en el contexto del NER. Mientras algunos casos de estos tipos son ejemplos buenos de designadores rígidos (p. ej., el año 2001), hay también muchos inválidos (p. ej., tomo mis vacaciones en “junio”). En el primer caso, el año *2001* refiere al *2001.º año del calendario gregoriano.* En el segundo caso, el mes de junio puede referir al mes de cualquier año (*junio pasado*, *el próximo junio*, *junio* 2020, etc.). La definición de *entidad nombrada* no es estricta y a menudo tiene que ser explicada en el contexto en qué se está utilizado.



## Características del Problema

El Reconocimiento de entidades nombradas a menudo se divide, conceptualmente y posiblemente también en su implementación, en dos problemas distintos: detección de nombres, y clasificación de los nombres según el tipo de entidad al que hacen referencia a (persona, organización, ubicación y otro). La primera fase generalmente se reduce a un problema de segmentación: los nombres son una secuencia contigua de tokens, sin solapamiento ni anidamiento, de modo que "Bank of America" es un nombre único, a pesar del hecho de que dentro de este nombre aparezca, la subcadena América que es a su vez un nombre.



Para evaluar la calidad de un sistema de NER se han definido varias medidas. La exactitud a nivel de token es una posibilidad, pero tiene dos problemas: la mayoría de los tokens en textos de la vida real no son parte de entidades nombradas, así que la exactitud de un sistema que pronostica siempre "no una entidad" es muy alto, generalmente mayor que el 90%; y un error en la delimitación de una entidad nombrada no es debidamente penalizado. Por ejemplo, detectar solo el primer nombre de la persona cuando le sigue su apellido se puntúa con ½ exactitud.

En conferencias académicas como CoNLL, se ha definido una variante del valor-F de la siguiente manera:

- Precisión es el número de entidades nombradas que coinciden exactamente con conjunto de evaluación. I.e. cuando se predice [Persona Hans] [Persona Blick], pero lo correcto era [Person Hans Blick], la precisión es cero. La precisión es después promediada por cada una de la entidades nombradas.

- El recobrado es el número de entidades del conjunto de evaluación que aparecen exactamente en la misma posición en las predicciones.

- El Valor-F es la media armónica de estos dos valores. Se deriva de la anterior definición que cualquier predicción que reconozca erróneamente un token como parte de una entidad nombrada o que deje de detectar un token que sí es una entidad nombrada o lo clasifique erróneamente no contribuirá ni a la precisión ni al recobrado.

Se han propuesto modelos de evaluación basados en un emparejamiento token-por-token. Tales modelos permiten una evaluación más detallada y hacer una comparación de los sistemas de extracción existentes, teniendo en cuenta también el grado de disparidad en predicciones no exactas.



## Propuestas de Solución 

Se han creado sistemas NER empleando técnicas basadas en gramáticas lingüísticas y modelos estadísticos, i.e. aprendizaje de máquina. Los sistema basados en gramáticas y elaborados a manos obtienen generalmente una mejor precisión, pero a expensas de un menor recobrado y meses de trabajo de lingüistas computacionales experimentados. El NER estadístico comúnmente requieren un conjunto de entrenamiento grande de datos anotados manualmente. Se han propuesto métodos semisupervisedos para evitar parte del esfuerzo de anotación.

Muchos clasificadores diferentes han sido utilizados para NER usando aprendizaje de máquina. Los campos aleatorios condicionales son una elección común.

## Ventajas y Desventajas

#### Desventajas

* Las investigaciones realizadas indican que incluso los sistemas NER más avanzadas son frágiles, dado que los sistemas NER desarrollados para un dominio no suelen comportarse bien en otros dominios.
*  La puesta a punto de un sistema NER para un nuevo dominio conlleva un esfuerzo considerable.
* 
