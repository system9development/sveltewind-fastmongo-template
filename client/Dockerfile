FROM node:18-alpine as builder

# start working in the /app directory
WORKDIR /app

# copy files and install dependencies
COPY ./sveltewind-fastmongo-template/client/ ./
# install the dependencies
RUN npm install 
# create the build files
RUN npm run build

# stage two of build
# copy build result and run.
FROM node:18-slim

WORKDIR /app
COPY --from=builder /app .
COPY . .

CMD ["npm", "start"]