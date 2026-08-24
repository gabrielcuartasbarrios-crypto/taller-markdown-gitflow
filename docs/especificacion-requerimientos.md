# Especificación de Requerimientos

## 1. Descripción del sistema

## 2. Integrantes

- Nombre: Gabriel Cuartas Barrios
- Nombre: Valentina Viafara Villegas
- Nombre: Valentina Gomez Villamarin
- Nombre: Manuela Reyes Nuñez
- Nombre: Santiago Garcia Arias

## 3. Requerimientos Funcionales

### RF-01 - [Nombre del requerimiento]

#### Resumen

#### Entradas

| Entrada | Tipo de dato | Descripción |
|---|---|---|

#### Reglas o condiciones

#### Salidas

| Salida | Tipo de dato | Descripción |
|---|---|---|

#### Resultado esperado


### RF-02 - [Consultar tutorías disponibles]

#### Resumen
El sistema debe permitir que los estudiantes consulten las tutorías disponibles indicando una fecha y, opcionalmente, una asignatura o tema de interés. El sistema deberá mostrar las tutorías que coincidan con los criterios de búsqueda y la información relevante de cada una.

#### Entradas

| Entrada | Tipo de dato | Descripción |
|---|---|---|
| fecha | String | Fecha en la que el estudiante desea consultar las tutorías disponibles. Es obligatoria. |
| asignatura | String | Asignatura que el estudiante desea consultar. Es opcional. |
| tema | String | Tema de interés que el estudiante desea consultar. Es opcional. |

#### Reglas o condiciones
- El estudiante debe indicar una fecha para realizar la búsqueda.
- La asignatura y el tema son filtros opcionales.
- El sistema debe buscar únicamente las tutorías que correspondan con los criterios proporcionados.
- Para cada tutoría encontrada, el sistema debe mostrar su identificador, tema, profesor responsable, fecha, hora y cantidad de cupos disponibles.
- Si no existen tutorías que coincidan con los criterios de búsqueda, el sistema debe informar al estudiante mediante un mensaje.
- La cantidad de cupos mostrada debe corresponder a los cupos que todavía se encuentran disponibles para la tutoría.

#### Salidas

| Salida | Tipo de dato | Descripción |
|---|---|---|
| tutoriasEncontradas | String | Lista de tutorías que coinciden con los criterios de búsqueda. |
| idTutoria | String | Identificador de la tutoría encontrada |
| tema | String | Tema de la tutoría |
| profesorResponsable | String | Nombre del profesor responsable de la tutoría |
| fecha | String | Fecha en la que se da la tutoría |
| hora | String | Hora en la que se da la tutoría |
| cuposDisponibles | int | Cantidad de cupos disponibles en la tutoría |
| mensaje | String | Mensaje informado al estudiante cuando no se encuentran tutorías que correspondan con la búsqueda |

#### Resultado esperado
El sistema presenta al estudiante las tutorías disponibles que coinciden con la fecha indicada y, si fueron especificados, con la asignatura o tema de interés. Para cada tutoría encontrada se muestra su identificador, tema, profesor responsable, fecha, hora y cantidad de cupos disponibles. Si no se encuentran tutorías que cumplan con los criterios de búsqueda, el sistema muestra un mensaje informando que no existen tutorías disponibles para los criterios indicados.

### RF-03 - [Nombre del requerimiento]

#### Resumen

#### Entradas

| Entrada | Tipo de dato | Descripción |
|---|---|---|

#### Reglas o condiciones

#### Salidas

| Salida | Tipo de dato | Descripción |
|---|---|---|

#### Resultado esperado


### RF-04 - [Nombre del requerimiento]

#### Resumen

#### Entradas

| Entrada | Tipo de dato | Descripción |
|---|---|---|

#### Reglas o condiciones

#### Salidas

| Salida | Tipo de dato | Descripción |
|---|---|---|

#### Resultado esperado


## 4. Gestión de Versiones

### Ramas utilizadas

### Proceso de integración

### Conflictos encontrados
