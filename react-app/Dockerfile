# Use the official Node.js image
FROM node:16-alpine

# Set working directory
WORKDIR /usr/src/app

# Install create-react-app globally (optional)
RUN npm install -g create-react-app

# Create a new React app in the current directory
RUN npx create-react-app .

# Expose port 3000
EXPOSE 3000

# Start the app
CMD ["npm", "start"]
