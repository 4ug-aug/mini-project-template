FROM node:20-alpine

WORKDIR /app

# Copy package files
COPY package*.json ./

# Install dependencies
RUN npm install --legacy-peer-deps

# Copy the rest of the application
COPY . .

# Expose Vite dev server port
EXPOSE 5173

# Start Vite dev server with host set to allow external connections
CMD ["npm", "run", "dev", "--", "--host"]