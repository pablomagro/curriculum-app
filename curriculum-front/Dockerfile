FROM node:lts-alpine
WORKDIR /usr/src/app
COPY package*.json ./
RUN ls -l
RUN npm install
COPY . ./
RUN ls -l
RUN npm run build
COPY nodeServer.js dist/nodeServer.js
WORKDIR /usr/src/app/dist
EXPOSE 8080
CMD [ "node", "nodeServer.js" ]
