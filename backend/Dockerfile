FROM node:20
EXPOSE 8080
ENV DB_HOST=mysql

# Use adduser for Alpine instead of useradd
RUN useradd expense
RUN mkdir /opt/server
RUN chown expense:expense -R /opt/server
WORKDIR /opt/server
COPY *.json .
COPY *.js .
RUN npm install
CMD [ "node" , "index.js"]