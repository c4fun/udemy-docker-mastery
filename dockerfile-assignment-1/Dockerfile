FROM node:6.14.4-alpine

MAINTAINER "pcfeng502@gmail.com"

# Use the alpine package manager to install tini
RUN apk add --update tini \
    && mkdir -p /usr/src/app

# Change the working directory
WORKDIR /usr/src/app

# Copy the package json file
COPY package.json package.json

# NPM install
RUN npm install \
    && npm cache clean --force

# COPY the folders
COPY . /usr/src/app 

# EXPOSE the port 3000, as the app runs on 3000
EXPOSE 3000

CMD /sbin/tini -- node ./bin/www

