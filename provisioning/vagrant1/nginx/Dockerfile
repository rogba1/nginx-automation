FROM alpine:3.4
RUN apk add --update nginx && rm -rf /var/cache/apk/*
RUN mkdir -p /tmp/nginx/client-body

ADD nginx.conf /etc/nginx/nginx.conf

RUN mkdir -p /var/www/site
ADD index.html /var/www/site/index.html

EXPOSE 80

#COPY nginx.conf /etc/nginx/nginx.conf
#COPY default.conf /etc/nginx/conf.d/default.conf
#COPY index.html /usr/share/nginx/html

CMD ["nginx", "-g", "daemon off;"]
