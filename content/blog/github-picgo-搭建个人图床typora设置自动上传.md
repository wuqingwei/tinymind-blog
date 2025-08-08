---
title: github picgo 搭建个人图床，typora设置自动上传
date: 2025-08-08T03:28:44.387Z
---

## 1. 准备工作

- **拥有 GitHub 账号**：如果没有，请先注册。
- **安装 PicGo**：从 [PicGo GitHub Releases](https://github.com/Molunerfinn/picgo/releases) 下载并安装适合你操作系统的版本


## 2. 创建 GitHub 图床仓库

1. **登录 GitHub**，点击右上角的 “+” 按钮，选择 “New repository”。
2. **设置仓库名**（如 `images`），选择公开（Public），创建仓库。
3. **记下仓库名**（格式为 `username/reponame`）

![image-20250702091512024](https://raw.githubusercontent.com/wuqingwei/image/main/img/image-20250702091512024.png)

## 3. 生成 GitHub Token

1. **进入 GitHub 个人设置**：点击右上角头像 → Settings。
2. **找到 Developer settings** → Personal access tokens → Tokens (classic)。
3. **生成新 Token**：勾选 `repo` 权限，设置有效期（建议非永久），生成并复制 Token（只显示一次，请妥善保存）

## 4. 配置 PicGo

1. **打开 PicGo**，进入图床设置，选择 “GitHub”。

2. **填写配置信息**：

    - **仓库名**：`username/reponame`
    - **分支名**：一般为 `main` 或 `master`
    - **Token**：粘贴刚才生成的 Token
    - **存储路径**：可自定义，如 `img/`
    - **自定义域名**（可选）：如 `https://raw.githubusercontent.com/username/reponame/main`，或使用 CDN 加速（如 `https://cdn.jsdelivr.net/gh/username/reponame`）

3. **设为默认图床**，保存配置。

 ![image-20250702101611771](https://raw.githubusercontent.com/wuqingwei/image/main/img/image-20250702101611771.png)

![image-20250702091228725](https://raw.githubusercontent.com/wuqingwei/image/main/img/image-20250702091228725.png)

![image-20250702091254210](https://raw.githubusercontent.com/wuqingwei/image/main/img/image-20250702091254210.png)

## 5. 上传图片

- **拖拽图片到 PicGo 窗口**，或点击“点击上传”按钮。
- **上传成功后**，PicGo 会自动复制图片链接到剪贴板，可直接粘贴到 Markdown 或网页中使用。
- typora设置：
- ![image-20250701183549534](https://raw.githubusercontent.com/wuqingwei/image/main/img/image-20250701183549534.png)

## 6. 访问图片

- **直接访问 GitHub 仓库**，可查看和管理上传的图片。
- **通过图片链接**（如 `https://raw.githubusercontent.com/username/reponame/main/img/example.jpg`）访问图片。


## 注意事项

- **Token 安全**：Token 只显示一次，务必妥善保存。
- **图片加载速度**：GitHub 图床免费稳定，但加载速度可能不如专业 CDN，大量访问或对速度要求高时可考虑 CDN 加速。
- **存储空间**：GitHub 免费仓库有空间，适合中小规模使用。