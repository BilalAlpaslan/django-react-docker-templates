###########################################################################################################
FROM node:13.12.0-alpine

# set working directory
RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app

# add dependencies
ADD ./frontend/package-lock.json /usr/src/app/package-lock.json

# install dependencies
RUN npm install --silent
RUN npm install react-scripts@3.4.1 -g --silent

# add app
ADD ./frontend /usr/src/app

# start app
CMD npm start 0.0.0.0:3000
###########################################################################################################
