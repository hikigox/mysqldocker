# mysqldocker
Instancia de docker con Mysql


En el docker compose los parámetros son los siguientes
versión: versión del compose
services: que imagen vamos a meter en el contenedor
mysql: la imagen
build: lo que se va a ejecutar o crear
context: tomar todo lo de la carpeta raíz
dockerfile: nuestro archivo dockerfile
container_name: nombre del contenedor
restart: que hacer cuando se dañe el contenedor
ports: puertos que se abren para el servicio (en este caso el puerto 33306 es el puerto del computador, mientras que el 3306 es el que simula el docker internamente)
environment: Variables de entorno
MYSQL_ROOT_PASWORD: contraseña de mysql root
MYSQL_DATABASE: crear una base de datos
volumes: carpetas que se crean de acuerdo a una referencia segun la imagen que creamos
networks: a cual red se esta conectado
mysql_network: tag para identificar cual es la network
aliases: etiqueta que se puede usar para referirse a este contenedor (ping mysql_host)
volumes: otra instancia de volumen pero con el objeto schemas
networks: esta es la creación de una nueva red
mysql_network: etiqueta con la que se referencia a la red dentro del compuse document
name: nombre de la red 
driver: el tipo de conexión que se va a utilizar

Luego lo que hacemos es ejecutar el comando docker compose up , el cual ejecuta el archivo y crea el contenedor.
