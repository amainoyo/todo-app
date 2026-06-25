# 📋 办理事项管理器 / Todo Manager

一个功能强大的纯前端任务管理工具，支持本地存储和 GitHub 云同步。

A powerful pure-frontend task management tool with local storage and GitHub cloud sync.

## ✨ 核心功能 / Features

| 功能 / Feature | 说明 / Description |
|---|---|
| ➕ 添加/编辑/删除 | 完整的 CRUD 操作 / Full CRUD operations |
| 🎨 颜色标签 | 6 种自定义颜色 / 6 custom colors |
| 📁 分类管理 | 工作/生活/学习/其他 / Work/Life/Study/Other |
| 🔴 优先级 | 高/中/低 / High/Medium/Low |
| 📅 截止日期 | 支持精确到分钟 / Precise to minute |
| ⏰ 过期提醒 | 自动标红 / Auto marked red |
| 🔍 多条件筛选 | 状态/分类/优先级 / Status/Category/Priority |
| 🔎 全文搜索 | 实时模糊匹配 / Real-time fuzzy match |
| 🖱️ 拖拽排序 | 手动调整顺序 / Manual reordering |
| ✅ 批量操作 | 完成/移动/删除 / Complete/Move/Delete |
| 📝 子任务 | 任务拆解 / Task breakdown |
| 🍅 番茄钟 | 25分钟工作 + 5分钟休息 / 25min work + 5min break |
| 📊 周报统计 | 7天完成柱状图 / 7-day completion chart |
| 📤 导入/导出 | JSON 格式 / JSON format |
| 🌙 深色模式 | 护眼 / Eye-friendly |
| 📱 移动适配 | 响应式设计 / Responsive design |
| ☁️ GitHub 同步 | 多设备同步 / Multi-device sync |

## 🚀 快速开始 / Quick Start

### 部署到 GitHub Pages / Deploy to GitHub Pages

```bash
git init
git add index.html
git commit -m "feat: init todo app"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/todo-app.git
git push -u origin main
```

然后在仓库 `Settings` → `Pages` 中启用 Pages（选择 main 分支）。

Then enable Pages in repo `Settings` → `Pages` (select main branch).

### 本地运行 / Local Run

直接用浏览器打开 `index.html`，或使用任意静态服务器：

Open `index.html` directly in browser, or use any static server:

```bash
# Python
python -m http.server 8000

# Node.js
npx serve
```

## 🔧 技术栈 / Tech Stack

- 纯 HTML/CSS/JavaScript（无依赖）
- GitHub Contents API（云同步）
- LocalStorage（本地缓存）
- 响应式设计（移动端友好）

Pure HTML/CSS/JavaScript (no dependencies).
GitHub Contents API for cloud sync.
LocalStorage for local cache.
Responsive design (mobile-friendly).

## 📂 项目结构 / Project Structure

```
todo-app/
├── index.html          # 主程序 / Main app
├── README.md           # 本文件 / This file
└── 使用指南.md          # 中文使用指南 / Chinese user guide
```

## ⚙️ GitHub 同步配置 / GitHub Sync Configuration

### 步骤 / Steps

1. **创建 Personal Access Token**：https://github.com/settings/tokens
   **Create a PAT** at https://github.com/settings/tokens
   - 勾选 `repo` 权限 / Select `repo` scope
   - 建议设置 90 天过期 / Set 90-day expiration

2. **在应用 ⚙️ 中配置** / **Configure in the app ⚙️**：
   - 填写 GitHub 用户名 / Username
   - 填写**数据仓库名**（如 `todo-data`，用于存储任务）
     Enter **data repository name** (e.g., `todo-data`)
   - 填写 Personal Access Token
   - 点击 **+ 创建** 按钮自动创建私有仓库
     Click **+ Create** to auto-create the private repository
   - 勾选"启用 GitHub 同步" / Enable GitHub sync

### 🔒 隐私架构 / Privacy Architecture

应用代码（公开）+ 任务数据（私有）分离：

App code (public) + Task data (private) are separated:

```
your-username/todo-app (public)        ← 应用代码 / App code
└── index.html

your-username/todo-data (private)     ← 任务数据 / Task data  
└── data/tasks.json
```

这样其他用户可以访问站点，但**看不到你的任务**。

Other users can visit the site but **cannot see your tasks**.

## 🔒 安全提示 / Security Notice

- Personal Access Token 仅存储在浏览器 localStorage 中
  PAT is only stored in browser localStorage
- 任何人访问你的电脑 + 此网站都能读取数据
  Anyone with access to your computer + this site can read the data
- 建议定期轮换 Token
  Recommend rotating Token regularly
- 强烈建议使用**专用 Token**（仅本应用，限定 90 天）
  Strongly recommend using a **dedicated Token** (only for this app, 90-day limit)

## 📜 License

MIT License

## 🤝 贡献 / Contributing

欢迎提交 Issue 和 Pull Request。
Issues and Pull Requests are welcome.