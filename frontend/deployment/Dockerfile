# Стадия сборки
FROM node:20-alpine as build
WORKDIR /client
COPY ./linked_dir_web .
RUN npm install && npm run build

# Стадия продакшн
FROM nginx:1.22.1 as prod
COPY --from=build /client/build /usr/share/nginx/html
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]