FROM node:18

RUN useradd -m taskUser
USER taskUser

WORKDIR /app
COPY . /app/

RUN npm install && npm run build

HEALTHCHECK --interval=30s --timeout=3s --retries=3 CMD curl -f http://localhost/health || exit 1

EXPOSE 3000
CMD ["npm", "start"]
