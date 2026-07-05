# 热点选题猎手 - 跨平台适配指南

本技能支持在以下AI平台使用：OpenClaw、Hermes、Codex、ChatGPT、Claude、通义千问、文心一言、腾讯混元、DeepSeek等。

---

## 快速开始

### 方式一：复制粘贴（最简单）

1. 打开 `prompts/system-prompt-zh.md`（中文）或 `prompts/system-prompt-en.md`（英文）
2. 全选复制全部内容
3. 粘贴到目标AI平台的System Prompt / 系统指令 / 角色设定框
4. 输入："生成本周热点选题"即可开始

### 方式二：文件上传

1. 下载整个技能包
2. 在支持文件上传的平台上传 `SKILL.md` 和 `references/` 目录
3. 在对话中引用上传的文件

### 方式三：API调用

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

---

## 各平台适配

### OpenClaw
- **方式**：Expert包导入 或 System Prompt粘贴
- **步骤**：将 `SKILL.md` 导入Expert管理页面，或直接粘贴 `system-prompt-zh.md`

### Hermes
- **方式**：System Prompt粘贴
- **步骤**：在对话设置中找到"角色设定"，粘贴 `system-prompt-zh.md`
- **注意**：如有长度限制，删除"参考资料"部分，保留核心流程

### Codex / ChatGPT
- **方式**：GPTs定制 或 System Prompt粘贴
- **步骤**：创建GPTs，在Instructions中粘贴 `system-prompt-zh.md`
- **增强**：可上传 `references/` 文件作为知识库

### Claude
- **方式**：Project Instructions
- **步骤**：创建Project，在Instructions中粘贴，上传references到Knowledge

### 通义千问 / 文心一言 / 腾讯混元 / DeepSeek
- **方式**：System Prompt粘贴
- **步骤**：在设置中找到"系统指令"，粘贴 `system-prompt-zh.md`

---

## 使用示例

### 基本用法
```
生成本周热点选题
```

### 指定行业
```
生成科技和AI行业的热点选题
```

### 指定版本
```
生成本周国内版热点选题
```

### 跨行业组合
```
生成本周跨行业组合选题
```

---

## 文件清单

```
qianjin-trending-hunter/
├── README.md
├── SKILL.md
├── PLATFORMS.md
├── LICENSE
├── prompts/
│   ├── system-prompt-zh.md
│   └── system-prompt-en.md
└── references/
    ├── industry-mapping.md
    ├── platform-matrix.md
    ├── viral-formulas.md
    └── compliance-guide.md
```

---

**License**: MIT
**GitHub**: https://github.com/ZOORO-NEW/qianjin-trending-hunter
