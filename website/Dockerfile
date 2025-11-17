FROM php:8.2-alpine

# Copier ton code
COPY index.php /var/www/html

# Exposer le port 80
EXPOSE 80

#Ajouter variable environnement
ENV USERNAME=toto
ENV PASSWORD=python

# Lancer le built-in server de PHP
CMD ["php", "-S", "0.0.0.0:80", "-t", "/var/www/html"]
