# Cloudflare Worker

## 1. 安装 Cloudflare

```bash
npm install -g wrangler

pnpm install -g wrangler
```

## 2. 登录

```bash
wrangler login
```

## 3. 创建项目

参考 [worker-tinygo example](https://github.com/syumai/workers/tree/main/_templates/cloudflare/worker-tinygo)

```bash
# 安装 gonew
go install golang.org/x/tools/cmd/gonew@latest

# install gotiny
brew tap tinygo-org/tools
brew install tinygo

# 创建项目
gonew github.com/syumai/workers/_templates/cloudflare/worker-tinygo your.module/my-app # e.g. github.com/syumai/my-app
cd my-app
go mod tidy
make dev # start running dev server
curl http://localhost:8787/hello # outputs "Hello!"
```

## 4. 部署

```bash
wrangler deploy
```

![deploy](./SCR-20241222-brto.png)
