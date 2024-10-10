FROM ubuntu:latest

# install nginx & wget
RUN apt-get update && apt-get install -y nginx wget

# expose port 80
EXPOSE 80

# create repertory
WORKDIR /var/www/html

# Copy index.html to /var/www/html
COPY index.html /var/www/html

# Copy nginx.local.conf to /etc/nginx/nginx.conf
COPY nginx.local.conf /etc/nginx/nginx.conf

# run nginx with nginx -g daemon off
CMD ["nginx", "-g", "daemon off;"]