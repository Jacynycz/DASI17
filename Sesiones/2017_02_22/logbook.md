# Información de la sesión 2 del grupo

La segunda sesión del grupo fué el 22 de Febrero del 2017, la cual dedicamos completamente a investigar y desarrollar los trabajos en grupo.

## Metodologia

- Definir caso de uso.
  - ¿Qué queremos conseguir?
  - _El framework se adapda a nosotros._ Meriem
  - Diseñar sistema de implementacion de agentes (AIDS - Agent Intelligence Developement System)
- Implementar primera versión en nuestro AIDS


## Objetivo: Robots mundo virtual - WOA

Lo que proponemos es hacer un sistema de coordinación de robots para realizar acciones en conjunto mediante interacciones entre ellos y el mundo virtual. La primera acción que realizarán los robots será recogida de recursos (madera, piedra, comida, etc.) según roles asignados.

### Tipos de agentes - Primera Versión

El objetivo del juego es crear casas. Para ello hay un entorno en el que surgen recursos automáticamente y hay tres agentes diferentes:

- __Recolector:__ Se encarga de conseguir materiales. En la primera versión solo habrá madera.
  - Sólo recogerá madera si tiene asignada misión de recoger madera.
  - Si se encuentra con otros recolectores puede asignarle misiones de recolección.
- __Artesano:__ Se encarga de buscar recolectores y asignarles la misión buscar materiales.
  - En la primera versión solo mandará buscar madera.
  - Si se encuentra con otro artesano le dice "hola" y se verá reflejado en el log del server.
  - Si un recolector le trae madrea, la procesa creando un paquete de construccion(BP). Este paquete será usado por los constructores.
- __Constructor:__ Se enarga de construir edificios.
  - Si se encuentra a un recolector le dice "hey! que pasa!".
  - Si se encuentra con un artesano le manda la misión de consegir paquetes de construccion(BPs).
  - Cuando consiguen un BP construyen una casa.
