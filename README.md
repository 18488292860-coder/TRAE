# 闲鱼克隆站点

高保真闲鱼首页克隆，纯静态单页（无构建步骤）。

## 线上地址

- 正式域名：https://xianyu.lxiaobai168.cc
- Pages 子域：https://xianyu-pages.pages.dev

## 目录结构

- `public/index.html` — 站点入口（Cloudflare Pages 构建输出目录）
- `src/worker.js` — 静态资源 Worker 入口（本地 `wrangler deploy` 用）
- `wrangler.jsonc` — Workers + Assets 绑定配置

## 部署

由 Cloudflare Pages 的 Git 集成自动部署：

- 仓库：`18488292860-coder/TRAE`
- 生产分支：`xianyu-clone`
- 构建命令：留空
- 构建输出目录：`public`

推送到 `xianyu-clone` 分支即自动构建发布。

也可手动部署：

```bash
npx wrangler pages deploy public --project-name=xianyu-pages --branch=xianyu-clone
```
