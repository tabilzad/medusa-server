FROM node:17.1.0

WORKDIR /app/medusa

COPY . .

RUN apt-get update

RUN apt-get install -y python

RUN npm install -g npm@latest

RUN npm install -g @medusajs/medusa-cli@latest

RUN npm install --loglevel=error

RUN npm run build


ENTRYPOINT ["./develop.sh", "develop"]
