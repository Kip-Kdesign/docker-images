FROM node:10.12.0-alpine

ENV NODE_PATH /usr/local/lib/node_modules

RUN \
    apk --no-cache --update add php php-openssl php-json php-mbstring php-phar bash \
    && php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');" \
    && php composer-setup.php --install-dir=/bin --filename=composer \
    && rm composer-setup.php \
    \
    && echo "npm..." \
    && npm install -g babel-cli babel-preset-env sass rollup \
