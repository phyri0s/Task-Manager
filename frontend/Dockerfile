FROM node:18

RUN useradd -m taskUser
USER taskUser

WORKDIR /app
COPY . /app/

RUN npm install && npm run build

EXPOSE 3000
CMD ["npm", "start"]
