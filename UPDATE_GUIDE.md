# 网站更新指南 / Website Update Guide

这个文档将帮助你轻松更新网站内容。

## 📁 文件结构

```
HaoranZhang.github.io/
├── index.html              # 主页文件（需要编辑的主要文件）
├── images/                 # 图片文件夹
│   ├── projects/          # 个人作品的图片
│   └── artwork/           # 艺术作品的图片
└── UPDATE_GUIDE.md        # 本更新指南
```

## 🎯 如何更新内容

### 1. 更新学术研究 (Academic Research)

在 `index.html` 中找到 `<!-- 学术研究 / Academic Research -->` 部分：

**添加新论文：**
1. 复制一个 `<div class="publication-item">...</div>` 块
2. 修改以下内容：
   - `<h3>`: 论文标题
   - `.authors`: 作者名单
   - `.venue`: 会议/期刊名称和年份
   - `<p>`: 论文简介
   - `.links` 中的 `<a>` 标签: PDF、代码、项目页面链接

**示例：**
```html
<div class="publication-item">
    <h3>Deep Learning for 3D Reconstruction</h3>
    <div class="authors">Zhang H., Li M., Wang X.</div>
    <div class="venue">SIGGRAPH 2025</div>
    <p>本文提出了一种新的3D重建方法...</p>
    <div class="links">
        <a href="paper.pdf" target="_blank">PDF</a>
        <a href="https://github.com/..." target="_blank">Code</a>
    </div>
</div>
```

### 2. 更新个人作品 (Personal Projects)

在 `index.html` 中找到 `<!-- 个人作品 / Personal Projects -->` 部分：

**添加新项目：**
1. 将项目图片保存到 `images/projects/` 文件夹
2. 复制一个 `<div class="gallery-item">...</div>` 块
3. 修改以下内容：
   - 图片路径: `<img src="images/projects/你的图片.jpg" alt="...">`
   - `<h3>`: 项目名称
   - `<p>`: 项目描述
   - `.tags`: 技术标签（如 OpenGL, Unity, Shader等）
   - `.links`: GitHub 和 Demo 链接

**示例：**
```html
<div class="gallery-item">
    <div class="gallery-item-image">
        <img src="images/projects/raytracer.jpg" alt="Ray Tracer">
    </div>
    <div class="gallery-item-content">
        <h3>实时光线追踪渲染器</h3>
        <p>基于CUDA的实时光线追踪渲染器，支持PBR材质和全局光照。</p>
        <div class="tags">
            <span>CUDA</span>
            <span>Ray Tracing</span>
            <span>C++</span>
        </div>
        <div class="links">
            <a href="https://github.com/..." target="_blank">GitHub →</a>
            <a href="demo.html" target="_blank">Demo →</a>
        </div>
    </div>
</div>
```

### 3. 更新艺术作品 (Artwork)

在 `index.html` 中找到 `<!-- 艺术作品 / Artwork -->` 部分：

**添加新作品：**
1. 将建筑设计作品图片保存到 `images/artwork/` 文件夹
2. 复制一个 `<div class="gallery-item">...</div>` 块
3. 修改以下内容：
   - 图片路径: `<img src="images/artwork/你的图片.jpg" alt="...">`
   - `<h3>`: 作品名称
   - `<p>`: 作品描述
   - `.tags`: 相关标签（如年份、类型等）

**示例：**
```html
<div class="gallery-item">
    <div class="gallery-item-image">
        <img src="images/artwork/museum.jpg" alt="Museum Design">
    </div>
    <div class="gallery-item-content">
        <h3>现代美术馆设计</h3>
        <p>这是一个融合传统与现代元素的美术馆设计，注重空间流动性。</p>
        <div class="tags">
            <span>建筑设计</span>
            <span>2021</span>
        </div>
    </div>
</div>
```

### 4. 更新个人信息

**修改导航栏名字：**
找到 `<nav>` 部分，修改 `<h1>Your Name</h1>`

**修改Hero区域：**
找到 `<section id="hero">` 部分，修改名字和简介

**修改页脚联系方式：**
找到 `<footer>` 部分，修改邮箱、GitHub、Google Scholar 链接

## 📸 图片建议

- **推荐格式**: JPG 或 PNG
- **推荐尺寸**: 宽度 600-1200px（会自动适应）
- **推荐比例**: 4:3 或 16:9
- **文件大小**: 尽量压缩到 500KB 以下

## 🚀 发布更新

1. 编辑 `index.html` 文件
2. 添加新图片到 `images/` 文件夹
3. 提交更改到 GitHub：
   ```bash
   git add .
   git commit -m "Update content"
   git push
   ```
4. 几分钟后，访问 `https://arcodius.github.io/HaoranZhang.github.io/` 查看更新

## 💡 提示

- 每次添加内容时，只需复制相应的 HTML 块并修改内容
- HTML 中有详细的中英文注释，帮助你找到需要修改的位置
- 不需要修改 CSS 样式，只需要修改内容部分
- 如果不确定，可以先在本地用浏览器打开 `index.html` 预览效果

## ❓ 常见问题

**Q: 图片不显示怎么办？**
A: 检查图片路径是否正确，确保图片文件已上传到对应文件夹。

**Q: 如何改变网站颜色？**
A: 在 `<style>` 标签中，找到颜色代码（如 `#3498db`）并修改。

**Q: 如何添加更多section？**
A: 复制任意一个 `<section>...</section>` 块，修改id和内容即可。
