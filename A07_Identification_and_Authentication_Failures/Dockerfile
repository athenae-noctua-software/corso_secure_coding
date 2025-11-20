FROM php:8.1-apache

# Abilita mod_rewrite per Apache
RUN a2enmod rewrite

# Installa estensioni PHP necessarie
RUN docker-php-ext-install mysqli pdo pdo_mysql

# Configura la directory di lavoro
WORKDIR /var/www/html

# I file dell'applicazione vengono montati via bind mount dal docker-compose
# Imposta i permessi corretti per la directory
RUN chown -R www-data:www-data /var/www/html && \
    chmod -R 755 /var/www/html

# Espone la porta 80
EXPOSE 80

