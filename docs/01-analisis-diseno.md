# Equipo Docente
## Integrantes
| Nombre | Usuario Gihub | Rol |  
| --- |---------------| --- |
| Adriana Rojas Molina | adriana71     | Estudiante A |   
| Adriana Rojas Molina Personal | adrianarojas  | Estudiante B |

## Fecha inicio practica
03/Septiembre/2026


## - Descripción del problema

1.- Se quiere generar un código para representar un sistema de monitoreo de tanques de almacenamiento.  
2.- El sistema tiene como objetivo principal vigilar el nivel del tanque en un instante de tiempo.  
3.- Para checar su nivel, cada tanque dispone de un sensor.  
4.- Los datos -data members- (que interesa conocer de cada tanque) son:   
- ID  
- Capacidad máxima (lt)  
- Nivel actual (lt)  
- Un estado de operación

5.- Los estados de operación serán: DETENIDO, LLENADO, VACIANDO  
6.- Las operaciones -function members- (que realiza cada tanque) son:
- consultar información
- llenar un tanque
- vaciar un tanque
- detener su operación
- consultar su nivel
- consultar su porcentaje de llenado
- obtener una lectura mediante un sensor de nivel  

7.- Considerar las reglas:  nivelActual >=0   nivelActual <=capacidadMaxima estas reglas se deben considerar para cuando se este llenando, vaciando un tanque.