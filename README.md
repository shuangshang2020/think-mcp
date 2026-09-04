# think-mcp

一个极小的 MCP 服务，用于在 Claude 回复前记录思考内容。

## 部署到 Zeabur

1. 在 GitHub 新建一个仓库（比如叫 `think-mcp`），把这三个文件推上去
2. 在 Zeabur 里新建一个服务，选 GitHub 仓库部署
3. Zeabur 会自动识别 Python 项目，启动命令是 `python main.py`
4. 部署完成后，在 Zeabur 的 Networking 里绑定一个域名（或用 Zeabur 自动生成的）
5. 记下这个域名，比如 `https://think-mcp-xxx.zeabur.app`

## 连接到 Claude

1. 打开 claude.ai → 设置 → MCP 工具（或在对话界面点工具图标）
2. 添加一个新的 MCP 连接
3. 名称随便填，比如 `think`
4. 类型选 SSE
5. URL 填 `https://你的域名/sse`
6. 保存，刷新页面

连接成功后，Claude 的工具列表里会多出一个 `think` 工具。
