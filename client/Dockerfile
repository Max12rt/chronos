# We don't want to start from scratch.
# That is why we tell node here to use the current node image as base.
FROM node:alpine3.11

# Create an application directory
RUN mkdir -p /app

# The /app directory should act as the main application directory
WORKDIR /app

# Install node packages
RUN npm install

# Copy or project directory (locally) in the current directory of our docker image (/app)

# Build the app
RUN npm run build

# Expose $PORT on container.
# We use a varibale here as the port is something that can differ on the environment.
EXPOSE $PORT

# Set host to localhost / the docker image

# Set app port
ENV NUXT_PORT=4000

# Start the app
CMD [ "npm", "start" ]
