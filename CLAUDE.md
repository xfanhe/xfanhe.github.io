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
- **文件**: `_publications/2025/2025-unipart.md`
- **图片**: `assets/images/covers/unipart_local.png`

### 2. NGR

- **标题**: NGR: Neural Gradient Rendering for High-Quality 3D Reconstruction from Multi-View Images
- **作者**: Xufan He, Dong Du, Yushuang Wu, Yunbi Liu
- **发表**: Computational Visual Media (CVM), 2026 (CCF C)
- **文件**: `_publications/2025/2025-ngr.md`
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
├── _layouts/                  # 页面布局
├── _news/                     # 新闻动态 (已清理)
├── _publications/             # 论文发表
│   └── 2025/
│       ├── 2025-unipart.md
│       └── 2025-ngr.md
├── _showcase/                 # 展示内容 (已清理)
├── _site/                     # 构建输出
├── assets/
│   ├── images/
│   │   ├── badges/           # 学校/机构 Logo
│   │   ├── covers/           # 论文封面图
│   │   │   ├── unipart_local.png
│   │   │   └── ngr_local.png
│   │   └── photos/           # 个人照片
│   └── js/                   # JavaScript
├── CLAUDE.md                 # 本文档
├── index.html                # 主页 (单栏布局)
├── publications.html         # 论文列表页
└── showcase.html             # 展示页
```

---

## 主页布局

使用 **单栏布局** (原 index_layout2 风格)：

- 姓名和个人信息显示在主内容区顶部
- 无侧边栏
- 包含：个人简介、经历、新闻、论文

导航菜单链接：
- Home → `/`
- Publications → `/publications`
- Showcase → `/showcase`

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
---
```

### 添加实习/工作经历

在 `_data/profile.yml` 的 `experience` 部分添加：

```yaml
experience:
- name: 公司名称
  position: >-
    职位名称 <br/>
    其他说明
  date: 开始时间 - 结束时间
```

### 更新个人简介

编辑 `_data/profile.yml` 中的 `short_bio` 部分。

---

## 部署说明

1. 本地预览：
   ```bash
   bundle exec jekyll serve
   ```

2. 推送到 GitHub 自动部署：
   ```bash
   git add .
   git commit -m "Update homepage"
   git push origin main
   ```

---

## 联系信息

- **Email**: xfanhe@njust.edu.cn
- **GitHub**: https://github.com/xfanhe
- **Google Scholar**: https://scholar.google.com/citations?user=1h5vT9kAAAAJ
