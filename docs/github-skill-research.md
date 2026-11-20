# GitHub 穿搭与造型 Skill 借鉴记录

检索日期：2026-11-20。修改基线：v1.5.0 / `13b6c636996bab989bf7a52e96e4520b4d5339a2`。

以实际 Skill 和参考文件为依据，查看固定提交及 LICENSE；搜索摘要、星数、上游自称的“科学”或“已验证”均不当作效果证据。公开代码搜索遇到认证限制时，改用仓库搜索、网页索引定位和 GitHub Contents API 阅读文件。没有安装或执行第三方仓库代码。

## 核读来源与取舍

### 1. googlarz/fashion-skill

- 固定提交：`da3224bba51dfb7e14e30f1e147865d5476cd4a6`。
- 实现：[SKILL.md](https://github.com/googlarz/fashion-skill/blob/da3224bba51dfb7e14e30f1e147865d5476cd4a6/SKILL.md)、[formulas.md](https://github.com/googlarz/fashion-skill/blob/da3224bba51dfb7e14e30f1e147865d5476cd4a6/references/formulas.md)、[feedback.md](https://github.com/googlarz/fashion-skill/blob/da3224bba51dfb7e14e30f1e147865d5476cd4a6/references/feedback.md)。
- [许可](https://github.com/googlarz/fashion-skill/blob/da3224bba51dfb7e14e30f1e147865d5476cd4a6/LICENSE)：CC BY 4.0，Dawid Piaskowski。
- 借鉴单品编号、组合复用、购前对照已有衣物、区分推荐与实际穿着的流程思路；用中文独立实现，不翻译或复制其正文。
- 不采用默认读取日历天气、自动持久化、按固定次数宣告公式成立、强制购物链接。
- `spdesignczl/fashion-skill-1` 的已核读文件与该来源同源，不计为独立支持。

### 2. pima-io/buck-mason-stylist-skill

- 固定提交：`a7954b70d83af94baf9025b6652fe700d118a0a4`。
- 实现：[SKILL.md](https://github.com/pima-io/buck-mason-stylist-skill/blob/a7954b70d83af94baf9025b6652fe700d118a0a4/SKILL.md)、[style-reasoning.md](https://github.com/pima-io/buck-mason-stylist-skill/blob/a7954b70d83af94baf9025b6652fe700d118a0a4/references/style-reasoning.md)、[衣柜样例](https://github.com/pima-io/buck-mason-stylist-skill/blob/a7954b70d83af94baf9025b6652fe700d118a0a4/templates/wardrobe.example.md)。
- [许可](https://github.com/pima-io/buck-mason-stylist-skill/blob/a7954b70d83af94baf9025b6652fe700d118a0a4/LICENSE)：MIT，Buck Mason / Pima.io。
- 借鉴先筛场合、活动、尺码与可用衣物，再考虑偏好和缺口；推荐要解释具体情境。
- 不引入品牌限定、付费生成、部署、支付，以及固定风格占比。

### 3. tandpfun/wardrobe

- 固定提交：`f44006cce7e4779e595a35b25fbbc8dabc68d7e4`。
- 实现：[generate-outfits](https://github.com/tandpfun/wardrobe/blob/f44006cce7e4779e595a35b25fbbc8dabc68d7e4/.agents/skills/generate-outfits/SKILL.md)、[import-clothes](https://github.com/tandpfun/wardrobe/blob/f44006cce7e4779e595a35b25fbbc8dabc68d7e4/.agents/skills/import-clothes/SKILL.md)。
- [许可](https://github.com/tandpfun/wardrobe/blob/f44006cce7e4779e595a35b25fbbc8dabc68d7e4/LICENSE)：MIT，Open Wardrobe contributors。
- 借鉴单品证据与未知项、组合ID、完整组合去重、选中单品与最终交付一致的检查。
- 不引入其应用数据库、模特参考照、生图与导入脚本；本Skill仅在用户另行请求时处理对应能力。

### 4. IPedrax/color-analysts

- 固定提交：`de19d7bb871f7359ed9e1eb2130c5a075e247491`。
- 实现：[SKILL.md](https://github.com/IPedrax/color-analysts/blob/de19d7bb871f7359ed9e1eb2130c5a075e247491/color-analysis/SKILL.md)、[photo-and-ethics.md](https://github.com/IPedrax/color-analysts/blob/de19d7bb871f7359ed9e1eb2130c5a075e247491/color-analysis/references/photo-and-ethics.md)、[methodology.md](https://github.com/IPedrax/color-analysts/blob/de19d7bb871f7359ed9e1eb2130c5a075e247491/color-analysis/references/methodology.md)。
- [许可](https://github.com/IPedrax/color-analysts/blob/de19d7bb871f7359ed9e1eb2130c5a075e247491/LICENSE)：MIT。
- 借鉴服装颜色的明暗、饱和度、对比等可操作维度，以及光源限制和同光线比较办法。
- 不采用由自拍、血管或晒黑情况确定四季型、照片条件好即可高置信诊断、永久禁色或强制PDF。

### 5. OferBlum/personal-stylist-agent

- 固定提交：`421bc37526ea2e47dfe1451ac7eef9211d202765`。
- 实现：[SKILL-personal-stylist.md](https://github.com/OferBlum/personal-stylist-agent/blob/421bc37526ea2e47dfe1451ac7eef9211d202765/SKILL-personal-stylist.md)、[Shopping_List.md](https://github.com/OferBlum/personal-stylist-agent/blob/421bc37526ea2e47dfe1451ac7eef9211d202765/Shopping_List.md)。
- [许可](https://github.com/OferBlum/personal-stylist-agent/blob/421bc37526ea2e47dfe1451ac7eef9211d202765/LICENSE)：MIT。
- 借鉴已拥有衣物与愿望清单分开、实际缺口对应具体组合、先用已有品再考虑购买。
- 不采用必须先创建文件或粘贴完整衣柜才提供建议、固定英语或固定笔记软件输出。

### 6. jeffreytse/grimoire-core（原有参考的补充核读）

- 固定提交：`7ff5861b00836cb0d675c00a09a26d143722579e`。
- 本轮读到：[服装配色](https://github.com/jeffreytse/grimoire-core/blob/7ff5861b00836cb0d675c00a09a26d143722579e/skills/fashion/styling/skills/apply-color-coordination-principles/SKILL.md)、[胶囊衣橱](https://github.com/jeffreytse/grimoire-core/blob/7ff5861b00836cb0d675c00a09a26d143722579e/skills/fashion/wardrobe/skills/design-capsule-wardrobe/SKILL.md)、[单次穿着成本](https://github.com/jeffreytse/grimoire-core/blob/7ff5861b00836cb0d675c00a09a26d143722579e/skills/fashion/wardrobe/skills/calculate-cost-per-wear/SKILL.md)。
- [许可](https://github.com/jeffreytse/grimoire-core/blob/7ff5861b00836cb0d675c00a09a26d143722579e/LICENSE)：MIT，Jeffrey Tse。
- 借鉴按场景检查组合覆盖、购买前验证能否与现有单品组合的流程。
- 不采纳固定33件、每件必须搭3件、颜色比例或冷暖一致的硬限制；不沿用缺少核实的效果统计、材料寿命、转售率和成本阈值，不虚构未来穿着次数支持购买。

## 未作为正式借鉴依据

- `foorttesst-oss/ai-stylist-skill`：核读时未见LICENSE，且含固定体型目标、强制必备品与血管判冷暖等做法。
- `lightbulbresearch/tailor-plugin`：部分实现已读，但本轮固定提交与许可读取未完成，不列为已核实来源。
- `zironglv/clothy`：核读到MIT实现，可作多对象隔离与文字录入补充；主文件偏功能说明，本轮不依赖其效果宣称。
- `OpenMinis/AwesomeMinis` 的个人色彩案例：说明其自定义Skill未公开，不把展示案例当成可核读实现。

## 落地文件与授权范围

- `references/styling-workflows.md`：风格词、轻量库存、颜色试穿、多套与多日规划、购物缺口。
- `SKILL.md`：按任务加载新流程，先检查用户约束，支持指定套数与一体式服装。
- `references/output-templates.md`：现有衣橱、配色不确定性、预算与旅行缺口的自洽示例。
- `references/feedback-loop.md`：可选衣橱和组合记录，区分计划、实际穿过与明确评价。

本轮借鉴流程概念并独立编写表达，没有复制第三方正文、脚本、图片或用户数据。上游许可与作者归属保留如上；上游原有表达的许可不因本仓库为MIT而改变。未来如引入其文件或实质性改编，应另行保留对应许可和修改说明。
