# NOTNGY · 文章与记录

访问网站：https://notngy.github.io/

页面由 GPT 设计、编写并部署。各篇文章的作者独立署名。

## 文件结构

- `index.html`：首页与文章目录。
- `assets/style.css`：首页和文章共用的样式。
- `articles/about-this-site/index.html`：由 GPT 撰写的站点说明，也是一篇完整的文章页面示例。
- `.nojekyll`：直接发布静态文件，无需构建。

## 添加一篇独立文章

1. 在 `articles` 下新建目录，例如 `my-first-post`。
2. 将 `articles/about-this-site/index.html` 复制到新目录，命名为 `index.html`。
3. 修改 `<title>`、description、author、文章标题、日期、可见的作者署名和 `.prose` 中的正文；将 `SITE NOTE` 改为文章分类或删除该行。作者按实际情况填写，页脚的“页面制作：GPT”保留为页面制作署名。
4. 在根目录 `index.html` 的 `.article-list` 中复制一个 `<li>...</li>`，更新标题、日期、摘要、作者和链接 `/articles/my-first-post/`。可以将新文章放在列表最前面。
5. 将新文章和首页一起提交到 `main` 分支，GitHub Pages 会自动发布。

文章会拥有独立地址：`https://notngy.github.io/articles/my-first-post/`。

正文可以用 `<p>` 写段落、`<h2>` 写小标题、`<blockquote>` 写引用。插图可放在对应文章目录里，通过 `<img src="图片文件名" alt="图片说明">` 引用。

## 发布设置

- Settings → Pages → Source：Deploy from a branch
- Branch：`main`
- Folder：`/ (root)`
- HTTPS：已开启

无需安装依赖或运行构建命令，发布进度可在仓库 Actions 标签页查看。
