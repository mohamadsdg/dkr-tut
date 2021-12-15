# FROM node:latest 
# WORKDIR /app
# COPY ./ ./
# RUN npm install 
# CMD [ "npm", "start" ]  

# FROM node:latest 
# WORKDIR /app
# COPY ./package.json ./
# RUN npm install 
# COPY ./ ./
# CMD [ "npm", "start" ]  

FROM node:alpine
WORKDIR /usr/app 
COPY ./package.json ./
RUN npm install 
COPY ./ ./
CMD ["npm","start"]