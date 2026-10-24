# TommyDeng.github.io

个人主页 —— 农夫、艺术家。

线上地址：<https://tommydeng.github.io/>

页面按 [Figma 设计稿](https://www.figma.com/design/bAIa44M92xtMQ1anqY5eAq/Untitled) 实现，桌面（1440px）与移动（390px）两档均按设计稿逐项校对过几何尺寸与配色。

## 技术栈

不依赖任何框架与构建工具，纯静态单页：

- `index.html` —— 全部结构 + 内嵌 CSS（单文件，约 13 KB）
- `assets/` —— 从 Figma 导出的 SVG 图标与手绘插画
- 字体走 Google Fonts：**Lora**（拉丁展示）、**Noto Serif SC**（中文标题）、**Noto Sans SC**（正文 / UI）

## 目录结构

```
.
├── index.html            # 页面本体（结构 + 内嵌样式）
├── assets/
│   ├── avatar.jpg        # 简介区手绘插画
│   ├── sprout.svg        # 导航 logo 与页脚
│   ├── utensils.svg      # 「每日菜谱」徽标
│   ├── sparkles.svg      # 「Nova AI」徽标
│   ├── globe.svg         # 访问网站图标
│   ├── github.svg        # 仓库链接图标
│   ├── github-contact.svg
│   ├── mail.svg
│   ├── arrow-up-right.svg
│   └── status-dot.svg
└── README.md
```

## 本地预览

直接双击 `index.html` 即可，或起一个静态服务器（字体与资源都用相对路径，无需配置）：

```bash
python3 -m http.server 8000
# 打开 http://localhost:8000
```

## 设计规范

集中定义在 `index.html` 的 `:root` 里，改这里即可整体换肤：

| 变量 | 值 | 用途 |
| --- | --- | --- |
| `--bg` | `#f7f5ed` | 页面底色 |
| `--card` | `#fcfbf6` | 卡片底色 |
| `--line` | `#dadfd0` | 描边与分隔线 |
| `--ink` | `#293b2e` | 主文字 |
| `--leaf` | `#4d6942` | 强调色 / 状态 / 链接 |
| `--muted` | `#727a6c` | 次要文字 |
| `--emblem` | `#ecf0e3` | 徽标与联系区块底色 |

版心宽度 `min(1040px, 100% - 48px)`，断点为 `max-width: 899px`（单列布局）。

## 响应式

| | 桌面 | 移动 |
| --- | --- | --- |
| 版心 | 1040px（左右留白 200px @1440） | 100% − 52px |
| 导航栏高 | 104px | 80px |
| 姓名 | 60px | 42px |
| 项目栅格 | 两列，间距 26px | 单列，间距 20px |

## 部署

仓库根目录即发布目录，推送到 `main` 后 GitHub Pages 会自动构建：

```bash
git add -A
git commit -m "update"
git push origin main
```

构建状态：`gh api repos/TommyDeng/TommyDeng.github.io/pages --jq .status`

## 当前项目

- **每日菜谱** —— 家庭共用的菜谱与「今天吃什么」小工具 · 已上线，持续维护
  <https://menu.tommydeng.org/>
- **Nova AI** —— 一个极简的自托管 LLM 聊天前端 · 已上线
  <https://ai.tommydeng.org/>

## 联系

- Email：<reget@sohu.com>
- GitHub：<https://github.com/TommyDeng>
