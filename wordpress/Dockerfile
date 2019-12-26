FROM wordpress:php7.2-fpm

RUN apt-get update && apt-get install -y zlib1g-dev tidy csstidy vim libmemcached-dev libzip-dev

RUN docker-php-ext-install zip

RUN curl -L -o /tmp/memcached.tar.gz "https://github.com/php-memcached-dev/php-memcached/archive/php7.tar.gz" && \
	mkdir -p memcached && \
	tar -C memcached -zxvf /tmp/memcached.tar.gz --strip 1 && \
	( \
	    cd memcached && \
	    phpize && \
	    ./configure && \
	    make -j$(nproc) && \
	    make install \
	) && \
	rm -r memcached && \
	rm /tmp/memcached.tar.gz && \
	docker-php-ext-enable memcached
