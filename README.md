<div align="center">

# 🌙 经期健康追踪系统
### Menstrual Health Tracker

<p>
  <a href="LICENSE"><img src="https://img.shields.io/badge/License-MIT-purple?style=flat-square"></a>
  <a href="https://www.python.org/"><img src="https://img.shields.io/badge/Python-3.9+-green?style=flat-square"></a>
  <img src="https://img.shields.io/badge/Version-1.2.0-9B7EC4?style=flat-square">
</p>

</div>

<details open>
<summary><b>🇨🇳 中文</b></summary>

**AI 驱动的经期健康追踪与多维分析系统** — 支持全生命阶段（初潮前→经期→备孕→孕期→产后→围绝经期→绝经后），提供周期规律分析、症状模式识别、智能预测、可视化仪表盘和科学建议。中英双语自动检测，共情交互体验。

## ✨ 核心功能

| 功能 | 描述 |
|------|------|
| 📊 **多维数据分析** | 周期规律、症状模式、情绪趋势、体征追踪、影响因素关联 |
| 🔮 **智能预测** | 近期加权 + 模式检测，自动适配个人周期变化 |
| 📈 **可视化仪表盘** | Chart.js 驱动的 HTML 仪表盘，热力图/趋势图/雷达图/时间线 |
| 🩺 **科学建议** | 3轮压力测试校验（科学准确性→个性化→安全性） |
| 💜 **共情交互** | 4种表达模式，7个生命阶段专属语气 |
| 👤 **用户档案系统** | 3级问卷，完整度追踪，自动状态切换 |
| 🌍 **全生命阶段** | 初潮前→经期→备孕→孕期→产后→围绝经期→绝经后 |
| 🌐 **双语支持** | 自动检测中文/英文，支持会话中切换 |

## 🚀 快速开始

### WorkBuddy 技能安装

在 WorkBuddy 中直接安装使用 — 提及经期相关话题时自动触发。

### 独立使用

```bash
# 分析数据并生成文本报告
python scripts/analyze.py ~/.workbuddy/data/menstrual_health.json

# 生成 HTML 仪表盘
python scripts/analyze.py ~/.workbuddy/data/menstrual_health.json --dashboard output.html
```

### 数据格式

```json
{
  "user_profile": {
    "life_stage": "menstruating",
    "typical_cycle_length": 28,
    "typical_period_length": 5
  },
  "cycles": [
    {
      "start_date": "2026-06-08",
      "end_date": "2026-06-14",
      "flow_level": "medium",
      "symptoms": { "cramps": { "present": true, "severity": 3 } },
      "mood_score": 7
    }
  ]
}
```

## 📁 项目结构

```
menstrual-health-tracker/
├── SKILL.md                     # WorkBuddy 技能定义（核心工作流）
├── README.md                    # 本文件
├── LICENSE                      # MIT 许可证
├── scripts/
│   └── analyze.py               # Python 分析引擎（600+ 行）
├── assets/
│   ├── dashboard.html           # Chart.js 仪表盘模板
│   ├── demo_data.json           # 测试用演示数据
│   └── demo_dashboard.html      # 预生成演示仪表盘
├── references/                   # 中文参考文档
│   ├── analysis_engine.md       # 分析维度与算法
│   ├── empathy_guide.md         # 共情交互模式
│   ├── life_stages.md           # 7个生命阶段适配逻辑
│   ├── medical_standards.md     # 循证医学参考
│   └── user_profile.md          # 用户档案系统与问卷
└── references-en/                # 英文参考文档
    ├── analysis_engine.md
    ├── empathy_guide.md
    ├── life_stages.md
    ├── medical_standards.md
    └── user_profile.md
```

## 🔬 分析引擎

Python 分析引擎 (`scripts/analyze.py`) 执行：

1. **周期规律** — 均值、标准差、变异系数、趋势斜率（线性回归）
2. **症状模式** — 频率分布、严重度趋势、高频症状排行
3. **情绪分析** — 周期日相关的情绪曲线
4. **智能预测** — 指数衰减加权平均 + 3种近期模式检测：
   - 模式一：与历史均值显著偏离
   - 模式二：近期比历史更规律
   - 模式三：稳定短周期模式（28-35天）
5. **事件影响** — 生活事件与周期变化的相关性
6. **健康预警** — 自动标记需关注的异常模式

## 🎨 仪表盘

HTML 仪表盘包含日历热力图、周期趋势图（含移动平均线）、症状雷达图、情绪曲线、预测时间线、智能洞察。配色：柔紫/珊瑚/绿/粉，暖白背景，支持深色模式。

## 🩺 医疗安全

所有建议均经过 3 轮压力测试，就医建议明确标注 ⚕️，不提供处方药推荐，孕期/产后严格安全边界，异常模式自动预警。

**免责声明**：本工具基于数据模式提供健康参考，不能替代专业医学诊断。

## 🤝 参与贡献

欢迎贡献！关注方向：更多症状分类体系、更多生命阶段适配、移动端 PWA 版本、多语言扩展。

## ☕ 支持项目

如果这个项目对你有帮助，欢迎请我喝杯咖啡：

<div align="center">
  <table>
    <tr>
      <td align="center"><img src="assets/donate/wechat-donate.jpg" width="200" alt="微信赞赏"/><br/>微信赞赏</td>
      <td align="center"><img src="assets/donate/alipay-donate.jpg" width="200" alt="支付宝赞赏"/><br/>支付宝赞赏</td>
    </tr>
  </table>
</div>

## 📄 许可证

MIT — 详见 [LICENSE](LICENSE)。

</details>

<details>
<summary><b>🇺🇸 English</b></summary>

**AI-powered menstrual cycle tracking & multi-dimensional analysis system** — covers all life stages (premenarche → menstruating → TTC → pregnant → postpartum → perimenopause → postmenopause). Features cycle regularity analysis, symptom pattern recognition, smart prediction, visual dashboards, and science-backed recommendations. Bilingual auto-detection with empathetic interaction.

## ✨ Features

| Feature | Description |
|---------|-------------|
| 📊 **Multi-Dimensional Analysis** | Cycle regularity, symptom patterns, mood trends, physical tracking, factor correlation |
| 🔮 **Smart Prediction** | Exponential-decay weighted average + pattern detection, auto-adapting to cycle changes |
| 📈 **Visual Dashboard** | Chart.js-powered HTML dashboard with heatmaps, trend charts, radar charts, timelines |
| 🩺 **Science-Backed Advice** | 3-round stress testing (scientific accuracy → personalization → safety) |
| 💜 **Empathetic Interaction** | 4 expression modes, 7 life-stage-specific tones |
| 👤 **User Profile System** | 3-tier questionnaire, completeness tracking, auto status switching |
| 🌍 **Full Life Stages** | Premenarche → Menstruating → TTC → Pregnant → Postpartum → Perimenopause → Postmenopause |
| 🌐 **Bilingual Support** | Auto-detect Chinese/English, switch mid-conversation |

## 🚀 Quick Start

### As a WorkBuddy Skill

Install directly in WorkBuddy — the skill auto-triggers on menstrual health related queries.

### Standalone Usage

```bash
# Analyze data and print report
python scripts/analyze.py ~/.workbuddy/data/menstrual_health.json

# Generate HTML dashboard
python scripts/analyze.py ~/.workbuddy/data/menstrual_health.json --dashboard output.html
```

### Data Format

```json
{
  "user_profile": {
    "life_stage": "menstruating",
    "typical_cycle_length": 28,
    "typical_period_length": 5
  },
  "cycles": [
    {
      "start_date": "2026-06-08",
      "end_date": "2026-06-14",
      "flow_level": "medium",
      "symptoms": { "cramps": { "present": true, "severity": 3 } },
      "mood_score": 7
    }
  ]
}
```

## 📁 Project Structure

```
menstrual-health-tracker/
├── SKILL.md                     # WorkBuddy skill definition (core workflow)
├── README.md                    # This file
├── LICENSE                      # MIT License
├── scripts/
│   └── analyze.py               # Python analysis engine (600+ lines)
├── assets/
│   ├── dashboard.html           # Chart.js dashboard template
│   ├── demo_data.json           # Demo data for testing
│   └── demo_dashboard.html      # Pre-generated demo dashboard
├── references/                   # Chinese reference docs (中文参考文档)
│   ├── analysis_engine.md       # Analysis dimensions & algorithms
│   ├── empathy_guide.md         # Empathetic interaction patterns
│   ├── life_stages.md           # 7 life stage adaptation logic
│   ├── medical_standards.md     # Evidence-based medical references
│   └── user_profile.md          # Profile system design & questionnaires
└── references-en/                # English reference docs
    ├── analysis_engine.md
    ├── empathy_guide.md
    ├── life_stages.md
    ├── medical_standards.md
    └── user_profile.md
```

## 🔬 Analysis Engine

The Python analysis engine (`scripts/analyze.py`) performs:

1. **Cycle Regularity** — mean, std, CV, trend slope (linear regression)
2. **Symptom Patterns** — frequency rate, severity trends, top symptoms
3. **Mood Analysis** — cycle-day correlated mood curves
4. **Smart Prediction** — exponential-decay weighted average + 3-mode recent pattern detection
5. **Event Impact** — correlation between life events and cycle changes
6. **Health Alerts** — automatic flagging of concerning patterns

## 🎨 Dashboard

The HTML dashboard features calendar heatmap, cycle trend chart with moving average, symptom radar chart, mood curve, prediction timeline, and smart insights. Color theme: soft purple/coral/green/pink on warm white background. Dark mode supported.

## 🩺 Medical Safety

All recommendations undergo 3-round stress testing. Medical referral suggestions are clearly labeled ⚕️. No prescription drug recommendations. Strict safety boundaries for pregnancy/postpartum. Automatic alert detection for concerning patterns.

**Disclaimer**: This tool provides health references based on data patterns. It does not replace professional medical diagnosis.

## 🤝 Contributing

Contributions welcome! Areas of interest: additional symptom taxonomies, more life stage adaptations, mobile PWA version, additional language support.

## ☕ Support

If this project helps you, consider buying me a coffee:

<div align="center">
  <table>
    <tr>
      <td align="center"><img src="assets/donate/wechat-donate.jpg" width="200" alt="WeChat Donate"/><br/>WeChat Donate</td>
      <td align="center"><img src="assets/donate/alipay-donate.jpg" width="200" alt="Alipay Donate"/><br/>Alipay Donate</td>
    </tr>
  </table>
</div>

## 📄 License

MIT — see [LICENSE](LICENSE) for details.

</details>

<div align="center">
  <sub>🌙 照顾好自己，每个阶段都值得被温柔对待 · Every stage deserves care</sub>
</div>
