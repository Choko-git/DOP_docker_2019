FROM node:10.15.0-alpine

WORKDIR /usr/my_result_container/

COPY . .

RUN npm install

EXPOSE 80

CMD ["npm", "start"]