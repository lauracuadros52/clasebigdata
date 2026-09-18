Proyecto Académico Big Data - Laura Jisseth Cuadros & Yamile Mosquera Vasquez

Optimización de la generación de indicadores diarios de producción mediante Big Data
1. Resumen:
En el área de producción es necesario contar diariamente con información que permita conocer cómo se comportaron las líneas y cuáles fueron los principales resultados de la operación. Para esto se utilizan indicadores relacionados con producción, utilización, eficiencia y tiempos de operación, entre otros.
Actualmente, esta información se obtiene a través de reportes descargados desde SAP. Sin embargo, el reporte que se descarga no queda inmediatamente listo para ser utilizado en Power BI. Antes de llegar al tablero, es necesario realizar diferentes actividades en Excel, como organizar la información, aplicar fórmulas, realizar cruces con otras fuentes y preparar las tablas que finalmente serán utilizadas para el análisis.
Este proceso funciona y permite obtener la información necesaria, pero también implica dedicar tiempo a tareas que son principalmente operativas y repetitivas. Además, cuando se trabaja con varios archivos o se deben realizar diferentes transformaciones, aumenta la posibilidad de cometer errores o de que una modificación en una fórmula afecte el resultado final.

________________________________________
2. Planteamiento del problema:
En la operación diaria de producción se generan grandes cantidades de información que permiten hacer seguimiento al comportamiento de las líneas. Una parte importante de esta información se encuentra disponible en SAP y puede ser descargada mediante reportes.
Sin embargo, obtener el reporte desde SAP no significa que la información esté lista para ser analizada.
En el proceso actual es necesario tomar el archivo descargado y realizar una serie de actividades en Excel antes de poder llevar la información a Power BI. Dependiendo de la información requerida, estas actividades pueden incluir limpieza de datos, organización de columnas, aplicación de fórmulas, cruces con otras tablas y generación de campos adicionales.
En otras palabras, el proceso actualmente puede resumirse de la siguiente manera:
SAP → Excel → Transformaciones → Cálculos → Validaciones → Power BI
El problema no está en que Excel no permita realizar estas actividades. De hecho, actualmente permite obtener los resultados necesarios. El problema está en que una parte importante del proceso depende de tareas manuales y de archivos que deben ser preparados antes de que la información pueda ser utilizada.
Esto puede generar varias dificultades. Por ejemplo, el proceso puede tomar una cantidad considerable de tiempo, existe dependencia de las fórmulas y estructuras creadas en el archivo y resulta más difícil mantener el mismo procedimiento cuando se incorporan nuevos datos o cuando el volumen de información aumenta.
Además, el tiempo que se dedica a organizar y preparar los datos es tiempo que no se puede dedicar al análisis de los resultados.
A partir de esta situación surge la necesidad de buscar una alternativa que permita automatizar las transformaciones que actualmente se realizan en Excel, manteniendo los resultados utilizados para el seguimiento de producción.

________________________________________
3. Justificación:
La información de producción tiene valor cuando puede estar disponible en el momento en que se necesita y cuando existe confianza en los resultados que presenta.
Actualmente, el proceso utilizado para generar los indicadores cumple con su objetivo, pero requiere una serie de actividades posteriores a la descarga de información desde SAP. Muchas de estas actividades son repetitivas y deben realizarse cada vez que se actualiza la información.
Esto representa una oportunidad para aplicar los conocimientos adquiridos en Big Data sobre un problema real del entorno laboral.
La propuesta consiste en trasladar progresivamente la lógica que hoy se encuentra en Excel hacia Databricks. De esta manera, las transformaciones quedarían definidas mediante código y podrían ejecutarse nuevamente cada vez que se disponga de información nueva.
Una de las principales ventajas de este cambio sería disminuir la cantidad de trabajo manual necesario para preparar los datos. También permitiría tener mayor claridad sobre el proceso que sigue la información desde que sale de SAP hasta que llega a Power BI.
Otro aspecto importante es que los datos de producción no solamente pueden utilizarse para construir indicadores. Una vez que se encuentran organizados y estructurados, también pueden ser analizados para encontrar comportamientos, relaciones y patrones que no necesariamente son evidentes en el reporte tradicional.
Por esto, además de automatizar el proceso, el proyecto contempla explorar el uso de Machine Learning para determinar qué variables pueden ayudar a explicar o anticipar el comportamiento de algunos indicadores de producción.

________________________________________
4. Objetivo general:
Optimizar el proceso de generación de los indicadores diarios de producción mediante la implementación de una solución de datos en Databricks que permita automatizar las principales transformaciones realizadas actualmente en Excel, reduciendo el tiempo y la intervención manual requerida para preparar la información utilizada en Power BI.
________________________________________
5. Objetivos específicos:
5.1	Analizar el proceso actual utilizado para transformar la información descargada desde SAP e identificar las principales actividades que se realizan manualmente en Excel.
5.2  Construir en Databricks un proceso de transformación de datos que permita limpiar, organizar y preparar la información proveniente de SAP.
5.3 Trasladar las principales fórmulas y transformaciones utilizadas actualmente en Excel a Databricks, verificando que los resultados obtenidos sean consistentes con el proceso actual.
5.4  Explorar los datos de producción mediante técnicas de analítica y Machine Learning, con el fin de identificar variables y patrones relevantes en el comportamiento de los indicadores.
5.5 Comparar el proceso actual con el proceso automatizado, considerando aspectos como tiempo de procesamiento, cantidad de actividades manuales y consistencia de los resultados.
   
________________________________________
6. Análisis económico: 
Costo actual del proceso: 
1 persona × 1 hora/día × 22 días = 22 horas-hombre/mes
Con un costo de $60.000 por hora
22 × $60.000 = $1.320.000 mensuales
Al año:
$1.320.000 × 12 = $15.840.000
Es decir, bajo este escenario, la empresa estaría destinando aproximadamente $15 millones al año en horas-hombre para la elaboración manual de los indicadores. 
Después de implementar la solución, el trabajo no desaparece completamente. Las personas seguirían haciendo actividades de:
•	Validación de información. 
•	Análisis de resultados. 
•	Revisión de excepciones. 

Por ejemplo, si después de la automatización solo fueran necesarios 20 minutos diarios:
1 × 0,33 × 22 = 7,33 horas/mes
 7,33 × $60.000 = $440.000 mensuales
Entonces:
Ahorro mensual = $1.320.000 − $440.000 = $880.000
Ahorro anual = $880.000 × 12 = $10.560.000

________________________________________
7. Alcance:
El proyecto se enfocará en el proceso de generación de indicadores de producción a partir de la información descargada desde SAP.
Para desarrollar el proyecto se cuenta con dos referencias principales:
•	El archivo original descargado desde SAP, sin procesamiento.
•	El archivo de Excel que actualmente contiene las transformaciones y organización de la información utilizada para Power BI.
El análisis permitirá entender qué ocurre con la información entre estos dos puntos y cuáles de esas actividades pueden trasladarse a Databricks.
El proyecto incluirá la construcción de las capas de datos, transformación de la información, validación de resultados, análisis exploratorio y evaluación de modelos de Machine Learning cuando los datos lo permitan.
No se busca modificar el proceso transaccional de SAP. El objetivo es trabajar sobre la información que actualmente se obtiene de este sistema y mejorar el proceso posterior de preparación y análisis.
<img width="1478" height="807" alt="Bigdata1" src="https://github.com/user-attachments/assets/2f24dc07-b020-4927-849e-f399c648d891" />
________________________________________

8. Visualizaciones Dashboard indicadores en Power BI:
   
Se desarrolló un dashboard en Power BI para visualizar los resultados generados por el proceso de automatización en Databricks. Este permite: Analizar la eficiencia mecánica y nivel de utilización por la línea de producción y presentación de producto, identificar cuellos de botella operativos causados por tiempos de mantenimiento y paradas improductivas, monitorear el volumen máximo de cajas producidas frente al porcentaje de cumplimiento de metas de la planta, entre otros. La visualización se alimenta de las tablas gold creadas en databricks, que contienen la información consolidada. Adicional, el pipeline de datos queda desplegado como un proceso automatizado en Databricks que permite refrescar las métricas de producción de forma periódica.
<img width="696" height="330" alt="Bigdata4" src="https://github.com/user-attachments/assets/fa065d86-68e7-43b8-8f7a-16d58f00d277" />

<img width="690" height="364" alt="Bigdata3" src="https://github.com/user-attachments/assets/17d1156f-a398-48f5-867d-27cb8eedf165" />

<img width="696" height="770" alt="Bigdata 2" src="https://github.com/user-attachments/assets/37967fd0-abe4-408b-a09a-5adaea69ed5b" />

