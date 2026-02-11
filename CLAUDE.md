# Xufan He Academic Homepage

## 项目概述

这是 **何许凡 (Xufan He)** 的学术主页，基于 Jekyll 构建，部署在 GitHub Pages 上。

- **姓名**: Xufan He (何许凡)
- **身份**: 南京理工大学数学与统计学院硕士研究生
- **导师**: [Dong Du](https://dongdu3.github.io/)
- **研究方向**: 3D Vision, Computer Graphics, Computer Vision

---

## 个人信息配置

### 基本资料

```yaml
# _data/profile.yml
primary_name: "Xufan He"
secondary_name: "何许凡"
navbar_name: "何许凡 | Xufan He"
email: "xfanhe@njust.edu.cn"
```

### 学术链接

- **Google Scholar**: `1h5vT9kAAAAJ`
- **GitHub**: `xfanhe`

### 教育背景

1. **硕士** (2024.9 - present)
   - 南京理工大学数学与统计学院
   - M.S. in Mathematics (Expected)

2. **本科** (2020.9 - 2024.6)
   - 南京理工大学
   - B.S. in Mathematics

### 实习经历

- **ByteDance** (2025年5月 - 至今)
  - Research Intern @ Game AIGC
  - Supervised by Yushuang Wu

---

## 论文发表

### 1. UniPart

- **标题**: UniPart: Part-Level 3D Generation with Unified 3D Geom-Seg Latents
- **作者**: Xufan He*, Yushuang Wu*, Xiaoyang Guo, Chongjie Ye, Jiaqing Zhou, Tianlei Hu, Xiaoguang Han, Dong Du
- **发表**: Preprint 2026
- **链接**: https://arxiv.org/abs/2512.09435
- **文件**: `_publications/2026/2026-unipart.md`
- **图片**: `assets/images/covers/unipart_local.png`
- **项目页面**: `/projects/unipart/` (包含视频演示、3D查看器、结果图库)

### 2. NGR

- **标题**: NGR: Neural Gradient Rendering for
- **作者**: Xufan He, Dong Du, Yushuang Wu, Yunbi Liu
- **发表**: Computational Visual Media (CVM), 2026 (CCF C)
- **链接**: https://arxiv.org/...
- **文件**: `_publications/2026/2026-ngr.md`
- **图片**: `assets/images/covers/ngr_local.png`

---

## 项目结构

```
xfanhe.github.io/
├── _config.yml                 # Jekyll 配置
├── _data/
│   ├── profile.yml            # 个人资料
│   ├── navigation.yml         # 导航菜单
│   └── authors.yml            # 作者信息
├── _includes/                 # HTML 组件
│   └── widgets/              # 页面小组件
├── _layouts/                  # 页面布局
│   ├── default.html
│   └── project.html           # 项目详情页布局（含3D Viewer支持）
├── _news/                     # 新闻动态 (保留目录)
├── _publications/             # 论文发表
│   └── 2026/
│       ├── 2026-unipart.md
│       └── 2026-ngr.md
├── _showcase/                 # 展示内容
├── projects/                   # 项目详情页
│   └── unipart/
│       ├── index.html
│       └── assets/
│           ├── images/          # 项目图片
│           ├── videos/          # 项目视频
│           └── models/          # 3D模型文件 (需自行添加)
├── _site/                     # 构建输出
├── assets/
│   ├── images/
│   │   ├── badges/           # 学校/机构 Logo
│   │   │   ├── njust.png      # 南京理工大学
│   │   │   └── bytedance.png # 字节跳动
│   │   ├── covers/           # 论文封面图
│   │   └── photos/           # 个人照片
│   ├── css/
│   │   └── global.css        # 全局样式
│   └── js/                   # JavaScript
├── CLAUDE.md                 # 本文档
├── index.html                # 主页 (单栏布局)
├── publications.html         # 论文列表页
└── showcase.html             # 展示页
```

---

## 主页布局

使用 **单栏布局**：

- 姓名和个人信息显示在主内容区顶部
- 无侧边栏
- 包含：个人简介、经历、新闻、论文

导航菜单链接：
- Home → `/`
- Publications → `/publications`
- Showcase → `/showcase`

---

## 项目详情页功能

### UniPart 项目页面 (`/projects/unipart/`)

支持多媒体内容展示：

| 内容类型 | 实现方式 |
|---------|---------|
| **图片** | `<img>` 标签，响应式网格布局 |
| **视频** | HTML5 `<video>` 标签，支持自动播放、静音、循环 |
| **3D Mesh Viewer** | Google Model Viewer (Web Components)，支持拖拽旋转、滚轮缩放、右键平移 |

### 页面结构

1. **Hero Section** - 标题、作者信息、Paper/Code/Model 链接
2. **Abstract** - 论文摘要
3. **Video Demo** - 视频演示
4. **Interactive 3D Demo** - 3D 模型交互查看器
5. **Method Overview** - 方法流程图
6. **Interactive Results** - 结果图片网格 (11张结果图)
7. **Applications** - 应用展示
8. **BibTeX** - 引用格式

### 3D 模型添加

将 `.glb` 或 `.gltf` 模型文件放到：

```
projects/unipart/assets/models/model.glb
```

然后在 `projects/unipart/index.html` 中更新 `src` 路径。

---

## 自定义配置

### 添加论文

在 `_publications/年份/` 目录下创建 Markdown 文件：

```yaml
---
title: "论文标题"
date: YYYY-MM-DD
selected: true
pub: "发表会议/期刊"
pub_date: "YYYY"
authors:
  - Xufan He
  - Other Authors
cover: /assets/images/covers/paper_image.png
links:
  Paper: https://arxiv.org/...
  Code: https://github.com/...
  Project: /projects/unipart/  # 添加项目页面入口
---
```

### 添加实习/工作经历

在 `_data/profile.yml` 的 `experience` 部分添加：

```yaml
experience:
- name: 公司名称
  logo: /assets/images/badges/company.png  # 支持Logo
  position: >-
    职位名称 <br/>
    其他说明
  date: 开始时间 - 结束时间
```

### 更新个人简介

编辑 `_data/profile.yml` 中的 `short_bio` 部分。

---

## 样式说明

### 全局样式 (`assets/css/global.css`)

- `.experience-logo` - 经历部分 Logo 样式 (48x48px)
- `.project-title` - 项目页面标题样式 (粗体，较小字号)
- `.project-authors` - 项目页面作者样式
- `.sup-normal` - 普通上标样式
- `.sup-sm` - 小上标样式
- `.institution` - 单位名称样式

### 经历卡片对齐

在 `_includes/widgets/experience_card.html` 中：
- `<li class="media mb-1 align-items-center">` - 添加 Bootstrap 的 `align-items-center` 类
- 确保 Logo 图片和右侧文字块垂直居中对齐

---

## 部署说明

1. 本地预览：
   ```bash
   bundle exec jekyll serve
   ```

2. 提交更改：
   ```bash
   git add .
   git commit -m "Update message"
   ```

3. 推送到 GitHub：
   ```bash
   git push origin main
   ```

---

## 联系信息

- **Email**: xfanhe@njust.edu.cn
- **GitHub**: https://github.com/xfanhe
- **Google Scholar**: https://scholar.google.com/citations?user=1h5vT9kAAAAJ
