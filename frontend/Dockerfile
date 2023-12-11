# Step 1: Use the official Node.js image as the base image
FROM node:latest

# Step 2: Set the working directory inside the container
WORKDIR /app

# Step 3: Copy package.json and package-lock.json (or yarn.lock)
COPY www/package*.json ./

# Step 4: Install dependencies
RUN npm install

# Install PM2 globally
RUN npm install pm2 -g

# Step 5: Copy the rest of your app's source code
COPY www/ .

# Step 6: Build your Next.js application
RUN npm run build

# Step 7: Define the command to run your app
CMD ["npm", "start"]
