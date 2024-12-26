FROM node:latest

RUN apt-get update && apt-get install -y \
  git \
  bash \
  && rm -rf /var/lib/apt/lists/*

WORKDIR /app

COPY . /app

RUN npm install

RUN npm install -g expo-cli

EXPOSE 19000
EXPOSE 19001
EXPOSE 19002

CMD ["npx", "expo", "start", "--tunnel"]
