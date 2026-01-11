# UI UX Pro Max

这是一个为 AI 编程助手（如 Claude Code, Codex, Cursor, Windsurf 等）提供专业 UI/UX 设计智能的 AI 技能包。它能跨多个平台和框架，辅助你构建高水准的用户界面。

<p align="center">
  <img src="screenshots/website.png" alt="UI UX Pro Max" width="800">
</p>

## 📖 项目概述

UI UX Pro Max 是一个可搜索的 UI 设计数据库，涵盖了 UI 风格、配色方案、字体搭配、图表类型、产品推荐、UX 指南以及特定技术栈的最佳实践。它通过技能（Skill）或工作流（Workflow）的形式集成到 AI 助手。

## ✨ 核心特性

- **57 种 UI 风格** - 包含玻璃拟态 (Glassmorphism)、黏土拟态 (Claymorphism)、极简主义、粗犷主义、新拟态 (Neumorphism)、Bento Grid、暗黑模式等。
- **95 套配色方案** - 针对 SaaS、电商、医疗、金融、美容等行业量身定制。
- **56 组字体搭配** - 精选 Google Fonts 字体组合及导入代码。
- **24 种图表类型** - 为仪表盘和数据分析提供专业建议。
- **10 大技术栈** - 支持 React, Next.js, Vue, Nuxt.js, Nuxt UI, Svelte, SwiftUI, React Native, Flutter, HTML+Tailwind。
- **98 条 UX 指南** - 包含最佳实践、反模式（Anti-patterns）和无障碍访问（Accessibility）规则。

## 📖 文档指南

关于开发、调试和高级使用的详细信息，请参阅 [开发与使用指南 (DEVELOPMENT.md)](DEVELOPMENT.md)。

## 🚀 安装指南

### 使用 CLI 安装（推荐）

```bash
# 全局安装 CLI 工具
npm install -g uipro-cli

# 进入你的项目目录
cd /path/to/your/project

# 为你的 AI 助手初始化
uipro init --ai claude      # Claude Code
uipro init --ai cursor      # Cursor
uipro init --ai windsurf    # Windsurf
uipro init --ai antigravity # Antigravity (.agent + .shared)
uipro init --ai copilot     # GitHub Copilot
uipro init --ai kiro        # Kiro
uipro init --ai codex       # Codex (Skills)
uipro init --ai gemini      # Gemini CLI
uipro init --ai all         # 安装到所有支持的助手
```

### 其他常用命令

```bash
uipro versions              # 列出可用版本
uipro update                # 更新到最新版本
uipro init --version v1.0.0 # 安装特定版本
```

### 手动安装

将对应的文件夹复制到你的项目根目录：

| AI 助手 | 需要复制的文件夹 |
| -------------- | ------------------------------------------------------------------- |
| Claude Code    | `.claude/skills/ui-ux-pro-max/`                                     |
| Cursor         | `.cursor/commands/ui-ux-pro-max.md` + `.shared/ui-ux-pro-max/`      |
| Windsurf       | `.windsurf/workflows/ui-ux-pro-max.md` + `.shared/ui-ux-pro-max/`   |
| GitHub Copilot | `.github/prompts/ui-ux-pro-max.prompt.md` + `.shared/ui-ux-pro-max/`|
| Codex          | `.codex/skills/ui-ux-pro-max/`                                     |

## 🛠️ 前置要求

运行搜索脚本需要安装 `uv` (Python 包管理工具)。

```bash
# 检查是否已安装 uv
uv --version

# Windows 安装命令
powershell -c "irm https://astral.sh/uv/install.ps1 | iex"
```

## 💡 使用方法

### 在对话中调用
安装完成后，你可以像平常一样与 AI 聊天，或者使用斜杠命令（取决于你的助手）：

- **Claude / Gemini**: 直接要求 AI “构建一个 SaaS 落地页”，技能会自动激活。
- **Cursor / Windsurf**: 使用 `/ui-ux-pro-max 构建一个 SaaS 落地页`。
- **Copilot**: 在聊天框输入 `/` 并选择 `ui-ux-pro-max`。

## 🙏 致谢

本项目灵感及部分基础架构源自以下优秀项目，在此深表谢意：

- **[nextlevelbuilder/ui-ux-pro-max-skill](https://github.com/nextlevelbuilder/ui-ux-pro-max-skill)** - 提供了核心的 UI/UX 数据库和多平台集成的最初构想。

## 📜 开源协议

本项目采用 [MIT License](LICENSE) 开源协议。
