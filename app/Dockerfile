FROM node:22.9.0-bookworm-slim

RUN apt update
RUN apt install -y git

RUN git clone --branch v1.0.0 https://github.com/michaelrk02/smartvote-app.git /smartvote-app
WORKDIR /smartvote-app

RUN npm install

CMD [ "npm", "run", "dev" ]
