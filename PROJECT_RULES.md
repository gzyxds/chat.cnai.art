# 项目规范

## 1. 代码风格规范

### 1.1 JavaScript/TypeScript
- 使用 ESLint + Prettier 进行代码格式化
- 使用 2 个空格缩进
- 单引号优先
- 语句末尾加分号
- 使用 async/await 处理异步操作

### 1.2 React/Next.js
- 函数组件优先
- 使用 TypeScript 类型定义
- 组件命名采用 PascalCase
- 使用 React Hooks 管理状态
- 页面文件放置在 `app` 目录下

## 2. 数据库设计规范

### 2.1 PostgreSQL
- 表名使用小写字母，单词间用下划线分隔
- 主键字段命名为 `id`
- 外键字段命名为 `[table_name]_id`
- 时间戳字段使用 `created_at` 和 `updated_at`
- 使用 `timestamp without time zone` 存储时间

### 2.2 索引设计
- 主键自动创建索引
- 频繁查询的字段创建索引
- 联合索引考虑查询顺序

## 3. 部署流程规范

### 3.1 本地开发
1. 克隆项目
2. 安装依赖 `npm install`
3. 复制 `.env.example` 为 `.env` 并配置
4. 启动开发服务器 `npm run dev`

### 3.2 Docker 部署
1. 确保 Docker 已安装
2. 配置 `.env` 文件
3. 启动容器 `docker-compose up -d`
4. 访问 `http://localhost:3000`

## 4. 安全规范

### 4.1 认证授权
- 使用 NextAuth.js 进行身份验证
- 敏感信息使用 AES 加密
- 管理员操作需要验证权限

### 4.2 环境变量
- 敏感信息存储在 `.env` 文件中
- `.env` 文件不提交到版本控制
- 生产环境使用不同的密钥

### 4.3 数据库安全
- 使用强密码保护数据库
- 限制数据库访问IP
- 定期备份重要数据

## 5. 其他规范

### 5.1 Git 工作流
- 使用 Git Flow 工作流
- 功能分支命名规范 `feature/xxx`
- 提交信息使用英文描述

### 5.2 文档规范
- 使用 Markdown 编写文档
- 保持文档与代码同步
- 重要变更更新 CHANGELOG.md