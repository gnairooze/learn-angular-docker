# Use an official Node.js runtime as a parent image
FROM node:22.12.0-alpine

WORKDIR /app
COPY package.json /app/package.json
RUN npm install && npm install -g @angular/cli@19.0.6
COPY . /app
CMD ng serve --host 0.0.0.0
