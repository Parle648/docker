FROM node:20-alpine
WORKDIR /server
COPY ./mock .
RUN npm install && npm run build
CMD ["npm", "start"]