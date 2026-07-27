# 低空经济月报（GitHub Pages 版）

纯静态单文件月报，适合用 GitHub Pages 免费托管，获得永久子域链接 `https://<用户名>.github.io/<仓库名>/`。

## 仓库根目录需包含的文件

| 文件 | 作用 |
|---|---|
| `index.html` | 最新月报（含「往期回顾」板块，链到各月存档） |
| `2026-07.html` | 2026 年 7 月存档页 |
| `.nojekyll` | 告诉 GitHub 不要用 Jekyll 构建（本项目是纯静态 HTML，无需构建） |
| `README.md` | 本说明 |

> 以后每月更新：把新的 `index.html`（当月）和上一个 `index.html` 存为 `YYYY-MM.html`（如 `2026-08.html`）一起提交，并在 `index.html` 的「往期回顾」里追加一条即可。链接不变。

## 上传与开启 Pages（3 步）

1. 在 github.com 新建一个**公开（public）**仓库（名字随意，如 `low-altitude-monthly`）。
2. 把本目录下的 4 个文件**直接传到仓库根目录**（不要连文件夹一起传）：
   - `index.html`
   - `2026-07.html`
   - `.nojekyll`
   - `README.md`
3. 仓库 → **Settings → Pages**（或新版「Pages」）→ Source 选 **Deploy from a branch** → Branch 选 **main**（或 master，看你默认分支）→ 目录选 **/(root)** → 点 Save。
   - 等约 1 分钟，访问 `https://<用户名>.github.io/<仓库名>/` 即可。

## 技术说明

- 图表库 ECharts 5.5.0 通过 jsDelivr CDN 引入（HTTPS），GitHub Pages 允许加载外部 CDN，无需改代码。
- 页面内部使用相对路径链接（`2026-07.html`），部署后 `/2026-07.html` 可直接访问。
- 无需构建、无需 Node/Python 环境，纯静态托管。

## ⚠️ 大陆访问提示

GitHub 及其 Pages 域名（`github.io`）在**中国大陆经常无法打开或极慢**。若读者主要在国内，建议：
- 用本仓库做**版本归档 / 源码管理**，对外分发改用其他方式（如已生成的 Word 文档、或绑定自定义域名 + 国内 CDN）；
- 或对 `github.io` 链接做国内镜像 / 反代。
