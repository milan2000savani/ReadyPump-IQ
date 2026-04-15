FROM node:24-alpine

WORKDIR /usr/src/app

# Install dependencies
COPY package*.json ./
RUN npm install

# Copy the rest of the app
COPY . .

# Build the app for production
RUN npm run build

# Expose the port Vite uses by default
EXPOSE 5173

# Start the app
CMD ["npm", "run", "dev"]