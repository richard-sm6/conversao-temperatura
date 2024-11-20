FROM ubuntu 
ARG NODE_MAJOR=23
RUN apt update && \
    apt install sudo -y 
RUN apt install curl -y
RUN curl -fsSL https://deb.nodesource.com/setup_23.x -o nodesource_setup.sh
RUN sudo -E bash nodesource_setup.sh
RUN sudo apt-get install -y nodejs
WORKDIR /app
COPY . .
RUN npm install
ENTRYPOINT [ "node", "server.js" ]
