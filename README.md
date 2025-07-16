# Personal Portfolio Website - GitHub Pages

一个现代化的个人作品集网站，基于HTML、CSS和JavaScript构建，专为GitHub Pages部署优化。

## 📋 目录

- [项目介绍](#项目介绍)
- [功能特性](#功能特性)
- [快速开始](#快速开始)
- [部署到GitHub Pages](#部署到github-pages)
- [内容修改指南](#内容修改指南)
- [自定义样式](#自定义样式)
- [项目结构](#项目结构)
- [技术栈](#技术栈)
- [浏览器支持](#浏览器支持)
- [贡献指南](#贡献指南)
- [许可证](#许可证)

## 🎯 项目介绍

这是一个响应式的个人作品集网站模板，具有现代化的设计和流畅的用户体验。网站包含以下主要部分：

- **个人介绍** - 展示你的个人信息和专业技能
- **简历** - 详细的工作经验和教育背景
- **作品集** - 展示你的项目和作品
- **博客** - 分享你的想法和文章
- **联系信息** - 让访客能够联系到你

## ✨ 功能特性

- 📱 **完全响应式设计** - 在所有设备上完美显示
- 🎨 **现代化UI** - 使用渐变色彩和阴影效果
- ⚡ **快速加载** - 优化的代码和资源
- 🔍 **SEO友好** - 良好的HTML结构和元数据
- 🎯 **无障碍访问** - 符合WCAG标准
- 📧 **联系表单** - 内置的联系表单功能
- 🖼️ **图片优化** - 支持多种图片格式
- 🌙 **深色主题** - 护眼的深色配色方案

## 🚀 快速开始

### 本地开发

1. **克隆仓库**
   ```bash
   git clone https://github.com/your-username/your-repo-name.git
   cd your-repo-name
   ```

2. **打开项目**
   - 直接在浏览器中打开 `index.html` 文件
   - 或使用本地服务器（推荐）：
     ```bash
     # 使用Python
     python -m http.server 8000
     
     # 使用Node.js
     npx serve .
     
     # 使用Live Server (VS Code扩展)
     ```

3. **访问网站**
   - 打开浏览器访问 `http://localhost:8000`

## 🌐 部署到GitHub Pages

### 方法一：自动部署（推荐）

1. **创建GitHub仓库**
   - 在GitHub上创建一个新的仓库
   - 仓库名建议使用：`your-username.github.io`

2. **上传代码**
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/your-username/your-repo-name.git
   git push -u origin main
   ```

3. **启用GitHub Pages**
   - 进入仓库设置 (Settings)
   - 找到 "Pages" 选项
   - 在 "Source" 中选择 "Deploy from a branch"
   - 选择 "main" 分支和 "/ (root)" 文件夹
   - 点击 "Save"

4. **访问你的网站**
   - 等待几分钟后，访问 `https://your-username.github.io`

### 方法二：使用GitHub Actions

1. 在项目根目录创建 `.github/workflows/deploy.yml` 文件
2. 配置自动部署工作流
3. 每次推送到main分支时自动部署

## 📝 内容修改指南

### 1. 个人信息修改

#### 修改头像和基本信息
编辑 `index.html` 文件中的侧边栏部分：

```html
<!-- 修改头像 -->
<img src="./assets/images/my-avatar.png" alt="你的名字" width="80">

<!-- 修改姓名和职位 -->
<h1 class="name" title="你的名字">你的名字</h1>
<p class="title">你的职位</p>
```

#### 修改联系信息
```html
<!-- 邮箱 -->
<a href="mailto:your-email@example.com" class="contact-link">your-email@example.com</a>

<!-- 电话 -->
<a href="tel:+1234567890" class="contact-link">+1 (234) 567-890</a>

<!-- 生日 -->
<time datetime="1990-01-01">January 1, 1990</time>

<!-- 地址 -->
<address>你的城市，你的国家</address>
```

#### 修改社交媒体链接
```html
<li class="social-item">
  <a href="https://github.com/your-username" class="social-link">
    <ion-icon name="logo-github"></ion-icon>
  </a>
</li>
```

### 2. 关于我部分修改

编辑 `index.html` 中的 "About me" 部分：

```html
<section class="about-text">
  <p>
    在这里写你的个人介绍...
  </p>
  <p>
    继续写更多关于你的信息...
  </p>
</section>
```

#### 修改服务/技能部分
```html
<li class="service-item">
  <div class="service-icon-box">
    <img src="./assets/images/icon-dev.svg" alt="web development icon" width="40">
  </div>
  <div class="service-content-box">
    <h4 class="h4 service-item-title">Web Development</h4>
    <p class="service-item-text">
      描述你的技能和服务...
    </p>
  </div>
</li>
```

### 3. 简历部分修改

#### 工作经验
```html
<li class="timeline-item">
  <h4 class="h4 timeline-item-title">职位名称</h4>
  <span>2020 — 2023</span>
  <p class="timeline-text">
    工作描述和成就...
  </p>
</li>
```

#### 教育背景
```html
<li class="timeline-item">
  <h4 class="h4 timeline-item-title">学位名称</h4>
  <span>2016 — 2020</span>
  <p class="timeline-text">
    学校名称和所学专业...
  </p>
</li>
```

#### 技能进度条
```html
<div class="skill-progress-bg">
  <div class="skill-progress-fill" style="width: 90%"></div>
</div>
```

### 4. 作品集部分修改

#### 添加新项目
```html
<li class="project-item active" data-filter-item data-category="web development">
  <a href="#">
    <figure class="project-img">
      <div class="project-item-icon-box">
        <ion-icon name="eye-outline"></ion-icon>
      </div>
      <img src="./assets/images/project-1.jpg" alt="项目名称" loading="lazy">
    </figure>
    <h3 class="project-title">项目名称</h3>
    <p class="project-category">Web Development</p>
  </a>
</li>
```

#### 项目分类
- `data-category="web development"` - Web开发
- `data-category="applications"` - 应用程序
- `data-category="web design"` - Web设计

### 5. 博客部分修改

#### 添加博客文章
```html
<li class="blog-post-item">
  <a href="#">
    <figure class="blog-banner-box">
      <img src="./assets/images/blog-1.jpg" alt="文章标题" loading="lazy">
    </figure>
    <div class="blog-content">
      <div class="blog-meta">
        <p class="blog-category">技术</p>
        <span class="dot"></span>
        <time datetime="2023-12-01">Dec 1, 2023</time>
      </div>
      <h3 class="h3 blog-item-title">文章标题</h3>
      <p class="blog-text">
        文章摘要...
      </p>
    </div>
  </a>
</li>
```

### 6. 联系表单修改

联系表单目前是静态的，要使其功能化，你需要：

1. **使用表单服务**（推荐）：
   - [Formspree](https://formspree.io/)
   - [Netlify Forms](https://www.netlify.com/docs/form-handling/)
   - [Google Forms](https://www.google.com/forms/about/)

2. **配置Formspree示例**：
```html
<form action="https://formspree.io/f/your-form-id" method="POST" class="contact-form" data-form>
  <div class="input-wrapper">
    <input type="text" name="name" class="form-input" placeholder="Name" required data-form-input>
    <input type="email" name="email" class="form-input" placeholder="Email address" required data-form-input>
  </div>
  <textarea name="message" class="form-input" placeholder="Your Message" required data-form-input></textarea>
  <button class="form-btn" type="submit" disabled data-form-btn>
    <ion-icon name="paper-plane"></ion-icon>
    <span>Send Message</span>
  </button>
</form>
```

## 🎨 自定义样式

### 修改颜色主题

编辑 `assets/css/style.css` 文件中的CSS变量：

```css
:root {
  /* 主色调 */
  --orange-yellow-crayola: hsl(45, 100%, 72%);
  --vegas-gold: hsl(45, 54%, 58%);
  
  /* 背景色 */
  --eerie-black-1: hsl(240, 2%, 13%);
  --eerie-black-2: hsl(240, 2%, 12%);
  --smoky-black: hsl(0, 0%, 7%);
  
  /* 文字颜色 */
  --white-1: hsl(0, 0%, 100%);
  --white-2: hsl(0, 0%, 98%);
  --light-gray: hsl(0, 0%, 84%);
}
```

### 修改字体

1. **更改Google Fonts**：
```html
<link href="https://fonts.googleapis.com/css2?family=Your-Font:wght@300;400;500;600&display=swap" rel="stylesheet">
```

2. **更新CSS变量**：
```css
:root {
  --ff-poppins: 'Your-Font', sans-serif;
}
```

### 修改布局

- **侧边栏宽度**：修改 `.sidebar` 的 `width` 属性
- **内容区域**：修改 `.main-content` 的样式
- **间距**：调整 `padding` 和 `margin` 值

## 📁 项目结构

```
jay0716/
├── index.html              # 主页面文件
├── README.md               # 项目说明文档
├── LICENSE                 # 许可证文件
├── assets/                 # 静态资源文件夹
│   ├── css/
│   │   └── style.css       # 主样式文件
│   ├── js/
│   │   └── script.js       # JavaScript功能文件
│   └── images/             # 图片资源
│       ├── my-avatar.png   # 个人头像
│       ├── project-*.jpg   # 项目图片
│       ├── blog-*.jpg      # 博客图片
│       ├── icon-*.svg      # 图标文件
│       └── logo.ico        # 网站图标
└── website-demo-image/     # 演示图片
    ├── desktop.png
    └── mobile.png
```

## 🛠️ 技术栈

- **HTML5** - 语义化标记
- **CSS3** - 样式和动画
  - CSS Grid 和 Flexbox 布局
  - CSS 变量（自定义属性）
  - 媒体查询（响应式设计）
- **JavaScript (ES6+)** - 交互功能
  - DOM 操作
  - 事件处理
  - 表单验证
- **Ionicons** - 图标库
- **Google Fonts** - 字体服务

## 🌐 浏览器支持

- ✅ Chrome (最新版本)
- ✅ Firefox (最新版本)
- ✅ Safari (最新版本)
- ✅ Edge (最新版本)
- ✅ 移动端浏览器

## 🤝 贡献指南

1. Fork 这个项目
2. 创建你的特性分支 (`git checkout -b feature/AmazingFeature`)
3. 提交你的更改 (`git commit -m 'Add some AmazingFeature'`)
4. 推送到分支 (`git push origin feature/AmazingFeature`)
5. 打开一个 Pull Request

## 📄 许可证

这个项目基于 MIT 许可证开源。查看 [LICENSE](LICENSE) 文件了解详情。

## 🙏 致谢

- 设计灵感来自现代作品集网站
- 图标来自 [Ionicons](https://ionic.io/ionicons)
- 字体来自 [Google Fonts](https://fonts.google.com/)

## 📞 支持

如果你在使用过程中遇到任何问题，请：

1. 查看 [Issues](https://github.com/your-username/your-repo-name/issues) 页面
2. 创建新的 Issue 描述问题
3. 或者联系我：your-email@example.com

---

**注意**：请记得将上述代码中的 `your-username`、`your-repo-name`、`your-email@example.com` 等占位符替换为你的实际信息。

祝你使用愉快！🎉
