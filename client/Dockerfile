# Stage 1: Build React app
FROM node:18 AS build

# Set working directory
WORKDIR /app

# Copy package files and install dependencies
COPY package.json package-lock.json ./
RUN npm install

# Copy the rest of the code and build
COPY . .
RUN npm run build

# Stage 2: Serve with Apache HTTP Server
FROM httpd:2.4

# Copy the build output from Stage 1
COPY --from=build /app/build /usr/local/apache2/htdocs/

# Copy .htaccess for React client-side routing
COPY .htaccess /usr/local/apache2/htdocs/

# Expose port 80
EXPOSE 80

# Start Apache in the foreground
CMD ["httpd-foreground"]
