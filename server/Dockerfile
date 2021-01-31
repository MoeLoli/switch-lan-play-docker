FROM node:lts-slim

RUN mkdir /app
WORKDIR /app
COPY . /app
RUN npm install
RUN npm run build

EXPOSE 11451

ENTRYPOINT [ "npm", "run", "server" ]
