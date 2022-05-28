# ARG BUILD_FROM
# FROM $BUILD_FROM

FROM node:14-slim
ENV CK_API_ENV=prod
RUN apt-get update && apt-get install -y python build-essential
RUN mkdir -p /node_modules
COPY ["./dist", "./package.json"]
RUN npm install --production --save-exact
COPY ["./node_modules"]
EXPOSE 3000
CMD npm start
