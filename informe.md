# Red de contenedores mysql y phomyadmin
## 1. Titulo
Implementación de un servidor de bases de datos MySQL y su administración mediante phpMyAdmin usando Docker
## 2. Tiempo de duración
40 Minutos
## 3. Fundamentos:
Docker es una plataforma que permite ejecutar aplicaciones dentro de contenedores, los cuales son entornos ligeros e independientes que incluyen todo lo necesario para que una aplicación funcione correctamente. A diferencia de las máquinas virtuales, los contenedores no requieren un sistema operativo completo, lo que los hace más rápidos y eficientes.

En esta práctica se implementan dos contenedores: MySQL y phpMyAdmin.
MySQL es un sistema gestor de bases de datos relacional de código abierto muy utilizado en entornos web. phpMyAdmin es una herramienta escrita en PHP que permite gestionar bases de datos MySQL desde una interfaz gráfica accesible a través del navegador.

Para que ambos contenedores se comuniquen, se crea una red personalizada en Docker. Gracias a esta red, phpMyAdmin puede acceder al servidor MySQL mediante el nombre del contenedor, sin necesidad de conocer su dirección IP.

Docker permite definir variables de entorno para configurar las credenciales de acceso, el nombre de la base de datos y otros parámetros. Además, mediante el uso de volúmenes, los datos almacenados en MySQL persisten incluso después de detener o eliminar el contenedor.

Esta arquitectura basada en contenedores facilita el despliegue de entornos de desarrollo reproducibles y portátiles. Por ejemplo, un equipo puede compartir un archivo docker-compose.yml que describe la configuración completa, y cualquier otro usuario podrá ejecutar la misma infraestructura con un solo comando (docker compose up -d).


## 4. Conocimientos previos.
   
Para realizar esta práctica se necesita tener claro los siguientes temas:

Comandos básicos de Linux (navegación de directorios, creación de carpetas, ejecución de comandos).

Manejo básico del navegador web.

Conceptos fundamentales de Docker: imágenes, contenedores, redes y volúmenes.

Conocimientos introductorios sobre bases de datos relacionales.

## 5. Objetivos a alcanzar

  Implementar contenedores con MySQL y phpMyAdmin.

Configurar una red personalizada en Docker para la comunicación entre contenedores.

Manipular archivos de configuración y variables de entorno.

Crear y gestionar una base de datos mediante la interfaz de phpMyAdmin.
  
## 6. Equipo necesario:
  
Computadora con Windows

Cuenta en Docker Hub 

Docker Desktop o Docker Engine versión 20.x o superior.

Conexión a Internet.

Editor de texto

## 7. Material de apoyo.
   
Documentación oficial de Docker

Guía de phpMyAdmin

Docker Cheat Sheet (PDF oficial)
  
## 8. Procedimiento


Paso 1. Crear una red personalizada
![alt text](<1. Crear una red personalizada.png>)
Paso 2. Crear el contenedor de MySQL
![alt text](<2.Crear el contenedor de MySQL.png>)
Paso 3. Crear el contenedor en phpMyAdmin.
![alt text](<3. Crear el contenedor de phpMyAdmin.png>)
Paso 4. Verificar el funcionamiento

Abrir en el navegador:
👉 http://localhost:8080

Iniciar sesión con:

Servidor: mysql-container

Usuario: root

Contraseña: root123
![alt text](<Captura de pantalla 2025-11-01 092731.png>)
Paso 5. Crear una base de datos de prueba
En phpMyAdmin → “Nueva” → Nombre: test_db → “Crear”.
![alt text](<Captura de pantalla 2025-11-01 093555.png>)
Paso 6. Resutaldo de los dos contenedores
![alt text](<Captura de pantalla 2025-11-01 093743.png>)

## 9. Resultados esperados:
    
Al finalizar la práctica, el estudiante habrá implementado correctamente dos contenedores comunicados entre sí a través de una red de Docker. Desde la interfaz de phpMyAdmin se podrá:

Visualizar la base de datos prueba_db creada automáticamente.

Crear nuevas bases de datos, tablas y registros.

Comprobar el funcionamiento del entorno de administración.

## 10. Bibliografía
    
Docker Inc. (2024). Docker Documentation. Recuperado de https://docs.docker.com/

phpMyAdmin Developers. (2024). phpMyAdmin Official Documentation. https://docs.phpmyadmin.net/

MySQL. (2024). MySQL Reference Manual. Oracle Corporation.

Vega, J. (2023). Introducción a la virtualización y contenedores. Editorial Universitaria.