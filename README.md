# math-modeling-writing

国赛数学建模写作技能：按全国大学生数学建模竞赛（CUMCM）中文论文风格，分章节撰写论文草稿的 Codex 技能。

## 功能

读取题目文本、Python 代码与运行结果，按《国赛写作指南》生成 Markdown 章节草稿，覆盖：

- 摘要
- 问题重述（含 1.3 我们的工作）
- 模型假设
- 符号说明
- 模型的建立与求解（逐问一级标题 + 定制化三级标题，每问含稳健性分析与结论）
- 模型评价（模型的优点 / 模型的缺点）
- 参考文献（GB/T 7714-2015）
- 附录

## 安装

将本目录复制到 `~/.codex/skills/math-modeling-writing`，或使用 Codex 的 skill-installer 安装。

## 使用

在 Codex 中直接请求，例如：

- “帮我写这篇数学建模论文的摘要”
- “按赛题结构写问题分析与模型建立与求解”
- “用 math-modeling-writing 生成整篇论文草稿”

技能会自动路由到 `references/sections/` 下对应模块，并按模块自检清单校验输出。

## 结构

- `SKILL.md`：路由表与硬性规则
- `references/guoshi-writing-guide.md`：国赛写作指南底稿
- `references/typography.md`：排版规范（Word 样式独立、1.5 倍行距、三线表、图表引用）
- `references/sections/`：8 个章节模块

## 说明

输出为 Markdown 草稿；Word / LaTeX 排版按 `references/typography.md` 执行。
