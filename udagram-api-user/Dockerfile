FROM node:13

# Create app directory
WORKDIR /usr/src/app

# COPY package*.json to app directory
COPY package*.json ./

# Install dependencies
RUN npm ci

# Copy all dependencies to app directory
COPY . .
EXPOSE 8080
CMD ["npm", "run", "dev"]