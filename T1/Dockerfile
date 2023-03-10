FROM debian
RUN apt update -y && apt upgrade -y && apt install -y apache2 libapache2-mod-php php php-mysql mariadb-client -y && apt clean && rm -rf /var/lib/apt/lists/*
ADD bookmedik /var/www/html/
ADD script.sh /opt/
RUN chmod +x /opt/script.sh && rm /var/www/html/index.html
ENTRYPOINT ["/opt/script.sh"]
