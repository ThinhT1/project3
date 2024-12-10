FROM node:16
# Create app directory
WORKDIR /usr/src/app

# Kiểm tra phiên bản Node.js
#RUN node -v

# Kiểm tra phiên bản TypeScript
#RUN tsc -v

# Install app dependencies
# A wildcard is used to ensure both package.json AND package-lock.json are copied where available (npm@5+)
COPY package*.json ./
RUN npm ci 
# Bundle app source
COPY . .
EXPOSE 8080
CMD [ "npm", "run", "prod" ]