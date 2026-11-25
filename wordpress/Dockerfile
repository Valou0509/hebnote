FROM php:8.2-apache
RUN apt-get update \
&& apt-get install -y --no-install-recommends curl \
&& rm -rf /var/lib/apt/lists/* \
&& docker-php-ext-install myssqli pdo pdo_mysql
WORKDIR /var/www/html
RUN curl -fsSL https://wordpress.org/latest.tar.gz -o wordpress.tar.gz \
&& tar -xzf wordpress.tar.gz --strip-components=1 -C /var/html \
&& rm wordpress.tar.gz \
&& chown -R www-data:www-data /var/www/html
EXPOSE 80
