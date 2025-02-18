# keep_coding_blog
***
基于 GO (Gin/Gorm) + PgSql + JavaScript (Vue) 搭建的简单的博客网站。

**目标:**

*   练习 Go 在 web 方向的 REST API 开发。
*   构建个人小型博客网站，用于发布计算机相关技术的学习总结。

***
### 博客系统改进方案 - 2025-02-18

#### 1. 安全性增强

##### 1.1 认证与授权
###### 1.1.1 完善 JWT Token 机制
```
- ✅增加 refresh token 机制
- ✅添加 token 黑名单
- ✅优化 token 过期时间配置
```

###### 1.1.2 增强 RBAC 系统
```
- ❌完善现有的 Role 字段实现
- ❌添加权限粒度控制
- ❌实现动态权限管理
```

###### 1.1.3 安全防护
```
- ❌实现登录失败次数限制
- ❌添加敏感操作二次验证
- ❌实现会话管理机制
```

##### 1.2 数据安全
###### 1.2.1 数据加密
```
- ❌优化密码加密存储(已实现 bcrypt)
- ❌实现敏感信息加密
- ❌添加数据传输加密
```

###### 1.2.2 输入验证
```
- ❌增强 API 参数验证
- ❌实现内容安全过滤
- ❌添加文件上传验证
```

###### 1.2.3 安全配置
```
- ❌优化 CORS 配置
- ❌实现安全响应头
- ❌添加 Rate Limiting
```

#### 2. 性能优化

##### 2.1 缓存系统
###### 2.1.1 数据缓存
```
- ❌实现热门文章缓存
- ❌添加用户信息缓存
- ❌优化标签查询缓存
```

###### 2.1.2 查询优化
```
- ❌优化 Post 查询性能
- ❌改进评论加载策略
- ❌实现分页缓存
```

##### 2.2 数据库优化
###### 2.2.1 索引优化
```
- ❌优化现有表索引
- ❌添加复合索引
- ❌实现搜索优化
```

###### 2.2.2 连接管理
```
- ❌优化数据库连接池配置
- ❌实现读写分离
- ❌添加数据库监控
```

#### 3. 功能扩展

##### 3.1 内容管理
###### 3.1.1 文章功能
```
- ❌添加文章草稿功能
- ❌实现文章审核流程
- ❌添加文章统计功能
```

###### 3.1.2 评论功能
```
- ❌实现评论嵌套回复
- ❌添加评论通知功能
- ❌实现评论审核机制
```

##### 3.2 用户系统
###### 3.2.1 账户安全
```
- ❌实现邮箱验证
- ❌添加密码重置功能
- ❌实现账户注销功能
```

###### 3.2.2 用户互动
```
- ❌实现用户关注功能
- ❌添加收藏功能
- ❌实现消息通知系统
```

#### 4. 可观测性

##### 4.1 日志系统
###### 4.1.1 日志完善
```
- ❌扩展现有 logrus 实现
- ❌添加操作审计日志
- ❌实现日志分级存储
```

###### 4.1.2 监控告警
```
- ❌实现异常监控
- ❌添加性能监控
- ❌实现业务监控
```

###### 4.2 诊断工具
###### 4.2.1 调试功能
```
- ❌实现请求跟踪
- ❌添加性能分析
- ❌实现健康检查
```