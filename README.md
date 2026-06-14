# Clash 配置仓库

## 📁 目录结构

```
clashConfig/
├── subconverter/          # 订阅转换模板
│   ├── cfUnlimitedData.ini  # 无限流量套餐配置
│   ├── mantou.ini           # 馒头配置
│   ├── AI.list              # AI 服务规则列表
│   ├── Direct.list          # 直连规则列表
│   ├── ProxyLite.list       # 精简代理规则列表
│   └── README.md            # 订阅转换说明
└── smart/                 # Smart 规则
```

## 🚀 快速开始

### 在线订阅转换

使用 [ACL4SSR 在线转换](https://acl4ssr-sub.github.io/) 或 [subconverter](https://sub.xeton.dev/) 将订阅链接转换为 Clash 配置。

**转换地址格式：**
```
https://raw.githubusercontent.com/Thorwfj/clashConfig/refs/heads/main/subconverter/cfUnlimitedData.ini
```

## 📋 配置说明

### cfUnlimitedData.ini - 无限流量套餐

专为无限流量套餐设计的配置，包含以下节点分组：

| 策略组 | 说明 |
|--------|------|
| 🚀 节点选择 | 主策略组，可选择自动或手动 |
| ♻️ 自动选择 | url-test 自动测速，选择延迟最低节点 |
| 🇨🇳 电信节点 | 匹配：电信、China Telecom、CT |
| 🇨🇳 联通节点 | 匹配：联通、China Unicom、CU |
| 🇨🇳 移动节点 | 匹配：移动、China Mobile、CM |
| ⭐ 优选域名 | 匹配：CF、Cloudflare、Workers |
| 🌐 IPv6优选 | 匹配：IPv6 |
| 🐸 手动切换 | 手动选择任意节点 |

### 自动测速配置

```
测试地址: http://www.gstatic.com/generate_204
测试间隔: 300 秒（5分钟）
切换容差: 50 ms
```

## 🔧 自定义规则

### 规则集来源

- [ACL4SSR](https://github.com/ACL4SSR/ACL4SSR) - 综合规则集
- [blackmatrix7](https://github.com/blackmatrix7/ios_rule_script) - iOS 规则脚本

### 分流规则

| 策略组 | 用途 |
|--------|------|
| 🎯 全球直连 | 国内网站直连 |
| 🚀 节点选择 | 需要代理的网站 |
| 🤖 AI | AI 服务（ChatGPT、Claude 等） |
| 📹 YouTube | YouTube 视频 |
| 🍀 Google | Google 服务 |
| 📲 Telegram | Telegram 即时通讯 |
| 🎥 Netflix | Netflix 流媒体 |
| 🎮 游戏平台 | Steam、Epic 等游戏平台 |
| 🐟 漏网之鱼 | 未匹配规则的流量 |

## 📝 更新日志

- **2026-06-15** - 初始化仓库，添加订阅转换模板
