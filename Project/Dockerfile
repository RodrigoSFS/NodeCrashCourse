ARG VERSION=20-alpine

FROM node:${VERSION}

WORKDIR /src

ARG VERSION

ENV PORT 3000

COPY package.json ./

RUN npm install

EXPOSE ${PORT}

COPY controllers ./controllers

COPY models ./models

COPY public ./public

COPY routes ./routes

COPY views ./views

COPY app.js ./

CMD [ "npm", "start" ]
