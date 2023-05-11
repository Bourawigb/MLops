FROM jenkins/jenkins:lts
USER root
RUN apt-get update && apt-get install -y python3-pip && rm -rf /var/lib/apt/lists/*
RUN curl -sSl https://get.docker.com | sh