FROM ghcr.io/blockscout/frontend:v2.3.5

USER root

RUN apk add --no-cache nginx && \
    chown -R node:node /app

COPY --chown=node:node nginx.conf /etc/nginx/nginx.conf

RUN mkdir -p /var/lib/nginx/tmp /var/lib/nginx/logs /var/log/nginx && \
    chown -R node:node /var/lib/nginx /var/log/nginx

USER node

EXPOSE 80

CMD bash -c ". ./entrypoint.sh & nginx -g 'daemon off;'"
