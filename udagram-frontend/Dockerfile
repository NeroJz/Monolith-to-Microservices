## Build
FROM beevelop/ionic:latest AS ionic

# Create app directory
WORKDIR /usr/src/app

# Copy package files and install dependencies
COPY package*.json ./
RUN npm ci

# Copy bundles to app directory
COPY . .
RUN ionic build

## Run
FROM nginx:alpine

# copy www /usr/share/nginx/html
COPY --from=ionic /usr/src/app/www /usr/share/nginx/html