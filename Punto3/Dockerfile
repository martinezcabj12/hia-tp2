# Imagen Base
FROM debian:13

# Actualizar e instalar dependencias
RUN apt-get update && apt-get install -y apache2 && apt-get install -y vim && apt-get clean

# Copiamos el sitio web al directorio de Apache
COPY index.html /var/www/html/

# Exponer el puerto 60
EXPOSE 60

# Apache necesita correr en foreground para que el contenedor no se detenga
CMD ["apachectl", "-D", "FOREGROUND"]
