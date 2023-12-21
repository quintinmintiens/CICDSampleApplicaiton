# Use an official Node.js runtime as the base image
FROM node:18

# Set the working directory inside the container
WORKDIR /app

# Copy package.json and yarn.lock files
COPY package.json yarn.lock /app/

# Install application dependencies
RUN yarn install --frozen-lockfile

# Copy the rest of the application code
COPY . /app
COPY test.js /app

# Expose port 3000 for the application
EXPOSE 3000

# Start the application when the container starts
CMD ["yarn", "start"]
