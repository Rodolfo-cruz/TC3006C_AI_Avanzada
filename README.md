# TC3006C_AI_Avanzada
Repositorio para almacenar archivos del portafolio de implementación, de análsis y del reto

# Valhalla Challenge: Sin Framework

Archivos a revisar para esta entrega y su ubicación dentro del repositorio:

* Jupyter notebook (archivo .ipynb): ubicado en la ruta Portafolio_Implementacion/Machine_Learning/Valhalla_Entrega1/Valhalla_Sin_Framework.ipynb
  
* PDF del Jupyter Notebook: ubicado en la ruta

## Correcciones indicadas y cómo se resolvieron

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

# Valhalla Challenge: Entrega 3

Archivos a revisar para esta entrega y su ubicación dentro del repositorio:

* Jupyter Notebook (archivo .ipynb): ubicado en la ruta TC3006C_AI_Avanzada/Portafolio_Analisis/Machine_Learning/Reporte_Performance1/Análisis_Reporte_Valhalla.ipynb
   
* PDF del Jupyter Notebook: ubicado en la ruta TC3006C_AI_Avanzada/Portafolio_Analisis/Machine_Learning/Reporte_Performance1/Análisis_Reporte_Valhalla.pdf

**Nota:** No tomar en cuenta los archivos de texto (.txt) a lo largo de la ruta de ubicación de los archivos, ya que sirvieron solamente para crear 
      las carpetas de la ruta, pero no hay contenido asociado al proyecto en ellos.

# Normatividad del reto elegido del artículo (toma de decisiones algorítmica):

**Nota:** No tomar en cuenta los archivos de texto .txt a lo largo de la ruta de ubicación de los archivos, ya que solamente sirvieron para generar 
          las carpetas de las rutas, pero dichos archivos no tienen contenido relacionado a la concentración.

**Archivos a revisar y su ubicación en el repositorio:**

* Ensayo en formato pdf: ubicado en la ruta: TC3006C_AI_Avanzada/Portafolio_Analisis/Analisis_contexto_normatividad/Entregable1/Analisis_contexto_normatividad.pdf

  ## Normatividad del reto:

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
    
