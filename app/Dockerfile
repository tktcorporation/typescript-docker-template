FROM node:14.5.0 AS build-stage

RUN npm i -g @nestjs/cli ts-node

COPY . /app

WORKDIR /app
RUN yarn
RUN yarn build

ENTRYPOINT ["/bin/bash", "-c"]

CMD ["yarn start"]

FROM node:14.5.0 AS runtime-stage

WORKDIR /app

COPY --from=build-stage /app/package.json ./
COPY --from=build-stage /app/yarn.lock ./

RUN yarn install --production

COPY --from=build-stage /app/dist ./dist

CMD ["/bin/bash", "-c", "node /app/dist/main"]

