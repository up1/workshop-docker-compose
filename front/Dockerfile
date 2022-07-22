FROM node:16-alpine3.15 AS step1
WORKDIR /work
COPY . .
RUN npm install
RUN npm run build #/work/dist/demo-angular

FROM nginx:1.23.1
COPY --from=step1 /work/dist/demo-angular /usr/share/nginx/html
