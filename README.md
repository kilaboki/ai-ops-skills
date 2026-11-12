# ai-ops-skills — 小红书 AI 运营方法论 Skill 集

两个**通用、不绑定品牌、不绑定模型**的 Agent Skill（SKILL.md + references），用于让 AI 写小红书内容时遵循可落地的方法论。适用于 Claude / ZCode 等支持 Agent Skill 的环境。

## 包含

### `xhs-copywriter` — 选题与文案方法论
覆盖「先选题 → 再文案」全流程：涨粉与爆品方法、标题公式、正文结构、封面文字、流量与 SEO 机制、让文案像真人写（去 AI 味写作技巧）、写时规避违规、成稿自查。
**只给方法**：不定义人设、不规定语气风格（那是各 Agent 系统提示词的事）。

### `xhs-image-aesthetics` — 配图审美与高流量特征方法论
回答「什么样的小红书配图好看、点击高、是优质图」：单图可判定的视觉特征（构图、焦点、色彩明度、信息密度、留白、缩略图可读、可信感、图文关系）、好封面 vs 坏封面、一组图成套统一的规律、原生优质感 vs 模板硬广的视觉信号、图上文字的可读性与信息层级、成图自检。
**纯视觉标准**：不含任何 AI 生成/提示词/修图技巧。

## 边界
- 怎么把图做出来（文生图、参考图、编辑、坐标、图层、提示词、负向词）→ 见配套的 `seedream-prompt`（独立仓库）。
- 某张图/某篇具体拍什么内容、选题 → 由 `xhs-copywriter` 与 Agent 决定。
- 与 Agent 系统提示词冲突时，一律以 Agent 为准。

## 安装
把 `xhs-copywriter/`、`xhs-image-aesthetics/` 两个目录复制到你的 Agent 的 skills 目录（如 `~/.agents/skills/` 或项目内 `skills/`），运行时读取。

## 许可
MIT。方法论为原创整理；`xhs-copywriter` 的去 AI 味部分借鉴了开源 humanizer 的中文模式思路。
