# wxcloud-to-ecs-skills

> 默认中文。This repository is Chinese-first, with a short English summary for international readability.

这是一个面向 **微信小程序云开发（Cloudbase / TCB）迁移** 场景的通用 skills 仓库。

它的目标不是记录某个具体项目的业务实现，而是沉淀一套可复用的迁移方法，帮助开发者将依赖云开发的小程序，逐步迁移到 **ECS 或其他自建服务器架构**。

## 仓库用途

本仓库用于指导以下迁移工作：

- 盘点当前云开发使用面
- 设计目标自建架构
- 将云函数迁移为常规后端服务或 API
- 将前端从云调用切换到自建 API
- 梳理文件、数据、任务、鉴权等平台能力替换关系
- 给出联调、灰度和回滚清单

它关注的是 **迁移方法**，不是某一个业务项目的细节。

## 适用范围

适用于包含以下一种或多种能力的微信小程序项目：

- 云函数
- 云数据库
- 云存储
- 定时触发器或后台任务
- 基于微信登录态的用户体系

## 核心原则

- 先盘点，再设计，再迁移
- 优先保持前端调用契约稳定
- 迁移期允许兼容壳，但必须明确收口
- 本地调试与正式流量必须隔离
- 切流前必须具备验证清单和回滚路径

## 当前 Skills

- `wxcloud-project-audit`：审计云开发使用现状并产出迁移清单
- `wxcloud-architecture-design`：设计目标架构与承载方案，包括 ECS 落位建议
- `wxcloud-function-migration`：指导云函数迁移为常规后端服务
- `wxcloud-frontend-cutover`：指导前端请求层切换、自测与灰度切流

## 文档

- `docs/migration-principles.md`：通用迁移原则
- `docs/migration-checklist.md`：通用验证与回滚清单

## English Summary

`wxcloud-to-ecs-skills` is a generic skills repository for migrating WeChat Mini Program projects from Cloudbase / TCB to self-hosted infrastructure such as ECS or other server-based architectures.

It focuses on migration methodology rather than project-specific business logic, including:

- auditing current cloud usage,
- designing the target architecture,
- migrating cloud functions into standard backend services,
- cutting frontend traffic over to self-hosted APIs,
- and validating rollout and rollback paths.
