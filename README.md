# Flova AI API Documentation

> Unofficial API documentation for [Flova.ai](https://www.flova.ai) - An AI-powered video creation platform.

**抓取时间**: 2026-04-23  
**来源**: https://www.flova.ai/zh-CN/v2/  
**警告**: 本文档由机器抓取生成，仅供学习研究参考，请勿用于非法用途。

---

## 目录

- [后端服务器](#后端服务器)
- [Firebase Auth API (v1)](#firebase-auth-api-v1)
- [Order/Payment API (v1)](#orderpayment-api-v1)
- [User API](#user-api)
- [Project API](#project-api)
- [Element API](#element-api)
- [Resource API](#resource-api)
- [Skill API](#skill-api)
- [Character API](#character-api)
- [Message/Chat API](#messagechat-api)
- [Auth API](#auth-api)
- [Feedback API](#feedback-api)
- [Model/Generator API](#modelgenerator-api)
- [Config API](#config-api)
- [CDN & Static Resources](#cdn--static-resources)

---

## 后端服务器

| 服务 | Base URL |
|------|----------|
| **gator** (主API) | `https://gator.uba.ap-southeast-1.volces.com` |
| **config** | `https://config.flova.ai` |
| **service API** | `https://service.flova.ai/api` |

---

## Firebase Auth API (v1)

**Base**: `https://gator.uba.ap-southeast-1.volces.com`

| 方法 | 端点 | 描述 |
|------|------|------|
| POST | `/v1/accounts:delete` | 删除账户 |
| POST | `/v1/accounts:lookup` | 查找账户 |
| POST | `/v1/accounts:sendVerificationCode` | 发送验证码 |
| POST | `/v1/accounts:signInWithCustomToken` | 自定义Token登录 |
| POST | `/v1/accounts:signInWithEmailLink` | 邮箱链接登录 |
| POST | `/v1/accounts:signInWithIdp` | 第三方身份提供商登录 |
| POST | `/v1/accounts:signInWithPassword` | 密码登录 |
| POST | `/v1/accounts:signInWithPhoneNumber` | 手机号登录 |
| POST | `/v1/accounts:signUp` | 注册 |
| POST | `/v1/token` | 获取Token |

---

## Order/Payment API (v1)

**Base**: `https://gator.uba.ap-southeast-1.volces.com`

| 方法 | 端点 | 描述 |
|------|------|------|
| POST | `/v1/orders/create-checkout-session` | 创建结账会话 |
| POST | `/v1/orders/create-portal-session` | 创建支付门户会话 |
| POST | `/v1/orders/create-subscription-checkout-session` | 创建订阅结账会话 |
| POST | `/v1/orders/preview-upgrade-subscription` | 预览升级订阅 |
| POST | `/v1/orders/refund_and_cancel` | 退款并取消 |
| POST | `/v1/orders/subscription-renewal-failure-info` | 订阅续费失败信息 |
| POST | `/v1/orders/unpaid-invoice-info` | 未支付账单信息 |
| POST | `/v1/orders/upgrade-subscription` | 升级订阅 |

---

## User API

**Base**: `https://gator.uba.ap-southeast-1.volces.com`

| 方法 | 端点 | 描述 |
|------|------|------|
| GET | `/v2/accounts/mfaEnrollment:start` | 启动MFA enrollment |
| POST | `/v2/accounts/mfaEnrollment:start` | 启动MFA enrollment |
| POST | `/v2/accounts/mfaSignIn:start` | 启动MFA登录 |
| POST | `/v2/accounts:revokeToken` | 撤销Token |
| GET | `/user/get_user_info` | 获取用户信息 |
| POST | `/user/update` | 更新用户信息 |
| POST | `/user/notifications/unread` | 获取未读通知 |
| POST | `/user/notifications/mark_read` | 标记通知已读 |
| POST | `/user/settings/get` | 获取用户设置 |
| POST | `/user/settings/update` | 更新用户设置 |
| POST | `/user/plan/credits/all` | 获取所有积分信息 |
| POST | `/user/plan/credits/obtain` | 获取积分 |
| POST | `/user/plan/credits/valid_v2` | 验证积分v2 |
| POST | `/user/plan/usage/consumption` | 积分消耗使用量 |
| POST | `/user/plan/usage/credits` | 积分使用量 |
| POST | `/user/free_quota_usage` | 免费配额使用情况 |
| POST | `/user/exploration_rewards` | 探索奖励 |

---

## Project API

**Base**: `https://gator.uba.ap-southeast-1.volces.com`

| 方法 | 端点 | 描述 |
|------|------|------|
| GET | `/v1/projects` | 获取项目列表 (v1) |
| GET | `/v2/projects` | 获取项目列表 (v2) |
| GET | `/v2/projects/` | 获取单个项目详情 |
| GET | `/project/list` | 项目列表 |
| POST | `/project/add` | 添加项目 |
| POST | `/project/get` | 获取项目 |
| POST | `/project/update` | 更新项目 |
| POST | `/project/delete` | 删除项目 |
| POST | `/project/copy` | 复制项目 |
| POST | `/project/export` | 导出项目 |
| POST | `/project/export_list` | 导出项目列表 |
| POST | `/project/export_resource` | 导出项目资源 |
| POST | `/project/export_resources` | 批量导出项目资源 |
| GET | `/project/export_status` | 导出状态 |
| POST | `/project/migrate` | 迁移项目 |
| POST | `/project/migrate_all` | 批量迁移项目 |
| GET | `/project/get_project_info` | 获取项目信息 |
| GET | `/project/project_revenue` | 项目收益 |
| GET | `/project/get_video_example` | 获取视频示例 |
| GET | `/project/get_video_example_feeds` | 获取视频示例流 |
| POST | `/project/input_status` | 输入状态 |
| POST | `/project/update_cover` | 更新项目封面 |
| GET | `/example/detail/` | 示例详情 |
| GET | `/example/detail?project_id=` | 按项目ID获取示例详情 |

---

## Element API

**Base**: `https://gator.uba.ap-southeast-1.volces.com`

| 方法 | 端点 | 描述 |
|------|------|------|
| POST | `/element/add` | 添加元素 |
| POST | `/element/add_resource` | 添加元素资源 |
| POST | `/element/get` | 获取元素 |
| POST | `/element/get_all` | 获取所有元素 |
| POST | `/element/get_list` | 获取元素列表 |
| POST | `/element/update` | 更新元素 |
| POST | `/element/delete` | 删除元素 |
| POST | `/element/delete_asset` | 删除元素资源 |
| POST | `/element/copy` | 复制元素 |
| POST | `/element/migrate` | 迁移元素 |

---

## Resource API

**Base**: `https://gator.uba.ap-southeast-1.volces.com`

| 方法 | 端点 | 描述 |
|------|------|------|
| POST | `/resource/get` | 获取资源 |
| POST | `/resource/list` | 资源列表 |
| POST | `/resource/list_by_ids` | 按ID列表获取资源 |
| POST | `/resource/create_resources` | 创建资源 |
| POST | `/resource/delete` | 删除资源 |
| POST | `/resource/favorite` | 收藏资源 |
| POST | `/resource/upload` | 上传资源 |
| POST | `/resource/upload_v2` | 上传资源v2 |
| POST | `/resource/upload_ticket` | 获取上传票据 |
| POST | `/resource/assign_asset_id` | 分配资源ID |
| POST | `/resource/alloc_new_asset_id` | 分配新资源ID |
| POST | `/resource/asset_resources` | 资产资源 |
| POST | `/resource/move_resource` | 移动资源 |
| POST | `/resource/move_asset` | 移动资产 |
| POST | `/resource/remove_asset` | 移除资产 |
| POST | `/resource/remove_resource_by_asset_id` | 按资产ID移除资源 |
| POST | `/resource/modify_description` | 修改资源描述 |
| POST | `/resource/modify_binding_role` | 修改绑定角色 |
| POST | `/resource/regenerate` | 重新生成 |
| POST | `/resource/redo` | 重做 |
| POST | `/resource/undo` | 撤销 |
| POST | `/resource/undo_redo_status` | 撤销/重做状态 |
| POST | `/resource/task_status` | 任务状态 |
| POST | `/resource/generate_video` | 生成视频 |
| POST | `/resource/generate_image` | 生成图片 |
| POST | `/resource/generate_audio` | 生成音频 |
| POST | `/resource/generate_music` | 生成音乐 |
| POST | `/resource/get_doubao_voice_list` | 获取豆包语音列表 |
| POST | `/resource/get_elevenlabs_voice_list` | 获取ElevenLabs语音列表 |
| POST | `/resource/add_shot` | 添加镜头 |
| POST | `/resource/remove_shot` | 移除镜头 |
| POST | `/resource/remove_from_shot` | 从镜头中移除 |
| POST | `/resource/fold_storyboard` | 折叠故事板 |
| POST | `/resource/operate_storyboard` | 操作故事板 |
| POST | `/resource/update_timeline` | 更新时间线 |
| POST | `/resource/update_document` | 更新文档 |

---

## Skill API

**Base**: `https://gator.uba.ap-southeast-1.volces.com`

| 方法 | 端点 | 描述 |
|------|------|------|
| GET | `/v2/skill` | 获取Skill列表 (v2) |
| GET | `/skill/list` | Skill列表 |
| GET | `/skill/list_public` | 公开Skill列表 |
| POST | `/skill/create` | 创建Skill |
| POST | `/skill/update` | 更新Skill |
| POST | `/skill/delete` | 删除Skill |
| POST | `/skill/copy` | 复制Skill |
| POST | `/skill/add_public` | 添加公开Skill |
| POST | `/skill/auto_modify_content` | 自动修改内容 |

---

## Character API

**Base**: `https://gator.uba.ap-southeast-1.volces.com`

| 方法 | 端点 | 描述 |
|------|------|------|
| GET | `/v2/characters` | 获取角色列表 (v2) |
| GET | `/characters` | 角色列表 |
| GET | `/profile/list` | 角色档案列表 |

---

## Message/Chat API

**Base**: `https://gator.uba.ap-southeast-1.volces.com`

| 方法 | 端点 | 描述 |
|------|------|------|
| POST | `/message/restore` | 恢复消息 |
| POST | `/message/enable_fast_generate` | 启用快速生成 |
| POST | `/message/query_fast_generate` | 查询快速生成 |
| POST | `/message/langsmith-url` | 获取LangSmith URL |
| POST | `/message/direct_chat/langsmith-url` | 获取直接聊天LangSmith URL |
| POST | `/stream_chat/direct_chat` | 直接聊天流 |
| POST | `/stream_chat/direct_chat_infos` | 直接聊天信息流 |

---

## Auth API

**Base**: `https://gator.uba.ap-southeast-1.volces.com`

| 方法 | 端点 | 描述 |
|------|------|------|
| POST | `/login` | 登录 |
| POST | `/logout` | 登出 |
| POST | `/google_login_v2` | Google登录v2 |
| POST | `/email_login` | 邮箱登录 |
| POST | `/email_login/send` | 发送邮箱验证码 |
| POST | `/sms_login` | 短信登录 |
| POST | `/sms_login/send` | 发送短信验证码 |
| POST | `/sms_login/bind/send_v2` | 发送绑定短信验证码v2 |
| POST | `/sms_login/bind/verify` | 验证绑定短信 |
| POST | `/invite/verify_and_use` | 验证和使用邀请码 |
| POST | `/enterprise/submit` | 提交企业认证 |

---

## Feedback API

**Base**: `https://gator.uba.ap-southeast-1.volces.com`

| 方法 | 端点 | 描述 |
|------|------|------|
| POST | `/feedback/submit` | 提交反馈 |
| POST | `/feedback/by_message_id` | 按消息ID提交反馈 |

---

## Model/Generator API

**Base**: `https://gator.uba.ap-southeast-1.volces.com`

| 方法 | 端点 | 描述 |
|------|------|------|
| GET | `/v2/generator` | 获取生成器 (v2) |
| POST | `/v2/generator` | 视频生成 (v2) |
| GET | `/v2/passwordPolicy` | 获取密码策略 |
| GET | `/v2/recaptchaConfig` | 获取reCAPTCHA配置 |
| POST | `/model/video_status` | 视频生成状态 |

---

## Config API

**Base**: `https://config.flova.ai`

| 方法 | 端点 | 描述 |
|------|------|------|
| GET | `?keys=...` | 获取配置项 |
| GET | `/service/2/abtest_config/` | A/B测试配置 |

---

## CDN & Static Resources

| 服务 | URL |
|------|-----|
| **静态资源** | `https://static.flova.ai` |
| **静态资源(CDN)** | `https://static-cdn-ap.flova.tv` |
| **S资源** | `https://s.flova.ai` |

---

## Web Frontend Routes

| 路由 | 描述 |
|------|------|
| `/` | 首页 |
| `/#explore` | 探索页 |
| `/account` | 账户页 |
| `/account/` | 账户详情页 |
| `/characters` | 角色库页 |
| `/generator` | 生成器页 |
| `/project` | 项目页 |
| `/projects` | 项目列表页 |
| `/projects/` | 项目详情页 |
| `/skill` | Skill页 |
| `/v2` | v2首页 |
| `/v2/characters` | v2角色页 |
| `/v2/generator` | v2生成器页 |
| `/v2/projects` | v2项目页 |
| `/v2/projects/` | v2项目详情页 |
| `/v2/skill` | v2 Skill页 |
| `/privacy-policy` | 隐私政策 |
| `/terms-of-service` | 服务条款 |

---

## 抓取方法说明

1. **静态分析**: 从网站Next.js构建产物中提取所有JS chunk
2. **正则匹配**: 在JS源码中搜索API路径模式
3. **动态Hook**: 通过浏览器DevTools Protocol hook `XMLHttpRequest` 和 `fetch`

---

## 免责声明

- 本文档仅供学习和研究使用
- Flova.ai 是其各自所有者的财产
- 请勿使用本文档进行任何非法活动

---

*Generated by Hermes Agent - 2026-04-23*
