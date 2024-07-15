<<<<<<< HEAD
# Stage 1: Build the React app
FROM node:16 as build

WORKDIR /app

COPY package.json ./
COPY package-lock.json ./

RUN npm install

COPY . ./

RUN npm run build

# Stage 2: Serve the React app using Nginx
=======
FROM node:16 AS build

WORKDIR /app

COPY package*.json ./

RUN npm install

COPY . .

RUN npm run build

>>>>>>> 785221bebfaef04d47860bb3ca0ede8ee9cb8da2
FROM nginx:alpine

COPY --from=build /app/build /usr/share/nginx/html

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]
<<<<<<< HEAD

=======
>>>>>>> 785221bebfaef04d47860bb3ca0ede8ee9cb8da2
