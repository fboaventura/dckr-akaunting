FROM nginx:alpine

RUN apk update && apk add --no-progress -q wget unzip

RUN wget -O /tmp/akaunting.zip https://akaunting.com/download.php?version=latest&utm_source=docker&utm_campaign=developers \
  && mkdir -p /var/www/akaunting \
  && unzip /tmp/akaunting.zip -d /var/www/akaunting \
  && rm /tmp/akaunting.zip

RUN find /var/www/akaunting/ -type d -exec chmod 755 {} \;
RUN find /var/www/akaunting/ -type f -exec chmod 644 {} \;
