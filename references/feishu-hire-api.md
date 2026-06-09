# 飞书招聘 API 关键信息

## 基础概念
- **人才（Talent）**：`talent_id` 唯一标识
- **职位（Job）**：`job_id` 唯一标识
- **投递（Application）**：`application_id` 唯一标识，关联人才+职位+招聘流程

## 核心流程
职位发布 → 人才投递 → 评估 → 笔试 → 面试 → Offer → 入职

## 接入方式
1. 创建企业自建应用
2. 申请接口权限（招聘相关 scope）
3. 使用 `tenant_access_token` 鉴权
4. 在 API 调试台测试

## 相关 API 模块（需从 API 调试台确认具体接口）
- Talent — 候选人查询/管理
- Application — 投递管理/状态流转
- Interview — 面试创建/安排/评价
- Assessment — 评估/推评
- Job — 职位管理
- Offer — Offer 管理

## 面试安排可能需要的接口
- 创建面试（interview）
- 查询面试官日程
- 关联会议室
- 发送面试通知（事件回调）