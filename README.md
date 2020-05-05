Práctica 8 - Acceso a base datos

El objetivo de la siguiente práctica es consolidar los conocimientos adquiridos sobre acceso a base de datos en Java. Para ello se propone las siguientes actividades:

1.  Realiza un programa que realice las siguientes acciones sobre las tablas creadas en beer.sql (se adjunta el fichero en Classroom).

1.  El programa principal únicamente llamará a los distintos métodos según la opción que seleccione el usuario: consulta, actualización o inserción.

2.  La opción consulta, nos llevará a un nuevo menú con varias opciones de consultas, en las que cada una de ellas llamarán a otro método que concretamente hará las siguientes acciones: 

3.  Codifica un método que realice una consulta sobre una de las tablas (la que prefieras). 

1.  La consulta no debe ser sobre la clave primaria de la tabla, por lo tanto, debe estar preparada para tratar varias filas. En este caso se le pedirá al usuario los valores que quiere que tengan los campos del where, esta opción será sin utilizar prepared statement.

2.  Realiza un ataque SQLInjection a tu aplicación desde la consola. Para ello, lee el siguiente [artículo](https://www.oscarblancarteblog.com/2016/11/15/sql-injection/). Deja unos comentarios en el código y readme del repositiorio de cómo has realizado el ataque.

3.  Codifica otro método que sea sobre la clave primaria, por tanto, devolverá una sola fila, con prepared statement.

4.  El resultado de las consultas, será escrito en un fichero txt con la información de la consulta realizada y los resultados de la misma.

1.  La opción update llamará a un método que ejecuta una actualización de los campos de una de las tablas de la base de datos.

1.  Esta opción pedirá al usuario el campo o campos que desea actualizar sobre la tabla, por tanto, la construcción de la sentencia update dependerá directamente de lo que introduzca el usuario sobre la tabla seleccionada. 

2.  Esta opción debe ser segura y prevenir de posibles ataques SQLInjection.

3.  Las excepciones producidas en cualquiera de los métodos deben elevarse hasta el main, donde serán tratadas de manera que muestre el mensaje de la excepción y el sqlstate.

1.  Continuando con el ejercicio anterior, añadiremos una nueva opción en el menú que será "transacciones", y que nos llevará a un nuevo menú para el que se mostrará las siguientes tres acciones:

1.  Actualización simple. Incluye en esta opción dos sentencias update de una de las tablas, en las que se le pida al usuario qué campo quiere actualizar de dicha tabla y el valor del mismo. ¿Se actualiza la tabla si falla la primera sentencia? ¿Y si falla la segunda se actualiza la primera?

2.  Transacción_1. Incluye una transacción que se compone de tres sentencias de actualización sobre una tabla, aunque habrá una cuarta sentencia de actualización que no forma parte de la transacción. Realiza el control adecuado y contesta a las siguientes preguntas (incluye las preguntas y respuestas al inicio del programa como comentario). 

1.  ¿Se actualiza la tabla si falla la primera, segunda o tercera sentencia?

2.  ¿Y si se ejecuta correctamente las tres primeras sentencias que forman parte de la transacción y falla la última qué ocurre?

3.  ¿Qué ocurre si dejas el autocommit a false y ejecutas el apartado b y luego el a?\
Transacción_2. Replica el apartado anterior en un nuevo método, pero incluyendo un savepoint a partir de la segunda sentencia. ¿Qué ocurre si falla la segunda sentencia? ¿Y si falla la tercera?
