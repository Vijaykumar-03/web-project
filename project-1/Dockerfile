FROM nginx:alpine

# Remove default nginx config
RUN rm /etc/nginx/conf.d/default.conf

# Create web root
RUN mkdir -p /var/www/html

# Copy custom nginx config
COPY nginx.conf /etc/nginx/conf.d/default.conf

# Copy your website files
COPY index.html /var/www/html/
COPY style.css /var/www/html/

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]
