# Import de la base
FROM debian

# Installation des composants
RUN apt-get update -y \
    && apt-get install -y git  \
    && apt-get install -y curl \
    && apt-get install -y sudo

# setup nodejs
RUN curl -sL "https://deb.nodesource.com/setup_12.x" | sudo -E bash - \
    && apt-get install -y nodejs

# Port TCP
EXPOSE 3000/tcp

# Clone et install du projet
RUN git clone "https://github.com/jponcy/fake-game-api.git" \
    && npm install \
    && bash npm run start:separed