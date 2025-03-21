# Prácticas de Docker - Fundamentos de Computación en la Nube

Este repositorio contiene las prácticas realizadas en el curso de **Fundamentos de Computación en la Nube**, correspondientes a la asignatura de **DAM**. Las tareas incluyen la creación y gestión de contenedores Docker, con distintos servicios como servidores web y FTP.

## Descripción de las prácticas

### Parte 1: Primer contenedor y exploración básica

En esta parte, se crea un contenedor usando la imagen `hello-world` y se exploran los comandos básicos de Docker para crear, ejecutar y gestionar contenedores.

### Parte 2: Despliegue de un servidor web con Apache

En esta práctica, se configura un servidor web utilizando la imagen `httpd`, donde se configura un contenedor para que sirva una página web desde el puerto 3000 del host.

### Parte 3: Despliegue de un servidor FTP con vsftpd

Se crea un servidor FTP utilizando la imagen `fauria/vsftpd`, configurando el acceso mediante FTP para transferir archivos entre el host y el contenedor.

## Comandos utilizados

### Parte 1:
- `docker run -d --name hello-world-container hello-world`
- `docker ps` 
- `docker ps -a`
- `docker exec -it hello-world-container bash`

### Parte 2:
- `docker run -d --name ceeciimg-apachewebserver -p 3000:80 httpd`
- `docker exec -it ceeciimg-apachewebserver bash`

### Parte 3:
- `docker run -d --name ceeciimg-ftpserver -e FTP_USER=ceeciimg -e FTP_PASS=1234 -e PASV_ENABLE=YES -e PASV_MIN_PORT=30000 -e PASV_MAX_PORT=30005 -p 21:21 -p 30000-30005:30000-30005 fauria/vsftpd`

## Recursos

- [Docker Documentation](https://docs.docker.com/)
- [VSFTPD Documentation](https://security.appspot.com/vsftpd.html)
- [Apache HTTPD Documentation](https://httpd.apache.org/)

## Autor

**ceeciimg** (github.com/ceeciimg)
