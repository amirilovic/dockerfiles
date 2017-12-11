FROM amirilovic/php-fpm

# Install xdebug
RUN pecl install xdebug && docker-php-ext-enable xdebug
RUN echo "xdebug.remote_enable=1\n\
xdebug.remote_handler=dbgp\n\
xdebug.remote_port=9000\n\
xdebug.remote_autostart=1\n\
xdebug.remote_connect_back=0\n\
xdebug.idekey=docker\n\
xdebug.remote_host=10.254.254.254\n\
xdebug.remote_log=/tmp/xdebug.log" >> /usr/local/etc/php/conf.d/docker-php-ext-xdebug.ini
