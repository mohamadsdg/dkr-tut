FROM node:alpine as builder

WORKDIR /app
COPY package.json .
RUN npm install 
COPY . .
RUN npm run build 

FROM nginx:alpine
EXPOSE 3000
COPY ./nginx.conf /etc/nginx/conf.d/nginx.conf
# COPY ./nginx/default.conf /etc/nginx/conf.d/default.conf
COPY --from=builder /app/build /usr/share/nginx/html