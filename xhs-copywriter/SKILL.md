---
name: xhs-copywriter
description: 小红书选题与文案的运营方法论库。给写小红书的 Agent 提供「选题→文案」全流程技巧：涨粉与爆品方法、标题公式、正文结构、封面文字、流量与SEO机制、让文案像真人写（去 AI 味）、以及写时规避违规。本 skill 只给方法，不定义人设/语气，与 Agent 系统提示词冲突时一律以 Agent 为准。触发词：小红书选题、写小红书文案、爆款文案、涨粉、标题怎么起、正文结构、封面文案、笔记没人看、像AI写的、去AI味、违禁词、会不会限流、运营技巧、起号、关键词布局。
metadata:
  revision: "2026-11-12"
  type: methodology
---

# 小红书选题与文案方法论

这是一套**方法**，不是人设，不是生成模板。Agent 自带系统提示词（人设、语气、品牌口径、写作风格）；本 skill 只在「怎么选题、怎么写成爆款、怎么写得不像 AI、怎么不踩违规」上提供可执行技巧。

## 最高优先级原则（先看这条）

1. **与 Agent 系统提示词冲突时，一律以 Agent 系统提示词为准。** 本 skill 的任何建议，遇到 Agent 已规定的人设/语气/口吻/口头禅/品牌事实/平台规则时让位。本 skill 不覆盖、不与之争。
2. 本 skill **不替 Agent 写人设、不指定语气风格**——这些是 Agent 的事。本 skill 只负责运营与文案的"方法层"。

## 工作流：先选题，再文案（对应现有程序流程）

| 阶段 | 做什么 | 调用 |
|---|---|---|
| 一 · 选题 | 定赛道与人群 → 找选题（对标拆解 / 信息差 / 情绪钩子 / 搜索需求）→ 产出一条可写选题（含标题方向、关键词、封面方向） | `references/topic.md` |
| 二 · 文案 | 按选题写：标题 + 正文结构 + 钩子 + 结尾 + 封面文字 + 关键词布局 | `references/viral-copy.md` |
| 二 · 文案（并行约束） | 边写边"像真人"（去 AI 指纹的写作技巧） | `references/humanize.md` |
| 二 · 文案（并行约束） | 边写边避违规（高频红线与替换法） | `references/compliance.md` |
| 三 · 自查 | 成稿后按清单核对（不依赖外部 skill；发布级审核可选 `xiaohongshu-publish-review`） | `references/checklist.md` |

> 写文案时，`viral-copy / humanize / compliance` 三份**同时生效**：结构按 viral-copy，语感按 humanize，红线按 compliance。三者优先级都低于 Agent 系统提示词。

## 路由（按需读，别一次全读）

- 不知道写什么 / 想涨粉起号 / 拆解对标 → `topic.md`
- 标题不会起、正文没结构、要涨粉与搜索流量 → `viral-copy.md`
- 文案太"AI 味"、太书面、太工整、像广告 → `humanize.md`
- 怕违禁、怕限流、不确定能不能写某句 → `compliance.md`
- 写完要检查 → `checklist.md`

## 与现有 skill 的关系

- **自包含**：装上本 skill，选题/写作/去AI味/防违规四件事的方法都在这儿，不必再分散装 humanizer-zh、写作技巧等多个 skill。
- **可衔接不依赖**：需要带官方规则基线、逐条分级、图片审核的**发布前正式审核**时，可选再调 `xiaohongshu-publish-review`；日常写时避违规，本 skill 的 `compliance.md` 已够。
- 与项目品牌资料冲突时以项目资料为准（即 Agent 侧），合规判断取更严一档。
