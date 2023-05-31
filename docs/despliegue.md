# Instalación/Despliegue

1.  Necesitarás crear dos archivos Dockerfile, uno para el backend y otro para el frontend. El Dockerfile especifica cómo se construirá cada imagen de contenedor estos ya estan en la raiz de cada proyecto dentro de github.

2. Configura el archivo docker-compose.yml: Este archivo es el núcleo de Docker Compose y define los servicios, volúmenes, redes y otras configuraciones necesarias para tu proyecto. Aquí es donde especificas qué imágenes de contenedor utilizar y cómo se deben configurar (Esto esta en desarrollo, se podria distribuir junto a los proyectos para su despliegue con docker facilmente..

3. Construye las imágenes de contenedor: Ejecuta el comando docker-compose build para construir las imágenes de contenedor basadas en los Dockerfiles y las configuraciones definidas en el archivo docker-compose.yml.

4. Inicia los contenedores: Ejecuta el comando docker-compose up para iniciar los contenedores según la configuración definida en el archivo docker-compose.yml. Esto creará y ejecutará los contenedores para el backend y el frontend, junto con cualquier otra configuración que hayas definido.

5. Accede a la aplicación: Una vez que los contenedores estén en ejecución, podrás acceder a tu aplicación web a través de la dirección IP y el puerto definidos en el archivo docker-compose.yml. Por ejemplo, si has configurado el frontend para ejecutarse en el puerto 80, podrías acceder a la aplicación en http://localhost:80.

Puertos obligatorios
1. El puerto del back tiene que ser 8083 ya que es el que esta configurado en mi archivo de configuracion de spring.
2. El puerto del front ha de ser 8080 ya que es el que esta configurado en el cors de mi back. (cors: es el crossOrigins basicamente los puertos desde los que mi back acepta conexion.).
