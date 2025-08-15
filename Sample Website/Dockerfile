# 1) Base image
FROM node:18-alpine

# 2) App directory
WORKDIR /app

# 3) Install deps (copy only package files for better caching)
COPY package*.json ./
RUN npm install --only=production

# 4) Copy the rest of the app
COPY . .

# 5) Expose port in the container
EXPOSE 3000

# 6) Start command
CMD ["npm", "start"]
