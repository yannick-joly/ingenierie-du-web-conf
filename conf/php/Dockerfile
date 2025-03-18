FROM debian:latest

# Met à jour les paquets et installe Apache + PHP
RUN apt update && apt install -y \
    apache2 \
    php libapache2-mod-php \
    && apt clean \
    && rm -rf /var/lib/apt/lists/*

# Expose le port HTTP
EXPOSE 80

# Lance Apache en mode foreground
CMD ["apachectl", "-D", "FOREGROUND"]
