FROM node:20 AS build
WORKDIR /app
COPY . .
RUN npm install
RUN npm run build

FROM nginx:alpine
COPY --from=buld /app/dist /user/share/nginx/html