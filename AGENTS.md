# AGENTS.md

## 📌 项目背景与权威数据源规则 (Single Source of Truth)

本仓库 (`kevinxft/kevinxft`) 为 GitHub Profile 个人主页与作品展示仓库。

### 1. 作品网址与内容数据源
所有应用、浏览器扩展、小程序与鸿蒙软件的**名称、官网链接、App Store / Chrome Web Store 地址、Homebrew Cask 命令、描述与图标资源**，必须以本地官网项目为唯一事实来源：

- **官方项目路径**: `/Users/kevin/Developer/Code/LanrenwenStudio/homebrew-apps/` (仓库: `LanrenwenStudio/homebrew-apps`)
- **核心数据文件**:
  - `src/data/apps.js` (所有作品的 ID、官网 URL、商店链接、Homebrew 指令、平台标签)
  - `src/data/translations.js` (所有作品的中英文名称与官方介绍)
  - `SHOWCASE_LOCK.md` (当前固定展示的作品清单)
- **官网主站**: `https://lanrenwen.com/`

### 2. 维护规则
- **严禁臆测链接**：后续更新 `README.md` 或展示内容时，必须优先读取 `homebrew-apps/src/data/apps.js` 获取真实可用的最新链接。
- **图标资源同步**：若新增或替换 App 图标，从 `homebrew-apps/assets/` 同步至本仓库的 `assets/profile-apps/` 目录。
- **品牌与域名规范**：
  - 展示站点固定为 `https://lanrenwen.com/`。
  - 各应用独立官网均挂载于 `lanrenwen.com` 二级域名（如 `https://keylaunch.lanrenwen.com`）或独立域名（如 `https://englishcc.com/`），以 `apps.js` 中的 `website` 字段为准。
