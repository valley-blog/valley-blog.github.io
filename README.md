# 分享 Blog

基于 **Jekyll + GitHub Pages** 的极简博客框架：支持分页、标签页、RSS、SEO、站点地图、深色风格。

## 使用方法

1. 新建公开仓库（个人主页：`<username>.github.io` 或项目仓库任意名称）。  
2. 上传本项目所有文件到仓库根目录。  
3. 在仓库 **Settings → Pages**：
   - Build and deployment: `Deploy from a branch`
   - Branch: `main` / `/root`
4. 访问：
   - 个人主页：`https://<username>.github.io`
   - 项目页：`https://<username>.github.io/<repo>`（需在 `_config.yml` 设置 `baseurl: "/<repo>"`）

## 写作

在 `_posts/` 新增文件：`YYYY-MM-DD-标题.md`，首部：
```yaml
---
layout: post
title: 一篇新文章
tags: [分享, 随笔]
---
```

## 自定义
- `_config.yml`：站点标题、导航、分页等
- `assets/css/main.css`：样式
- `_layouts/` 与 `_includes/`：布局/组件
- `tags.md`：标签页

## 可选
- `CNAME`：自定义域名
- `images/`：文章图片资源
