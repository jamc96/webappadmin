# build environment
FROM node:12.2.0-alpine as build
COPY . /src
WORKDIR /src
RUN npm install && \
    npm run build

# production environment
FROM nginx:1.16.0-alpine
COPY --from=build /src/build /usr/share/nginx/html
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]