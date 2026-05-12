# 游资短线交易系统 Skill

## 项目结构

```
youzi-trading-skill/
├── README.md           # 项目说明文档
├── LICENSE            # MIT开源协议
├── SKILL.md           # Hermes Agent Skill文件
├── examples/          # 使用示例
│   ├── 持仓诊断示例.md
│   ├── 选股建议示例.md
│   └── 亏损复盘示例.md
└── docs/              # 详细文档
    ├── 23位游资心法.md
    ├── 九大核心模块.md
    ├── 三大实战战法.md
    └── 常见问题FAQ.md
```

## 快速开始

### 1. 安装

```bash
# Hermes Agent
cp SKILL.md ~/.hermes/skills/investment/youzi-trading/

# OpenClaw
cp SKILL.md ~/.openclaw/skills/investment/youzi-trading/

# Claude Code
cp SKILL.md ~/.claude/skills/investment/youzi-trading/
```

### 2. 使用

在AI Agent中提到以下关键词即可自动触发：
- "短线"、"游资"、"打板"、"龙头"、"涨停板"
- "怎么炒股"、"如何选股"、"买什么股票"

### 3. 示例

```
用户：我的持仓10只股票，9只都在亏损

AI：基于游资心法诊断：
1. 是否在弱市做短线？
2. 是否持有跟风股？
3. 是否满仓操作？

建议：
- 清理跟风股，只留龙头
- 降低仓位到30-50%
- 弱市空仓休息
```

## 核心特性

- ✅ 23位游资完整心法
- ✅ 九大核心模块（选股、仓位、回撤、情绪、止损、概率、复盘、系统、执行力）
- ✅ 三大实战战法（龙头主升、打板、超跌反弹）
- ✅ 择时策略（强势/震荡/弱势市场）
- ✅ 常见错误纠正
- ✅ 游资名言（必背）

## 贡献

欢迎提交Issue和Pull Request！

## 许可证

MIT License - 详见 [LICENSE](LICENSE) 文件

## 作者

**Andy** - AI产品专家
- 微信：AI PMAndy
- GitHub: [@AIPMAndy](https://github.com/AIPMAndy)
