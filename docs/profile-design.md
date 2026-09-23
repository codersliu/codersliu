# 个人主页改造说明

## 调研与选择

调研日期：2026-09-23。目标是 GitHub Profile README，不修改独立博客。

| 参考 | 观察 | 本版选择 |
| --- | --- | --- |
| [Simon Willison 的主页](https://github.com/simonw/simonw) | 将正在做的项目与近期产出放在核心位置。 | 首屏定位，随后展示有具体实现内容的项目。暂不增加缺少公开数据源的自动动态。 |
| [Awesome GitHub Profile README](https://github.com/abhisheknaiidu/awesome-github-profile-readme) | 包含简洁、描述型、动态图与徽章等多种方向。 | 用简洁排版、项目叙述和原创视觉建立辨识度。 |
| [GitHub Readme Stats](https://github.com/anuraghazra/github-readme-stats) | 提供统计卡片。 | 当前公开仓库无法代表主要 Agent 工作，不以公开语言比例或 star 数作为能力证明。 |
| [Capsule Render](https://github.com/kyechan99/capsule-render) | 可生成 README 装饰横幅。 | 使用仓库内原创 SVG，主题与 Agent 执行流程一致，无远端图片服务依赖。 |
| [Metrics](https://github.com/lowlighter/metrics) | 通过工作流生成统计图。 | 删除本版不再使用的统计图与定时工作流，避免无效自动提交。 |
| [GitHub Profile README 文档](https://docs.github.com/en/account-and-profile/how-tos/profile-customization/managing-your-profile-readme) | 同名公开仓库中的根 README 展示在账号首页。 | 保持标准 Markdown / HTML / SVG，无构建与部署服务。 |

## 信息架构

1. 原创主题横幅：Agent Engineering，展示 TASK → TOOLS → VERIFY 执行流程。
2. 个人定位与导航：明确 Agent 工程、AI 开发工具、文档智能。
3. 独立实现项目：Agent Harness、ForgeX、Review Desk、Atlas；补充项目折叠展示。
4. 参与项目：WorkClaw 单独列出，避免将团队能力误归为个人成果。
5. 工程关注点与联系方式。

## 内容依据与边界

项目能力摘要来自各仓库当前 README；独立实现与参与开发的归属由本人确认。项目介绍不等于本次独立验证了这些项目的实现或运行效果。不添加未经证实的用户数、性能提升、开源贡献数或生产落地声明。

私有项目使用文字介绍，不给公众展示无法访问的源码链接，不复制私有源代码、内部环境、账号、密钥或配置。Atlas 与 Review Desk 保留当前验证边界。WorkClaw 暂未细分个人负责模块，因此仅声明参与开发并介绍项目背景。

原主页将 Agent Harness 描述为文档工具链；现按实际项目 README 更正为 Windows 桌面智能体执行框架。

## 维护

- 正文维护 `README.md`；四个主项目保持一致的「用途 / 实现 / 技术 / 必要边界」结构。
- 横幅位于 `assets/hero-light.svg` 与 `assets/hero-dark.svg`，由 `<picture>` 按系统颜色偏好选择；默认浅色图。
- 横幅只承担视觉定位，关键信息在正文也有文本表达，支持辅助阅读与移动端。
- 原统计图、统计工作流与第三方徽章不再使用；主页无需 token、定时任务或外部渲染服务。
- 后续有公开仓库、演示或文章时，为对应项目补充可访问的证据链接。
