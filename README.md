# QuantPulse Pro（QPP）📈

微信小程序 · 金融理财教育工具，基于微信云开发（云函数 + 云数据库）。

[![GitHub stars](https://img.shields.io/github/stars/people-you-and-me/people-dev?style=social)](https://github.com/people-you-and-me/people-dev)

> 小程序链接：`#小程序://QPULSE/STkGC3kJ1oGLIdg` ｜ AppID：`wx800c9911501eaa55`

## 📱 演示

**扫码体验**（用微信「扫一扫」识别小程序码）：

<p align="center">
  <img src="docs/images/miniprogram-code.png" width="220" alt="小程序码"/>
</p>

**界面截图**：

<p align="center">
  <img src="docs/images/screenshot-home.png" width="200" alt="市场页"/>
  <img src="docs/images/screenshot-invest.png" width="200" alt="学习/投资页"/>
  <img src="docs/images/screenshot-quiz.png" width="200" alt="风险问卷页"/>
</p>

> ⚠️ 以上二维码与截图目前为**占位图**，请替换 `docs/images/` 下的同名文件为真实素材（生成方法见文末 [添加演示素材](#添加演示素材)）。

## ✨ 功能

- **市场**：基金 / 股票 / 金融概念检索、每日市场简报
- **学习**：投资模拟盘、金融概念知识库
- **风险问卷**：10 题风险评估，输出评分与资产配置建议
- **我的**：手机号登录、收藏、点赞、个人资料

## 🛠 技术栈

- 前端：微信小程序原生（WXML / WXSS / JavaScript）
- 后端：微信云开发 —— 云函数（Node.js）+ 云数据库

## 📂 目录结构

```
QuantPulse-Pro/
├── miniprogram/                    # 小程序前端
│   ├── app.js / app.json / app.wxss
│   ├── pages/                      # 8 个页面
│   │   ├── login/                  # 登录
│   │   ├── index/                  # 市场
│   │   ├── invest/                 # 学习 / 投资模拟
│   │   ├── mine/                   # 我的
│   │   ├── quiz/ quiz-result/      # 风险问卷
│   │   ├── brief-detail/           # 市场简报详情
│   │   └── concept-detail/         # 金融概念详情
│   ├── custom-tab-bar/             # 自定义底部导航
│   ├── styles/                     # 设计变量
│   └── utils/                      # API 封装、图标、题库、时间工具
├── cloudfunctions/                 # 云函数（Node.js）
│   ├── login/ getUserProfile/      # 登录与用户资料
│   ├── searchFund/                 # 基金检索
│   ├── searchStock/                # 股票检索
│   ├── searchFinanceConcept/       # 金融概念检索（含知识库）
│   ├── getMarketBrief/             # 市场简报
│   ├── getAssessments/             # 获取风险评估
│   ├── saveAssessment/             # 保存风险评估
│   └── getMyLikes/                 # 我的点赞
├── docs/                           # 设计文档、实现计划与演示素材
├── project.config.json             # 微信开发者工具工程配置
└── project.private.config.json
```

## 🚀 如何运行

1. 下载并安装[微信开发者工具](https://developers.weixin.qq.com/miniprogram/dev/devtools/download.html)。
2. 导入项目：选择本目录，AppID 填 `wx800c9911501eaa55`（或使用自己的测试号）。
3. 开通云开发（开发者工具 → 云开发 → 创建环境），并创建所需的云数据库集合。
4. 对每个云函数右键 →「上传并部署：云端安装依赖」。
5. 编译运行。

## 🧩 云函数

| 云函数 | 说明 |
| --- | --- |
| `login` | 手机号登录 |
| `getUserProfile` | 获取用户资料 |
| `searchFund` / `searchStock` | 基金 / 股票检索 |
| `searchFinanceConcept` | 金融概念检索（含内置知识库） |
| `getMarketBrief` | 每日市场简报 |
| `getAssessments` / `saveAssessment` | 风险评估问卷的读取与保存 |
| `getMyLikes` | 我的点赞 |

> 云函数依赖 `wx-server-sdk`（见各 `cloudfunctions/*/package.json`）。部署时选择「云端安装依赖」即可自动安装，无需手动上传 `node_modules`。

## 📝 添加演示素材

**小程序码**（`docs/images/miniprogram-code.png`）：

1. 登录[微信公众平台](https://mp.weixin.qq.com) → 你的小程序
2. 左侧「设置」→「基本设置」→ 找到「小程序码」，点击「下载」或截图
3. 重命名为 `miniprogram-code.png`，替换 `docs/images/` 下同名文件

**界面截图**（`docs/images/screenshot-*.png`）：

1. 微信开发者工具打开项目 → 编译预览
2. 使用工具自带「截图」功能，或真机预览后手机截图
3. 分别替换 `screenshot-home.png` / `screenshot-invest.png` / `screenshot-quiz.png`

## 📄 许可证

（待补充，建议选择 MIT License）

---

<p align="center">
  <sub>📎 分享 / 扫码直达仓库</sub><br/>
  <img src="docs/images/qrcode-github.png" width="150" alt="GitHub 仓库二维码"/>
</p>
