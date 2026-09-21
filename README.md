# github-test-page

一个纯静态的简易测试网页，单文件（`index.html`），无构建、无依赖，可直接上传到 GitHub 并开启 GitHub Pages 访问。

## 功能

- 点击计数器（+1 / 重置，数据存在浏览器 localStorage）
- 深色 / 浅色主题切换（记忆上次选择）
- 响应式布局，手机端正常显示

## 本地预览

直接双击 `index.html` 用浏览器打开即可；或在该目录起一个本地服务：

```bash
python -m http.server 8080
# 然后访问 http://localhost:8080
```

## 上传到 GitHub 并部署 Pages

1. 在 GitHub 新建一个仓库（例如 `test-page`），**不要**勾选初始化 README。
2. 在本目录执行：

   ```bash
   git init
   git add .
   git commit -m "init: simple test page"
   git branch -M main
   git remote add origin https://github.com/<你的用户名>/test-page.git
   git push -u origin main
   ```

3. 打开仓库 → **Settings** → **Pages** → Source 选择 `Deploy from a branch`，Branch 选 `main` / `root`，保存。
4. 等 1~2 分钟，访问 `https://<你的用户名>.github.io/test-page/`。

> 提示：仓库是 Public 才能用免费的 Pages（Private 需要付费计划）。
