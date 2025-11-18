---
title: nav
---

# nav — 项目概览

**概述**: 本仓库是作者的个人网址导航页面（基于 VitePress），用于整理常用站点与在线工具。

**主要用途**: 作为静态文档站点（导航页），通过 `vitepress` 渲染 `docs` 目录下内容。

**主要文件/目录**:

- `docs/index.md`: 站点首页（包含 `MNav` 的引用）。
- `docs/nav/MNav.vue`: 首页导航组件，负责最近使用记录与渲染 `NAV_DATA`。
- `docs/nav/data.ts`: 导航项数据源（`NAV_DATA`）。
- `docs/.vitepress/theme/`: 自定义主题与组件目录（包含 `MLayout.vue`, `MNavLinks.vue`, `MNavLink.vue`, `MNavVisitor.vue`, `MDocFooter.vue` 等）。
- `package.json`: 启动/构建脚本与项目信息。

**已发现的未使用或暂时未启用的组件**:

- `docs/.vitepress/theme/unused/MAsideSponsors.vue`: 原位于 `components/`，已移动到本 `unused/` 目录以表示当前未启用。
  - 说明: 该组件已移至 `unused/`（保留以便将来启用），若希望彻底删除请回复“删除组件”。

**已删除的资源**:

- `docs/public/sponsor/` 下的赞助图片已按你的要求从仓库中删除（`wechat*.jpg|webp` 与 `alipay*.jpg|webp`）。
  - 说明: 这些图片只在赞助组件中被引用，且该组件已移入 `unused/`。如需恢复，请从版本控制回退或我可以帮你恢复到 `unused/` 下的备份位置。

（经仓库内引用检查，`MNavLinks` / `MNavLink` / `MNavVisitor` / `MDocFooter` / `MLayout` 都有被使用或通过主题注册。）

**如何本地调试/运行**:
（默认使用 `pnpm`，脚本见 `package.json`）

在 Windows `cmd.exe` 中运行：

```bat
pnpm install
pnpm dev
```

构建静态站点：

```bat
pnpm run build
```

开发脚本说明（摘自 `package.json`）:

- `dev`: `cross-env NODE_ENV=development vitepress dev docs --port=8732`
- `build` / `build:docs`: `vitepress build docs`

**建议与下一步**:

- 若目标是减小仓库体积，可删除该文件或保留在 `docs/.vitepress/theme/unused/` 以便未来恢复。
- 若希望保持“禁用但保留”策略，可在 `MLayout.vue` 的注释中加入更明确的使用说明（什么时候启用、依赖项）。
- 我可以：
  - 自动移除/移动未使用组件到 `docs/.vitepress/theme/unused/`（需你确认）；
  - 运行 `pnpm dev` 并截图（需要你允许我运行命令或由你在本机运行）。

生成时间: 2025-11-18

作者: 自动分析脚本（由你进一步确认）
