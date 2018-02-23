# P2_Quiz

## Introducción ##
Este es un programa hecho en JavaScript que permite:
* Gestionar una lista de preguntas y respuestas, es decir, debe permitir que el usuario pueda añadir nuevas preguntas con sus respuestas, borrar las preguntas y respuestas existentes, editarlas, consultarlas, etc.
* Probar a contentar correctamente una pregunta, es decir, debe el usuario podrá elegir una determinada pregunta, e intentar contestarla correctamente.
* Jugar a contestar correctamente todas las preguntas, es decir, el usuario le pedirá al programa que presente todas las preguntas existentes de una en una, en orden aleatorio, y sin repeticiones, para intentar acertar las respuesta. Cuando se produzca un fallo se detendrá el juego.

## Comandos del programa ##
### help (y la abreviatura h) ###
El programa debe responder a este comando mostrando un mensaje de ayuda que liste todos los comandos existentes y una breve descripción de cada uno de ellos.

### list ###
El programa debe responder a este comando listando todas las preguntas (no deben mostrarse las respuestas) almacenadas en el programa. Cada pregunta se precederá de un identificador numérico que podrá utilizarse en otros comandos para referirse a esa pregunta.

### show <id> ###
En respuesta a este comando, el programa mostrará la pregunta y la respuesta asociadas al identificador id. Debe comprobarse que se ha introducido un valor para id y que éste es correcto.

### add ###
Este comando se utilizará para añadir interactivamente un nuevo quiz al programa. En primer lugar se le pedirá al usuario que introduzca el texto de la pregunta, y a continuación se le pedirá que introduzca el texto de la respuesta correcta.

### delete <id> ###
Este comando se usará para eliminar del programa el quiz asociado al identificador id. Debe comprobarse que se ha introducido un valor para id y que éste es correcto.

### edit <id> ###
Este comando se usará para editar la pregunta y las respuesta del quiz indicado. Primero se le mostrará al usuario el texto de la pregunta para que lo modifique, y a continuación se hará lo mismo con el texto de la respuesta. Debe comprobarse que se ha introducido un valor para id y que éste es correcto.

### test <id> ###
Este comando sirve para que el usuario pruebe el quiz asociado con el identificador id. Se le presentará al usuario la pregunta del quiz para que introduzca una respuesta. Una vez contestada la pregunta, se le indicara si ha contestado correctamente o no. Debe comprobarse que se ha introducido un valor para id y que éste es correcto.

### play (y la abreviatura p) ###
Este es el comando principal del programa. Se usa para jugar a contestar todas las preguntas correctamente. Este comando presentará todas las preguntas existentes de una en una al usuario para que las responda. Si una pregunta se responde correctamente, entonces se debe continuar presentando otra pregunta al azar. Se sigue jugando hasta que se falle una respuesta. El objetivo del juego es alcanzar el mayor número de respuestas acertadas consecutivamente. No deben mostrarse preguntas repetidas. Cuando no existan más preguntas que mostrar, se termina el juego, indicando al usuario el número de quizzes que ha contestado correctamente.

### credits ###
El programa responde a este comando mostrando el nombre de los alumnos autores de la práctica.

### quit (y la abreviatura q) ###
Se usa para terminar la ejecución del programa.

### Nota: ###
Algunos de los comando anteriores pueden invocarse tecleando únicamente la primera letra del nombre del comando. Así, "h" sería equivalente a ejecutar "help".

## Persistencia ##
* El programa permite guardar las preguntas que maneja en un fichero de texto llamado quizzes.json.
* El programa permite leer este fichero cuando arranca para cargar las preguntas existentes.
* Cada vez que se añada, borre o modifique una pregunta, se actualiza el contenido de este fichero.
* El contenido del fichero quizzes.json es un texto JSON con todas las preguntas manejadas. Es un array de objetos quiz, donde cada objeto quiz es un diccionario con las claves question y answer, y los valores asociados son el texto de la pregunta y el de la respuesta.
* Si este fichero no existe cuando arranca el programa, se crea con unas preguntas por defecto.
* En caso de que al leer o escribir en este fichero se produzca algún error, se aborta la ejecución del programa.
