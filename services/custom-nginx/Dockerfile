FROM nginx:1.23.1
COPY ./nginx.conf.template /nginx.conf.template

# Replace the start-up command with one that templates in all environment variables to
# /nginx.conf.template and uses the result to overwrite the nginx.conf for this container
CMD ["/bin/sh" , "-c" , "envsubst < /nginx.conf.template > /etc/nginx/nginx.conf && exec nginx -g 'daemon off;'"]
