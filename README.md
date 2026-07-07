# wxcloud-to-ecs-skills

微信云开发迁移阿里云 ECS / CloudBase 迁移自建服务器 / 小程序云函数迁移 / 微信小程序云开发迁移 / TCB 迁移后端服务。

Keywords: WeChat Mini Program, CloudBase, TCB, Aliyun ECS, cloud function migration, self-hosted backend, Codex Skills.

本仓库旨在提供一套通用的迁移方法论，协助开发者将依赖微信小程序云开发（Cloudbase/TCB）的项目，逐步迁移至 ECS 或其他自建服务器架构。

本仓库重点在于**迁移方法与路径规划**，不包含具体业务逻辑。

---

## 仓库目标

通过沉淀可复用的迁移流程，覆盖以下关键环节：

* **现状评估**：盘点当前云开发使用情况。
* **架构设计**：规划目标自建架构。
* **后端迁移**：将云函数改造为常规后端服务（API）。
* **前端改造**：实现前端从云调用向自建 API 的平滑切换。
* **基础服务替换**：梳理文件存储、数据库、定时任务及用户鉴权等能力的替代方案。
* **风险控制**：制定联调、灰度发布及应急回滚清单。

## 适用场景

适用于深度依赖以下云开发能力的小程序项目：

* 云函数（Cloud Functions）
* 云数据库（Cloud Database）
* 云存储（Cloud Storage）
* 定时触发器及后台任务
* 基于云开发构建的微信登录体系

## 迁移核心原则

* **评估先行**：先盘点、再设计、后迁移。
* **契约优先**：优先保持前端调用接口契约的稳定性。
* **明确收口**：迁移期间允许使用兼容层（适配器），但必须明确代码边界。
* **环境隔离**：确保本地调试与正式生产环境的流量彻底隔离。
* **安全交付**：切流前必须具备完善的验证清单和明确的回滚路径。

## 技能组件 (Skills)

* `wxcloud-project-audit`：审计云开发现状并生成迁移资产清单。
* `wxcloud-architecture-design`：设计目标架构及 ECS 承载方案。
* `wxcloud-function-migration`：云函数至常规后端服务的迁移指南。
* `wxcloud-frontend-cutover`：前端请求层改造、自测与灰度切流实施方案。

## 核心文档

* `docs/migration-principles.md`：通用迁移原则指南。
* `docs/migration-checklist.md`：生产环境迁移验证与回滚标准清单。
