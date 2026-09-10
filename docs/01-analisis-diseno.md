# Equipo Docente
## Integrantes
| Nombre | Usuario Gihub | Rol |  
| --- |---------------| --- |
| Adriana Rojas Molina | adriana71     | Estudiante A |   
| Adriana Rojas Molina Personal | adrianarojas  | Estudiante B |

## Fecha inicio practica
03/Septiembre/2026


## 1 Descripción del problema

1.- Se quiere generar un código para representar un sistema de monitoreo de tanques de almacenamiento.  
2.- El sistema tiene como objetivo principal vigilar el nivel del tanque en un instante de tiempo.  
3.- Para checar su nivel, cada tanque dispone de un sensor.  
4.- Los datos -data members- (que interesa conocer de cada tanque) son:   
- ID  
- Capacidad máxima (lt)  
- Nivel actual (lt)  
- Un estado de operación

5.- Los estados de operación serán: DETENIDO, LLENANDO, VACIANDO  
6.- Las operaciones -function members- (que realiza cada tanque) son:
- consultar información
- llenar un tanque
- vaciar un tanque
- detener su operación
- consultar su nivel
- consultar su porcentaje de llenado
- obtener una lectura mediante un sensor de nivel  

7.- Considerar las reglas:  nivelActual >=0   nivelActual <=capacidadMaxima estas reglas se deben considerar para cuando se este llenando, vaciando un tanque.  

## 2 Identificación de objetos

** ¿Qué elementos del problema pueden representarse mediante objetos? **
1) Tanque  representa el tanque de almacenamiento, es el objeto que se tiene que vigilar, contiene liquido o gas
2) Sensor  representa el sensor asociado a un tanque, es el objeto que da la lectura del nivel actual del tanque  
   cuando está DETENIDO, LLENANDO, VACIANDO  

## 3 Estado y comportamiento

| Objeto propuesto | Responsabilidad | Información que debe conservar | Comportamientos que debe realizar |
| Tanque | contiene líquido | capacidad maxima, nivel actual, identificación, estado | llenado, vaciado |
| Sensor| lectura nivel actual | identificación, lectura actual| leer nivel |

## 4 Relaciones entre los objetos

El problema solo tiene dos objetos: Tanque y Sensor
El objeto Tanque requiere de un objeto específico una lectura de su nivel actual
El objeto Sensor está relacionado con solo y solo un tanque
El objeto Tanque no puede funcionar si no existe un sensor
El objeto Sensor no le interesa el estado del tanque o su capacidad, su trabajo es solo dar un dato. El objeto Tanque es
quien debe realizar las operaciones de llenado, vaciado, etc.

## 5 Diseño de clases

| Clase | Atributos propuestos | Tipo de dato | Métodos propuestos      | Responsabilidad                                                                                          |
|--|----------------------|--------------|-------------------------|----------------------------------------------------------------------------------------------------------|
| Tanque | ID                   | Alfanumérico | Consultar información   | Devuelve información de capacidad, nivel actual, porcentaje de llenado, estado                           |
|  | capacidadMaxima      | Numérico     | Llenar tanque           | Incrementa el nivel por una cantidad de lt tomando como inicio una lectura del nivel                     |
|  | nivelActual          | Numérico     | Vaciar tanque           | Decrementa el nivel por una cantidad de lt tomando como inicio una lectura del nivel                     |
|  | estado               | Numérico     | Detener operación       | Detiene el llenado o vaciado de un tanque, se llama hasta que llegue a un nivel o llegue a un porcentaje |
|  |                      |              | Consultar nivel         | Devuelve el nivel del tanque, para hacerlo debe obtener la lectura del sensor                            |
|  |                      |              | Consultar % de llenado  | Devuelve el % correspondiente al nivel actual del tanque                                                 |
|  |                      |              | Consultar estado        | Devuelve el estado en el que esta el tanque (llenando, vaciando, detenido)                               |
|  |                      |              | Obtener lectura sensor  | Solicita la lectura de un sensor                                                                         |
| Sensor | ID                   | Alfanumérico | Consulta informacion    | Devuelve el ID de un sensor                                                                              |
|  | lecturaActual        | Numerico     | Devuelve valor obtenido | Devuelve el nivel actual en lts del tanque                                                               |

## 6 Diagrama UML
Aquí va el diagrama del repositorio
Aquí va el otro diagrama

![DiagramaUML](images/diagramaUMLSistemaMonitoreo.png)
