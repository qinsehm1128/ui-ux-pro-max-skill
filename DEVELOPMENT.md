# UI UX Pro Max 开发与使用指南

本指南旨在帮助开发者了解如何开发、调试以及在不同项目中使用 **UI UX Pro Max** 技能包。

## 🚀 快速开始

### 1. 环境准备
- **Bun**: 项目核心包管理器和运行时。
- **Python (uv)**: 技能包内部的搜索脚本依赖 `uv` 运行。
- **Node.js**: 部分 CLI 功能的兼容性支持。

### 2. 依赖安装
在项目根目录下运行：
```bash
bun install
```

---

## 🛠️ 开发与调试

### 1. CLI 开发
CLI 源代码位于 `cli/` 目录下。

- **进入目录**: `cd cli`
- **本地运行**: `bun run src/index.ts --help`
- **构建项目**: `bun run build` (输出到 `dist/` 目录)
- **链接本地命令**: 
  ```bash
  bun link
  ```
  执行后，你可以在系统任何地方直接使用 `uipro` 命令，且修改代码后立即生效。

### 2. 技能数据开发
技能核心数据存储在以下位置：
- [data/](file:///d:/bunProject/ui-ux-pro-max-skill/.shared/ui-ux-pro-max/data/): 包含 CSV 格式的 UI 样式、颜色、字体等数据库。
- [scripts/](file:///d:/bunProject/ui-ux-pro-max-skill/.shared/ui-ux-pro-max/scripts/): 包含 Python 搜索脚本。

如果你添加了新的 UI 风格或技术栈，请确保同步更新 `cli/assets` 目录下的副本。

---

## 📦 如何在其他项目中使用

### 方法 A：全局安装（最简便）
将本地开发的 CLI 安装到全局：
```bash
cd cli
bun install -g .
```
然后在你的目标项目目录运行：
```bash
uipro init --ai cursor
```

### 方法 B：手动集成
如果不想使用 CLI，可以直接复制对应文件夹：
- **Cursor**: 复制 `.cursor/` 和 `.shared/` 到目标项目根目录。
- **Claude**: 复制 `.claude/` 到目标项目根目录。

---

## 📝 常用命令手册

| 命令 | 说明 |
| :--- | :--- |
| `uipro init --ai all` | 为当前项目安装所有支持的 AI 助手配置 |
| `uipro versions` | 查看当前可用的版本列表 |
| `uipro update` | 更新到最新版本 |
| `bun run build` | (在 cli 目录下) 编译 TypeScript 代码 |

---

## ⚠️ 常见问题

1. **`uipro` 命令冲突？**
   如果之前安装过官方版本，请先卸载：`npm uninstall -g uipro-cli`。
2. **搜索脚本报错？**
   请确保 `uv` 已正确安装并配置在环境变量中。
3. **AI 助手不响应？**
   确保 `.shared/ui-ux-pro-max` 文件夹存在，且对应的 `.md` 指令文件路径正确。
