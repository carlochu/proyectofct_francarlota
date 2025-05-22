FROM php:8.2-apache

# Instala la extensión mysqli
RUN docker-php-ext-install mysqli

# Habilita la extensión mysqli (normalmente no es necesario si install funciona correctamente)
# RUN docker-php-ext-enable mysqli

# Habilita mod_rewrite
RUN a2enmod rewrite

# Copia los archivos de la página web al directorio de Apache
COPY . /var/www/proyect_fc/html

# Asegúrate de que los permisos sean correctos
RUN chown -R www-data:www-data /var/www/proyect_fc/html
RUN chmod -R 755 /var/www/proyect_fc/html

# Exponer el puerto 80
EXPOSE 80