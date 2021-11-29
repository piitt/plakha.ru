FROM php:7.4-fpm-alpine
MAINTAINER Alexandr Plakhotnikov mxplaha@gmail.com

WORKDIR /app_plakha.ru/html

RUN deluser www-data && \
    if getent group www-data; then delgroup www-data;fi && \
    addgroup -g 1000 www-data && \
    adduser -u 1000 -S -G www-data -s /sbin/nologin www-data && \
    install -d -m 0755 -o www-data -g www-data /app_plakha.ru/html && \
    chown -c -f -h -R 1000:1000 /app_plakha.ru/html


