FROM node:alpine as builder
WORKDIR '/usr/app/FibApp'
COPY ./package.json ./
RUN npm install
COPY . .
RUN npm run build

FROM nginx 
EXPOSE 3000
COPY ./nginx/default.conf /etc/nginx/conf.d/default.conf
COPY --from=0 /usr/app/FibApp/build /usr/share/nginx/html


