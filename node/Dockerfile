# Set the base image to Ubuntu
FROM node:0.12.14-wheezy

# File Author / Maintainer
MAINTAINER Theodoros Ploumis

# Install nodemon
RUN npm install -g nodemon

RUN mkdir /src
WORKDIR /src

# Provides cached layer for node_modules
ADD package.json /src/package.json
RUN npm set progress=false && npm install

# Now add files again
ADD . /src

# Expose port
EXPOSE  8080

# Run app using nodemon
CMD ["nodemon", "/src/index.js"]
