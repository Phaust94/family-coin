FROM ghcr.io/blockscout/frontend:v2.3.5

USER root

RUN apk add --no-cache nginx

COPY nginx.conf /etc/nginx/http.d/default.conf

EXPOSE 80

USER node

CMD sh -c "npm start & nginx -g 'daemon off;'"
