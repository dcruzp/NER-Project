### Seminario de Sistemas de Recuperación de Información

##### Integrantes

- Daniel de la Cruz CXXX

- Mauricio Mahmud Sánchez C312

---



# Características del NLP

El **procesamiento de lenguaje natural**, abreviado **NLP** por sus siglas en inglés, es un campo de las ciencias de la computación, de la inteligencia artificial y de la lingüística que estudia las interacciones entre las computadoras y el lenguaje humano. Se ocupa de la formulación e investigación de mecanismos eficaces computacionalmente para la comunicación entre personas y máquinas por medio del lenguaje natural, es decir, de las lenguas del mundo.  Los modelos aplicados se enfocan no solo a la comprensión del lenguaje de por sí, sino a aspectos generales cognitivos humanos y a la organización de la memoria.

Cualquier lengua humana puede ser tratada puede ser procesadas. Lógicamente , limitaciones de interés económico o practico hace que solo las lenguas mas habladas o utilizadas en el mundo digital tangan aplicaciones en uso. Las lenguas humanas pueden expresarse por escrito (texto) , oralmente (voz) y también, mediante signos. Naturalmente, el procesamiento del lenguaje natural esta mas avanzado en el tratamiento de  textos, donde hay muchos mas datos y son mas fáciles de conseguir en formato digital. Los audios aunque también estén el formato digital hay que procesarlos para transcribirlos a letras o caracteres y a partir de ahí tratar los datos.  



#### Características más comunes

...

# Dificultades de Procesamiento

Creemos que existen dos problemas principales de los actuales sistemas de reconocimiento de entidades nombradas. El primer problema es la necesidad de sintonizar el sistema para cada nuevo dominio o idioma. Hay una gran caída en la calidad de la salida cuando un sistema diseñado para un dominio se usa para otro. La transición de un idioma a otro es aún más problemática.
El segundo problema es la falta de conocimiento semántico y externo, que es crucial para que las personas reconozcan los nombres en los textos, especialmente en textos informales como publicaciones en foros de Internet. 

#### Ambigüedad

Las lenguas naturales son inherente-mente ambiguas en diferentes niveles:

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

El reconocimento de  entidades nombradas intenta detectar y clasificar correctamente expresiones textuales en un conjunto de clases predefinidas. Las clases pueden variar, pero muy a menudo se utilizan clases como personas, organizaciones o ubicaciones. 

Cada Entidad tiene dos propiedades principales:  *amplitud* y *tipo*. Supongamos que nuestro texto contiene "Banco de Inglaterra". El tipo de entidad es organización y tiene tres palabras Marcar a *Inglaterra* de tipo organización es seguramente incorrecto, así como marcar "Banco de Inglaterra" como país. Marcar a "Inglaterra" como país es cuestionable(en este caso) y la exactitud de esta salida depende de nuestras necesidades. Como se puede apreciar, existen varias definiciones posibles para de la respuesta correcta. Mas adelante se describen métricas de evaluación usadas para el reconocimiento de entidades nombradas junto con múltiples definiciones del resultado deseado.  

**Métrica de Evaluación** 

En cualquier área de la búsqueda de información es importante avaluar y comparar resultados de nuevos métodos. Por tanto, existe la necesidad de utilizar algunas medidas objetivas que cubran bien el propósito de la investigación 

A diferencia de otras tareas de Procesamiento de Lenguaje Natural (Ej Machine Translation) El Reconocimiento de Entidades Nombradas usa conjunto estándar de métricas(aunque el uso puede variar) que es generalmente aceptado. Este conjunto incluye tres metricas que desciben el rendimiento de los sistemas de NER, cada para diferentes aspectos de la tarea. Estas métricas se denominan *precisión*, *recuperación* y $medida-F$ (también puntuación $F$ o puntuación $F_1$)

Vamos a definir esas métricas en una clasificación general de objetos dentro de  dos clases: positivas y negativas. Existen las siguientes 4 clases de resultados de clasificación.

- Positiva(P) - objetos positivos marcados como positivos. 
- Negativo(N) - objetos negativos marcados como negativo
- Falso positvo (FP) - objetos negativos marcados como positivos
- Falso Negativo(FN) -objetos positivos marcados como negativos 

Ahora podemos fácilmente definir *precisión*, *recuperación* y *medida-F* como sigue: 
$$
\mbox{presicion} = \frac{P}{P+FP}
$$

$$
\mbox{recuperacion} = \frac{P}{P+FN}
$$

$$
\mbox{Medida-F} = \frac{2P}{2P+FP+FN}
$$

*Precisión* es una medida de confianza, que los objetos marcados como positivos son realmente positivos. *Recuperación* es una mediad de confianza, que todos los objetos están marcados. Es obvio que *precisión* y *recuperación* describen diferentes aspectos del resultados. Sin embargo esas medidas están compitiendo. Esto es importante en la evaluación de un clasificador, porque el clasificador de alta memoria (o precisión) puede ser mejor para varias tareas. *Medida-F* es la media armónica entre *precisión* y *recuperación* y representan la perspectiva en general. 

Ahora es posible definir lo que se cuanta como P, N, FP,FN. Se propusieron múltiples definiciones. las siguientes secciones cubren las mas comunes.

## Características del Problema

El Reconocimiento de entidades nombradas a menudo se divide, conceptualmente y posiblemente también en su implementación, en dos problemas distintos: detección de nombres, y clasificación de los nombres según el tipo de entidad al que hacen referencia a (persona, organización, ubicación y otro). La primera fase generalmente se reduce a un problema de segmentación: los nombres son una secuencia contigua de tokens, sin solapamiento ni anidamiento, de modo que "Bank of America" es un nombre único, a pesar del hecho de que dentro de este nombre aparezca, la subcadena América que es a su vez un nombre.

Para evaluar la calidad de un sistema de NER se han definido varias medidas. La exactitud a nivel de token es una posibilidad, pero tiene dos problemas: la mayoría de los tokens en textos de la vida real no son parte de entidades nombradas, así que la exactitud de un sistema que pronostica siempre "no una entidad" es muy alto, generalmente mayor que el 90%; y un error en la delimitación de una entidad nombrada no es debidamente penalizado. Por ejemplo, detectar solo el primer nombre de la persona cuando le sigue su apellido se puntúa con ½ exactitud.

En conferencias académicas como CoNLL, se ha definido una variante del valor-F de la siguiente manera:

- Precisión es el número de entidades nombradas que coinciden exactamente con conjunto de evaluación. I.e. cuando se predice [Persona Hans] [Persona Blick], pero lo correcto era [Person Hans Blick], la precisión es cero. La precisión es después promediada por cada una de la entidades nombradas.

- El recobrado es el número de entidades del conjunto de evaluación que aparecen exactamente en la misma posición en las predicciones.

- El Valor-F es la media armónica de estos dos valores. Se deriva de la anterior definición que cualquier predicción que reconozca erróneamente un token como parte de una entidad nombrada o que deje de detectar un token que sí es una entidad nombrada o lo clasifique erróneamente no contribuirá ni a la precisión ni al recobrado.

Se han propuesto modelos de evaluación basados en un emparejamiento token-por-token. Tales modelos permiten una evaluación más detallada y hacer una comparación de los sistemas de extracción existentes, teniendo en cuenta también el grado de disparidad en predicciones no exactas.

### Lenguajes

Los resultados muestran que existen grandes diferencias entre los lenguajes, que probablemente se deban a sus propiedades(orden de palabra, morfología, reglas para escribir nombres propios, etc).

La búsqueda se realizo principalmente en Ingles. El mejor sistema en CoNLL-2003 fue creado por Florianet al.(2003). Alcanzo el 88,76% de la medida F. Aunque muchos sistemas tienen muchos resultados en la actualidad, a menudo se les compara con este sistema. Los resultados mas avanzados fueron obtenidos por Lin y Wu (2009) (90,90%), Ratinov y Roth (2009) (90,57%), Turian (2010) (90,36%) y Tkachenko y Simanovsky (2012) (91,02%). 

El Español fue uno de los idiomas, que fueron tratados en la conferencia CoNLL-2002. El mejor sistema para el espannol para este conferencia fue creado por Carreras (2002). Estaba basado en AdaBoost y alcanzo 81.39%. Ferrandez (2006) introdujo el sistema basado en una combinacion de maching learning y un enfoque basado en reglas. El sistema de maching learning se utilizo como entrada para la parte basada en reglas, que tomo las decisiones finales. Para nuestro mejor conocimiento, actualmente sostiene el mejor resultado para el Español con 83.37%. Otro sistema fue presentado por Kozareva (2007) que combina varios métodos de maching learning  usando votacion ponderada. El sistema evita el uso de características morfológicas y sintácticas porque esas características reducen la adaptabilidad del sistema. Su puntuación final en los datos de CoNLL-2002 fue de 78.59%, que seria el tercer lugar en la conferencia original. Konkol (2015) introdujeron un sistema independiente del idioma, que alcanzo un 83,08% en español, peor solo en un 0,29% que el mejor sistema dependiente del idioma. 

El  alemán comenzó con el CoNLL-2003. En CoNLL-2003, el mejor sistema para el alemán (Florian et al., 2003) tenía 72,41%. Faruqui y Padó (2010) presentaron un sistema que superó a los sistemas anteriores con un 78,2%. Su éxito se basó en el uso de similitudes semánticas y morfológicas de palabras. Recientemente, una tarea compartida de GermEval NER (Benikova et al., 2014) presentó una serie de sistemas. Los organizadores del taller anunciaron tres mejores sistemas (Benikova et al., 2014). 

Hay sistemas para el Chino (Fu y Luke 2005), Japones (Sasano y Kurohashi, 2008), Estonio(Tkachenko, 2013), Húngaro (Varga, Simon, 2007), turco (Demir y Ozgur, 2014), lenguas indias(Ekbal y Saha, 2011), Búlgaro (Georgiev, 2009), árabe(Shaalan, 2014). 

Es evidente que el lenguaje tiene un gran impacto en el rendimiento del sistema. La mayor parte de la investigación se realiza en Ingles, que parece ser uno de los idiomas mas fáciles. Todos los lenguajes tienen alguna propiedades especiales, que juegan un papel crucial en el rendimiento. Esas propiedades incluyen el nivel de inflexión y la libertad del orden de las palabras.(Konkol y Konopík, 2014), capitalizacion(Faruqui y Padó, 2010) tokenización (tokenización diferente para entidades en Chino) (Gao et al., 2005), aglutinación (Shaalan, 2014). 

### Multilingual

La tarea NER se definió en MUC-6 (Grishman y Sundheim, 1996). Esta conferencia se centró exclusivamente en el inglés. Las siguientes conferencias otorgaron gradualmente más importancia al procesamiento de varios idiomas. En MUC-7 / MET-2, los sistemas NER presentados procesaban inglés, japonés y chino, pero no era obligatorio evaluar el sistema en todos estos idiomas, de hecho, la mayoría de los sistemas fueron evaluados en solo uno de estos idiomas. (pro, 1998). 

Tanto para CoNLL-2002 (Tjong Kim Sang, 2002) como para CoNLL-2003 (Tjong Kim Sang y De Meulder, 2003), todos los sistemas tuvieron que ser evaluados en un par de idiomas (holandés y español, inglés y alemán). Aunque los sistemas presentados en estas conferencias generalmente se consideran multilingües, tenían diferentes niveles de independencia lingüística. Podría decirse que los sistemas fueron capaces de adaptarse a un nuevo idioma solo hasta cierto punto sin el trabajo de un experto (por ejemplo, se requirió una parte del discurso, nomenclátores).

Actualmente, existen múltiples sistemas de vanguardia, que son (o deberían poder) procesar una amplia gama de idiomas (Lin y Wu, 2009; Konkol et al., 2015; Steinberger et al., 2013) . Estos sistemas evitan herramientas deliberadamente dependientes del lenguaje como lematizadores, etiquetadores POS o etiquetadores de fragmentos por dos razones. Primero, no están disponibles para muchos idiomas. En segundo lugar, estas herramientas no suelen ser multilingües o solo admiten un conjunto limitado de idiomas. Entonces es difícil integrarlos y gestionarlos en un único sistema altamente multilingüe (Steinberger et al., 2013).  

La clave de los sistemas altamente multilingües es su adaptabilidad. Un sistema altamente multilingües necesita poder adaptarse a un nuevo lenguaje fácilmente, sin mucho esfuerzo 

### Dominio 

Otro aspecto de los NER es el dominio de los datos. NER se aplico en una amplia variedad de dominios, incluidos Wikipedia , artículos de noticias , discursos parlamentarios, aplicaciones biomédicas, redes sociales, negocios, etc. Algunos dominios parecen ser mas fáciles que otros dominios, ejemplo Periódico y Redes Sociales. Se ha demostrado que el sistema entrenado en un dominio se desempena significativamente peor en los otros dominios. Caimarita y Altun (2005) han demostrado una brecha mayor al 26% cuando entrenaron un sistema en el corpus CoNLL y lo usaron en textos de Wall Street Journal. Se informó una degradación similar del rendimiento en (Poibeau y Kosseim, 2001) para NER entrenado en el corpus MUC-6 y utilizado para textos mas informales como correos electrónicos. El dominio también evoluciona con el tiempo. El idioma y el estilo de los textos cambian. Aparecen entidades (nuevas empresas, nuevos bancos , oficinas , etc ) y desaparecen (empresas compradas, pensiones, etc). 

El propósito general es crear un sistema de dominio independiente, sistemas que trabajan para todos los dominios similarmente al humano. Actualmente, hay dos enfoques. El primer enfoque, creamos un dominio dependiente y una capa de adaptación. que es responsable de alterar el sistema para otros dominios (Guo, 2009). En el segundo enfoque, se trata directamente de crear sistemas de dominio independiente. El primer paso en este sentido es remplazar características de dominio dependiente. (gazetteers rules, etc) con características mas generales (Faruqui and Pado, 2010) para limitar el trabajo necesario para entrenar el sistema para otro dominio. 

### Esquema de anotación 

El reconocimiento de algunas clases es mucho más difícil que otras clases, p. Ej. si elegimos reconocer los nombres de pila, es más fácil que las ubicaciones, porque la variabilidad de los nombres de pila suele ser menor que la variabilidad de los nombres de las ubicaciones. El número de clases también es un factor. Generalmente, la clasificación es más difícil si el número de clases es alto, porque las clases probablemente estarían juntas (es decir, más difíciles de separar) y se necesitarían más parámetros o reglas. Se necesita cierta cantidad de datos para entrenar a cada clase. Con un gran número de clases, es necesario anotar más datos (en el enfoque de aprendizaje automático) o escribir más reglas (en el enfoque basado en reglas). 

Otro punto de vista es la estructura de las entidades. Las clases de entidad pueden estar simplemente en el mismo nivel o pueden organizarse jerárquicamente, p. Ej. persona es una superclase de actor. Sekine y col. (2002) definieron y extendieron gradualmente una jerarquía compleja, que contiene alrededor de 150 clases. La jerarquía se puede definir de varias formas. Sekine y col. (2002) usa jerarquía semántica (la persona es una superclase de actor), pero también hay ejemplos de jerarquía funcional (el nombre de la persona es superclase para el apellido y el nombre)

### Corpus 

Para la evaluación de la tarea NER, es necesario crear un corpus con entidades marcadas. Si utilizamos un enfoque de aprendizaje automático supervisado, también necesitamos el corpus para la estimación de parámetros óptimos. Muy a menudo, el corpus es creado por humanos y lo llamamos datos de oro. A veces, el corpus se puede crear automáticamente a partir de recursos ya existentes (Hahm et al., 2014; Nothman et al., 2008). Este enfoque generalmente nos permite crear un corpus mucho más grande, pero el corpus contiene errores. Usamos el término datos de plata para dicho corpus.

El corpus generalmente se divide en partes con diferentes propósitos. La parte de entrenamiento del corpus se utiliza para entrenar los parámetros del sistema. La parte de prueba se utiliza solo para la evaluación final del sistema. Evaluar el sistema en el conjunto de prueba durante su desarrollo es una mala práctica, porque los resultados finales probablemente sean mejores de lo que serían con datos invisibles. La parte restringida o de validación se utiliza para verificar el diseño del sistema durante el desarrollo y también para encontrar los hiperparámetros óptimos del modelo (por ejemplo, tamaño de las ventanas para las características, parámetros para la combinación de modelos).

En el enfoque de *maching* *learning* el tamaño de los datos tiene un gran impacto en los resultados. Un sistema complejo entrenado con muy pocos datos no podrá generalizar y los resultados en datos invisibles pueden ser catastróficos. Este problema se llama sobreajuste. Un sistema menos complejo necesita menos datos, pero es posible que no pueda modelar el problema correctamente. Por este motivo, a menudo se utiliza la validación cruzada. En esta técnica, el corpus (o la parte de formación y validación) se divide en N partes con N>2. En la i-ésima iteración (i = 1,...., N), el sistema se entrena en todas las partes excepto en la i-ésima parte y la i-ésima parte se utiliza para la evaluación. De esta manera, todos los datos se utilizan tanto para la formación como para la evaluación. 

Se han elaborado los corpus más utilizados para las conferencias CoNLL. Se crearon corpus para cuatro idiomas: español, holandés, inglés y alemán. Estos corpora utilizan cuatro clases de entidad PER (nombres de personas), ORG (organizaciones), LOC (ubicaciones) y MISC (varios). Los tamaños de estos corpus son alrededor de 250.000 tokens. 



## Propuestas de Solución 

Se han creado sistemas NER empleando técnicas basadas en gramáticas lingüísticas y modelos estadísticos, i.e. aprendizaje de máquina. Los sistema basados en gramáticas y elaborados a manos obtienen generalmente una mejor precisión, pero a expensas de un menor recobrado y meses de trabajo de lingüistas computacionales experimentados. El NER estadístico comúnmente requieren un conjunto de entrenamiento grande de datos anotados manualmente. Se han propuesto métodos semisupervisedos para evitar parte del esfuerzo de anotación.

Muchos clasificadores diferentes han sido utilizados para NER usando aprendizaje de máquina. Los campos aleatorios condicionales son una elección común.

Los cuatro principales enfoques aplicados en NER son:
- Basado en reglas:
	Estos sistemas NER se basan en reglas hechas a mano, es decir, las reglas pueden diseñarse utilizando diccionarios geográficos específicos de dominio y patrones sintáctico-léxicos. Un ejemplo es el enfoque de inferencia de reglas Brill para la entrada de voz. Este sistema genera reglas automáticamente basadas en el etiquetador de parte del discurso de Brill. En cuanto el dominio biomédico, se encuentra ProMiner, que aprovecha un diccionario de sinónimos preprocesado para identificar menciones de proteínas y genes potenciales en texto biomédico.
	Los sistemas basados en reglas funcionan muy bien cuando el lexicón es exhaustivo. Debido a reglas específicas de dominio y diccionarios incompletos, a menudo se observan alta precisión y baja recuperación de dichos sistemas, la transferencia de estos sistemas a otros dominios, no es posible.
- Aprendizaje no supervisado:
	Un enfoque típico del aprendizaje no supervisado es el clustering. Dichos sistemas extraen entidades con nombre de los grupos en función de la similitud de contexto. La idea clave es que los recursos léxicos, los patrones léxicos y las estadísticas calculadas en un corpus grande, pueden usarse para inferir menciones de entidades nombradas.
	Como ejemplo de lo anterior, podemos encontrar sistemas no supervisados para la construcción de diccionarios geográficos y con esto la resolución a la ambigüedad de la entidad nombrada. El sistema anterior combina extracción de entidad y desambiguación basadas en heurísticas simples pero altamente efectivas.
- Aprendizaje supervisado basado en características:
	Aplicando el aprendizaje supervisado, NER se convierte en una tarea de clasificación de múltiples clases o etiquetado de secuencias. Dadas muestras de datos anotados, las características están cuidadosamente diseñadas para representar cada ejemplo de entrenamiento. Los algoritmos de aprendizaje supervisado son usados para aprender un modelo de reconocimiento de patrones similares a partir de datos no vistos. La representación del vector de características es una abstracción sobre el texto donde una palabra está representada por uno o varios valores booleanos, numéricos o nominales. Basado en estas características, se han aplicado muchos algoritmos de aprendizaje supervisado en NER, incluidos modelos ocultos de Markov (HMM), árboles de decisión, modelos de máxima entropía, máquinas de vectores de soporte (SVM), y campos aleatorios condicionales (CRF).
- Aprendizaje profundo:
	El aprendizaje profundo es un campo de aprendizaje automático que se compone de múltiples capas de procesamiento, para aprender representaciones de datos con múltiples niveles de abstracción. Las principales ventajas de aplicar técnicas de aprendizaje profundo a NER son:
	1. Se beneficia de la transformación no lineal, que genera asignaciones no lineales de entrada a salida. En comparación con los modelos lineales (Log-linear HMM y CRF de cadena lineal), los modelos de aprendizaje profundo pueden aprender características complejas e intrincadas de los datos a través de funciones de activación no lineal.
	2. El aprendizaje profundo ahorra un esfuerzo significativo en el diseño de funciones NER. Los enfoques tradicionales basados en características, requieren una considerable cantidad de habilidades de ingeniería y experiencia en el dominio. Los modelos de aprendizaje profundo, por otro lado, son efectivos para aprender automáticamente representaciones útiles y factores subyacentes a partir de datos sin procesar.
	3. En tercer lugar, los modelos NER neuronales profundos, se pueden entrenar en un paradigma de extremo a extremo, por descenso de gradiente. Esta propiedad nos permite diseñar sistemas NER más complejos.

## Ventajas y Desventajas

#### Desventajas

* Las investigaciones realizadas indican que incluso los sistemas NER más avanzadas son frágiles, dado que los sistemas NER desarrollados para un dominio no suelen comportarse bien en otros dominios.
*  La puesta a punto de un sistema NER para un nuevo dominio conlleva un esfuerzo considerable.
* 
