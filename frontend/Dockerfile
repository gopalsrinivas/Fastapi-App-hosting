# Use Node.js as base image
FROM node:18

# Set working directory
WORKDIR /frontend

# Copy package.json and install dependencies
COPY package.json ./
RUN npm install

# Copy the frontend code
COPY ./ ./

# Expose Next.js development port
EXPOSE 3000

# Command to run Next.js
CMD ["npm", "run", "dev"]
