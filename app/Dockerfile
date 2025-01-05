# Use an official Node.js runtime as a parent image
FROM node:22.12.0-alpine AS angular-node

WORKDIR /app

COPY . .
RUN npm install
RUN npm run build

FROM httpd:2.4.62-alpine3.21

WORKDIR /usr/local/apache2/htdocs
COPY --from=angular-node /app/dist/myapp .

