# Verwenden Sie ein Node.js-Image als Basis
FROM node:14

# Setzen Sie das Arbeitsverzeichnis in den Container
WORKDIR /app

# Kopieren Sie die Package.json- und Package-lock.json-Dateien in den Container
COPY ./app/package*.json ./

# Installieren Sie die Abhängigkeiten
RUN npm install

# Installieren Sie Vite global in den Container
RUN npm install -g vite

# Kopieren Sie den Rest des Codes in den Container
COPY ./app .

# Öffnen Sie den Port 6547 für die Anwendung
EXPOSE 6547

# Starten Sie die Anwendung im Entwicklungsmodus mit npm run dev
CMD ["npm", "run", "dev"]
