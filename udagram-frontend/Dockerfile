FROM node:12

WORKDIR /usr/src/app

COPY package*.json ./

RUN npm install

RUN npm install -g ionic

COPY . .

RUN ionic build

EXPOSE 8100

CMD ["ionic", "serve", "--address", "0.0.0.0"]
