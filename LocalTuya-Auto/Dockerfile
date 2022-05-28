# ARG BUILD_FROM
# FROM $BUILD_FROM

FROM node:14-slim
ENV CK_API_ENV=prod
RUN apt-get update && apt-get install -y python build-essential
RUN mkdir -p /node_modules
COPY ["./package.json"]
RUN npm install
COPY ["./node_modules"]
CMD npm run build
EXPOSE 3000
CMD npm start
