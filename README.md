# Hello World 页面 — GitHub Pages 部署指南

本目录只有一个文件 `index.html`，无需任何构建工具，可直接部署到 GitHub Pages。

## 方式一：网页上传（最简单，2 分钟）

1. 打开 https://github.com/new ，新建一个公开仓库，比如叫 `hello-world`（不要勾选初始化 README）。
2. 进入刚建好的仓库，点右上角 **Add file → Upload files**。
3. 把本目录里的 `index.html` 拖进去，点 **Commit changes**。
4. 进入仓库 **Settings → Pages**，在 Branch 下拉框选 `main`（或 `master`），目录选 `/ (root)`，点 **Save**。
5. 等待 1~2 分钟，刷新页面，顶部会出现访问地址：
   `https://<你的GitHub用户名>.github.io/hello-world/`

## 方式二：命令行推送

```bash
cd hello-world-github-pages
git init
git add index.html
git commit -m "hello world"
git branch -M main
git remote add origin https://github.com/<你的用户名>/hello-world.git
git push -u origin main
```

推送后同样到仓库 **Settings → Pages** 开启 Pages（Branch 选 `main` / root）。

## 常见问题

- **想让地址更短**（`https://<用户名>.github.io/`）：把仓库命名为 `<你的GitHub用户名>.github.io`，`index.html` 放根目录即可。
- **绑定自定义域名**：仓库里加一个 `CNAME` 文件（内容写你的域名），并在 Pages 设置里填 Custom domain，GitHub 会自动配 HTTPS。
