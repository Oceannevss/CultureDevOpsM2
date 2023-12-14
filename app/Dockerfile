FROM node:13.6.0-alpine

#Create app directory
RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app

#install app dependancies
COPY package*.json ./
RUN rm -rf package-lock.json node_modules
RUN npm install

#Bundle app sources
COPY . /usr.src/app

USER node
CMD [ "npm", "start" ]