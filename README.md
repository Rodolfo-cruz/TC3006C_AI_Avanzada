# TC3006C_AI_Avanzada

Repositorio para almacenar archivos del portafolio de implementación, de análsis y del reto

**Nota general:** no tomar en cuenta los archivos de texto (.txt) ubicados a lo largo de las rutas de los archivos, ya que no hay
                  contenido asociado al proyecto en ellos. 

# Portafolio de análisis

En el portafolio de análisis se incluyen los siguientes proyectos y actividades:

## Módulo 1 estadística:

Los archivos a revisar del módulo de estadística pertenecientes al portafolio de análisis son los siguientes:

* Actividades 1 a 5 y actividad integradora 1: ubicadas en la ruta **Portafolio_Analisis/Módulo 1. Estadística**

## Módulo 2: Análisis y reporte sobre el desempeño del modelo

Para el análisis y reporte sobre el desmepeño del modelo, los archivos a revisar son:

* Jupyter Notebook: ubicado en la ruta **Portafolio_Analisis/Machine_Learning/Análisis_Reporte_Valhalla.ipynb**
  
* PDF del Jupyter Notebook: ubicado en la ruta **Portafolio_Analisis/Machine_Learning/Análisis_Reporte_Valhalla.pdf**

## Reto: ensayo sobre ética y normatividad

Para el ensayo sobre ética y normatividad asociadas al reto y al caso real analizado de discriminación algorítmica, el archivo
a revisar es:

* PDF del ensayo: ubicado en la ruta **Portafolio_Analisis/Analisis_contexto_normatividad/Analisis_contexto_normatividad.pdf**

## Aspectos a corregir y cómo se resolvieron

### Módulo 2: Análisis y reporte sobre el desempeño del modelo

* **Gráfica de subconjuntos (entrenamiento, validación, prueba) y del modelo obtenido sin evidenciar una tendencia específica:** Ésta situación
  se resolvió en primer lugar creando 3 dataframes adicionales, uno para cada subconjunto de datos a utilizar en todo el proceso de análsis de
  los modelos, pero con la diferencia de que en esta ocasión, cada dataframe tendrá sus datos correspondientes ordenados de forma ascendente
  en base a la variable predictora de grados celsius, además, una vez creados los 3 dataframes con los datos de cada subconjunto estando debidamente
  ordenados, ahora se procede a graficar para cada dato real en celsius, su correspondiente valor en grados Valks, esto
  se realiza para cada subconjunto de datos, es decir, que se tendrá una serie de puntos que representarán a aquellos datos para entrenamiento, otra serie de
  puntos para representar los datos de validación y una tercerá correspondiente a los de prueba, por lo que después de graficar las 3 series de puntos (1 por subset de datos),
  el siguiente paso consistió en que se agregara a la gráfica previa, la recta que simboliza al modelo de regresión lineal calculado para los datos en cuestión, el cual
  corresponde prácticamente a la tendencia que siguen los datos del subconjunto de validación del modelo, ya que la gráfica del modelo tras terminar su etapa de validación nos
  indica qué tan adecuadamente el modelo "mejorado" en términos de sus hiperparámetros, es capaz de ajustarse a los datos reales para predecir el valor de los mismos de la forma
  más precisa y confiable posible, por lo tanto, al graficar el modelo mejorado en la etapa de validación, se observa que la recta color rojo que representa a dicho modelo, se aproxima
  en su gran mayoría a los datos verdaderos de los 3 subconjuntos de datos, lo cual indica que dicho modelo resulta ser un ajuste mayormente adecuado para los datos reales analizados,
  motivo por el cual, en resumen, al ordenar de forma ascendente los datos anteriormente obtenidos de forma aleatoria antes de graficarlos, se garantizó que se evidenciara alguna tendencia o
  patrón entre los datos en cuestión, ya que de esa manera fue posible ilustrar adecuadamente la cantidad de cambio en la variable Valks en función de la cantidad de cambio en grados celsius,
  arrojando como resultado una tendencia decreciente entre los grados celsius y valks, es decir que la tendencia encontrada entre los datos de las variables básicamente radica en que conforme
  se aumente la cantidad de grados celsius, la cantidad de grados valks disminuirá, por lo cual, en caso de querer que la temperatura del ambiente sea más fría para erradicar el calentamiento global,
  será necesario ingresar en la máquina reguladora de temperatura, valores en valks que sean positivos y que además sean de una magnitud medianamente considerable, para lograr generar la cantidad de frío
  adecuada para compensar el calor del cambio climático. por lo que también será muy importante asegurarse de que no se ingresen valks negativos o muy pequeños a la máquina reguladora, ya que esto provocará
  que el ambiente se torne aún más cálido y como consecuencia la crisis del calentamiento global se agrave aún más. 

### Reto: ensayo sobre ética y normatividad

* **Extensión del documento superior a lo requerido:** Esta situación se resolvió investigando más información sobre la temática de IA en la toma de decisiones y en base a dicha información,
  resumir aún más el contenido escrito anteriormente, asegurando que el contenido resumido tenga exactamente el mismo significado que el contenido extenso original, además de ampliar la cantidad
  de referencias empleadas para toda la investigación en general, propiciando que la investigación en general esté más fundamentada y a la vez se comunique el mismo mensaje pero con una cantidad
  considerablemente menor de palabras.

* **Estructura del documento no adecuada para su comprensión:** La situación se resolvió agregando secciones a lo largo del ensayo, con el objetivo principal de delimitar el contenido del mismo, en
  el sentido de poder identificar fácilmente cuáles párrafos pertenecen a cada sección del ensayo y en consecuencia, la comprensión del ensayo sea mucho mejor, además de que también el ensayo siga
  una secuencia clara y ordenada de temas abordados para que la lectura del ensayo sea mayormente amigable para el lector y éste mismo pueda captar fácil y rápidamente la idea principal del tema central.

* **Agregar caso práctico que ejemplique lo expliado en el documento:** Esta situación se resolvió investigando en distintas fuentes bibliográficas, entre ellas un artículo publicado por el sitio web
  Harvard Business Review, un caso práctico en el que un algortimo basado en IA manda por Facebook anuncios de ofertas laborales para trabajos de cajero de supermercado a un 85% de mujeres y trabajos como
  taxistas a un 75% de hombres de piel negra, lo que constituye una violación a los derechos humanos, además de discriminación racial (racismo), lo cual indica que el algoritmo de IA en este caso está
  gravemente sesgado y por tanto su entrenamiento resulta ser de una calidad mayormente deficiente, lo que conduce a su vez a clasificaciones igualmente erradas e incluso discriminatorias.

* **Identificar si los elementos analizados en el ensayo se pueden trasladar al reto:** La situación se resolvió agregando un breve párrafo al ensayo en la sección titulada **Análisis ético y normativo de la solución del reto**, en el cual se explica que el principal elemento analizado en el ensayo que se puede trasladar al reto radica en que de similar manera a cómo se identificó el evitar diagnósticos erróneos en medicina como
principio ético de dicha disciplina, en el contexto del reto, uno de los principios éticos consiste en evitar la reproducción, copia, distribución, publicación, venta, entre otras acciones ilícitas que es posible
llevar a cabo para explotar la información proporcionada por la plataforma Kaggle, lo que además llega a violar los derechos de autor y de propiedad intelectual de la misma, además de transgredir incluso el derecho a la
privacidad de la información del propietario de los datos (Kaggle), por lo cual lo anterior se investigó en el sitio oficial de Kaggle en la sección titulada como **Condiciones de uso. Kaggle** donde básicamente se exponen todo el conjunto de normas y principios éticos y legales que deben seguir todos aquellos usuarios que formen parte de la comunidad digital, entre los cuales se encuentran aquellos principios que rigen la compartición
y uso de los datos, información y otros servicios ofrecidos por la plataforma en beneficio de sus usuarios, por lo que en base a esto, en el ensayo también se explica que básicamente las normas para compartir los datos de
Titanic y entre los miembros del equipo consiste en evitar el plagio de los datos provistos por Kaggle, además del uso indecuado de los mismos (divulgación, publicación, alteración no autorizadas) por parte de todos los
miembros del equipo durante todo el desarrollo del reto, garantizando así que durante todo el reto, el equipo utilice los datos solamente para los propósitos establecidos en el reto y no para llevar a cabo acciones fuera
de dicho ámbito de tal manera que se respete el derecho a la privacidad y no se comprometa la seguridad de la plataforma de Kaggle.

* **Agregar las referencias que surgan de esta mejora a la lista de referencias ya incorporadas:** Esto se resolvió básicamente actualizando en el archivo editable de word, la lista de referencias incorporadas en el ensayo
  de tal forma que de las 2 referencias que tenía originalmente el ensayo, la versión final y corregida del mismo pasó a tener 6 referencias en total, por lo que hubo un aumento de 4 referencias debida a las mejoras
  que se implementaron en el ensayo a raíz de la retroalimentación recibida por el profesor de reto, mejorando de esa manera la calidad de toda la investigación realizada. 
  
# Portafolio de implementación

En el portafolio de implementación se incluyen los siguientes proyectos o actividades:

## Módulo 1 estadística: 

Los archivos a revisar del módulo de estadística pertenecientes al portafolio de implementación son los siguientes:

* Actividades 6 a 13 y actividad integradora 2: ubicadas en la ruta **Portafolio_Implementacion/Módulo 1. Estadística**

## Módulo 2: Valhalla Challenge sin framework

Archivos a revisar para esta entrega y su ubicación dentro del repositorio:

* Jupyter notebook (archivo .ipynb): ubicado en la ruta **Portafolio_Implementacion/Machine_Learning/Valhalla_Entrega1/Valhalla_Sin_Framework.ipynb**
  
* PDF del Jupyter Notebook: ubicado en la ruta **Portafolio_Implementacion/Machine_Learning/Valhalla_Entrega1/Valhalla_Sin_Framework.pdf**

## Módulo 2: Valhalla Challenge con framework

Archivos a revisar y su ubicación:

* Jupyter notebook (archivo .ipynb): ubicado en **Portafolio_Implementacion/Machine_Learning/Valhalla_Entrega2/Valhalla2.ipynb**
  
* PDF del Jupyter Notebook: ubicado en **Portafolio_Implementacion/Machine_Learning/Valhalla_Entrega2/Valhalla2.pdf**

## Correcciones indicadas y cómo se resolvieron

### Módulo 2: Valhalla Challenge sin framework

* **Tasa de aprendizaje muy grande (repetir simulación con valores de alpha más pequeños hasta encontrar uno adecuado):** se resolvió reduciendo el valor de la tasa de
  aprendizaje de 0.003 a 0.0001, dado la tasa de aprendizaje de 0.003 aún era grande, por lo que el algoritmo no lograba converger adecuadamente, ya que el algoritmo
  pasaba por alto el punto de convergencia, sin embargo, al reducir el alpha a 0.0001 y correr la simulación una cierta cantidad de veces más, el algorimo logró ajustarse
  cada vez más al punto de convergencia ideal, al reducir los valores de J a valores mayormente pequeños, siendo éstos: 18.55 en el caso del subconjunto de entrenamiento y
  29.73 para el caso del subconjunto de prueba, en comparación con los valores J superiores a 200 que resultaban de correr la simulación con un alpha de 0.003 (tasa de aprendizaje grande),
  además se tuvo que correr la simulación varias veces debido a que los datos empleados en la misma se generan de forma aleatoria, por lo que en cada ejecución de la simulación, se obtenían
  valores de J diferentes, por lo que se repitió la simulación hasta encontrar un modelo que se ajustara lo mejor posible a los datos y que tuviera los valores de J más pequeños.

* **No entrenar 2 modelos distintos:** se resolvió implementando una función adicional para el entrenamiento del modelo llamada model_train() que recibe como parámetro de entrada los datos
  para entrenar el modelo y su vez invoca a la función gradiente_descendente() para llevar a cabo todo el proceso del algoritmo utilizando exclusivamente los datos para entrenamiento, para
  finalmente imprimir como salida la ecuación del modelo de regresión lineal que mejor se ajusta a los datos, junto con el valor de J para el subconjunto de entrenamiento. Además, también se
  implementó otra función adicional llamada model_test() que recibe como argumento de entrada esta vez el subconjunto de datos para poner a prueba el modelo definido en el entrenamiento, además,
  dicha función model_test() calcula las predicciones de los valks para los datos en celsius en el subconjunto de prueba haciendo uso de la función de hipótesis h, para posteriormente calcular
  el valor de J, pero esta vez usando los datos del subconjunto de prueba y el número de registros que tiene dicho subconjunto, por lo que después de calcular las predicciones para los datos del
  subconjunto de prueba junto con el valor J para el subconjunto de prueba, la función model_test() diseñada exclusivamente para probar el modelo, procede a retornar el conjunto de predicciones
  obtenidas y el valor J para el subconjunto de datos de prueba, por lo que al tener una función exclusivamente para entrenar los modelos y otra exclusivamente para probarlos, se elimina el hecho de
  entrenar 2 modelos distintos, 1 por cada subconjunto de datos.

* **El desempeño del modelo sobre el testing set no es adecuado:** se resolvió modificando el valor de ciertos parámetros del modelo antes de cada ejecución de la simulación, en concreto modificando el
  valor de 2 parámetros principales, alpha (tasa de aprendizaje del modelo) y el número máximo de iteraciones del mismo, por ejemplo se corrió la simulación con un alpha de 0.0001 y un máximo de iteraciones
  de 10,000, lo cual provocó que la recta del modelo pasara a estar inclinada hacia la izquierda (pendiente negativa) en lugar de hacia la derecha (pendiente positiva), lo cual propició que el modelo se acercara
  mucho más a los datos que antes cuando la pendiente del modelo era positiva, sin embargo, dicho modelo no se terminaba de ajustar de forma mayormente adecuada a los datos reales, por lo cual, se corrió otra
  simulación, esta vez con un alpha de 0.0001 y un máximo de 50,000 iteraciones, lo cual resultó en que el modelo resultante se ajustaba ligeramente mejor a los datos reales, aunque tampoco se terminaba de ajustar
  de forma mayormente adecuada, lo cual condujo a repetir nuevamente la simulación con un alpha de 0.0001 y un máximo de 100,000 iteraciones, lo cual después de varias ejecuciones dada la aleatoriedad de los datos,
  se logró que el modelo resultante se ajustara adecuadamente en su gran mayoría a los datos reales con un mínimo margen de error, además, conforme se obtuvieran valores predichos positivos más cercanos a 100 en cada simulación, el modelo resultante se ajustaba cada vez mejor a los datos reales, por lo cual después de varias repeticiones de la simulación con alpha de 0.0001 y máximo de 100,000 iteraciones a causa de la aleatoriedad presente en los datos, se lograron obtener predicciones con valores positivos muy próximos a 100, en concreto 97.9 como máximo, indicando que el modelo se ajustaba adecuadamente en su gran mayoría a los datos de prueba, motivo por el cual el desempeño del modelo final obtenido sobre el testing set fue bastante adecuado.

* **No se calcula el valor de la función de costo para subconjunto de entrenamiento y para subconjunto de prueba:** se resolvió incluyendo en las funciones model_train() y model_test() el cálculo para el valor de la función de costo J en base al modelo obtenido en el entrenamiento, esto con la finalidad de que se evidencie el valor de J para cada subconjunto de datos (entrenamiento y prueba), para lo cual, dentro de las funciones model_train() y model_test() se manda a llamar a la función J_function() cuya función consiste en calcular el valor del costo J para cada uno de los 2 subconjuntos de datos en su respectiva función correspondiente (al subset de entrenamiento se asocia con la función model_train(), mientras que el subset de prueba está asociado con la función model_test()), por lo tanto, tomando en cuenta lo anterior, se calcula el valor J para cada subconjunto por separado en su respectiva función asociada, lo cual resuelve el hecho de que anteriormente se calculaba el valor de J por cada subconjunto de datos, pero a la vez entrenando 2 modelos diferentes, en concreto 1 exclusivo para el subconjunto de entrenamiento y un segundo exclusivamente para el subconjunto de prueba, por lo cual al calcular el valor de J en 2 funciones distintas, cada una asociada al entrenamiento y prueba respectivamente del modelo, se logra visualizar de una forma mucho más clara las distinciones entre el entrenamiento y la puesta a prueba del modelo obtenido, entre las que se encuentran el hecho de que se logre distinguir con facilidad cuál función o funciones se encargan de llevar a cabo el proceso de entrenamiento del modelo a partir del subconjunto de entrenamiento y aquella otra función cuyo propósito principal básicamente consiste en probar el modelo ya obtenido previamente pero sin generar otro modelo nuevo a partir del subconjunto de prueba que es diferente al de entrenamiento. 

  ## Normatividad del reto o socio formador:

1. **Normatividad asociada a falta de confiabilidad de los algoritmos:** Asegurar que los datos con los que se entrenan los algoritmos sean de alta calidad(libres de errores
   o inconsistencias en su estructura), con el fin de evitar que debido a las inconsistencias en los datos, los algoritmos no logren aprender adecuadamente y como consecuencia,
   generen predicciones erradas que se alejen mucho de la realidad y por tanto carezcan de confiabilidad.

2. **Normatividad asociada a la falta de implicación humana en los algoritmos:** Los métodos de funcionamiento de los algoritmos de IA deberían ser accesibles para aquellas personas
   a las que les afecta de forma significativa la decisión tomada por éstos para poder anticipar lo que pasará si realizan algunas acciones en específico o si por el contrario no las
   llevan a cabo con el fin de preparase para experimentar las consecuencias de dichas acciones u omisiones, no obstante, al no involucrar personas en la toma de decisiones algorítmica,
   las decisiones resultantes de dichos algoritmos no son claramente comprendidas en su gran mayoría, lo cual puede ocasionar que en caso de presentarse algún inconveniente con el impacto
   de alguna decisión algorítmica sobre la vida de las personas, las personas afectadas no serán capaces de comprender las razones detrás de dicha decisión tomada por el algoritmo y como
   consecuencia, sus alternativas de acción para mitigar o evitar el efecto de la decisión tomada por el algoritmo serán muy limitadas.

3. **Normatividad asociada a la incapacidad de rendir cuentas sobre las decisiones algorítmicas:** La responsabilidad de las decisiones tomadas por algoritmos de inteligencia artificial idealmente
   le correspondería a los desarrolladores y/o programadores de los mismos, dado que son las personas que en pimer lugar dieron las instrucciones a dichos algoritmos sobre cuáles acciones realizar
   en caso de que sucedan diferentes situaciones, por lo que en caso de que el algoritmo tome una decisión que afecte profundamente a una persona en algún contexto específico de su vida cotidiana,
   a dicha persona afectada le será muy complicado poder saber quién es el responsable de la configuración de dicho algoritmo de IA para así poder actuar incluso legalmente si la situación lo
   ameritara, no obstante al dejar que los algoritmos tomen decisiones, ya sean de bajo, medio o alto impacto, es muy difícil encontrar a las personas responsables de dichas
   decisiones, por lo cual muchas veces no es posible actuar para mitigar el efecto de las decisiones automatizadas al desconocer muchos de los detalles que se encuentran detrás
   de la decisión tomada por un algoritmo, constituyendo así una falta a los principios éticos de nuestra sociedad, ya que los afectados no podrán contar con la información necesaria
   sobre el funcionamiento del algoritmo y detalles sobre cómo éste tomó una determinada decisión que afecte significativamente su vida en algún contexto, violando así el derecho a la información
   que tenemos como personas.
    
