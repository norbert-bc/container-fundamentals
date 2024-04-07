FROM alpine:latest

LABEL org.opencontainers.image.authors="norbert.bereczki@icloud.com"
LABEL org.opencontainers.image.source=https://github.com/norbert-bc/container-fundamentals
LABEL org.opencontainers.image.description="Fork Containter Fundamentals - Static Website Image"
LABEL org.opencontainers.image.licenses=APACHE2
LABEL server_type="edge_server"

RUN apk update
RUN apk add --no-cache nginx
COPY config/nginx.conf /etc/nginx/
COPY web_content/ /var/www
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
