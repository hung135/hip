# [Choice] Node.js version (use -bullseye variants on local arm64/Apple Silicon): 16, 14, 12, 16-bullseye, 14-bullseye, 12-bullseye, 16-buster, 14-buster, 12-buster
ARG VARIANT=16-bullseye
#FROM mcr.microsoft.com/vscode/devcontainers/javascript-node:0-${VARIANT}
FROM debian:bullseye
# [Optional] Uncomment this section to install additional OS packages.
RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
    && apt-get -y install --no-install-recommends openjdk-11-jdk nodejs npm
RUN apt-get -y install iputils-ping docker.io postgresql-client
# [Optional] Uncomment if you want to install an additional version of node using nvm
# ARG EXTRA_NODE_VERSION=10
# RUN su node -c "source /usr/local/share/nvm/nvm.sh && nvm install ${EXTRA_NODE_VERSION}"
RUN npm install -g generator-jhipster 
# [Optional] Uncomment if you want to install more global node modules
# RUN su node -c "npm install -g generator-jhipster"  
# RUN su node -c "npm install -g generator-jhipster-nodejs"
RUN apt-get -y install locales curl maven

RUN echo "LC_ALL=en_US.UTF-8" >> /etc/environment
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen
RUN echo "LANG=en_US.UTF-8" > /etc/locale.conf
RUN locale-gen en_US.UTF-8
 
 
