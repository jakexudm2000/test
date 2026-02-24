# Test Repository

这是一个测试仓库，用于演示和测试 [opencode](https://github.com/anomalyco/opencode) GitHub Actions 集成。

## 项目简介

本仓库集成了 `opencode` GitHub Action，这是一个 AI 驱动的编程助手。当用户在 Issue 或 Pull Request 的评论中使用 `/oc` 或 `/opencode` 指令时，AI 助手会自动响应并根据需求生成或修改代码。

## 功能

- **AI 编程助手**：通过在评论中输入 `/oc <描述>` 或 `/opencode <描述>`，自动触发 AI 完成编码任务。
- **Issue 驱动开发**：支持基于 Issue 描述自动生成代码并创建 Pull Request。
- **Pull Request 审查**：在 PR 评论中使用指令，AI 助手可对代码进行修改和优化。

## 使用方法

1. 在任意 Issue 或 Pull Request 中添加评论。
2. 评论内容以 `/oc` 或 `/opencode` 开头，后跟具体的任务描述。
3. GitHub Actions 工作流会自动触发，AI 助手将完成相应的编码工作。

### 示例

```
/oc 为该项目添加一个 Hello World Python 脚本
```

```
/opencode 修复登录功能中的 bug
```

## 工作流配置

本仓库使用 `.github/workflows/opencode.yml` 配置工作流，监听 Issue 评论和 PR 审查评论事件，并使用 `anomalyco/opencode` Action 执行任务。

所用 AI 模型：`anthropic/claude-sonnet-4-20250514`
