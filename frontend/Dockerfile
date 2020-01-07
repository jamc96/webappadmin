# base image
FROM node:12.2.0-alpine

# copy app to source
COPY . /src

# set working directory
WORKDIR /src

# install and cache app dependencies
RUN npm install --silent && \
    npm install react-scripts@3.3.0 -g --silent

# expose port
EXPOSE 3000

# start app
CMD [ "npm", "start" ]