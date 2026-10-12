# 邵东村 · 文化 IP 与乡村振兴展示网站

一个关于江苏宜兴湖㳇镇邵东村的综合门户单页网站，主打**贡茶古道文化 IP、古琴大师成公亮故事、山间古韵与乡村振兴实践**。纯静态、零依赖、响应式，可直接用 GitHub Pages 免费托管。

## 站点内容

页面自上而下分为以下板块：

- **村情速览**：人口、面积、竹林、区位等基础画像（含三面环山、溪水纵横地貌特征）
- **贡茶古道**：阳羡贡茶历史脉络、境会亭、廿三弯、赐福寺，以及白居易《夜闻贾常州崔湖州茶山境会亭欢宴》诗引
- **琴声里的廿三弯**：古琴大师成公亮与邵坞的十四天交集
- **山间古韵**：项羽传说、青隐寺、东岭水库、村史源流
- **物产与体验**：毛竹、笋干、阳羡茶、山泉 + 徒步溯溪线路
- **三张王牌 / 三个真问题**：机遇与挑战并陈——资源稀缺性、流量自然性、底蕴厚度，对比有流量没留量、配套薄弱+灾后恢复、人口空心化与人才断档
- **乡村振兴**：邵东村的振兴实践，两年主线与分步实施路线图（弱化个人署名，聚焦村落行动）

## 本地预览

```bash
cd 邵东村网页
python3 -m http.server 8123
# 浏览器打开 http://127.0.0.1:8123/
```

或直接用浏览器打开 `index.html`。

## 目录结构

```
邵东村网页/
├── index.html              # 网站主文件（自包含 HTML/CSS/JS）
├── assets/                 # 备用资源目录（图片等）
├── .nojekyll               # 关闭 GitHub Pages 的 Jekyll 处理
├── .github/workflows/
│   └── deploy.yml          # 推送到 main 后自动部署到 Pages
└── README.md
```

## 发布到 GitHub Pages（后续步骤）

1. 在 GitHub 新建一个公开仓库（建议名 `shaodong-village` 或 `shaodong-village-site`）。
2. 将本目录内容推送到 `main` 分支：
   ```bash
   git init
   git add .
   git commit -m "邵东村网站初版"
   git branch -M main
   git remote add origin https://github.com/<你的用户名>/<仓库名>.git
   git push -u origin main
   ```
3. 仓库 → **Settings → Pages → Build and deployment → Source 选择 "GitHub Actions"**。
4. 推送后 Actions 会自动构建并发布，几分钟即可在 `https://<用户名>.github.io/<仓库名>/` 访问。

> 若不想要 Action 自动部署，也可在 Pages 设置里直接选 "Deploy from a branch → main → /(root)"，无需 `deploy.yml`。

## 数据说明

本站内容据邵东村公开村情、村志资料、驻村工作记录及公开报道整理。涉及人口、资产、项目补助标准等数据，须以主管部门正式文件与现场核实为准；民间传说与可考史实已尽量分别标注。镇名"湖㳇镇"亦作"湖父镇"，以官方标准地名为准。

© 2026 邵东村 · 仅供文化交流与乡村振兴宣传使用。
