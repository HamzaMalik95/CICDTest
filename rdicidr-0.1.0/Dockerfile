# select your base image to start with
FROM node:14
# Create app directory
# this is the location where you will be inside the container
WORKDIR /app
# Install app dependencies
COPY src/ ./
COPY index.html ./
COPY manifest.json ./
COPY package*.json ./
RUN npm install --prefix package.json --no-audit
RUN npm lint --prefix package.json --no-audit
RUN npm prettier --prefix package.json --no-audit
RUN npm test --prefix package.json --no-audit
RUN npm build --prefix package.json --no-audit

# Make this port accessible from outside the container
# Necessary for your browser to send HTTP requests to your Node app
EXPOSE 3000

COPY . ./
CMD npm install;npm audit fix;npm run;npm start