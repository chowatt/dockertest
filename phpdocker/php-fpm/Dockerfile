FROM alpine
WORKDIR "/application"

# Fix debconf warnings upon build
ARG DEBIAN_FRONTEND=noninteractive

# Install selected extensions and other stuff
RUN apt-get update \
    && apt-get -y --no-install-recommends install  php-memcached php7.2 php7.2-mysql php7.2-gd php7.2-gmp php7.2-imap php7.2-ldap php7.2-soap \
    && apt-get install -y nginx \
    && apt-get clean; rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* /usr/share/doc/*
    