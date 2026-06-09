# Wiki Schema

## Domain
赵亚琦个人知识库——覆盖道教哲学（无极大道、物极必反、阴阳太极）、投资理财（基金定投、止盈策略、行业分析）、段子创作（夫妻互怼、短视频脚本）、逆脉之轮（世界观构建、力量体系、角色设计）、中医养生（喉痹调理、体质辩证）、设计排版（平面设计、CorelDRAW自动化）、以及其他深度思考话题（未解之谜、复杂科学、AI哲学）。

## Conventions
- File names: lowercase, hyphens, no spaces (e.g., `fund-stop-profit-rules.md`)
- Every wiki page starts with YAML frontmatter (see below)
- Use `[[wikilinks]]` to link between pages (minimum 2 outbound links per page)
- When updating a page, always bump the `updated` date
- Every new page must be added to `index.md` under the correct section
- Every action must be appended to `log.md`
- Language: 中文为主，专业术语保留英文

## Frontmatter
```yaml
---
title: 页面标题
created: YYYY-MM-DD
updated: YYYY-MM-DD
type: entity | concept | comparison | query | summary
tags: [from taxonomy below]
sources: [raw/articles/source-name.md]
confidence: high | medium | low
contested: true
contradictions: [other-page-slug]
---
```

## Tag Taxonomy
- 道教哲学: 无极大道, 物极必反, 阴阳, 太极, 无为, 庄子, 老子, 王阳明
- 投资理财: 基金, 定投, 止盈, 行业分析, 券商, 国债, 股票
- 段子创作: 夫妻互怼, 短视频, 脚本结构, 赵总段子
- 逆脉之轮: 世界观, 力量体系, 角色设计, 阵营, 剧情
- 中医养生: 喉痹, 阴虚, 体质, 方剂, 经典
- 设计: 平面设计, CorelDRAW, 排版, 自动化
- 哲学思考: 未解之谜, 复杂科学, AI, 文明循环
- 生活: 家庭, 育儿, 宠物

Rule: every tag on a page must appear in this taxonomy. If a new tag is needed, add it here first, then use it.

## Page Thresholds
- **Create a page** when an entity/concept appears in 2+ sources OR is central to one source
- **Add to existing page** when a source mentions something already covered
- **DON'T create a page** for passing mentions or minor details
- **Split a page** when it exceeds ~200 lines
- **Archive a page** when its content is fully superseded

## Entity Pages
One page per notable entity. Include:
- Overview / what it is
- Key facts and dates
- Relationships to other entities ([[wikilinks]])
- Source references

## Concept Pages
One page per concept or topic. Include:
- Definition / explanation
- Current state of knowledge / 赵总的理解
- Open questions or debates
- Related concepts ([[wikilinks]])

## Comparison Pages
Side-by-side analyses. Include:
- What is being compared and why
- Dimensions of comparison (table format preferred)
- Verdict or synthesis
- Sources

## Update Policy
When new information conflicts with existing content:
1. Check the dates — newer sources generally supersede older ones
2. If genuinely contradictory, note both positions with dates and sources
3. Mark the contradiction in frontmatter: `contradictions: [page-name]`
4. Flag for user review in the lint report
