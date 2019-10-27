FROM nginx:1.16.0-alpine
COPY ./default.conf /etc/nginx/conf.d/default.conf && COPY ./app/homework.html /app/homework.html
RUN touch /var/run/nginx.pid && chown -R 1001 /app /var/cache/nginx /var/run/nginx.pid
EXPOSE 8080
USER 1001