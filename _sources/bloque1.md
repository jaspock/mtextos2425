
(label_introduccion)=
Introducción. Minería de textos y procesamiento del lenguaje natural
====================================================================

En este bloque se abordan aspectos relacionados con la obtención de textos, así como de su preprocesamiento y tratamiento con técnicas básicas de procesamiento del lenguaje natural. El profesor de este bloque es Miquel Esplà Gomis. 

La *minería de textos* es el conjunto de técnicas y herramientas desarrolladas para extraer información de grandes colecciones textuales, tanto información implícita como explícita.

Esa información está codificada en textos, es decir, en un idioma o lengua. La minería de textos necesita, por tanto, interpretar (en mayor o menor medida) los textos y a partir de esa interpretación extraer la información. La disciplina computacional que idea y desarrolla sistemas para la interpretación lingüística de los textos es el procesamiento del lenguaje natural (PLN o NLP por sus siglas en inglés: *Natural Language Processing*), disciplina híbrida entre la lingüística y la computación.

Este segundo bloque de la asignatura cubre dos aspectos principales: 
1- la obtención de contenidos textuales de Internet, una de las principales fuentes de este timpo de informaicón, y
2- los conceptos fundamentales del procesamiento del lenguaje natural.
También se comentarán herramientas y recursos útiles para la minería de textos.

## Prácticas a entregar para este bloque

Durante las dos sesiones de este bloque, vamos a realizar una serie de prácticas que permitirán experimentar con algunos de los elementos incluidos en los contenidos teóricos de la asignatura. En la primera sesión de este bloque, las prácticas se centrarán en explorar diferentes estrategias para la obtención de documentos de textos a partir de Internet, extracción de texto relevante de éstos, y preprocesamiento del texto extraido. En la segunda sesión nos centraremos en explorar algunas de las estrategias estudiadas en el contenido teórico, concretamente centradas en la obtención de representaciones vectoriales del texto, y de cómo se pueden usar para explotar la información descargada y almacenada.

**Esta sección se encuentra en construcción**, y la versión definitiva estará disponible durante la primera sesión de este bloque, el día 6 de marzo de 2025. En cualquier caso, **plazo de entrega para el informe de prácticas de este bloque acaba el 27 de marzo de 2025** a las 23.59 horas. Las prácticas, excepto casos puntuales, se han de hacer en parejas. Recuerda que hay un examen final de la asignatura, por lo que es muy recomendable que ambos miembros del equipo se impliquen de igual manera. La entrtega se realizará Entrega un único PDF final a través de una tutoría de UACloud

A la hora de corregir los informes de prácticas, no se penalizará el uso de asistentes generativos de texto. El uso de ciertas herramientas de inteligencia artificial puede aumentar tus capacidades profesionales. Sin embargo, el abuso de su uso hasta el punto de despersonalizar tus entregas, desproveerlas de tu estilo personal, de tus propios razonamientos o de contenido relevante sí afectará negativamente a tu nota. Todo esto suele ser bastante fácil de detectar, pero para casos dudosos el profesor podrá realizar una pequeña prueba con el estudiante en la que no se permita el uso de asistentes generativos de texto para comprobar la consistencia entre lo entregado y lo que el estudiante es capaz de producir por sí mismo.

## Primera sesión (06/03/2025)

**<span style="font-size: 1.15em">Contenidos a preparar antes de la sesión del 06/03/2025</span>**

Las actividades a realizar antes de clase son:

- Lectura de la [entrada sobre web scpraping](https://link.springer.com/content/pdf/10.1007/978-3-319-32010-6_483.pdf?pdf=inline%20link) en la *Encyclopedia of Big Data*. Es un documento corto e introductorio que no te llevará más de 30 minutos 🕒️ de trabajo.
- Lectura de las páginas de la 1 a la 12, y de la 169 a la 172 del libro [Website scraping with Python](https://link.springer.com/book/10.1007/978-1-4842-3925-4) de *Gábor László Hajba*. En estas secciones se amplían los conceptos introducidos por el anterior documento, y se introduce una orientación más práctica a la tarea de scraping. Esta lectura te llevará aproximadamente 1 hora 🕒️ de trabajo.
- Lectura del artículo [*Comparison of text preprocessing methods*](https://www.cambridge.org/core/services/aop-cambridge-core/content/view/43A20821D65F1C0C4366B126FC794AE3/S1351324922000213a.pdf/comparison-of-text-preprocessing-methods.pdf), en el que se describen y evalúan diferentes estrategias de preprocesamiento de texto para tareas de PLN. Lee sólo hasta la sección 3.5. Esta lectura te llevará alrededor de 1,5 horas 🕒️ de trabajo.
- En el documento anterior se habla de la tokenización de texto a nivel de oración, palabra y carácter, pero se omite un tipo de tokenización muy relevante a día de hoy: la tokenización a nivel de subpalabra. Por eso se sugiere también la lectura del [apartado sobre tokenización](https://huggingface.co/docs/transformers/main/tokenizer_summary) del tutorial sobre Transformers de HuggingFace. Puedes desplazarte en el documento hasta el apartado que se centra en la tokenización a nivel de subpalabra y leer desde ese punto hasta el final para una introducción a las estrategias más habituales. Esta lectura te llevará alrededor de 30 minutos 🕒️ de trabajo.
- Lectura del artículo [A review of the challenges with massive web-mined corpora used in large language models pre-training](https://arxiv.org/pdf/2407.07630). En este artículo se hace un repaso de los retos principales referentes a la construcción de grandes corpus textuales a partir de contenidos recolectados de internet en uno de los escenarios más habituales: el entrenamiento de grandes modelos de lengua. Esta lectura te llevará alrededor de 1 hora 🕒️ de trabajo.

En total, todo el trabajo previo a la clase te llevará alrededor de 4 horas 🕒️. Ten en cuenta que algunos contenidos sólo son accesibles de forma gratuita desde dentro de la red de la Universidad. Si los consultas desde casa, puedes utilizar la utilidad RED UA disponible en UACloud para acceder a ellos.

**Nota adicional**: Si la adquisición de textos de Internet te interesa y en el futuro quieres ampliar tus conocimientos, el libro [Web Scraping with Python](https://www.oreilly.com/library/view/web-scraping-with/9781098145347/) de Ryan Mitchell (actualmente en su tercera edición) me parece una guia exhaustiva y con un planteamiento muy práctico sobre las principales estrategias y retos para profundizar en esta tarea.

