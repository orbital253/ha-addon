# ARG BUILD_FROM
# FROM $BUILD_FROM

FROM node:14-slim
RUN apt-get update || : && apt-get install python -y
RUN apt-get -y install build-essential
RUN mkdir -p /workspace/node_modules
COPY ["./dist", "./package.json", "/workspace/"]
WORKDIR /workspace
RUN yarn --production
COPY ["./node_modules", "/workspace/node_modules/"]
EXPOSE 3000
CMD npm start
