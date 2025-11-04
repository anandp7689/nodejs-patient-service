# patient/Dockerfile
FROM node:18-alpine

WORKDIR /app

COPY package*.json ./
# optional: if you don't have package.json, we'll create a minimal runtime step
# If you don't have package.json then consider adding simple one to set start script.
RUN npm ci --only=production || true

COPY . .

ENV PORT=3000
EXPOSE 3000

# default start (adjust if you add package.json scripts)
CMD ["node", "patient.js"]
