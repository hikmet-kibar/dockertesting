FROM ubuntu:latest
EXPOSE 5000
WORKDIR /usr/src/app
COPY . .

RUN apt-get update
RUN apt-get install -y curl
RUN curl https://deb.nodesource.com/setup_14.x | apt-get install -y nodejs

RUN apt-get install -y npm
RUN npm install
RUN npm install -g serve

# Set BEFORE npm run build
ENV REACT_APP_BACKEND_URL http://localhost:8080/
RUN npm run build


CMD ["serve", "-s", "-l", "5000", "build"]
