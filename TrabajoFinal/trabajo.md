Realizado por:
Isidro Mansilla Pérez
y
Francisco Manuel Gómez Sánchez

#ATAQUE A SERVIDORES WEB

##Ataque DOS Y DDOS

**Ataque DOS**


Se denominan ataques de denegación de servicio (Denegation Of Service), es un ataque a un sistema ordenadores que causa que sus usuarios no puedan hacer uso del servicio. Normalmente provoca la pérdida de la conectividad por el consumo del ancho de banda de la red de la víctima o sobrecarga de los recursos computacionales del sistema de la víctima.

Es un ataque para que no hace falta tener grandes conocimientos de informática para realizarlo y tampoco sería muy arriesgado realizar al ataque contra un servidor ya que se pueden utilizar otros equipos intermedios para luego poder borrar los datos


Hay 3 tipos  de denegación de servicio:

- Consumo de recursos: el atacante intenta consumir los recursos del servidor hasta agotarlos
	
- Destrucción o alteración de la configuración: Se intenta modificar la información de la 	  máquina, este tipo de ataques necesitan de una técnica más sofisticada.
	
- Destrucción o alteración física de los equipos: este es muy simple, consiste en destruir 		   físicamente el servidor o alguno de sus componentes.


Nosotros nos centraremos en explicar la primera


Los sistemas DOS más utilizados son:

- Mail Bombing: envío masivo de mensajes a una máquina hasta saturar el servicio.

- Smurfing: consiste en transmitir a la red una trama ICMP correspondiente a la petición de un ping. Esta trama lleva como direccion de origen la dirección IP de la victima y como dirección de destino la direccion broadcast de la red atacada. De esta forma todos los equipos de la red contestan a la victima de tal modo que puede llegar a saturar su ancho de banda.

- SYN Flood: El sistema atacante utiliza un IP inexistente y envia multitud de tramas SYN (Se usa para sincronizar los números de secuencia en tres tipos de segmentos: petición de conexión, confirmación de conexión (con ACK activo) y la recepción de la confirmación (con ACK activo)) de sincronización a la victima. Como la victima no puede contestar a peticionario porque se está utilizando una IP inexistente las peticiones llenan la cola de tal manera que las solicitudes reales no puedan ser atendidas


**Ataques DDOS**

Ataque de denegación de servicio (DOS) donde existen múltiples focos distribuidos y sincronizados que focalizan su ataque en un mismo destino. Es decir, en definitiva  es un ataque DOS con la capacidad de acceso  de varios atacantes desde cualquier parte del mundo.


Existen varios tipo de ataques DDOS:

- Denegación de servicio

- Saturación de la red: Debido a que los paquetes de estos ataques comparten las mismas rutas que el resto de comunicaciones


Al ser muchos atacantes conectados mejora mucho el ancho de banda de este, con lo cual tiene mas probabilidad de éxito. Normalmente no son muchos atacantes coordinados ya que:

- Es arriesgado para el atacante usar su equipo

- Es difícil coordinar a muchos atacantes


El método utilizado es:

- Se buscan sistemas vulnerables

- Se realiza un ataque sobre estos y se les instala un programa y están conectados con el atacantes

- El programa busca un segundo nivel de sistemas, que finalmente serán estos los que realice el ataque

- Los atacantes dan la orden para que todos los equipos ataque a la victima


**Ataque de Fuerza Bruta**


Este tipo de ataque se utiliza para recuperar claves probando las combinaciones posibles hasta encontrar la correcta.

Es un método muy costoso ya que son métodos de prueba y error. El tiempo para encontrar la clave es proporcional a la complejidad que tenga la contraseña.

También existen los ataques de diccionario, ya que como muchos usuarios eligen contraseñas con significado, los atacantes por fuerza bruta probarían usando cualquier combinación posible, mientras que los atacantes con diccionario prueban con palabras conocidas.

Además hay un tercer tipo de ataque que utiliza características de los dos anteriores y es conocido como ataque híbrido, y se centran en ataque a contraseñas compuestas por una palabra tradicional seguida de letras y números, por ejemplo:

“megustaelpan123”


**Cross  Site Scripting (XSS)**


En XSS se manipula la entrada de parámetros de una aplicación con el objetivo de obtener una salida determinada que no sea la habitual al funcionamiento del sistema.

Algunas estadísticas afirman que el 90% de todos los sitios web tienen al menos una vulnerabilidad, y el 70% de todas las vulnerabilidades son XSS.

Se puede dividir en dos grandes grupos: XSS persistente o directo, y XSS reflejado o indirecto.

Inyección en un formulario:


Se trata del ataque mas sencillo. Consiste en inyectar código en un formulario que después al enviarlo al servidor, sera incluido en el código fuente de alguna página. Una vez insertado en el código fuente, cada vez que se cargue la página se ejecutara el código insertado en ella.

Inyección por medio de elementos

En este tipo de sistema de inyección de código se utiliza cualquier elemento que viaje entre el navegador y la aplicación, como pueden ser los atributos usados en las etiquetas HTML utilizadas en el diseño

Inyección por medio de recursos

Aparte de los elementos en la url y los formularios, hay otras formas en la que se puede actuar como son las cabeceras HTTP. Estas cabeceras son mensajes con los que se comunican el navegador y el servidor.

**Inyección SQL**

Es un método de infiltración de código que se vale de una vulnerabilidad informática presente en una aplicación a la hora de validar las entradas para realizar operaciones sobre una base de datos.

La inyección directa de comandos SQL es una técnica donde un atacante crea o altera comandos SQL existentes para exponer datos ocultos, sobrescribirlos, o peor aún, ejecutar comandos peligrosos a nivel de sistema en el equipo que hospeda la base de datos. Esto se logra a través de la práctica, tomando la entrada del usuario y combinándola con parámetros estáticos para elaborar una consulta SQL.

La vulnerabilidad se puede producir automáticamente cuando un programa "crea descuidadamente" una sentencia en tiempo de ejecución, o bien durante la fase de desarrollo. En cualquier caso, siempre que el programador necesite y haga uso de parámetros a ingresar por parte del usuario, a efectos de consultar una base de datos; ya que, justamente, dentro de los parámetros es donde se puede incorporar el código SQL intruso.

Al ejecutarse la consulta en la base de datos, el código SQL inyectado también se ejecutará y podría hacer un sinnúmero de cosas, como insertar registros, modificar o eliminar datos, autorizar accesos e, incluso, ejecutar otro tipo de código malicioso en el computador.

Uno de los ataques que utiliza inyección SQL es el llamado “Ataque a ciegas por Inyección SQL (Blind SQL injection)”, se produce por una falla de seguridad, cuando no se muestran mensajes de error al no producirse resultados correctos ante una consulta a la base de datos, mostrándose siempre el mismo contenido (es decir, solo hay respuesta si el resultado es correcto).

El problema para la seguridad de la página radica en que esta técnica es utilizada en combinación con diccionarios o fuerza bruta para la búsqueda, carácter por carácter, de una contraseña, un nombre de usuario, un número de teléfono o cualquier otra información que albergue la base de datos atacada; para ello se utiliza código SQL específico que "va probando" cada carácter consiguiendo un resultado positivo acumulable cuando hay una coincidencia.

**Demostración ataque por inyección SQL**

Vamos a realizar este ataque desde una maquina virtual Kali Linux, usando la herramienta sqlmap, que nos ahorrará la tediosa tarea
de prueba-error.

Para comenzar esta tarea debemos encontrar una página web que sea vulnerable, para hacer esta busqueda más sencilla utilizaremos 
google dorks, operadores avanzados de búsqueda, que se incluyen dentro del texto que quieres buscar y permiten delimitar los resultados 
de tu búsqueda a algo más concreto y así ahorrarte tiempo.

Nosotros hemos usado este, pero posiblemente nos arrojé gran cantidad de páginas que ya no presentan la vulnerabilidad, por ello,
debemos probar más dorks.

**inurl: noticia.php?id=**

Esta es la página que nosotros hemos elegido:

![imagen](https://github.com/FranGS/swap1516/blob/master/TrabajoFinal/Imagenes/busquedaPagina.png)

![imagen](https://github.com/FranGS/swap1516/blob/master/TrabajoFinal/Imagenes/Pagina.png)

Ahora usando **sqlmap** sacamos las bases de datos que contenga:

![imagen](https://github.com/FranGS/swap1516/blob/master/TrabajoFinal/Imagenes/ataque1.png)

![imagen](https://github.com/FranGS/swap1516/blob/master/TrabajoFinal/Imagenes/ataque2.png)

Seguido esto sacamos las tablas de la base de dato elegida:

![imagen](https://github.com/FranGS/swap1516/blob/master/TrabajoFinal/Imagenes/ataque3.png)

![imagen](https://github.com/FranGS/swap1516/blob/master/TrabajoFinal/Imagenes/ataque4.png)

Elegimos la tabla y sacamos sus columnas:

![imagen](https://github.com/FranGS/swap1516/blob/master/TrabajoFinal/Imagenes/ataque5.png)

![imagen](https://github.com/FranGS/swap1516/blob/master/TrabajoFinal/Imagenes/ataque6.png)

Terminado todo este proceso sólo nos quedaría el paso de sacar la información de la columna elegida mediante el comando:

**sqlmap -u http://www.alovera.es/noticias.php?id=306 -D [nombreBD] -T [nombreTabla] -C [nombreColumna] --dump --threads [nHebras]**

El problema de sacar esto último es que este campo suele ser el que contiene la información sensible como nombres, mails y contraseñas.
Así que hemos evitado dar este último paso y de esta manera concluiría nuestro ataque por inyección SQL.
