FROM node:18-alpine as builder

# start working in the /app directory
WORKDIR /app

# copy files and install dependencies
COPY ./sveltewind-fastmongo-template/client/ ./
# install the dependencies
RUN npm install 
# create the build files
RUN npm run build

ENTRYPOINT [ "vite", "preview" ]

# # stage two of build
# # copy build result and run.
# FROM nginx:1.18-alpine

# # Enter nginx stage
# WORKDIR /usr/share/nginx/html
# # Clear out the directory
# RUN rm -rf ./* 
# # Copy over the build artifacts
# COPY --from=builder /app/build .

# ENTRYPOINT [ "nginx", "-g", "daemon off;" ]
