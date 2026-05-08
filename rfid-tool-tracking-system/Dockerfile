FROM node:20

WORKDIR /app

COPY . .

RUN npm install -g pnpm
RUN pnpm install --frozen-lockfile

RUN pnpm --filter @workspace/api-server run build

EXPOSE 8080

CMD ["node", "--enable-source-maps", "./artifacts/api-server/dist/index.mjs"]