---
layout: post
title: Aprendizaje Reforzado
---
Para los sistemas de recomendación existen 3 tipos de aprendizajes:

* Supervisado: Simular y predecir que feedback nos puede dar un usuario a partir de sus rating e interacciones, tanto de el como de usuarios similares y globales.
* No supervisado: No muy utilizado, pero genera recomendaciones a partir de clusterings de ítems similares:
* Reforzado: En tiempo real, un agente entrega una recomendación y a partir de una función de recompensa y el feedback del usuario, se puede ir modificando su política para mejorar la recomendación.

Hoy exploraremos los modelos reforzados.

Se llama aprendizaje reforzado ya que el sistema aprende por ensayo y error, con el objetivo de ser mas recompensado por el usuario al entregar recomendaciones eficaces. Algunos problemas asociados a estos modelos:
1.	Cold start
2.	Cambios dinámicos de preferencias de usuarios
3.	Catalogo dinámico de productos
4.	Cambios de contexto en la plataforma (contenido consumido varia del dispositivio que es consumido)
5.	Información cambia constantemente, contexto es dependiente temporal

Para estos modelos se pueden establecer dos tipos de formas de seleccionar contenido para recomendar.

* Exploración: intentar descubrir que puede gustarle al usuario
* Explotación: utilizar lo que ya se del usuario para hacer una recomendación
Hacer recomendaciones de exploración permiten conocer mas el usuario y generar mejor contenido a mayor plazo, a diferencia de otros modelos como ALS que abusan de la explotación.

La explotación puede hacer que el usuario no consuma alternativas que puedan entregar una mayor recompensa.  Sin embargo, como se recomienda contenido que es relevante genera una recompensa que es a corto plazo pero segura. Por otro lado, la exploración podría causar que se recomiende contenido que no sea del agrado del usuario y este termine por abandonar el sistema, pero podríamos obtener conocimiento nuevo para familias de recomendaciones futuras que nos permita entregar un set de contenido para el futuro.

Es por todo lo anterior que lo que se busca es un balance entre exploración y explotación para optimizar de mejor manera las recomendaciones. Algunos conceptos claves de este tipo de modelos son:
1.	Enviroment: ambiente de recomndeaciones y feedbacks
2.	State: configuración del estado actual
3.	Agent: quien ejecuta acciones y aprende a interactuar con el entorno
4.	Action: set de acciones
5.	Step: Cambiar de un estado a otro cuando se realiza una acción.
6.	Reward: incentivo como premio o castigo para el aprendizaje
7.	Target: Lo que se busca maximizar
8.	Policy: Qué acción tomar en cada paso, el modelo aprende a optimizar estas decisiones
9.	Episode: Conjunto de steps.

### Multiarmed Bandits
Son agentes que se encargaran de recomendar contenido y obtener una recompensa positiva o negativa para reajustar sus recomendaciones. Si inferimos una distribución de probabilidad de éxito por cada item, el agente intentará maximizar su recompensa positiva aprendiendo de los gustos de los usuarios durante el entrenamiento.
Una estrategia para recomendar es generar una exploración inicial a partir de una cantidad K o un porcentaje de las recomendaciones totales, para luego explotar contenido conocido. De esta manera abrimos chances de nuevo conocimiento del usuario pero manteniendo la recompensa a corto plazo.
