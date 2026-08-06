![数学建模论文写作封面](assets/math-modeling-cover.png)

# math-modeling-writing

国赛数学建模写作技能：按全国大学生数学建模竞赛中文论文风格，分章节撰写论文草稿的 Codex 技能。

## 功能一览

- 读取题目文本、Python 代码与运行结果，按《国赛写作指南》生成 Markdown 章节草稿
- 覆盖 8 个章节：摘要、问题重述、模型假设、符号说明、模型建立与求解、模型评价、参考文献、附录
- 模型建立与求解采用逐问一级标题与定制化三级标题，每问含稳健性分析与结论
- 内置“评委视角”自检清单，摘要强制反 AI 自检
- 内置排版规范：Word 样式独立、1.5 倍行距、三线表、图表引用规则
- 内置阶段二 md2word：Markdown 无损转国赛 Word（.docx，WPS 可打开），公式转原生 OMML、三线表、公式居中右编号，附无损校验与 vision 渲染复核

## 安装

将本目录复制到 `~/.codex/skills/math-modeling-writing`，或使用 Codex 的 skill-installer 安装。

## 使用示例

- “帮我写这篇数学建模论文的摘要”
- “按赛题结构写问题分析与模型建立与求解”
- “用 math-modeling-writing 生成整篇论文草稿”

## 目录结构

- `SKILL.md`：路由与硬性规则
- `references/guoshi-writing-guide.md`：国赛写作指南底稿
- `references/typography.md`：排版规范
- `references/sections/`：8 个章节模块
- `phase2-md2word/`：Markdown → Word 转换与验证脚本（依赖引导见其 SKILL.md）

## 说明

输出为 Markdown 草稿，Word / LaTeX 排版按 `typography.md` 执行；正文中的数字均与运行结果文件核对，不编造。需要 Word 成品时，用 `phase2-md2word` 一键转换并复核（转换→无损校验→渲染 vision QA→WPS 打开复核）。
