FROM jenkins/ssh-agent:5.12.0-jdk17

ENV DEBIAN_FRONTEND noninteractive

USER root

RUN apt-get update && apt-get install -y --no-install-recommends \
    curl \
    python3.0 \
    python3-pip \
    unzip \
    ansible \
    git

RUN groupadd -g 987 docker && usermod -aG docker jenkins
RUN curl "https://awscli.amazon"

USER jenkins
