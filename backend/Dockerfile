FROM node:20
EXPOSE 8080
# in host network we should use DB_HOST as localhost
# in bridge network we should use DB_HOST as mysql
ENV DB_HOST="mysql"
RUN mkdir /opt/server
WORKDIR /opt/server
COPY package.json .
COPY *.js .
# Installing project dependencies
RUN npm install
CMD ["node", "index.js"]

