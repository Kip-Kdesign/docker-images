FROM composer:1.7.2

# See: https://github.com/jbergknoff/Dockerfile/tree/bad54f3a3dff00a2ecc7c28360c3a8f9359b95be/sass

RUN apk --update add build-base && \
    git clone https://github.com/sass/sassc && \
    cd sassc && \
    git clone https://github.com/sass/libsass && \
    SASS_LIBSASS_PATH=$(pwd)/libsass make && \
    mv bin/sassc /usr/bin/sass && \
    cd .. && \
    rm -rf sassc && \
    apk del build-base && \
    apk add libstdc++ && \
    rm -rf /var/cache/apk/*
