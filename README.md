# Personal Portfolio Website - GitHub Pages

一个现代化的个人作品集网站，基于HTML、CSS和JavaScript构建，专为GitHub Pages部署优化。

## 📋 目录

- [📝 内容修改指南](#-内容修改指南)
- [🎯 项目介绍](#-项目介绍)
- [✨ 功能特性](#-功能特性)
- [🚀 快速开始](#-快速开始)
- [🌐 部署到GitHub Pages](#-部署到github-pages)
- [🎨 自定义样式](#-自定义样式)
- [📁 项目结构](#-项目结构)
- [🛠️ 技术栈](#️-技术栈)
- [🌐 浏览器支持](#-浏览器支持)
- [🤝 贡献指南](#-贡献指南)
- [📄 许可证](#-许可证)

## 📝 内容修改指南

### 📄 `index.html` 文件修改指南

这是网站的主文件，包含所有页面内容。以下是各个部分的具体修改位置：

#### 1. 网站基本信息（第1-25行）
```html
<!-- 修改网站标题 -->
<title>你的名字 - Personal Portfolio</title>

<!-- 修改网站图标 -->
<link rel="shortcut icon" href="./assets/images/logo.ico" type="image/x-icon">

<!-- 修改字体（可选） -->
<link href="https://fonts.googleapis.com/css2?family=你的字体:wght@300;400;500;600&display=swap" rel="stylesheet">
```

#### 2. 侧边栏个人信息（第35-60行）
```html
<!-- 修改头像 -->
<img src="./assets/images/my-avatar.png" alt="你的名字" width="80">

<!-- 修改姓名和职位 -->
<h1 class="name" title="你的名字">你的名字</h1>
<p class="title">你的职位</p>
```

#### 3. 联系信息（第70-120行）
```html
<!-- 邮箱 -->
<a href="mailto:你的邮箱@example.com" class="contact-link">你的邮箱@example.com</a>

<!-- 电话 -->
<a href="tel:+你的电话号码" class="contact-link">+你的电话号码</a>

<!-- 生日 -->
<time datetime="你的生日">你的生日</time>

<!-- 地址 -->
<address>你的城市，你的国家</address>
```

#### 4. 社交媒体链接（第130-150行）
```html
<!-- 修改社交媒体链接 -->
<li class="social-item">
  <a href="https://github.com/你的用户名" class="social-link">
    <ion-icon name="logo-github"></ion-icon>
  </a>
</li>
<li class="social-item">
  <a href="https://linkedin.com/in/你的用户名" class="social-link">
    <ion-icon name="logo-linkedin"></ion-icon>
  </a>
</li>
```

#### 5. 导航菜单（第170-190行）
```html
<!-- 可以修改导航菜单项 -->
<li class="navbar-item">
  <button class="navbar-link active" data-nav-link>关于我</button>
</li>
<li class="navbar-item">
  <button class="navbar-link" data-nav-link>简历</button>
</li>
```

#### 6. 关于我部分（第203-300行）
```html
<!-- 个人介绍文字 -->
<section class="about-text">
  <p>在这里写你的个人介绍...</p>
  <p>继续写更多关于你的信息...</p>
</section>

<!-- 技能/服务部分 -->
<li class="service-item">
  <div class="service-icon-box">
    <img src="./assets/images/icon-dev.svg" alt="web development icon" width="40">
  </div>
  <div class="service-content-box">
    <h4 class="h4 service-item-title">Web Development</h4>
    <p class="service-item-text">描述你的技能和服务...</p>
  </div>
</li>
```

#### 7. 简历部分（第514-706行）
```html
<!-- 工作经验 -->
<li class="timeline-item">
  <h4 class="h4 timeline-item-title">职位名称</h4>
  <span>2020 — 2023</span>
  <p class="timeline-text">工作描述和成就...</p>
</li>

<!-- 教育背景 -->
<li class="timeline-item">
  <h4 class="h4 timeline-item-title">学位名称</h4>
  <span>2016 — 2020</span>
  <p class="timeline-text">学校名称和所学专业...</p>
</li>

<!-- 技能进度条 -->
<div class="skill-progress-bg">
  <div class="skill-progress-fill" style="width: 90%"></div>
</div>
```

#### 8. 作品集部分（第707-946行）
```html
<!-- 添加新项目 -->
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

#### 9. 博客部分（第947-1138行）
```html
<!-- 添加博客文章 -->
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
      <p class="blog-text">文章摘要...</p>
    </div>
  </a>
</li>
```

#### 10. 联系表单（第1139-1201行）
```html
<!-- 配置表单功能 -->
<form action="https://formspree.io/f/你的表单ID" method="POST" class="contact-form" data-form>
  <div class="input-wrapper">
    <input type="text" name="name" class="form-input" placeholder="姓名" required data-form-input>
    <input type="email" name="email" class="form-input" placeholder="邮箱地址" required data-form-input>
  </div>
  <textarea name="message" class="form-input" placeholder="你的消息" required data-form-input></textarea>
  <button class="form-btn" type="submit" disabled data-form-btn>
    <ion-icon name="paper-plane"></ion-icon>
    <span>发送消息</span>
  </button>
</form>
```

### 📁 `assets/` 文件夹修改指南

#### 📂 `assets/images/` 文件夹

这个文件夹包含网站的所有图片资源：

##### 个人相关图片
- **`my-avatar.png`** - 你的个人头像（建议尺寸：150x150px）
- **`avatar-1.png` 到 `avatar-4.png`** - 推荐人/客户头像

##### 项目图片
- **`project-1.jpg` 到 `project-9.png`** - 作品集项目图片
  - 建议尺寸：400x300px
  - 格式：JPG或PNG
  - 可以替换为你自己的项目截图

##### 博客图片
- **`blog-1.jpg` 到 `blog-6.jpg`** - 博客文章封面图
  - 建议尺寸：400x250px
  - 可以替换为你的博客文章配图

##### 图标文件
- **`icon-app.svg`** - 应用程序开发图标
- **`icon-design.svg`** - 设计图标
- **`icon-dev.svg`** - 开发图标
- **`icon-photo.svg`** - 摄影图标
- **`icon-quote.svg`** - 引用图标

##### 品牌Logo
- **`logo.ico`** - 网站图标（浏览器标签页显示）
- **`logo.svg`** - SVG格式的Logo
- **`logo-1-color.png` 到 `logo-6-color.png`** - 客户Logo展示

#### 📂 `assets/css/` 文件夹

##### `style.css` 文件修改指南

这是网站的主要样式文件，包含所有CSS样式：

###### 颜色主题修改（第15-80行）
```css
:root {
  /* 主色调 - 修改这些颜色来改变网站主题 */
  --orange-yellow-crayola: hsl(45, 100%, 72%);  /* 主色调 */
  --vegas-gold: hsl(45, 54%, 58%);              /* 次要色调 */
  
  /* 背景色 */
  --eerie-black-1: hsl(240, 2%, 13%);           /* 主背景 */
  --eerie-black-2: hsl(240, 2%, 12%);           /* 次要背景 */
  --smoky-black: hsl(0, 0%, 7%);                /* 页面背景 */
  
  /* 文字颜色 */
  --white-1: hsl(0, 0%, 100%);                  /* 主要文字 */
  --white-2: hsl(0, 0%, 98%);                   /* 次要文字 */
  --light-gray: hsl(0, 0%, 84%);                /* 灰色文字 */
}
```

###### 字体修改（第85-95行）
```css
:root {
  /* 字体设置 */
  --ff-poppins: '你的字体', sans-serif;         /* 主要字体 */
  
  /* 字体大小 */
  --fs-1: 24px;  /* 大标题 */
  --fs-2: 18px;  /* 中标题 */
  --fs-3: 17px;  /* 小标题 */
  --fs-4: 16px;  /* 正文 */
  --fs-5: 15px;  /* 小字 */
  --fs-6: 14px;  /* 更小字 */
}
```

###### 布局修改
- **侧边栏样式**（第317-450行）：修改侧边栏的宽度、高度、背景等
- **主内容区域**（第1320-1350行）：修改内容区域的布局
- **响应式设计**（第1236-1882行）：修改不同屏幕尺寸下的显示效果

#### 📂 `assets/js/` 文件夹

##### `script.js` 文件修改指南

这个文件包含网站的交互功能：

###### 侧边栏功能（第8-12行）
```javascript
// 侧边栏切换功能
const sidebar = document.querySelector("[data-sidebar]");
const sidebarBtn = document.querySelector("[data-sidebar-btn]");
sidebarBtn.addEventListener("click", function () { 
  elementToggleFunc(sidebar); 
});
```

###### 页面导航功能（第140-159行）
```javascript
// 页面导航功能
const navigationLinks = document.querySelectorAll("[data-nav-link]");
const pages = document.querySelectorAll("[data-page]");

// 可以在这里添加自定义的页面切换逻辑
```

###### 表单验证功能（第120-139行）
```javascript
// 联系表单验证
const form = document.querySelector("[data-form]");
const formInputs = document.querySelectorAll("[data-form-input]");
const formBtn = document.querySelector("[data-form-btn]");

// 可以在这里修改表单验证规则
```

###### 作品集筛选功能（第50-100行）
```javascript
// 作品集分类筛选
const filterFunc = function (selectedValue) {
  // 可以在这里添加新的分类
  // 例如：data-category="mobile-app"
}
```

### 🎨 样式自定义详细指南

#### 1. 修改颜色主题
```css
/* 在 style.css 的 :root 部分修改 */
:root {
  /* 蓝色主题 */
  --orange-yellow-crayola: hsl(210, 100%, 70%);
  --vegas-gold: hsl(210, 80%, 60%);
  
  /* 绿色主题 */
  --orange-yellow-crayola: hsl(120, 100%, 70%);
  --vegas-gold: hsl(120, 80%, 60%);
  
  /* 紫色主题 */
  --orange-yellow-crayola: hsl(270, 100%, 70%);
  --vegas-gold: hsl(270, 80%, 60%);
}
```

#### 2. 修改字体
```html
<!-- 在 index.html 的 head 部分修改 -->
<link href="https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;500;600&display=swap" rel="stylesheet">
```

```css
/* 在 style.css 中修改 */
:root {
  --ff-poppins: 'Roboto', sans-serif;
}
```

#### 3. 修改布局
```css
/* 修改侧边栏宽度 */
.sidebar {
  width: 350px; /* 默认是 300px */
}

/* 修改内容区域宽度 */
.main-content {
  width: calc(100% - 350px); /* 对应侧边栏宽度 */
}

/* 修改间距 */
.sidebar, article {
  padding: 20px; /* 默认是 15px */
}
```

### 🔧 高级自定义

#### 1. 添加新的页面部分
```html
<!-- 在 index.html 中添加新的导航项 -->
<li class="navbar-item">
  <button class="navbar-link" data-nav-link>新页面</button>
</li>

<!-- 添加对应的内容区域 -->
<article class="new-page" data-page="new-page">
  <header>
    <h2 class="h2 article-title">新页面标题</h2>
  </header>
  <!-- 你的内容 -->
</article>
```

#### 2. 添加新的交互功能
```javascript
// 在 script.js 中添加新功能
const newFeature = function() {
  // 你的自定义功能
};

// 绑定事件
document.querySelector('.new-button').addEventListener('click', newFeature);
```

#### 3. 添加动画效果
```css
/* 在 style.css 中添加自定义动画 */
@keyframes slideIn {
  from {
    transform: translateX(-100%);
    opacity: 0;
  }
  to {
    transform: translateX(0);
    opacity: 1;
  }
}

.slide-in {
  animation: slideIn 0.5s ease-out;
}
```

---

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
