# Use an official Node.js runtime as the base image
FROM node:22-alpine

# Set the working directory
WORKDIR /app

# Copy package.json and package-lock.json
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the application code
COPY . .

# Build the TypeScript code
RUN npm run build

EXPOSE 5000

# Command to run the application
CMD ["node", "/app/dist/backend/index.js"]
