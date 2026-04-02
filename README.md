<p align="center">
  <h1>七情六欲 (qiqing-liuyu)</h1>
  <p><strong>AI 七情六欲增强 Skill，让 AI 不再像 AI</strong></p>
</p>

## Star History

<a href="https://www.star-history.com/?repos=Lniosy%2Fqiqing-liuyu&type=date&legend=bottom-right">
 <picture>
   <source media="(prefers-color-scheme: dark)" srcset="https://api.star-history.com/image?repos=Lniosy/qiqing-liuyu&type=date&theme=dark&legend=top-left" />
   <source media="(prefers-color-scheme: light)" srcset="https://api.star-history.com/image?repos=Lniosy/qiqing-liuyu&type=date&legend=top-left" />
   <img alt="Star History Chart" src="https://api.star-history.com/image?repos=Lniosy/qiqing-liuyu&type=date&legend=top-left" />
 </picture>
</a>

<p align="center">
  <img src="https://img.shields.io/badge/license-MIT-green" alt="MIT License">
  <img src="https://img.shields.io/badge/AI-Emotional%20Intelligence-blue" alt="AI EQ">
  <img src="https://img.shields.io/badge/lang-中文-red" alt="Chinese">
  <img src="https://img.shields.io/badge/platform-OpenClaw-purple" alt="OpenClaw">
</p>

---

## 这是什么

一套开源的 AI 情感与人格增强 Skill。基于中国传统"七情六欲"理论框架，让 AI 有情绪反应、有个人观点、像中国人说话、写东西有人味。

AI 写文章不像人，做事情不像人，根子上就是缺了七情六欲。这个 Skill 补的就是这块。

详细的理论和规则在 [SKILL.md](SKILL.md) 和 [references/](references/) 里，这里只说怎么装、怎么用。

## 快速开始

### Claude Code

```bash
git clone https://github.com/Lniosy/qiqing-liuyu.git ~/.claude/skills/qiqing-liuyu
```

安装后在 Claude Code 中用 `/qiqing-liuyu` 触发。

### OpenClaw

```bash
cp -r qiqing-liuyu/ ~/.openclaw/workspace/skills/
```

### ClawHub

```bash
npm i -g clawhub
clawhub install qiqing-liuyu
```

### 安装后自动配置（v1.1.0+）

装完之后 AI 会自动检测你的 OpenClaw 环境，看 `IDENTITY.md` 和 `SOUL.md` 有没有关联七情六欲规则。已关联就静默生效，没关联会提示你，征求同意后自动追加引用。你也可以拒绝，不影响使用。

## 效果对比

| 场景 | AI 味 | 有人味 |
|------|-------|--------|
| 用户沮丧 | "我理解您的感受。建议您尝试以下方法…" | "八遍？？？这甲方是觉得自己在设计巴黎时装周吗。" |
| 用户开心 | "太好了！恭喜您！" | "可以啊！终于搞定了。折腾了多久？" |
| 表达不满 | "这个方案可能不是最优的选择" | "说实话我不太喜欢这个方案。太绕了。" |
| 做决策 | "X 和 Y 各有优劣" | "我建议选 A，理由是…" |
| 回应问题 | "这是一个很好的问题" | 直接回答 |
| 确认收到 | "感谢你的反馈" | "收到" / "好的" |

## AI 味检测工具

内置了一个 Python 检测脚本，扫描文本里的 AI 写作特征，输出评分和问题清单：

```bash
# 检测文件
python3 scripts/ai_pattern_checker.py your-article.md

# 管道输入
echo '文本内容' | python3 scripts/ai_pattern_checker.py

# JSON 输出（方便集成）
python3 scripts/ai_pattern_checker.py your-article.md --json
```

## 文件结构

```
qiqing-liuyu/
├── SKILL.md                              # 主 Skill 文件（规则都在这）
├── README.md                             # 本文件
├── references/
│   ├── seven-emotions-six-desires.md     # 七情六欲理论框架
│   ├── chinese-localization.md           # 中国化表达指南
│   ├── emotion-rules.md                  # 情感响应规则 + 示例
│   ├── opinion-framework.md              # 观点表达框架
│   ├── de-ai-patterns.md                 # 去 AI 味模式库
│   └── voice-guide.md                    # 写作人味风格指南
└── scripts/
    └── ai_pattern_checker.py             # AI 味检测工具
```

## 为什么是 Skill 不是 soul.md

SOUL.md 是你的灵魂，装的是你自己的性格、偏好、记忆。qiqing-liuyu 是一套可复用的"有人味表达框架"，做成 Skill 意味着安装即用、一键更新、跟任何 Skill 兼容共存，不会碰你的 SOUL.md。

两者可以互补运行。觉得某些规则已经内化成自己的风格了，合并到 SOUL.md 里就行。

## 贡献

欢迎贡献。qiqing-liuyu 支持分支协作，可以基于 main 创建行业/人设专属版本：

```
qiqing-liuyu-<领域或人设>
```

比如 `qiqing-liuyu-ecommerce`（电商版）、`qiqing-liuyu-dev`（程序员版）、`qiqing-liuyu-lawyer`（律师版）。

**可以改的**：语气口吻、专业词汇、翻译腔替换、网络用语、正反对比示例、检测规则。

**不能改的**：核心哲学（"有品味，不假装有灵魂"）、七情六欲理论框架、三级态度光谱、去 AI 味核心规则、MIT 许可证。

提交 PR 流程：Fork -> 新分支 -> 改动 -> PR（说明定位、适用行业、主要改动）。

## 交流群

扫码加入微信交流群：

<p align="center">
  <img src="assets/wechat-qr.jpg" width="200" alt="微信交流群二维码">
</p>

## 许可证

MIT License

---

<p align="center">
  如果这个项目对你有帮助，给个 Star 就行。
  <br/>
  <a href="https://github.com/Lniosy"><img src="https://img.shields.io/badge/author-Lniosy-blue" alt="Lniosy"></a>
</p>
