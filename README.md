# Práctica Docker

## Ejercicio 1

### 1.1 Crear una máquina virtual con Alpine llamada "Alpine base"
![Ej 1.1](img/ej1-1.png)

### 1.2 Instalar Docker en la máquina virtual
![Ej 1.2](img/ej1-2.png)

### 1.3 Comprobar que todo se ha instalado correctamente
![Ej 1.3](img/ej1-3.png)

---

## Ejercicio 2

### 2.1 Buscar por terminal la imagen hello-world
![Ej 2.1](img/ej2-1.png)

### 2.2 ¿Cuál de todas las imágenes es la oficial?
![Ej 2.2](img/ej2-2.png)

### 2.3 Buscar en DockerHub con la casilla "Docker Official Image" y comprobar que coincide
![Ej 2.3](img/ej2-3.png)

### 2.4 Descargar y ejecutar la imagen elegida
![Ej 2.4](img/ej2-4.png)

### 2.5 Descargar y ejecutar la imagen hello-seattle
![Ej 2.5](img/ej2-5.png)

### 2.6 Mostrar las imágenes descargadas
![Ej 2.6](img/ej2-6.png)

### 2.7 Intentar borrar la imagen hello-seattle ¿Por qué da error?
![Ej 2.7](img/ej2-7.png)

### 2.8 Listar los contenedores con `ls` sin parámetros
![Ej 2.8](img/ej2-8.png)

### 2.9 Listar los contenedores con `ls -a` ¿Para qué sirve la opción -a?
![Ej 2.9](img/ej2-9.png)

### 2.10 Eliminar el contenedor que usa hello-seattle y la imagen
![Ej 2.10](img/ej2-10.png)

### 2.11 Listar las imágenes y comprobar que se ha borrado
![Ej 2.11](img/ej2-11.png)

---

## Ejercicio 3

### 3.1 Crear la imagen smr/hola-mundo con `docker image tag`
![Ej 3.1](img/ej3-1.png)

### 3.2 Borrar la imagen original (hello-world)
![Ej 3.2](img/ej3-2.png)

### 3.3 Guardar la nueva imagen en el fichero smr-hola-mundo.tar
![Ej 3.3](img/ej3-3.png)

### 3.4 Borrar la imagen smr/hola-mundo y comprobar que no hay imágenes
![Ej 3.4](img/ej3-4.png)

### 3.5 Añadir la imagen con `docker image load` usando el .tar
![Ej 3.5](img/ej3-5.png)

---

## Ejercicio 4

### 4.1 Descargar la imagen oficial de mysql
![Ej 4.1](img/ej4-1.png)

### 4.2 Crear el contenedor mysql_smr con password de root "smr"
![Ej 4.2](img/ej4-2.png)

### 4.3 Ejecutar `docker container exec -it mysql_smr mysql -u root -p`
![Ej 4.3](img/ej4-3.png)

### 4.4 Comprobar que se puede conectar al MySQL del contenedor
![Ej 4.4](img/ej4-4.png)

### 4.5 Crear la base de datos con `CREATE DATABASE prueba;`
![Ej 4.5](img/ej4-5.png)

### 4.6 Comprobar que se ha creado con `show databases;`
![Ej 4.6](img/ej4-6.png)

---

## Ejercicio 5

### 5.1 Parar el contenedor mysql_smr y volver a iniciarlo
![Ej 5.1](img/ej5-1.png)

### 5.2 Conectarse de nuevo a MySQL y comprobar que la bbdd prueba sigue estando
![Ej 5.2](img/ej5-2.png)

### 5.3 Eliminar el contenedor mysql_smr
![Ej 5.3](img/ej5-3.png)

### 5.4 Volver a crearlo con los mismos parámetros y comprobar que la bbdd prueba no existe
![Ej 5.4](img/ej5-4.png)

### 5.5 Salir del contenedor y eliminarlo
![Ej 5.5](img/ej5-5.png)

---

## Ejercicio 6

### 6.1 Crear el directorio mysql_data
![Ej 6.1](img/ej6-1.png)

### 6.2 Crear el contenedor mysql con /var/lib/mysql guardado en mysql_data
![Ej 6.2](img/ej6-2.png)

### 6.3 Crear de nuevo la bbdd dentro del MySQL del contenedor
![Ej 6.3](img/ej6-3.png)

### 6.4 Salir y eliminar el contenedor
![Ej 6.4](img/ej6-4.png)

### 6.5 Crear el contenedor sin volúmenes y comprobar que la bbdd no existe
![Ej 6.5](img/ej6-5.png)

### 6.6 Salir y eliminar el contenedor
![Ej 6.6](img/ej6-6.png)

### 6.7 Crear el contenedor mapeando la carpeta a mysql_data
![Ej 6.7](img/ej6-7.png)

### 6.8 Comprobar que la bbdd sigue estando en MySQL
![Ej 6.8](img/ej6-8.png)

---

## Ejercicio 7

### 7.1 Crear el directorio php_data
![Ej 7.1](img/ej7-1.png)

### 7.2 Crear el archivo index.php con `phpinfo();`
![Ej 7.2](img/ej7-2.png)

### 7.3 Arrancar el contenedor php_smr (php:8.0-apache) con volumen y puerto 8085
![Ej 7.3](img/ej7-3.png)

### 7.4 Acceder desde el navegador a http://ip_maquina_virtual:8085
![Ej 7.4](img/ej7-4.png)

### 7.5 Reiniciar la máquina virtual
![Ej 7.5](img/ej7-5.png)

### 7.6 Comprobar que la URL da error
![Ej 7.6](img/ej7-6.png)

### 7.7 Borrar el contenedor
![Ej 7.7](img/ej7-7.png)

### 7.8 Crear de nuevo el contenedor con reinicio automático (siempre)
![Ej 7.8](img/ej7-8.png)

### 7.9 Reiniciar la máquina virtual
![Ej 7.9](img/ej7-9.png)

### 7.10 Comprobar que la URL ahora sí funciona
![Ej 7.10](img/ej7-10.png)
