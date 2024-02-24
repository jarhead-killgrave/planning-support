FROM node:20-alpine AS build-stage

# Set the working directory
WORKDIR /app

# Copy the package.json and package-lock.json
COPY package*.json ./

# Install the dependencies
RUN yarn install

# Copy the rest of the files
COPY . .

FROM build-stage AS development-stage

CMD ["yarn", "serve"]
