FROM node:17.9.1-alpine

RUN yarn global add http-server

WORKDIR /app

COPY package*.json ./

RUN yarn install

COPY . .

RUN yarn build

ENV HOST=0.0.0.0

EXPOSE 80

CMD ["http-server", "dist", "-p 80"]
