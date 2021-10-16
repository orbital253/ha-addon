# ARG BUILD_FROM
# FROM $BUILD_FROM

FROM nikolaik/python-nodejs:python3.10-nodejs14-slim
RUN mkdir -p /workspace/node_modules
COPY ["./dist", "./package.json", "/workspace/"]
WORKDIR /workspace
RUN yarn --production
COPY ["./node_modules", "/workspace/node_modules/"]
EXPOSE 3000
CMD npm start
