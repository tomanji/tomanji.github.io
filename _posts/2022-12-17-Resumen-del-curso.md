---
layout: post
title: Resumen del curso
---

Estos son algunos de los sistemas de recomendación que existen y que vimos en este curso:

* Los primeros sistemas recomendadores surgieron en la década de los 90 a partir de la noción del filtrado colaborativo, donde se utilizan las interacciones históricas de los usuarios en el sistema para predecir y recomendar contenido que pueda ser de agrado para un usuario. Por una parte es posible generar recomendaciones que tengan relación a los ítems consumidos por el usuario y como también a partir de usuarios que tengan gustos similares. Problemas asociados a estos métodos son el coldstart y problemas con catálogos muy reducidos.
* Otro tipo de sistemas recomendadores son los basados en contenido en donde se busca encontrar una similitud en los ítems a recomendar a partir de la información que contienen. Un ejemplo de esto puede ser en una plataforma donde los usuarios ven películas, nos encontremos con que a uno le gusten y vea muchas películas de terror, por lo que este género de cine promete ser un tópico relevante para generar nuevas recomendaciones. 
* Los modelos latentes surgen a partir de la matriz de preferencia, corresponden a representaciones vectoriales de las calificaciones de los usuarios en un espacio vectorial de menor dimensión con los cuales se pueden hacer predicciones.
* Deep learning es el conjunto de algoritmos que son los más potentes hoy en día, son capaces de modelar complejas características del sistema y como optimizar las recomendaciones a partir de múltiples tipo de información asociada tanto al usuario como al sistema y los ítems. 

### 10 grandes problemas de los sistemas de recomendación
 Lista creada por Denis Parra profesor del curso, donde se especifican algunos problemas relevantes y desafíos que traen consigo los sistemas de recomendación actuales.
1. Filtro Burbuja: Realizar recomendaciones implica omitir cierto contenido que a otros o a poca gente les gusta, de manera que nos acostumbramos y creemos que a todos nos gusta lo mismo. Se plantea que una forma de contrarrestar esto es mostrando contenido que no sea relevante. ¿De qué nos estamos perdiendo?
2. Las IA no son inteligentes: El objetivo o recompensa de los sistemas de recomendación están hechos por personas, de manera que las IAs son entrenadas para maximizar la recompensa sin entender ni dar explicabilidad a los resultados.
3. Falta de control y transparencia: No existen grandes niveles de control sobre lo que está haciendo el algoritmo.
4. Sesgo: Los algoritmos generan recomendaciones que maximizan su recompensa, sin embargo el sesgo asociado al tipo de contenido puede venir tanto del usuario, como del modelo o los datos.
6. Interactividad y múltiples fuentes de datos.
