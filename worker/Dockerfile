FROM node:alpine
WORKDIR "/usr/app/FibApp"
COPY ./package.json ./
RUN npm install
COPY . .
CMD ["npm", "run", "start"]