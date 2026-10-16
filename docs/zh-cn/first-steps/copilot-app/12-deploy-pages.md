---
title: "第 12 课 - 使用 GitHub Pages 部署网站"
description: "使用 GitHub Copilot app 配置 Pages 工作流、审查拉取请求，并验证已发布的 Space Quiz。"
authors:
  - jamesmontemagno
lastUpdated: 2026-10-12
---

将 Space Quiz 部署到 GitHub Pages，为它提供公开访问地址。Copilot 可以准备工作流并引导部署，但你仍需审查更改并确认网站已上线。

本课将完成以下操作：

- 请求 Copilot 配置 GitHub Pages 部署。
- 在合并前审查工作流和拉取请求。
- 跟进部署过程并验证已发布的网站。

## 场景

Space Quiz 已在 GitHub 存储库中，但其他人还没有便捷的体验方式。使用 GitHub Pages 发布这个单文件网站后，用户可以通过公开 URL 访问它，无需添加服务器或运行时依赖项。

## 请求 Copilot 部署网站

在 `space-quiz` 的 Copilot app 会话中发送以下提示：

```plaintext
为此存储库启用 GitHub Pages。创建一个 GitHub Actions 工作流，在需要时构建网站并将其部署到 GitHub Pages。如果尚无 README，请添加一个说明应用和本地运行方法的 README。根据这些更改创建拉取请求，并在必需检查通过后合并。持续监控部署，直到成功，然后报告网站的最终访问 URL。如果你没有权限启用 Pages 或合并拉取请求，请准确说明我需要批准或执行的操作；网站上线前不要报告成功。
```

![三阶段示意图：已合并的 space-quiz 拉取请求；GitHub Actions Deploy website 运行成功，其中包含 Build website、Upload artifact 和 Deploy to Pages 步骤；以及通过 yourname.github.io/space-quiz/ 访问的已发布 Space Quiz。](../../../_images/first-steps-app-pages-deploy.svg)

> [!WARNING]
> 此提示要求智能体创建并合并拉取请求，以及更改存储库的 Pages 设置。继续之前，请审查 diff、部署权限和 GitHub 发出的任何审批请求。

## 审查工作流并验证部署

1. 确认仅当存储库尚无 README 时才添加 README。
2. 审查拉取请求中的更改，包括工作流的构建和部署步骤。
3. 仅在拉取请求的必需检查通过后合并。
4. 跟进 GitHub Actions 部署运行，直到成功。
5. 打开报告的 URL，确认 Space Quiz 已加载。

如果智能体无法启用 Pages 或合并拉取请求，请按它提供的具体说明操作。只有部署成功且网站可以正常加载后，才能将任务视为完成。

## 总结和后续步骤

现在，Space Quiz 已作为网站发布。你也亲自验证了部署，而不是只依赖智能体的报告。接下来学习[第 13 课：回顾与后续步骤][next-lesson]。

[next-lesson]: ../13-review/
