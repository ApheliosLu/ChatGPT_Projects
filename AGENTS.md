# ChatGPT_Projects 项目指南

## 项目定位与当前状态

本仓库用于学习和实践 Codex 驱动的 VibeCoding。当前仅有初始 Git 提交；尚未初始化应用代码，也没有 `package.json`、`src/`、构建、lint 或测试命令。

开始实现前，先说明将采用的结构、依赖和验证方式；不要假设已有可运行的项目或命令。初始化完成后，及时把实际命令和目录结构更新到本文件。

## 计划技术栈

除非用户另有指定，首次搭建 Web 应用时使用：

- Next.js 14、TypeScript、Tailwind CSS
- Next.js API Routes
- Prisma + SQLite
- Vercel（仅在用户明确要求部署时使用）

## 代码约定（代码落地后适用）

- 使用函数式 React 组件和 Hooks。
- React 组件文件使用 PascalCase；工具函数使用 camelCase。
- API 路由统一返回 `{ success: boolean, data?: unknown, error?: string }`。
- 数据库访问统一经由 Prisma Client。
- 不提交 `.env` 或 `prisma/dev.db`；任何密钥、生产配置或 CI/CD 配置的改动必须先征得用户同意。

## 工作方式

- 个人协作偏好、Git 和依赖安装规则由 `C:\\Users\\q1209\\.codex\\AGENTS.md` 统一定义；本文件仅补充本仓库规则。
- 新功能开发需要隔离时，先说明建议的 `codex/` 分支名和原因，获得用户同意后再创建。
- 任务命中仓库内 `.agents/skills/` 的技能时，先读取并遵循其 `SKILL.md`。
- 修改行为或修复问题前，先进行必要的需求澄清和设计；实现时采用测试优先；报告完成前提供实际验证结果。
