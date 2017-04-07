FROM ihadgraft/php:7.0

RUN apk update \
  && apk add php7-fpm \
  && apk add php7-opcache \
  && rm -rf /var/cache/apk/*

RUN ln -s /usr/sbin/php-fpm7 /usr/sbin/php-fpm

ADD www.conf /etc/php7/php-fpm.d/www.conf

CMD ["php-fpm", "-F"]
