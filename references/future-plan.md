# 招聘流程自动化 — 后续规划（待启动）

## 当前已实现
- ✅ **Pretalk 笔记格式化** — 输入自由文本 → 输出 9 字段模板

## 待实现功能

### 推评（推评文案生成）
- pretalk 模板 + 简历内容 → 生成推评文案
- 简历来源：PDF/Word/飞书链接/文字粘贴
- 输出：候选人优势 + 意向程度 + 推评建议

### 面试安排（自动化）
- 接入飞书招聘网页，通过 Playwright 自动化操作
- 流程：确认推评通过 → 查面试官时间 → 订会议室 → 填面试信息

### 技术选型
- 走**浏览器自动化**路线（Playwright），不依赖飞书 API 权限
- 原因是：无飞书开发者权限，无法创建企业内部应用

### 飞书开放平台参考
- 招聘 API 文档：`https://open.feishu.cn/document/server-docs/hire-v1/recruitment-development-guide`
- 有 Markdown 版本（.md 后缀），适合 AI 读取
- 核心模块：Talent / Application / Interview / Assessment / Job / Offer
- 如果后续 IT 开了权限，可改用 API 直调更稳定

### 保存时间
- 2026-06-09：确定路线为浏览器自动化，暂缓推进