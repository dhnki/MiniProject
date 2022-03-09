# build stage
FROM node:lts-alpine as build-stage
WORKDIR /home/runner/work/MiniProject/MiniProject/board-app
RUN npm install --production
COPY . .
RUN npm run build

# production stage
FROM nginx:stable-alpine as production-stage
COPY --from=build-stage /app/dist /usr/share/nginx/html
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
