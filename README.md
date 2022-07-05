# ProyectoIA
Dadas las características de los alquileres de una casa disponible en Airbnb en New Orleans (características, ubicación, etc.) vamos a predecir cuánto debería cobrar un alquiler a corto plazo en Nueva Orleans por noche en función de su ubicación y comodidades
Dadas las características de los alquileres de una casa disponible en Airbnb en New Orleans (características, ubicación, etc.) vamos a predecir cuánto debería cobrar un alquiler a corto plazo en Nueva Orleans por noche en función de su ubicación y comodidades

Vamos a usar el dataset de kaggle esta competición New Orleans Airbnb Listings and Reviews | Kaggle, que tiene 6028 número de muestras (casas de Airbnb) y con las siguientes columnas más representativas:

1.	id: Identificador único de Airbnb para el anuncio
2.	name: Hombre del anuncio
3.	description: Descripción detallada del anuncio
4.	neighborhood_overview: Descripción del barrio por parte del anfitrión
5.	host_id: Identificador único de Airbnb para el anfitrión/usuario
6.	host_since: La fecha de creación del anfitrión/usuario. En el caso de los anfitriones que son huéspedes de Airbnb, podría ser la fecha en que se registraron como
7.	host_location: La ubicación autodeclarada del anfitrión
8.	host_response_time: El tiempo medio que tarda un anfitrión en responder a un mensaje en la plataforma Airbnb.
9.	host_response_rate: La velocidad con la que un anfitrión responde a un mensaje en la plataforma de Airbnb.
10.	property_type: Tipo de propiedad auto seleccionada. Los hoteles, camas y desayunos son descritos como tales por sus anfitriones en este campo
11.	room_type: Tipo de casa [Casa entera/apartamento|Habitación privada|Habitación compartida|Hotel]
12.	accommodates: La capacidad máxima del listado
13.	bathrooms_text: El número de baños del anuncio. En el sitio web de Airbnb, el campo de los baños ha pasado de ser un número a
14.	bedrooms: Número de habitaciones
15.	beds: Número de camas
16.	amenities: Lista de servicios incluidos en el alquiler
17.	price: precio diario en moneda local
18.	minimum_nights: número mínimo de noches de estancia para el listado
19.	maximum_nights: número máximo de noches de estancia para el anuncio
20.	has_availability: Tiene disponibilidad [t=true; f=false]
21.	number_of_reviews: El número de reseñas que tiene el anuncio
22.	first_review: La fecha de la primera/antigua revisión
23.	review_scores_rating: Puntuación global de las calificaciones
24.	instant_bookable: Reserva instantánea [t=true; f=false]

Métrica de machine learning: Vamos a usar el (MAE) (Error Absoluto Medio) debido a que es muy usado para medir los errores en sectores financieros, el error se calcula como un promedio de diferencias absolutas entre los valores objetivo y las predicciones. El MAE es una puntuación lineal, lo que significa que todas las diferencias individuales se ponderan por igual en el promedio.
Por ejemplo, si el precio de una casa es $100 y un modelo predice 200$, entonces el error es del 100%. Pero si el precio es de $20 y el modelo predice $10 el error es del 50%. 

Métrica de negocio: Se tomará las siguientes métricas de negocio:
•	Aumento de alquileres, se espera que los alquileres aumenten en un 15% de lo contrario no valdrá la pena la ejecución del modelo para suplir los costes de este
•	Un aumento del número de puntuaciones en el rango (4.0 – 5.0) de cada alquiler, se espera que aumenten en un 10%
