FROM ubuntu:jammy

RUN apt update
RUN apt install -y openjdk-21-jre
RUN apt install -y git

RUN git clone --recursive --branch v1.0.5 https://github.com/michaelrk02/smartvote-api.git /smartvote-api
WORKDIR /smartvote-api

RUN ./gradlew bootJar

COPY ./system.config /smartvote-api/app/config/system.config
COPY ./hosts.config /smartvote-api/app/config/hosts.config

CMD [ "./run-agent-deployment" ]
