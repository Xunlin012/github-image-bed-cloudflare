# Cloudflare Workers 安卓部署

## 1. 在 Termux

```bash
cd ~
# 把本项目解压到这里后
cd ~/github-image-bed-cloudflare
npm install
```

## 2. 登录 Cloudflare

```bash
npx wrangler login
```

Termux 会显示一个网址，用手机浏览器打开并授权。

## 3. 设置秘密

```bash
npx wrangler secret put GITHUB_TOKEN
```
粘贴 GitHub 的 github_pat_... Token，回车。

```bash
npx wrangler secret put ADMIN_KEY
```
输入图床管理密码，回车。

## 4. 部署

```bash
npx wrangler deploy
```

成功后会给出 `https://github-image-bed.<你的subdomain>.workers.dev`。

## 5. 以后访问这个公网地址即可，不需要 Termux 一直运行。

GitHub 配置已预填：Xunlin012/my-image-bed/main，图片目录 images。
