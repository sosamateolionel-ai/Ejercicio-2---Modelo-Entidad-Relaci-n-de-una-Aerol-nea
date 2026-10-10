# Ejercicio 2 - Modelo Entidad-Relación de una Aerolínea

## Descripción

Este ejercicio consiste en diseñar un modelo Entidad-Relación (DER) para un sistema de gestión de una aerolínea. El modelo permite representar los vuelos, aviones, empleados, tripulaciones, pasajeros y reservas, junto con las relaciones existentes entre ellos.

## Entidades y atributos

### 1. Vuelo

Representa los vuelos programados por la aerolínea.

* `id_vuelo`: identificador del vuelo.
* `origen`: lugar de salida.
* `destino`: lugar de llegada.
* `horario`: horario del vuelo.
* `codigo_vuelo`: código asignado al vuelo.

### 2. Avion

Representa los aviones utilizados para realizar los vuelos.

* `id_avion`: identificador del avión.
* `matricula`: matrícula del avión.
* `modelo`: modelo del avión.
* `numero_vuelo`: número de vuelo asociado.
* `capacidad`: cantidad máxima de pasajeros.

### 3. Empleado

Representa al personal que trabaja para la aerolínea.

* `id_Empleado`: identificador del empleado.
* `nombre`: nombre del empleado.
* `apellido`: apellido del empleado.
* `rol`: función que desempeña.
* `dni`: documento de identidad.

### 4. Tripulacion

Representa la asignación de empleados a los vuelos.

* `id_vuelo`: identificador del vuelo.
* `id_empleado`: identificador del empleado.

### 5. Pasajero

Representa a las personas que viajan en los vuelos.

* `id_pasajero`: identificador del pasajero.
* `nombre`: nombre del pasajero.
* `apellido`: apellido del pasajero.
* `numero_vuelo`: número de vuelo asociado.
* `dni`: documento de identidad.

### 6. Reserva

Representa las reservas realizadas para viajar en un vuelo.

* `id_reserva`: identificador de la reserva.
* `codigo`: código de reserva.
* `numero_asiento`: asiento asignado.
* `codigo_vuelo`: código del vuelo reservado.
* `id_pasajero`: identificador del pasajero.

## Relaciones y cardinalidades

* **Avion – Vuelo (Opera):** un avión puede operar varios vuelos, mientras que cada vuelo utiliza un avión.
* **Empleado – Tripulacion (Asignado):** permite asociar empleados con las tripulaciones correspondientes.
* **Vuelo – Tripulacion (Asigna):** permite relacionar los vuelos con sus tripulaciones.
* **Vuelo – Reserva (Tiene):** un vuelo puede tener varias reservas, mientras que cada reserva corresponde a un vuelo.
* **Pasajero – Reserva (Realiza):** permite relacionar a los pasajeros con sus reservas.

## Objetivo

Diseñar una base de datos que permita administrar las operaciones principales de una aerolínea, incluyendo la programación de vuelos, la asignación de aviones y empleados, la identificación de pasajeros y la gestión de reservas y asientos.

