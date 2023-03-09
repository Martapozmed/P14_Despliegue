FROM php:7.4-apache-bullseye
MAINTAINER Marta Pozo Medina "mpozmed410@g.educaand.es"
RUN apt update -y && apt upgrade -y && docker-php-ext-install mysqli pdo pdo_mysql && apt install mariadb-client -y && apt clean && rm -rf /var/lib/apt/lists/*
ADD bookmedik /var/www/html/
ADD script.sh /opt/
RUN chmod +x /opt/script.sh
ENTRYPOINT ["/opt/script.sh"]
