FROM node:lts-alpine

RUN npm install -g http-server

WORKDIR /app/

COPY package*.json ./

RUN npm install

COPY . /app/

RUN npm run build

WORKDIR /app/frontend

EXPOSE 8080

CMD ["http-server", "-p", "8080", "."]
