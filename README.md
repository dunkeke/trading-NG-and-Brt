# 合约交易分析终端（锁定展示版）

本仓库包含单文件前端页面 `index.html`，已启用只读锁定模式，用于展示或审阅，不可在页面内新增/编辑/导出数据。

## 本地预览

使用任意静态服务器即可预览：

```bash
python3 -m http.server 8000
```

然后在浏览器访问 `http://localhost:8000`。

## 部署到 GitHub Pages

1. 将本仓库推送到 GitHub。
2. 打开仓库 **Settings** → **Pages**。
3. 在 **Build and deployment** 中选择：
   - **Source**: Deploy from a branch
   - **Branch**: `main`（或你的默认分支）
   - **Folder**: `/ (root)`
4. 保存后等待 GitHub Pages 构建完成，页面将发布在提示的 URL。

> 如果希望将页面放到子路径（如 `https://<user>.github.io/<repo>/`），请确保直接使用根目录的 `index.html`。

## 说明

- 页面为纯静态文件，无需额外构建流程。
- 如需解除锁定模式，请移除 `index.html` 中的 `lockApp()` 调用及相关样式。
