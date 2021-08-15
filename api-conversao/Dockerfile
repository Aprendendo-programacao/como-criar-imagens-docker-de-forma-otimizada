FROM node:14-alpine3.14

WORKDIR /app

# Copiar "package.json" e "package-lock.json" para o container
COPY package*.json ./

RUN npm install

# Copiar todos os arquivos do projeto para o container
COPY . .

EXPOSE 8080

CMD ["node", "index.js"]