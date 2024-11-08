FROM node:20-alpine
EXPOSE 8080
ENV DB_HOST=mysql
RUN useradd expense
RUN mkdir /opt/server
RUN chown expense:expense -R /opt/server
WORKDIR /opt/server
COPY *.json .
COPY *.js .
RUN npm install 
CMD [ "node" , "index.js"]