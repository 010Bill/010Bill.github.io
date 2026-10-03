# 个人学术主页

纯静态页面，无构建步骤。`index.html` 内联了全部 CSS，外部依赖只有 Font Awesome 的 CDN 图标。

上线地址：https://010bill.github.io

## 文件

- `index.html` — 主页全部内容与样式
- `avatar.jpg` — 默认头像（生活照）
- `avatar-formal.jpg` — 悬停切换的证件照
- `fig-resolve.jpg` / `fig-edusro.jpg` / `fig-d3.jpg` — 论文总览图缩略图
- `og-image.jpg` — 分享卡片图（1200×630），发链接到微信/Slack 时的预览
- `favicon.svg` / `favicon.ico` — 浏览器标签页图标（🦄）。SVG 版交给系统
  emoji 字体渲染，各平台显示本地那只；ico 是 Noto 版，给不支持 SVG 图标的浏览器兜底
- `apple-touch-icon.png` — 手机加到主屏时的图标（仍是头像，没跟着换）
- `.nojekyll` — 关闭 GitHub Pages 的 Jekyll 处理

## 部署（GitHub Pages）

1. 新建公开仓库，名字必须是 `010Bill.github.io`
2. 把本目录下所有文件（含隐藏的 `.nojekyll`）放到仓库根目录
3. Settings → Pages → Source 选 `Deploy from a branch`，分支 `main`，目录 `/ (root)`
4. 等 1–3 分钟，访问 https://010bill.github.io

命令行方式（在本目录下执行）：

```bash
git init
git add -A
git commit -m "Add academic homepage"
git branch -M main
git remote add origin https://github.com/010Bill/010Bill.github.io.git
git push -u origin main
```

## 需要你填的位（在 index.html 里搜关键词即可定位）

| 搜索 | 要做什么 |
| --- | --- |
| `填导师姓名` | About 第一段的导师姓名 |
| `草稿` | 研究兴趣那段建议用你自己的话重写 |
| `class="links"` | 八处论文链接位，填好地址后去掉注释；不需要的整行删掉 |
| `cv.pdf` | 把 CV 放到仓库根目录，取消左侧栏 CV 按钮的注释 |
| `你的ID` | Google Scholar 建好后填 user 参数并取消注释 |
| `<span class="a">, ` | CASER、EIG-Mem 的作者名（逗号后留空的位置） |
| `Shuaishuai Zhang</span>, </span>` | Applied Soft Computing 的共同作者 |

## 上线前待办

- **确认 COLING 年份**：EIG-Mem 现在写的是 COLING 2026，如果投的是 2027 那轮要改（搜 `COLING`，两处）
- **实习数据需公司批准**：κ 0.58→0.81、8,000+ 条这些数字上线后会被搜索引擎索引，先走内部审批
- **RESOLVE.pdf 挂上主页前先清干净**：现在第一页还留着 LNCS 模板占位符（`First Author1`、`example.com`）
- **EduSRO 的 PDF 是匿名投稿版**，别直接挂，等正式版
- **审一遍公开仓库**：主页会把流量引到 GitHub，检查 `personalized-edu-backen`、`basedate`、`mood` 里有没有硬编码密钥、公司内部数据、未发表论文的实验脚本；空 README 的仓库建议先转私有
- 页脚「最后更新」日期随内容同步
