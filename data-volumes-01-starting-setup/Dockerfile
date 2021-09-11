FROM node:14
WORKDIR /data
COPY package.json .
RUN npm install
COPY . .
EXPOSE 80
VOLUME /data/node_modules 
CMD ["npm", "start"]
