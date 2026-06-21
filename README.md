# 香港澳门五日游

这是一个单页静态网站，手机端打开后可以直接浏览，也支持添加到主屏幕。

## 工作流

1. 直接修改 `index.html`、`manifest.webmanifest`、`sw.js` 等文件。
2. 提交并推送到 `master` 或 `gh-pages`。
3. GitHub Actions 会自动部署到 GitHub Pages。
4. 手机再次打开站点时，会优先拉取最新版本。
5. 如果浏览器还缓存着旧页面，服务工作线程会尽量自动切换到新版本并刷新。

## 手机查看

- 直接用手机浏览器打开线上地址。
- 如果需要长期使用，选择“添加到主屏幕”。
- 更新后重新打开页面即可看到最新内容。

## 本地调试

- 这是纯静态站点，不需要安装依赖。
- 直接打开 `index.html` 也能预览。

## 发布说明

- GitHub Pages 的部署配置在 [`.github/workflows/pages.yml`](.github/workflows/pages.yml)。
- 站点离线与更新逻辑在 [`sw.js`](sw.js)。
- 可安装信息在 [`manifest.webmanifest`](manifest.webmanifest)。
