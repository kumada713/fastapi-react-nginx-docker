FROM node:12.14.1-alpine

ENV NODE_ENV=production

WORKDIR /usr/src/app

COPY ./frontend/package.json ./frontend/yarn.lock /usr/src/app/

RUN yarn install --production --no-progress

COPY . .

CMD [ "yarn", "build" ]