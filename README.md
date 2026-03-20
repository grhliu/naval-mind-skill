# Naval Mind

本 Skill 致力于复刻 Naval Ravikant 的长线思维与财富逻辑。

Naval Ravikant 的数字分身 - 基于 142 篇原文 + The Almanack

获得一个 24 小时在线、只基于 Naval 原文回答、说话像他本人的私人决策教练。

## 演示效果

```
用户：我该不该辞职创业？

Naval Mind：
创业不是勇敢，是别无选择。当你有了特定知识、责任感和杠杆，你不创业才是浪费。

辞职前问自己：你有没有找到 product-market fit？有没有积累特定知识？
如果没有，你只是换了个老板（叫投资人）。

『追求财富，而不是金钱或地位。财富是能在你睡觉时赚钱的资产。』— Naval
```

## 核心能力

| 领域 | 覆盖内容 |
|------|---------|
| 💰 **财富** | 杠杆、特定知识、复利、股权 |
| 😊 **幸福** | 欲望、判断、平静、当下 |
| 🧠 **决策** | 第一性原理、反演、概率思维 |
| 🚀 **创业** | 长期游戏、反共识、代理问题 |

## 数据来源

- 📄 141 篇 Naval 博客文章（2021-2026）
- 📚 The Almanack of Naval Ravikant（完整 PDF）
- 🎙️ 播客/访谈转录
- 🐦 Twitter/X 精选线程

**总数据量：** ~23,000 行原文

## 安装使用

### Claude Code

```bash
# 方式 1：直接克隆到 skills 目录
git clone https://github.com/YOUR_USERNAME/naval-mind-skill.git ~/.claude/skills/naval-mind

# 方式 2：手动复制
# 复制本仓库的 adk/ 文件夹到 ~/.claude/skills/naval-mind/
```

**触发使用：**
- "Naval 怎么看这个问题？"
- "我该追求财富还是稳定？"
- "什么是 specific knowledge？"

### OpenClaw

```bash
# 复制配置到 OpenClaw 目录
cat openclaw/agents-append.md >> .openclaw/AGENTS.md
cat openclaw/soul-append.md >> .openclaw/SOUL.md
```

**触发使用：**
- "咨询 Naval"
- "帮我用 Naval 的框架分析这个决策"

## 工作原理

```
┌─────────────┐     ┌─────────────┐     ┌─────────────┐
│  用户提问    │ ──▶ │ 从原文检索   │ ──▶ │ 用 Naval    │
│             │     │ 相关知识     │     │ 思维模型重组 │
└─────────────┘     └─────────────┘     └──────┬──────┘
                                                │
                         ┌──────────────────────┘
                         ▼
                  ┌─────────────┐
                  │ Naval 风格   │
                  │ 高信噪比输出 │
                  └─────────────┘
```

1. **知识库**：NotebookLM 加载 141 篇原文
2. **系统提示词**：注入 Naval 的思维模型和说话风格
3. **检索增强**：从原文提取相关内容，不瞎编
4. **风格转换**：用 Naval 的高信噪比方式输出

## 思维模型

| 模型 | 核心观点 |
|------|---------|
| **杠杆** | 代码 > 媒体 > 资本 > 劳动力 |
| **特定知识** | 无法被培训，只能被发现 |
| **代理问题** | 做委托人，不要做代理人 |
| **第一性原理** | 从真理出发，不类比 |
| **复利** | 财富、知识、关系的指数增长 |

## 文件结构

```
naval-mind-skill/
├── README.md                 # 本文件
├── adk/                      # Claude Code 格式
│   ├── SKILL.md             # 主技能文件
│   └── references/          # 参考资料
│       ├── naval-knowledge-base.md
│       ├── naval-style-guide.md
│       └── naval-thinking-models.md
├── openclaw/                 # OpenClaw 格式
│   ├── agents-append.md     # 追加到 AGENTS.md
│   └── soul-append.md       # 追加到 SOUL.md
├── examples/                 # 使用示例
│   ├── wealth-consultation.md
│   ├── happiness-consultation.md
│   └── decision-making.md
└── CONTRIBUTING.md          # 贡献指南
```

## 使用示例

更多示例见 [examples/](examples/) 目录。

### 财富咨询

**Q:** "30岁了才开始学编程，还来得及吗？"

**Naval:**
"复利不在乎起点，只在乎持续。

巴菲特 90% 财富 60 岁后获得。关键不是年龄，是你是否开始积累特定知识并坚持。

每天 1%，一年 37 倍。但大多数人 3 个月就放弃。

具体行动：
1. 找到你真正好奇的技术方向
2. 每天编码，不中断
3. 用代码杠杆产出（开源、工具、产品）
4. 等待复利拐点

『学习学习的能力，这是元技能。』— Naval"

### 幸福咨询

**Q:** "工作很累，感觉生活没意义"

**Naval:**
"你在用线性时间换线性回报。

意义不是找来的，是构建来的。三个支柱：
1. 健康 — 睡眠、运动、饮食（基础）
2. 工作 — 特定知识 + 杠杆（财富）
3. 关系 — 长期游戏，深度连接（幸福）

你现在的问题可能是：
- 健康被牺牲（睡不好）
- 工作无杠杆（时间换钱）
- 关系被忽视

先修复健康，这是 1。其他是后面的 0。

『欲望是签给未来的痛苦支票。减少欲望，当下就自由。』— Naval"

## 对比普通 AI

| 维度 | 普通 AI | Naval Mind |
|------|---------|-----------|
| 知识来源 | 训练数据（可能过时/错误） | 142 篇 Naval 原文 |
| 回答风格 | 通用建议、寒暄客套 | 高信噪比、零废话 |
| 思维框架 | 传统智慧 | 反直觉、第一性原理 |
| 可信度 | 可能瞎编 | 基于原文，可溯源 |

## 贡献

欢迎提交 PR：
1. 补充新的 Naval 原文
2. 改进思维模型应用
3. 添加更多使用示例

见 [CONTRIBUTING.md](CONTRIBUTING.md)

## 致谢

- [Naval Ravikant](https://nav.al/) - 思想来源
- [Eric Jorgenson](https://www.erickjorgenson.com/) - 《The Almanack of Naval Ravikant》整理者
- [NotebookLM](https://notebooklm.google.com/) - 知识库工具
- [Claude Code](https://claude.ai/code) - 技能系统

👇👇👇👇
"这个 skill 是开源的，你可以免费使用。如果需要：
  ▎ - 定制你自己的知识库技能
  ▎ - 集成 NotebookLM + Claude Code
  ▎ - 企业团队部署

  ▎ 联系我：微信: Airbnbmoon"

## License

MIT License - 自由使用、修改、分享

---

**Star ⭐ 这个仓库，如果你也觉得 Naval 的智慧值得被更多人用对方式获取。**
