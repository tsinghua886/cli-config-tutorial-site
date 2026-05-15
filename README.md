# CLI API 中转站配置教程

这是一个面向 Windows 用户的单页配置教程，用于生成、检查、测试和保存 Claude Code、Codex CLI、Gemini CLI 的第三方 API 中转站配置。

页面重点解决三个问题：

- 不确定第三方站点支持哪种协议时，可以通过 Base URL、API Key、模型名进行连通性测试。
- 不熟悉 CLI 配置格式时，可以通过表单自动生成对应配置。
- 需要长期维护多份中转站配置时，可以在浏览器本地保存、载入、重命名和删除配置。

项目是纯前端单页文件，不需要后端服务，也不需要安装依赖。

## 支持内容

当前页面包含两种模式：

- 详细版：适合首次配置或需要排查问题的用户，包含协议识别、Windows 步骤、配置生成器、API Key 连通性测试和保存列表。
- 精简版：适合已经了解流程的用户，用更短的步骤快速生成 Claude Code、Codex CLI、Gemini CLI 配置。

支持的 CLI：

- Claude Code：生成 Anthropic 兼容配置。
- Codex CLI：生成 OpenAI Responses API 兼容配置。
- Gemini CLI：生成 Gemini API 兼容环境变量命令。

## 使用方式

### 在线使用

如果已经启用 GitHub Pages，可以直接访问：

```text
https://tsinghua886.github.io/cli-config-tutorial-site/
