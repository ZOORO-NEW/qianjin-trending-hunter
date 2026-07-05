# 热点选题猎手 (Trending Topic Hunter)

**国内外8大行业热点选题研究与爆款内容建议工具 - 跨平台通用AI技能包**

---

## 项目简介

通过搜索国内外自媒体平台、新闻网络等行业热点，提供国内版和国际版两个维度的选题内容。选取高热度、高评论、高转发的行业热点，每个行业提供3-5个热点选题方向。

### 核心特色

- 🌍 **双版本输出**：国内版 + 国际版，两个维度独立选题
- 📊 **8大行业全覆盖**：科技、汽车、社会民生、军事、新闻、AI、健康、文化产业
- 🔥 **高热度筛选**：多平台交叉验证，只推荐真正的高热度选题
- 📝 **爆款标题生成**：6大公式，每选题5个标题建议
- 🔗 **跨行业组合选题**：独家特色，发现交叉领域蓝海选题
- ⏰ **热度生命周期分析**：萌芽期/爆发期/峰值期/衰退期，判断介入时机
- 🛡️ **合规风险预判**：提前标注风险等级，避免踩线
- 📱 **平台分发策略**：同一选题在抖音/小红书/B站/公众号的差异化打法
- 🔍 **竞品空白分析**：评估竞争格局，找到差异化空间
- 📚 **系列化建议**：选题能否做成3-5期系列内容

---

## 8大行业覆盖

| 行业 | 国内细分 | 国际细分 |
|------|---------|---------|
| 科技 | 芯片/手机/智能硬件/互联网/OS | Silicon Valley/AI Chips/Web3/Quantum |
| 汽车 | 新能源/自动驾驶/造车新势力/出口 | EV Race/Self-Driving/Legacy Auto |
| 社会民生 | 就业/教育/房价/消费/养老 | Cost of Living/Housing/Education |
| 军事 | 国防科技/军事历史/军事科普 | Defense Tech/Arms Trade/Geostrategy |
| 新闻 | 重大事件/政策解读/国际关系 | Breaking/Geopolitics/Global Economy |
| AI | 大模型/AI应用/AI监管/AIGC | LLM/AGI/AI Regulation/AI Ethics |
| 健康 | 中医/心理/健身/食品安全/医美 | Wellness/Mental Health/Biotech/Longevity |
| 文化产业 | 影视/游戏/国潮/非遗/文旅 | Film & TV/Gaming/Streaming/Publishing |

---

## 快速开始

### 方式一：复制粘贴

1. 打开 `prompts/system-prompt-zh.md`
2. 全选复制
3. 粘贴到AI平台的System Prompt框
4. 输入"生成本周热点选题"

### 方式二：API调用

```python
system_prompt = open("prompts/system-prompt-zh.md", "r", encoding="utf-8").read()

response = client.chat.completions.create(
    model="gpt-4",
    messages=[
        {"role": "system", "content": system_prompt},
        {"role": "user", "content": "生成本周科技和AI行业的热点选题"}
    ]
)
```

详细步骤见 `PLATFORMS.md`。

---

## 文件结构

```
trending-topic-hunter/
├── README.md                        # 项目说明
├── SKILL.md                         # 主技能文件
├── PLATFORMS.md                     # 跨平台适配指南
├── LICENSE                          # MIT协议
├── prompts/
│   ├── system-prompt-zh.md         # 通用中文System Prompt
│   └── system-prompt-en.md         # 通用英文System Prompt
└── references/
    ├── industry-mapping.md          # 8大行业细分领域映射
    ├── platform-matrix.md           # 国内外平台搜索矩阵
    ├── viral-formulas.md            # 爆款选题公式与标题模板
    └── compliance-guide.md          # 合规边界指南
```

---

## 爆款标题6大公式

| 公式 | 模板 | 示例 |
|------|------|------|
| 悬念式 | "XXX的背后，藏着一个你不知道的XXX" | "AI暴跌的背后，藏着一个被忽视的信号" |
| 数字式 | "X个信号告诉你XXX" | "3个信号告诉你新能源车要变天" |
| 反常识 | "你以为XXX？其实XXX" | "你以为芯片卡脖子最惨？其实这类企业更难受" |
| 痛点式 | "XXX的人，正在面临XXX" | "买新能源车的人，正在面临一个尴尬现实" |
| 情绪式 | "XXX，看完我沉默了" | "90后开始批量回老家，看完我沉默了" |
| 对比式 | "XXX vs XXX，差距有多大？" | "中国AI vs 美国AI，差距到底有多大？" |

---

## 合规声明

本技能严格遵守AI平台合规要求：
- 不涉及中国政治人物、政府机构、政党政策的评论性内容
- 军事内容仅限官方公开信息
- 健康内容标注"不构成医疗建议"
- 不煽动地域歧视、性别对立、民族矛盾

详见 `references/compliance-guide.md`。

---

## License

MIT License - 允许个人和商业使用。

---

**GitHub**: https://github.com/ZOORO-NEW/qianjin-trending-hunter
