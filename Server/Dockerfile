# Use Node 18 Alpine as base image
FROM node:18-alpine

# Set working directory
WORKDIR /app

# Copy package.json and package-lock.json
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the code
COPY . .

# Create directories for uploads if they don't exist
RUN mkdir -p public/images

# Expose port 4000
EXPOSE 4000

# Start the server
CMD ["npm", "start"]