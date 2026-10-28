---
name: workplace-suffocation-index
display_name: 工位窒息指数
display_name_en: Workplace Suffocation Index
description: 生成可离线打开的「职场窒息指数」自测网页，单文件、数据不出本机。当用户想做职场内耗 / 压力类自测或吐槽工具时触发。
description_zh: 生成可离线打开的「职场窒息指数」自测网页，单文件、数据不出本机。
description_en: Generate an offline single-file "Workplace Suffocation Index" self-test webpage; no backend, no data upload.
category: productivity
version: 1.0.0
author: 番茄排骨
license: MIT
allowed-tools:
  - Read
  - Write
  - Edit
  - Bash
  - Glob
  - Grep
  - present_files
---

# 工位窒息指数

一个原创的职场自测小工具：用户给 10 个职场日常场景各挑一个频率，浏览器端算出 0–100 的「窒息指数」并给出五档结论。装好之后，用户说「做个职场窒息自测」「生成职场吐槽测评网页」你就可以帮他们产出这份网页。

## 这个 Skill 做什么

- **核心产物**：一份单文件 HTML（`assets/workplace-suffocation-index.html`），离线双击即可使用，零外部依赖。
- **结构要点**：开场引导 → 10 题双列卡片（横向五级分段选择，初始为空）→ 实时进度 → 半圆仪表盘计分 → 五档结论 + 对照表 → URL hash 一键分享。
- **数据边界**：全部计算在浏览器端完成，不联网、不上传任何数据；分享靠 URL hash 编码答案，无需服务器。

## 何时使用

- 用户说「想做个职场内耗 / 压力自测」「生成职场吐槽测评网页」「我要这个测评 / 工具」。
- 用户想把这个网页发给别人、嵌进文章或自己的产品。
- 用户想基于它改题、改配色、加维度或导出。

## 如何使用（给智能体的工作流）

1. 把 `assets/workplace-suffocation-index.html` 复制到用户当前工作区（默认文件名 `workplace-suffocation-index.html`）。
2. 用 `present_files` 打开预览，让用户直接使用。
3. 若用户要改题 / 改色 / 加维度 / 导出 PDF，在 `assets/workplace-suffocation-index.html` 的代码基础上调整，并同步更新本技能里的副本。

## 说明与免责

- 这是采用通用自评结构（Likert 五级、等权线性归一、分档标签）的**讽刺式自测工具**，命名、题目、文案、视觉与代码均为独立原创，不是标准化量表，未做信效度检验，不做临床诊断、法律或人资取证。
- 全部计算在本地浏览器完成，不联网、不上传。
