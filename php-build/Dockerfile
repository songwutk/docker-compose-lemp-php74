FROM phpdockerio/php74-fpm:latest
WORKDIR "/var/www/"

# Fix debconf warnings upon build
ARG DEBIAN_FRONTEND=noninteractive

# Install selected extensions and other stuff
RUN apt-get update \
    && apt-get -y --no-install-recommends install  php-memcached php7.4-mysql php7.4-pgsql php-redis php7.4-sqlite3 php7.4-gd php-imagick php7.4-intl php7.4-ldap php-mongodb php7.4-soap php-ssh2 php7.4-xsl php-yaml \
    && apt-get clean; rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* /usr/share/doc/*

RUN apt-get install -y \
    curl 

#RUN docker-php-ext-install pdo_mysql mbstring exif pcntl bcmath gd mysqld

# Install git
RUN apt-get update \
    && apt-get -y install git \
    && apt-get clean; rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* /usr/share/doc/*
