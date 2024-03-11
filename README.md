# Examen librería

## Crear una librería 

Creando un jar pero sin escoger ninguna como Main Class. En nuestro caso hicimos esto con el programa Libreria donde tendremos las clases Entrada y Salida.

Para ello haremos: 

*Ir a project structures > Artifacts > + > JAR > Seleccionar Main class (No seleccionamos ninguna como Main porque no nos interesa) > From modules with dependencies > Apply > OK*

*Build > Artifacts > Select JAR > Build*


## Utilizar una librería creada

Tras haber creado la libreria de entrada/salida la utilizaremos en nuestro programa Calculadora tanto para pedir datos como para recibirlos. 

*Project Structure > Libraries > + > Seleccionamos donde se encuentra el jar de nuestro programa de librería > Apply > OK > Creamos el método en el programa que queremos usarla.*

En nuestro caso, en el programa creación de librería usaremos los métodos de Entrada y Salida de la librería en que tengamos estos métodos de forma que los usaremos para mostrar y pedir los datos. 


## Crear una nueva rama

Ahora vamos a modificar nuestro programa Calculadora, antes teniamos 4 operaiones básicas (Suma, Resta, Multiplicación y División), ahora queremos añadir umna nueva operación, las raíces. Teniendo en cuenta que un cambio podría ser fatal para nuestra ya funcional Calculadora, crearemos otra rama, diferente de la Main en la que trabajaremos añadiendo la nueva función. Para ello utilizaremos el comando: 

git branch Raiz

y para cambiar de Rama el comando: 

git checkout Raiz

## Merge con Squash

Ya tenemos nuestra nueva Calculadora con esa nueva función añadida, ahora podemos añadir esos cambios en la Main, para eso haremos un Squash ya que de esa forma podremos mezclar los dos programas. Para ello usaremos el comando 

git --squash Raiz 

Ahora tenemos toda la información de los commits hechos en Raiz en solo un commmit. 


## Release

Hacemos otra vez los pasos de Creacion de Una Libreria. Y realizaremos un tag en el último commit para poder subir el -jar y tener así una release con el código y poder usarlo como una librería.

# ¿Cómo hariamos si quisieramos que la función Raiz solo calculase las raíces cuadradas por ejemplo?

Primero, tendriamos que cambiar nuestro código de opción ya que tendriamos que hacer que esta función fuese dependiente de la opción que escogiesemos. De forma que en el caso de que alguien escogiera realizar la operación Raiz, solo se pidiese un solo dato. El radicando. Después cambiariamos el código dentro de getRaiz para que la operación que realizase fuera raíz cuadrada de forma que quedase de tal forma:

Math.sqrt(dato1);

