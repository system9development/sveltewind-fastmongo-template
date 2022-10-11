FROM node:18-alpine

WORKDIR /app

# copy files and install dependencies
COPY ./sveltewind-fastmongo-template/client/ ./
RUN npm install
RUN npm run build

CMD ["npm", "start"]