# Especificación de Requerimientos

## 1. Descripción del sistema

## 2. Integrantes

- Nombre: Gabriel Cuartas Barrios
- Nombre: Valentina Viafara Villegas
- Nombre: Valentina Gomez Villamarin
- Nombre: Manuela Reyes Nuñez
- Nombre: Santiago Garcia Arias

## 3. Requerimientos Funcionales

### RF-01 - [Regitrar Información de Tutoría]

#### Resumen

El requerimiento #1 permite registrar la información necesaria sobre la tutoría, tal como el código del profesor, el tema de la tutoría, la fecha, la hora de inicio, y su cantidad máxima de cupos. 

#### Entradas

| Entrada | Tipo de dato | Descripción |
|---|---|---|
|profesor|Integer|Codigo del profesor|
|tema|String|Tema de la tutoría|
|fecha|String|Fecha de la tutoría|
|hora_inicio|String|Hora de inicio de la tutoría|
|cupo_max|Integer|Cantidad máxima de cupos|

#### Reglas o condiciones

No se permitirá programar una tutoría para una fecha anterior a la fecha actual y la cantidad máxima de participantes deberá estar entre 1 y 10 estudiantes. 

#### Salidas

| Salida | Tipo de dato | Descripción |
|---|---|---|
|id|Integer|Identificador único de la tutoría|
|confirmacion|String|Mensaje de confirmación de registro de tutoría exitoso|

#### Resultado esperado

La tutoría se registra con éxito, se le asigna un código único de identificación, se le notifica al profesor que fue creada exitosamente y cumple con las reglas de capacidad maxima y condiciones de fecha. 

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

### RF-03 - [Solicitar inscripción]

#### Resumen

Si un estudiante encuentra una tutoría de su interés podrá solicitar su inscripción utilizando su código estudiantil e identificador de la tutoría. 

#### Entradas

| Entrada | Tipo de dato | Descripción |
|---|---|---|
|codigo| String | código estudiantil |
|identificador| String | identificador de la tutoría|

#### Reglas o condiciones

- El estudiante deberá encontrarse activo en la universidad.
- La tutoría debe existir.
- La tutoría deberá tener al menos un cupo disponible. 
- El estudiante no debe encontrarse previamente escrito en la tutoría. 

#### Salidas

| Salida | Tipo de dato | Descripción |
|---|---|---|
|mensaje de confirmación | String | el sistema deberá mostrar un mensaje de confirmación|

#### Resultado esperado

Cuando la inscripción se haya realizado con éxito, el sistema deberá registrar la inscripción, actualizar la cantidad de cupos disponibles y mostrar un mensaje de confirmación.

### RF-04 - [Cancelar Participación]

#### Resumen

El sistema debe permitirle al estudiante cancelar la inscripción a una tutoría. 

#### Entradas

| Entrada | Tipo de dato | Descripción |
|---|---|---|
| Código Estudiantil | String | Código alfanumérico de identificación del estudiante |
| Identificador de Tutoría | String | Código generado al registrar el espacio de tutoría |

#### Reglas o condiciones

- Condición 1. Debe existir una inscripción previa
- Condición 2. La tutoría no debe haber comenzado

#### Salidas

| Salida | Tipo de dato | Descripción |
|---|---|---|
| Mensaje de confirmación | String | Un mensaje generado por el sistema que indica que la inscripción a la tutoría fue cancelada |


#### Resultado esperado

El sistema debe haber eliminado la inscripción y liberado el cupo que correspondía al estudiante que canceló. En caso de que no se pueda cancelar, el sistema debe mostrar un mensaje que indique el porqué no fue posible cancelar la inscripción.

## 4. Gestión de Versiones

### Ramas utilizadas

- main
- develop
- feature/RF-01
- feature/RF-02
- feature/RF-03
- feature/RF-04

### Proceso de integración

```
main
   ↓
develop
   ↓
feature/RF-04
   ↓
develop
   ↓
feature/RF-02
   ↓
develop
   ↓
feature/RF-01
   ↓
develop
   ↓
feature/RF-03
   ↓
develop
   ↓
main
```

### Conflictos encontrados

Se encontraron conflictos durante el merge de las ramas feature/RF-01, feature/RF-02 y feature/RF-03 debido a un agrandamiento de las tablas realizado en la rama feature/RF-04 en Markdown. Durante todos los git merge se aplicaron los cambios actuales (current changes) para unir lo desarrollado en un único documento.