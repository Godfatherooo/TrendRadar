<div align="center" id="trendradar">

<a href="https://github.com/sansan0/TrendRadar" title="TrendRadar">
  <img src="/_image/banner.jpg" alt="TrendRadar Banner" width="50%">
</a>

🚀 最快<strong>30秒</strong>部署的热点助手 —— 告别无效刷屏，只看真正关心的新闻资讯

<a href="https://trendshift.io/repositories/14726" target="_blank"><img src="https://trendshift.io/api/badge/repositories/14726" alt="sansan0%2FTrendRadar | Trendshift" style="width: 250px; height: 55px;" width="250" height="55"/></a>

[![GitHub Stars](https://img.shields.io/github/stars/sansan0/TrendRadar?style=flat-square&logo=github&color=yellow)](https://github.com/sansan0/TrendRadar/stargazers)
[![GitHub Forks](https://img.shields.io/github/forks/sansan0/TrendRadar?style=flat-square&logo=github&color=blue)](https://github.com/sansan0/TrendRadar/network/members)
[![License](https://img.shields.io/badge/license-GPL--3.0-blue.svg?style=flat-square)](LICENSE)
[![Version](https://img.shields.io/badge/version-v3.0.4-blue.svg)](https://github.com/sansan0/TrendRadar)
[![MCP](https://img.shields.io/badge/MCP-v1.0.1-green.svg)](https://github.com/sansan0/TrendRadar)

[![企业微信通知](https://img.shields.io/badge/企业微信-通知-00D4AA?style=flat-square)](https://work.weixin.qq.com/)
[![Telegram通知](https://img.shields.io/badge/Telegram-通知-00D4AA?style=flat-square)](https://telegram.org/)
[![dingtalk通知](https://img.shields.io/badge/钉钉-通知-00D4AA?style=flat-square)](#)
[![飞书通知](https://img.shields.io/badge/飞书-通知-00D4AA?style=flat-square)](https://www.feishu.cn/)
[![邮件通知](https://img.shields.io/badge/Email-通知-00D4AA?style=flat-square)](#) 
[![ntfy通知](https://img.shields.io/badge/ntfy-通知-00D4AA?style=flat-square)](https://github.com/binwiederhier/ntfy)


[![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-自动化-2088FF?style=flat-square&logo=github-actions&logoColor=white)](https://github.com/sansan0/TrendRadar)
[![GitHub Pages](https://img.shields.io/badge/GitHub_Pages-部署-4285F4?style=flat-square&logo=github&logoColor=white)](https://sansan0.github.io/TrendRadar)
[![Docker](https://img.shields.io/badge/Docker-部署-2496ED?style=flat-square&logo=docker&logoColor=white)](https://hub.docker.com/r/wantcat/trendradar)
[![MCP Support](https://img.shields.io/badge/MCP-AI分析支持-FF6B6B?style=flat-square&logo=ai&logoColor=white)](https://modelcontextprotocol.io/)

</div>


> 本项目以轻量，易部署为目标

## 📑 快速导航

<div align="center">

| [🎯 核心功能](#-核心功能) | [🚀 快速开始](#-快速开始) | [🐳 Docker部署](#-docker-部署) | [🤖 AI分析专区](#-ai-智能分析部署) |
|:---:|:---:|:---:|:---:|
| [📝 更新日志](#-更新日志) | [🔌 MCP客户端](#-mcp-客户端) | [❓ 答疑与常见问题](#问题答疑与1元点赞) | [⭐ 项目相关](#项目相关) |

</div>

- 感谢**耐心反馈 bug** 的贡献者，你们的每一条反馈让项目更加完善😉;  
- 感谢**为项目点 star** 的观众们，**fork** 你所欲也，**star** 我所欲也，两者得兼😍是对开源精神最好的支持;  
- 感谢**关注[公众号](#问题答疑与1元点赞)** 的读者们，你们的留言、点赞、分享和推荐等积极互动让内容更有温度😎。  

<details>
<summary>👉 点击查看<strong>致谢名单</strong> (当前 <strong>🔥49🔥</strong> 位)</summary>

### 数据支持

本项目使用了 [newsnow](https://github.com/ourongxing/newsnow) 项目提供的 API 接口获取多平台数据


### **全网热点聚合**

- 知乎
- 抖音
- bilibili 热搜
- 华尔街见闻
- 贴吧
- 百度热搜
- 财联社热门
- 澎湃新闻
- 凤凰网
- 今日头条
- 微博

默认监控 11 个主流平台，也可自行增加额外的平台

<details>

### **智能推送策略**

**三种推送模式**：

| 模式 | 适用人群 | 推送时机 | 显示内容 | 适用场景 |
|------|----------|----------|----------|----------|
| **当日汇总**<br/>`daily` | 📋 企业管理者/普通用户 | 按时推送(默认每小时推送一次) | 当日所有匹配新闻<br/>+ 新增新闻区域 | 日报总结<br/>全面了解当日热点趋势 |
| **当前榜单**<br/>`current` | 📰 自媒体人/内容创作者 | 按时推送(默认每小时推送一次) | 当前榜单匹配新闻<br/>+ 新增新闻区域 | 实时热点追踪<br/>了解当前最火的内容 |
| **增量监控**<br/>`incremental` | 📈 投资者/交易员 | 有新增才推送 | 新出现的匹配频率词新闻 | 避免重复信息干扰<br/>高频监控场景 |

**附加功能 - 推送时间窗口控制**（可选）：

此功能独立于上述三种推送模式,可与任意模式搭配使用:

- **时间窗口限制**: 设定推送时间范围（如 09:00-18:00 或 20:00-22:00）,只在指定时间内推送
- **推送频率控制**:
  - 窗口内多次推送: 时间窗口内每次执行都推送
  - 每天仅推送一次: 时间窗口内只推送一次（适合当日汇总或当前榜单模式）
- **典型场景**:
  - 工作时间推送: 只在工作日 09:00-18:00 接收消息
  - 晚间汇总推送: 希望在晚上固定时间（如 20:00-22:00）收到汇总
  - 避免打扰: 防止非工作时间收到推送通知

> 提示: 此功能默认关闭,需在 `config/config.yaml` 中手动启用 `push_window.enabled`

```

[![Star History Chart](https://api.star-history.com/svg?repos=sansan0/TrendRadar&type=Date)](https://www.star-history.com/#sansan0/TrendRadar&Date)


## 📄 许可证

GPL-3.0 License

---

<div align="center">

[🔝 回到顶部](#trendradar)

</div>
