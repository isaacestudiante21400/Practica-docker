# Práctica Docker

## Ejercicio 1

### 1.1 No uso Alpine pero dejo unas capturas de como he bajado la imagen
![Ej 2.1](capturasdespliegue/ejercicio1/1.png)

![Ej 2.1](capturasdespliegue/ejercicio1/2.png)

---

## Ejercicio 2

### 2.1 Buscar por terminal la imagen hello-world
![Ej 2.1](capturasdespliegue/ejercicio2/1.png)

### 2.2 Buscar en DockerHub con la casilla "Docker Official Image" y comprobar que coincide
![Ej 2.1](capturasdespliegue/ejercicio2/2.png)

### 2.3 Descargar y ejecutar la imagen elegida
![Ej 2.1](capturasdespliegue/ejercicio2/3.png)

### 2.4 Descargar y ejecutar la imagen hello-seattle
![Ej 2.1](capturasdespliegue/ejercicio2/4.png)

### 2.5 Intentar borrar la imagen hello-seattle ¿Por qué da error?
![Ej 2.1](capturasdespliegue/ejercicio2/5.png)
Da error porque está activa, habría que forzar el borrado

### 2.6 Listar los contenedores con `ls -a` ¿Para qué sirve la opción -a?
![Ej 2.1](capturasdespliegue/ejercicio2/6.png)

### 2.7 Eliminar el contenedor que usa hello-seattle y la imagen
No tengo la captura pero se elimina mediante "docker container rm -f nombre_contenedor", el -f es la clave

---

## Ejercicio 3

### 3.1 Crear la imagen smr/hola-mundo con `docker image tag`
![Ej 2.1](capturasdespliegue/ejercicio3/1.png)

### 3.2 Borrar la imagen original (hello-world)
![Ej 2.1](capturasdespliegue/ejercicio3/2.png)

### 3.3 Guardar la nueva imagen en el fichero smr-hola-mundo.tar
![Ej 2.1](capturasdespliegue/ejercicio3/3.png)

### 3.4 Borrar la imagen smr/hola-mundo y comprobar que no hay imágenes
![Ej 2.1](capturasdespliegue/ejercicio3/4.png)

### 3.5 Añadir la imagen con `docker image load` usando el .tar
![Ej 2.1](capturasdespliegue/ejercicio3/5.png)

---

## Ejercicio 4

### 4.1 Descargar la imagen oficial de mysql
### 4.2 Crear el contenedor mysql_smr con password de root "smr"
### 4.3 Ejecutar `docker container exec -it mysql_smr mysql -u root -p`
### 4.4 Comprobar que se puede conectar al MySQL del contenedor
![Ej 2.1](capturasdespliegue/ejercicio4/1.png)

### 4.5 Crear la base de datos con `CREATE DATABASE prueba;`
### 4.6 Comprobar que se ha creado con `show databases;`
![Ej 2.1](capturasdespliegue/ejercicio4/2.png)

---

## Ejercicio 5

### 5.1 Parar el contenedor mysql_smr y volver a iniciarlo
### 5.2 Conectarse de nuevo a MySQL y comprobar que la bbdd prueba sigue estando
![Ej 2.1](capturasdespliegue/ejercicio5/1.png)
![Ej 2.1](capturasdespliegue/ejercicio5/2.png)

### 5.3 Eliminar el contenedor mysql_smr
### 5.4 Volver a crearlo con los mismos parámetros y comprobar que la bbdd prueba no existe
![Ej 2.1](capturasdespliegue/ejercicio5/3.png)
![Ej 2.1](capturasdespliegue/ejercicio5/4.png)

---

## Ejercicio 6

### 6.1 Crear el directorio mysql_data
### 6.2 Crear el contenedor mysql con /var/lib/mysql guardado en mysql_data
![Ej 2.1](capturasdespliegue/ejercicio6/1.png)

### 6.3 Crear de nuevo la bbdd dentro del MySQL del contenedor
![Ej 2.1](capturasdespliegue/ejercicio6/2.png)

### 6.4 Salir y eliminar el contenedor
### 6.5 Crear el contenedor sin volúmenes y comprobar que la bbdd no existe
![Ej 2.1](capturasdespliegue/ejercicio6/3.png)
![Ej 2.1](capturasdespliegue/ejercicio6/4.png)

### 6.6 Salir y eliminar el contenedor
### 6.7 Crear el contenedor mapeando la carpeta a mysql_data
![Ej 2.1](capturasdespliegue/ejercicio6/5.png)

### 6.8 Comprobar que la bbdd sigue estando en MySQL
![Ej 2.1](capturasdespliegue/ejercicio6/6.png)

---

## Ejercicio 7

### 7.1 Crear el directorio php_data
### 7.2 Crear el archivo index.php con `phpinfo();`
### 7.3 Arrancar el contenedor php_smr (php:8.0-apache) con volumen y puerto 8085
![Ej 2.1](ejercicio7/1.png)

### 7.4 Acceder desde el navegador a http://ip_maquina_virtual:8085
![Ej 2.1](ejercicio7/2.png)

### 7.5 Reiniciar la máquina virtual
### 7.6 Comprobar que la URL da error
![Ej 2.1](ejercicio7/3.png)

### 7.7 Borrar el contenedor
### 7.8 Crear de nuevo el contenedor con reinicio automático (siempre)
![Ej 2.1](ejercicio7/4.png)

### 7.9 Reiniciar la máquina virtual
### 7.10 Comprobar que la URL ahora sí funciona
![Ej 2.1](ejercicio7/5.png)
