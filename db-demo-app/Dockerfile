# Use a lightweight Node.js image based on Alpine Linux
FROM node:alpine

# Set the working directory inside the container to /app
WORKDIR /app/

# Copy package.json and package-lock.json to optimize layer caching (install dependencies before copying the entire code)
COPY package*.json ./

# Install dependencies listed in package.json
RUN npm install

# Copy the rest of your application files to the container
COPY . .

# Expose the port that the application will run on (example: 3000)
EXPOSE 3000

# Set the command to run when the container starts
CMD ["node", "index.js"]
