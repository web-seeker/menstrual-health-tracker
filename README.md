# 🌙 Menstrual Health Tracker

**经期健康追踪与多维分析系统** — AI-powered menstrual cycle tracking with multi-dimensional analytics, scientific insights, and empathetic interaction.

[![License: MIT](https://img.shields.io/badge/License-MIT-purple.svg)](LICENSE)
[![Python 3.9+](https://img.shields.io/badge/Python-3.9+-green.svg)](https://www.python.org/)
[![WorkBuddy Skill](https://img.shields.io/badge/WorkBuddy-Skill-9B7EC4.svg)](https://www.codebuddy.cn)

---

## ✨ Features

| 功能 | 描述 |
|------|------|
| 📊 **多维数据分析** | 周期规律、症状模式、情绪趋势、体征追踪、影响因素关联 |
| 🔮 **智能预测** | 近期加权 + 模式检测，自动适配个人周期变化 |
| 📈 **可视化仪表盘** | Chart.js 驱动的 HTML 仪表盘，热力图/趋势图/雷达图/时间线 |
| 🩺 **科学建议** | 3轮压力测试校验（科学准确性→个性化→安全性） |
| 💜 **共情交互** | 4种表达模式，7个生命阶段专属语气 |
| 👤 **用户档案系统** | 3级问卷，完整度追踪，自动状态切换 |
| 🌍 **全生命阶段** | 初潮前→经期→备孕→孕期→产后→围绝经期→绝经后 |

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
├── .gitignore
├── scripts/
│   └── analyze.py               # Python analysis engine (600+ lines)
│       • analyze()               # Multi-dimension analysis
│       • generate_recommendations()  # 3-round stress-tested advice
│       • generate_dashboard()    # HTML dashboard generation
│       • print_report()          # CLI text report
│       • add_cycle()             # Data management helpers
├── assets/
│   ├── dashboard.html           # Chart.js dashboard template
│   ├── demo_data.json           # Demo data for testing
│   └── demo_dashboard.html      # Pre-generated demo dashboard
└── references/
    ├── analysis_engine.md       # Analysis dimensions & algorithms
    ├── empathy_guide.md         # Empathetic interaction patterns
    ├── life_stages.md           # 7 life stage adaptation logic
    ├── medical_standards.md     # Evidence-based medical references
    └── user_profile.md          # Profile system design & questionnaires
```

## 🔬 Analysis Engine

The Python analysis engine (`scripts/analyze.py`) performs:

1. **Cycle Regularity** — mean, std, CV, trend slope (linear regression)
2. **Symptom Patterns** — frequency rate, severity trends, top symptoms
3. **Mood Analysis** — cycle-day correlated mood curves
4. **Smart Prediction** — exponential-decay weighted average + 3-mode recent pattern detection:
   - Mode 1: Significant deviation from historical mean
   - Mode 2: Recent cycles more regular than historical
   - Mode 3: Stable short-cycle pattern (28-35 days)
5. **Event Impact** — correlation between life events and cycle changes
6. **Health Alerts** — automatic flagging of concerning patterns

## 🎨 Dashboard

The HTML dashboard features:
- **Calendar Heatmap** — visualize 4+ years of cycle data
- **Cycle Trend Chart** — line chart with moving average
- **Symptom Radar** — multi-symptom frequency distribution
- **Mood Curve** — emotional patterns across cycle days
- **Prediction Timeline** — next period, ovulation, fertile window
- **Smart Insights** — personalized recommendations with severity levels

Color theme: soft purple/coral/green/pink on warm white background. Dark mode supported.

## 🩺 Medical Safety

- All recommendations undergo 3-round stress testing
- Medical referral suggestions are clearly labeled ⚕️
- No prescription drug recommendations
- Strict safety boundaries for pregnancy/postpartum
- Automatic alert detection for concerning patterns

**Disclaimer**: This tool provides health references based on data patterns. It does not replace professional medical diagnosis.

## 🤝 Contributing

Contributions welcome! Areas of interest:
- Additional symptom taxonomies
- More life stage adaptations
- i18n support
- Mobile PWA version

## ☕ Support

如果这个项目对你有帮助，欢迎请我喝杯咖啡：

<div align="center">
  <table>
    <tr>
      <td align="center"><img src="assets/donate/wechat-donate.jpg" width="200" alt="微信赞赏"/><br/>微信赞赏</td>
      <td align="center"><img src="assets/donate/alipay-donate.jpg" width="200" alt="支付宝赞赏"/><br/>支付宝赞赏</td>
    </tr>
  </table>
</div>

## 📄 License

MIT — see [LICENSE](LICENSE) for details.
