FROM node:9-alpine
ENV NAME="Felipe Gomes da Silva"
WORKDIR /src
COPY app/ .
RUN npm install --quiet
EXPOSE 3000
CMD npm start