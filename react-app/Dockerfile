FROM node:16-alpine

# Set working directory
WORKDIR /app

# Install dependencies
COPY package.json ./
RUN npm install

# Copy the source files
COPY . .

# Expose port 3000
EXPOSE 3000

# Start React app
CMD ["npm", "start"]
