FROM node:24-alpine AS builder
WORKDIR /app
RUN mkdir /app/build -p
RUN echo "Hello World (1)" > /app/build/index.html

FROM httpd:2-alpine
WORKDIR /usr/local/apache2/htdocs/
COPY --from=builder /app/build /usr/local/apache2/htdocs/
EXPOSE 80
