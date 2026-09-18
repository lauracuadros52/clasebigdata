Proyecto Académico Big Data - Laura Jisseth Cuadros & Yamile Mosquera Vasquez

Optimización de la generación de indicadores diarios de producción mediante Big Data

1. Resumen:
   
<p align="justify">En el área de producción es necesario contar diariamente con información que permita conocer cómo se comportaron las líneas y cuáles fueron los principales resultados de la operación. Para esto se utilizan indicadores relacionados con producción, utilización, eficiencia y tiempos de operación, entre otros.

<p align="justify">Actualmente, esta información se obtiene a través de reportes descargados desde SAP. Sin embargo, el reporte que se descarga no queda inmediatamente listo para ser utilizado en Power BI. Antes de llegar al tablero, es necesario realizar diferentes actividades en Excel, como organizar la información, aplicar fórmulas, realizar cruces con otras fuentes y preparar las tablas que finalmente serán utilizadas para el análisis.

<p align="justify">Este proceso funciona y permite obtener la información necesaria, pero también implica dedicar tiempo a tareas que son principalmente operativas y repetitivas. Además, cuando se trabaja con varios archivos o se deben realizar diferentes transformaciones, aumenta la posibilidad de cometer errores o de que una modificación en una fórmula afecte el resultado final.

________________________________________
2. Planteamiento del problema:
   

<p align="justify">En la operación diaria de producción se generan grandes cantidades de información que permiten hacer seguimiento al comportamiento de las líneas. Una parte importante de esta información se encuentra disponible en SAP y puede ser descargada mediante reportes.

<p align="justify">Sin embargo, obtener el reporte desde SAP no significa que la información esté lista para ser analizada.
En el proceso actual es necesario tomar el archivo descargado y realizar una serie de actividades en Excel antes de poder llevar la información a Power BI. Dependiendo de la información requerida, estas actividades pueden incluir limpieza de datos, organización de columnas, aplicación de fórmulas, cruces con otras tablas y generación de campos adicionales.

<p align="justify">En otras palabras, el proceso actualmente puede resumirse de la siguiente manera:

<p align="justify">SAP → Excel → Transformaciones → Cálculos → Validaciones → Power BI

<p align="justify">El problema no está en que Excel no permita realizar estas actividades. De hecho, actualmente permite obtener los resultados necesarios. El problema está en que una parte importante del proceso depende de tareas manuales y de archivos que deben ser preparados antes de que la información pueda ser utilizada.

<p align="justify">Esto puede generar varias dificultades. Por ejemplo, el proceso puede tomar una cantidad considerable de tiempo, existe dependencia de las fórmulas y estructuras creadas en el archivo y resulta más difícil mantener el mismo procedimiento cuando se incorporan nuevos datos o cuando el volumen de información aumenta.

<p align="justify">Además, el tiempo que se dedica a organizar y preparar los datos es tiempo que no se puede dedicar al análisis de los resultados.
A partir de esta situación surge la necesidad de buscar una alternativa que permita automatizar las transformaciones que actualmente se realizan en Excel, manteniendo los resultados utilizados para el seguimiento de producción.

________________________________________
3. Justificación:
   

<p align="justify">La información de producción tiene valor cuando puede estar disponible en el momento en que se necesita y cuando existe confianza en los resultados que presenta.
Actualmente, el proceso utilizado para generar los indicadores cumple con su objetivo, pero requiere una serie de actividades posteriores a la descarga de información desde SAP. Muchas de estas actividades son repetitivas y deben realizarse cada vez que se actualiza la información.

<p align="justify">Esto representa una oportunidad para aplicar los conocimientos adquiridos en Big Data sobre un problema real del entorno laboral.

<p align="justify">La propuesta consiste en trasladar progresivamente la lógica que hoy se encuentra en Excel hacia Databricks. De esta manera, las transformaciones quedarían definidas mediante código y podrían ejecutarse nuevamente cada vez que se disponga de información nueva.

<p align="justify">Una de las principales ventajas de este cambio sería disminuir la cantidad de trabajo manual necesario para preparar los datos. También permitiría tener mayor claridad sobre el proceso que sigue la información desde que sale de SAP hasta que llega a Power BI.

<p align="justify">Otro aspecto importante es que los datos de producción no solamente pueden utilizarse para construir indicadores. Una vez que se encuentran organizados y estructurados, también pueden ser analizados para encontrar comportamientos, relaciones y patrones que no necesariamente son evidentes en el reporte tradicional.

________________________________________
4. Objetivo general:

<p align="justify">Optimizar el proceso de generación de los indicadores diarios de producción mediante la implementación de una solución de datos en Databricks que permita automatizar las principales transformaciones realizadas actualmente en Excel, reduciendo el tiempo y la intervención manual requerida para preparar la información utilizada en Power BI.
   
________________________________________
5. Objetivos específicos:
   
<p align="justify">5.1	Analizar el proceso actual utilizado para transformar la información descargada desde SAP e identificar las principales actividades que se realizan manualmente en Excel.
   

<p align="justify">5.2  Construir en Databricks un proceso de transformación de datos que permita limpiar, organizar y preparar la información proveniente de SAP.


<p align="justify">5.3 Trasladar las principales fórmulas y transformaciones utilizadas actualmente en Excel a Databricks, verificando que los resultados obtenidos sean consistentes con el proceso actual.


<p align="justify">5.4 Comparar el proceso actual con el proceso automatizado, considerando aspectos como tiempo de procesamiento, cantidad de actividades manuales y consistencia de los resultados.
   
________________________________________
6. Análisis económico:
   

<p align="justify">Costo actual del proceso:
1 persona × 1 hora/día × 22 días = 22 horas-hombre/mes
Con un costo de $60.000 por hora
22 × $60.000 = $1.320.000 mensuales
Al año:
$1.320.000 × 12 = $15.840.000

<p align="justify">Es decir, bajo este escenario, la empresa estaría destinando aproximadamente $15 millones al año en horas-hombre para la elaboración manual de los indicadores. 
Después de implementar la solución, el trabajo no desaparece completamente. Las personas seguirían haciendo actividades de:
•	Validación de información. 
•	Análisis de resultados. 
•	Revisión de excepciones. 

  
<p align="justify">Por ejemplo, si después de la automatización solo fueran necesarios 20 minutos diarios:
  1 × 0,33 × 22 = 7,33 horas/mes
  7,33 × $60.000 = $440.000 mensuales
  Entonces:
  Ahorro mensual = $1.320.000 − $440.000 = $880.000
  Ahorro anual = $880.000 × 12 = $10.560.000

________________________________________
7. Alcance:

<p align="justify">El proyecto se enfocará en el proceso de generación de indicadores de producción a partir de la información descargada desde SAP.
Para desarrollar el proyecto se cuenta con dos referencias principales:
•	El archivo original descargado desde SAP, sin procesamiento.
•	El archivo de Excel que actualmente contiene las transformaciones y organización de la información utilizada para Power BI.

<p align="justify">El análisis permitirá entender qué ocurre con la información entre estos dos puntos y cuáles de esas actividades pueden trasladarse a Databricks.
El proyecto incluirá la construcción de las capas de datos, transformación de la información, validación de resultados, análisis exploratorio y evaluación de modelos de Machine Learning cuando los datos lo permitan.
No se busca modificar el proceso transaccional de SAP. El objetivo es trabajar sobre la información que actualmente se obtiene de este sistema y mejorar el proceso posterior de preparación y análisis.


<img width="1478" height="807" alt="Bigdata1" src="https://github.com/user-attachments/assets/2f24dc07-b020-4927-849e-f399c648d891" />

________________________________________
8. Arquitectura de datos:

<p align="justify"> La solución propuesta utiliza una arquitectura basada en Databricks, en la cual la información pasa por diferentes etapas antes de ser consumida en Power BI. </p>

Databricks Volume

<p align="justify"> Los archivos de información de producción son almacenados inicialmente en Databricks Volumes, permitiendo centralizar la información antes de iniciar su procesamiento. </p>

Bronze – Datos crudos

<p align="justify"> En esta capa se conservó la información original sin transformaciones, permitiendo mantener la trazabilidad de los datos desde su origen. </p>

Silver – Transformación

<p align="justify"> En esta etapa se realizaron las principales actividades de limpieza, organización y transformación de los datos. También se preparan las variables necesarias para el cálculo de los indicadores. </p>

Gold – Datos para análisis

<p align="justify"> En esta capa se consolidaron los datos y resultados que fueron utilizados para alimentar el dashboard de Power BI y facilitar el análisis de los indicadores de producción. </p>

<img width="326" height="400" alt="Tablas gold" src="https://github.com/user-attachments/assets/4ddddf33-384f-4775-a928-38e6a41d64d8" />


Databricks Jobs


<p align="justify"> Los Jobs permiten automatizar la ejecución del pipeline, haciendo posible que el proceso pueda ejecutarse nuevamente cuando se incorporen nuevos datos. </p>


Power BI – Visualización

<p align="justify"> Finalmente, las tablas Gold son utilizadas como fuente para Power BI, donde se construye el dashboard de indicadores de producción. Esta herramienta permite visualizar y analizar información relacionada con producción, eficiencia, utilización, cumplimiento de metas, mantenimiento y paradas improductivas, facilitando el seguimiento de la operación y la toma de decisiones. </p>


<img width="700" height="330" alt="Bigdata4" src="https://github.com/user-attachments/assets/fa065d86-68e7-43b8-8f7a-16d58f00d277" />




<img width="700" height="364" alt="Bigdata3" src="https://github.com/user-attachments/assets/17d1156f-a398-48f5-867d-27cb8eedf165" />




<img width="700" height="770" alt="Bigdata 2" src="https://github.com/user-attachments/assets/37967fd0-abe4-408b-a09a-5adaea69ed5b" />


________________________________________
9. Resultados obtenidos:

<p align="justify">La implementación de Databricks permitió transformar el proceso de generación de indicadores de producción, pasando de un esquema con alta intervención manual en Excel a un flujo de datos más automatizado, estructurado y trazable. La integración de las capas Bronze, Silver y Gold con Power BI facilita la actualización y análisis de la información, mientras que el uso de Databricks Jobs permite reutilizar el proceso con nuevos datos. De esta manera, la solución contribuye a reducir tareas operativas y establece una base para futuros análisis avanzados y modelos predictivos.</p>


<p align="justify">El proyecto fue desarrollado con la información disponible para el análisis. Para fortalecer los resultados futuros, se plantea incorporar un histórico más amplio de datos de producción, incluir nuevas fuentes de información y evaluar modelos de Machine Learning que permitan identificar patrones y anticipar el comportamiento de los indicadores.

