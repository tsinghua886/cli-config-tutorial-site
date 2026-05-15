  # CLI API 中转站配置教程

  -一个面向 Windows 用户的单页教程，用于生成和保存 Claude Code、Codex CLI、Gemini CLI 的第三方 API 中转站配置。
  +这是一个面向 Windows 用户的单页配置教程，用于生成、检查、测试和保存 Claude Code、Codex CLI、Gemini CLI 的第三方 API
  中转站配置。
  +
  +页面重点解决三个问题：
  +
  +- 不确定第三方站点支持哪种协议时，可以通过 Base URL、API Key、模型名进行连通性测试。
  +- 不熟悉 CLI 配置格式时，可以通过表单自动生成对应配置。
  +- 需要长期维护多份中转站配置时，可以在浏览器本地保存、载入、重命名和删除配置。
  +
  +项目是纯前端单页文件，不需要后端服务，也不需要安装依赖。
  +
  +## 支持内容
  +
  +当前页面包含两种模式：
  +
  +- 详细版：适合首次配置或需要排查问题的用户，包含协议识别、Windows 步骤、配置生成器、API Key 连通性测试和保存列表。
  +- 精简版：适合已经了解流程的用户，用更短的步骤快速生成 Claude Code、Codex CLI、Gemini CLI 配置。
  +
  +支持的 CLI：
  +
  +- Claude Code：生成 Anthropic 兼容配置。
  +- Codex CLI：生成 OpenAI Responses API 兼容配置。
  +- Gemini CLI：生成 Gemini API 兼容环境变量命令。
  +
  +## 使用方式
  +
  +### 在线使用
  +
  +如果已经启用 GitHub Pages，可以直接访问：
  +
  +```text
  +https://tsinghua886.github.io/cli-config-tutorial-site/
  +```
  +
  +### 本地使用
  +
  +下载仓库后，直接用浏览器打开：
  +
  +```text
  +index.html
  +```
  +
  +页面是静态 HTML 文件，不需要运行服务器。
  +
  +## 配置流程
  +
  +一般建议按下面流程操作：
  +
  +1. 准备第三方 API 站点提供的 Base URL、API Key 和模型名。
  +2. 在页面中选择对应 CLI，或先使用自动识别功能判断站点支持的协议。
  +3. 填写表单并生成配置。
  +4. 复制生成的配置或命令，写入本机对应配置文件或环境变量。
  +5. 使用连通性测试确认 API Key、模型名和协议是否可用。
  +6. 可选：把当前配置保存到浏览器本地列表，方便下次快速载入。
  +
  +## 数据与隐私
  +
  +本页面不会主动把保存列表上传到服务器。
  +
  +需要注意：
  +
  +- 保存列表使用浏览器 `localStorage`，数据只保存在当前浏览器和当前站点域名下。
  +- 如果保存配置时包含 API Key，API Key 会留在本机浏览器存储中。
  +- 连通性测试会向你填写的第三方 Base URL 发起请求，用于确认 API Key 和模型是否可用。
  +- 不建议在公共电脑或不可信浏览器中保存真实 API Key。
  +
  +## 文件说明
  +
  +- `index.html`：网站主体文件，包含页面结构、样式和脚本。
  +- `README.md`：项目说明文档。
  +- `.gitignore`：忽略系统临时文件和日志文件。
  +
  +## GitHub Pages 发布
  +
  +仓库推送到 GitHub 后，可以这样发布：
  +
  +1. 打开 GitHub 仓库页面。
  +2. 进入 `Settings`。
  +3. 打开左侧 `Pages`。
  +4. `Source` 选择 `Deploy from a branch`。
  +5. `Branch` 选择 `main`，目录选择 `/root`。
  +6. 保存后等待 GitHub Pages 部署完成。

   ## 使用

  -直接打开 `index.html` 即可使用。页面内的保存列表使用浏览器本地存储，不会上传 API Key。
  +页面适合以下场景：
  +
  +- 新手按步骤配置 Claude Code、Codex CLI 或 Gemini CLI。
  +- 已经有中转站账号，但不确定 Base URL 应该填到哪一级路径。
  +- 需要在多个第三方站点或多个模型之间切换。
  +- 需要保存多份配置，避免反复手动输入。
  +
  +## 注意事项
  +
  +- 第三方站点必须明确支持对应协议，配置才可靠。
  +- Codex CLI 通常需要 OpenAI Responses API 兼容接口。
  +- Claude Code 通常需要 Anthropic Messages API 兼容接口。
  +- Gemini CLI 的自定义 Base URL 支持情况可能和 CLI 版本有关。
  +- 页面生成的配置应以第三方站点官方文档为最终准则。

   ## 版权

  -Copyright (c) flower
  +Copyright (c) flower.
  +
  +本项目由 flower 维护。未经授权，请勿删除页面和文档中的版权信息。
