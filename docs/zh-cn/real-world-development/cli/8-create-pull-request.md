---
title: "第 8 课 - 创建并合并功能拉取请求"
description: "一起审查筛选功能、说明、技能更新、QA 配置文件和测试，然后创建拉取请求并使用 Agent Merge。"
authors:
  - geektrainer
lastUpdated: 2026-09-18
---

筛选功能实现、说明更新、技能更新、质量保证 (QA) 配置文件和测试都保存在同一个分支中。现在可以一起审查这些更改并创建拉取请求了。星级评分拉取请求 (PR) 是你亲自合并的；这次将由 **Agent Merge** 管理合并流程。

> [!NOTE]
> 通常会将功能、说明更新、技能更新和 QA 智能体拆分到几个独立的 PR 中。为了简化研讨会流程，你将整个筛选和质量工作流保留在同一个会话和分支中，并通过此 PR 提交所有更改。

本课将完成以下任务：

- 了解 Agent Merge 及其如何自动执行合并生命周期。
- 检查完整的功能更改和验证证据。
- 创建筛选功能 PR。
- 仅在审查后启用 Agent Merge，并确认 PR 已合并。

## 场景

在整个筛选工作流中，你使用 Copilot 规划、实现并验证了一项功能。Tailspin Toys 现在希望自动处理剩余的 PR 工作，同时由开发者掌控合并授权。

## 认识 Agent Merge

**Agent Merge** 会自动完成合并拉取请求所需的剩余工作。启用后，Copilot 会处理阻止 PR 合并的问题，例如修复失败的持续集成 (CI) 检查、回复审查意见，以及在需要时变基；之后，如果存储库允许，它会启用 GitHub 自动合并。

到目前为止，都是由你亲自选择 **Merge pull request**。Agent Merge 可以接手这项工作。启用之前，请先审查更改并确认它们已准备就绪。

## 使用 Agent Merge 管理 PR

所有代码都已完成。现在一起审查更改、创建 PR，并让 Agent Merge 管理后续流程。

1. 返回 Codespace。
2. 输入 `/agent` 打开智能体对话框。
3. 在选项列表中选择 **Default**，然后按 <kbd>Enter</kbd>。
4. 使用命令 `/pr create` 创建新的 PR。
5. 使用 `/pr agentmerge` 启用 Agent Merge。
6. Copilot 会监视 PR 的持续集成流程。所有检查通过后，它会执行合并。
7. 确认 Copilot 显示类似 `"PR #14 was squash-merged successfully."` 的消息。

> [!IMPORTANT]
> Agent Merge 不会绕过必需的审批、分支保护、合并队列、存储库设置或缺失的权限。如果合并受阻，请查看报告的原因；在存储库允许的情况下，完成审查后手动合并。

## 总结和后续步骤

你已自动化开发流程中的多个部分，包括生成代码、测试和验证代码，现在还包括拉取请求流程。本课中，你：

- 了解了 Agent Merge 及其如何自动执行合并生命周期。
- 检查了完整的功能更改和验证证据。
- 创建了筛选功能 PR。
- 在审查后启用了 Agent Merge，并确认 PR 已合并。

接下来，[探索其他实用的 Copilot CLI 斜杠命令][next-lesson]，了解上下文、模型、共享和可选的云端委派。

## 资源

- [使用 Copilot CLI 管理拉取请求][manage-prs]
- [Copilot CLI 命令参考][cli-reference]

[previous-lesson]: ../7-qa-agent/
[next-lesson]: ../9-cli-power-tools/
[manage-prs]: https://docs.github.com/copilot/how-tos/copilot-cli/use-copilot-cli/manage-pull-requests
[cli-reference]: https://docs.github.com/copilot/reference/copilot-cli-reference/cli-command-reference
