# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## 项目概况

- **用途**: Claude Code + Git 协作开发的主项目目录
- **仓库**: https://github.com/PyDev-Cui/Claude-Code
- **远程**: `origin` → GitHub
- **默认分支**: `main`
- **工作目录**: `D:\ClaudeCode\MyProjects` — 所有子项目均在此目录下

## Git 协作流程

- 所有代码变更先经用户审核确认后再提交
- 提交信息用中文或英文均可，保持简洁
- 首次推送新分支时自动设置 upstream
- 推送前确保 `.claude/` 目录被 `.gitignore` 排除

## 技术栈

暂无固定技术栈 — 根据用户每次创建的项目类型灵活选择：

| 项目类型 | 常用工具 |
|---------|---------|
| Python | pip, venv, pytest |
| Node.js | npm, yarn, vitest |
| 前端 | Vite, React, Next.js |
| Go | go mod, go build |

## 目录结构

```
D:\ClaudeCode\MyProjects/
├── CLAUDE.md        ← 本文件，给 Claude Code 的指引
├── README.md        ← 项目说明
├── .gitignore       ← Git 忽略规则
├── .claude/         ← Claude Code 本地配置（已忽略 git）
└── <项目文件>       ← 后续创建的项目代码
```

## 工作方式

1. 用户提出需求 → Claude 设计实现方案
2. Claude 编写/修改代码
3. 用户审核变更，确认无误
4. Claude 执行 `git add` / `git commit` / `git push`

## Git 命令速查

```powershell
# 查看状态
git status
git diff

# 提交
git add -A && git commit -m "feat: 描述变更"
git push

# 分支
git checkout -b feature-xxx
git branch -d feature-xxx
```
