# 游资短线交易系统 Skill

> 基于23位著名游资心法的A股超短线交易分析系统。核心：情绪周期、龙头战法、概率思维、风险优先。

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Version](https://img.shields.io/badge/version-2.0-blue.svg)](https://github.com/AIPMAndy/youzi-trading-skill)
[![Hermes Agent](https://img.shields.io/badge/Hermes-Agent-blue)](https://github.com/NousResearch/hermes-agent)

## 简介

这是一个基于《23位著名游资心法解读版》和实战经验总结的A股超短线交易分析系统Skill，适用于Hermes Agent、OpenClaw、Claude Code等AI Agent平台。

**v2.0 重大更新**：
- ✅ 增加输入/输出契约（信息不足时先澄清）
- ✅ 明确硬规则和软规则（风险优先）
- ✅ 增加市场环境判断模块（先判断市场强弱）
- ✅ 压缩23位游资名单为策略原型索引
- ✅ 增加澄清模式和边界场景示例
- ✅ 分离README和SKILL（SKILL.md是唯一规范）

## 快速开始

### 安装

```bash
# Hermes Agent
mkdir -p ~/.hermes/skills/investment/youzi-trading
cp SKILL.md ~/.hermes/skills/investment/youzi-trading/

# OpenClaw
mkdir -p ~/.openclaw/skills/investment/youzi-trading
cp SKILL.md ~/.openclaw/skills/investment/youzi-trading/

# Claude Code
mkdir -p ~/.claude/skills/investment/youzi-trading
cp SKILL.md ~/.claude/skills/investment/youzi-trading/
```

### 使用

在AI Agent中提到以下关键词即可自动触发：
- "A股短线"、"游资"、"打板"、"龙头股"、"涨停板"
- 持有A股并问"怎么操作"、"如何选股"

### 示例

```
用户：我的A股持仓10只，9只都在亏损

AI：在给你建议之前，我需要了解几个关键信息：
1. 当前A股市场环境如何？（强势/震荡/弱势？）
2. 你的持仓具体是哪些股票？行业分布如何？
3. 你的投资周期是多久？（短线1-3天，还是波段1-2周？）

有了这些信息，我才能给你更精准的建议。
```

## 核心特性

### 硬规则（必须遵守）
1. **无数据不下结论**：没有市场环境、持仓信息，不给具体操作建议
2. **无市场背景不点股**：不了解当前市场强弱，不推荐具体股票
3. **弱市不做**：市场处于弱势时，建议空仓休息
4. **亏损单不过夜**：短线第一原则，被套必须次日止损
5. **避免杠杆/追高/摊平**：不建议融资、不建议追高、不建议补仓

### 软规则（建议遵守）
1. **只做龙头**：优先推荐龙头股
2. **永远不要满仓**：建议仓位控制
3. **只做主升浪**：优先推荐主升浪

### 输入契约（分析前必须收集的信息）
- 市场环境（强势/震荡/弱势）
- 用户持仓（持有几只？盈亏如何？）
- 投资周期（短线/波段/中线）
- 风险承受能力

### 输出契约（固定回答格式）
- 诊断（问题是什么）
- 依据（基于哪条游资心法）
- 动作（具体操作建议）
- 风险（可能的风险）
- 缺失信息（还需要什么信息）

## 23位游资策略原型索引

| 流派 | 代表人物 | 核心心法 |
|---|---|---|
| 情绪周期派 | 养家、涅槃重生 | 群体博弈、情绪周期 |
| 纪律执行派 | 职业炒手、Asking | 耐心+顺势+知行合一 |
| 龙头战法派 | 赵老哥、著名刺客 | 只做龙头、只做主升浪 |
| 打板技术派 | 令狐冲、小鳄鱼 | 盘感和打板、板+主线+人气 |
| 熊市生存派 | 不动明王、瑞鹤仙 | 熊市先保命、只做最强反弹 |
| 趋势狙击派 | 章盟主、浓汤野人 | 趋势狙击、大资金板块作战 |
| 低吸回踩派 | 乔帮主 | 低吸龙头回踩 |
| 空杯心派 | 葛卫东、万法归宗 | 听市场而非猜市场 |

**共性**：只做强势、主线、人气和赚钱效应；买点重确认，卖点重纪律，仓位重随势。

## 文档结构

```
youzi-trading-skill/
├── README.md              # 本文件（项目概览）
├── SKILL.md              # 核心Skill文件（唯一规范）
├── CHANGELOG.md          # 版本更新日志
├── LICENSE               # MIT开源协议
├── examples/             # 使用示例
│   ├── 持仓诊断示例.md
│   ├── 选股建议示例.md
│   ├── 亏损复盘示例.md
│   └── 边界场景示例.md   # 新增
└── .github/
    └── README.md         # GitHub展示页
```

## 适用场景

### ✅ 适用
- A股超短线交易（1-3天）
- 有一定交易经验的投资者
- 能够控制情绪的投资者
- 有时间盯盘复盘的投资者

### ❌ 不适用
- 港股、美股、期货、期权
- 长期价值投资
- 新手小白（需先学习基础知识）
- 上班族（没时间盯盘）

## 贡献

欢迎提交Issue和Pull Request！

### 贡献指南
1. Fork本仓库
2. 创建特性分支 (`git checkout -b feature/AmazingFeature`)
3. 提交更改 (`git commit -m 'Add some AmazingFeature'`)
4. 推送到分支 (`git push origin feature/AmazingFeature`)
5. 开启Pull Request

## 参考资料

- 《23位著名游资心法解读版 上册》
- Andy的游资研究笔记（XMind）
- 炒股养家、职业炒手、Asking、赵老哥等游资实战经验

## 作者

**Andy** - AI产品专家，前腾讯/百度AI产品专家，大模型独角兽VP
- 微信：AI PMAndy
- GitHub: [@AIPMAndy](https://github.com/AIPMAndy)

## 致谢

- 感谢23位游资的实战经验分享
- 感谢Hermes Agent团队提供的AI Agent平台
- 感谢Codex提供的深度分析报告
- 感谢所有为本项目做出贡献的开发者

## 许可证

本项目采用 MIT 许可证 - 详见 [LICENSE](LICENSE) 文件

---

## 版本历史

- **v2.0** (2026-05-12) - 重大更新：增加输入/输出契约、硬规则/软规则、市场环境判断模块
- **v1.0** (2026-05-12) - 初始版本：基于23位游资心法

---

**最后的话**

> "投资是一时苦，打工是一世苦，要持续研究投资交易。"
> 
> "交易的认知就是一层窗户纸，捅破了认知和操作就会突飞猛进。"

---

**详细文档请查看 [SKILL.md](SKILL.md)**
