FROM node:16
RUN apt-get update
ENV NODE_ENV=development
WORKDIR /opt/
COPY ./package.json ./yarn.lock ./
ENV PATH /opt/node_modules/.bin:$PATH
RUN yarn install
WORKDIR /opt/app
COPY ./ .
EXPOSE 3000
CMD ["yarn", "dev"]
