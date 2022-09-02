# docker-compose-lemp-php74

# Generate Self signed Certificate

sudo openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout custom.key -out custom.crt


# Add new php8 extension


docker exec -it php74-fpm /bin/sh

php -m to review installed extension
