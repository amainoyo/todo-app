# 📖 User Guide (English)

## Contents
- [Basic Operations](#basic-operations)
- [Advanced Features](#advanced-features)
- [GitHub Cloud Sync](#github-cloud-sync)
- [Pomodoro Timer](#pomodoro-timer)
- [FAQ](#faq)

---

## Basic Operations

### 1️⃣ Add a Task

1. Type the task title in the input field at the top
2. (Optional) Select a due date
3. Choose a category: 💼 Work / 🏠 Life / 📚 Study / 📌 Other
4. Choose a priority: 🔴 High / 🟡 Medium / 🟢 Low
5. Pick a color label (6 options)
6. Click ➕ Add Task

### 2️⃣ Manage Tasks

| Action | How |
|--------|-----|
| Complete | Click the round checkbox on the left |
| Edit | Click ✏️ button |
| Delete | Click 🗑️ button |
| Reorder | Hold and drag |

### 3️⃣ Subtasks

Click **+ Add subtask** below a task to break it into smaller steps. Each subtask can be checked independently.

---

## Advanced Features

### 🔍 Search & Filter

- **Search box**: Real-time title matching
- **Status filter**: All / Pending / Completed / Overdue
- **Category filter**: By Work/Life/Study/Other
- **Priority filter**: By High/Medium/Low

You can combine multiple filter conditions.

### ✅ Batch Operations

1. Check the **"Select"** checkbox on each task
2. Click batch action buttons:
   - ✅ Batch Complete
   - 📁 Batch Move to category
   - 🗑️ Batch Delete

### 📤📥 Import/Export

- **Export**: Click 📤 Export to download a JSON file
- **Import**: Click 📥 Import to load a previously exported JSON
- Filename format: `tasks-2026-06-25.json`

### 📊 Weekly Statistics

The bar chart at the bottom shows tasks completed each day (Sun → Sat). Today is highlighted.

### 🌓 Dark Mode

Click the 🌓 button in the top-right to toggle dark/light theme. The setting is saved automatically.

---

## GitHub Cloud Sync

### 🔑 Create a Personal Access Token

1. Visit https://github.com/settings/tokens
2. Click **Generate new token** → **Generate new token (classic)**
3. Fill in Note (e.g., `todo-app`)
4. **Check the `repo` scope**
5. Click **Generate token**
6. **Copy and save** the token (you won't see it again)

### ⚙️ Configure Sync

1. Click **⚙️** in the top-right corner of the app
2. Fill in:
   - **GitHub Username**: Your GitHub username
   - **Repository**: e.g., `todo-app`
   - **Branch**: Default `main`
   - **File Path**: Default `data/tasks.json`
   - **Personal Access Token**: The token you just created
3. **Check** "Enable GitHub sync"
4. Click **Save**

### 📡 Sync Mechanism

- **First load**: Pulls saved tasks from GitHub
- **On every change**: Auto-pushes to GitHub after 1.5 seconds
- **Fallback**: Local storage is preserved if GitHub fails

### 🔄 Multi-device Usage

Configure with the same token on different devices to automatically sync all tasks.

---

## Pomodoro Timer

### 🍅 Start

1. Click **▶ Start**
2. Timer counts down from 25:00
3. After 25 minutes, an alert sounds and break mode begins
4. After 5 minutes of break, alert sounds again
5. Every 4 completed pomodoros, a small dot lights up at the bottom

### Controls

| Button | Action |
|--------|--------|
| ▶ Start | Begin timer |
| ⏸ Pause | Pause (text changes when running) |
| 🔄 Reset | Reset to 25:00 |

---

## FAQ

### Q: Where is my data stored?
**A**: By default in browser LocalStorage. After enabling GitHub sync, also in your GitHub repo.

### Q: Can I use it on another browser/computer?
**A**:
- Without GitHub sync: No (data is local)
- With GitHub sync: Yes, configure with the same Token

### Q: Is my Token safe?
**A**: The Token is only stored in your browser's LocalStorage. It is never sent to any server except GitHub's API. Don't use it on public computers.

### Q: What if GitHub sync fails?
**A**: A red error appears in the top-right. Check:
1. Token is valid (not expired or revoked)
2. Network is working
3. Repository exists and you have write access

### Q: Is mobile supported?
**A**: Yes! Responsive design works on phones. Both portrait and landscape work.

### Q: Will data conflict between devices?
**A**: Simple "last write wins" model. For collaborative editing, use a more specialized tool.

---

## Keyboard Shortcuts

| Shortcut | Action |
|----------|--------|
| Enter (in input) | Add task |

> More shortcuts can be customized in `~/.claude/keybindings.json`.