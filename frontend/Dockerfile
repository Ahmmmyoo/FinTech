# Dockerfile for React Frontend

# Use a lightweight Node.js base image
FROM node:20-alpine

# Set the working directory inside the container
WORKDIR /app

# Install latest npm
RUN npm install -g npm@latest

# Copy package.json and package-lock.json to the working directory
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the project files to the container
COPY . .

# Build the React app for production
EXPOSE 5173

# Start the React app
CMD ["npm", "run", "dev", "--", "--host", "0.0.0.0"]
