ARG WORDPRESS_VERSION

FROM wordpress:${WORDPRESS_VERSION}

##
## install redis & enable redis plugin
RUN pecl install redis && docker-php-ext-enable redis

WORKDIR /usr/src/wordpress

RUN set -eux; \
	find /etc/apache2 -name '*.conf' -type f -exec sed -ri -e "s!/var/www/html!$PWD!g" -e "s!Directory /var/www/!Directory $PWD!g" '{}' +; \
	cp -s wp-config-docker.php wp-config.php
