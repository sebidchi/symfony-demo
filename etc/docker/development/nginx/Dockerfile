FROM nginx:latest

RUN rm -rf /var/cache/apk/*

COPY sf3.conf /etc/nginx/conf.d/default.conf

RUN mkdir -p /app/var/logs/nginx \
    && touch /app/var/logs/nginx/access.log && ln -sf /dev/stdout /app/var/logs/nginx/access.log \
    && touch /app/var/logs/nginx/error.log  && ln -sf /dev/stdout /app/var/logs/nginx/error.log