# 扒人 Â· 六路采集工具

> 输入一个人名/主题名，6 路并行采集信息，父进程汇总后直接呈现。

---

## 安装配置

### 1. 配置搜索 API

默认使用 Tavily 搜索。先获取 API Key（https://tavily.com/#api），然后告诉 Agent：

```
> 帮我配置 Tavily 搜索，API Key 是: sk-xxx...
```

Agent 会自动完成配置，无需手动编辑配置文件。

### 2. 配置 Chrome 调试端口（登录平台用）

采集小红书、微博等需登录的平台，需开启 Chrome 远程调试：

```
# 1. 完全关闭所有 Chrome 窗口
# 2. 按 Win+R，输入以下命令后回车：
"C:\Program Files\Google\Chrome\Application\chrome.exe" --remote-debugging-port=18800 --remote-allow-origins=*
# 3. Chrome 启动后，登录需要采集的平台（小红书/微博等）
# 4. 登录完成后告诉 Agent：Chrome 已登录小红书
```

> â ï¸ Chrome 148+ 需加 --user-data-dir 参数
> --user-data-dir="C:\Users\你的用户名\AppData\Local\Google\Chrome\User Data"

---

## 一句话用法

```
> 六路采集 Elon Musk
> 六路采集 特朗普
```

## 采集维度

| # | 维度 | 说明 |
|---|------|------|
| 1 | 著作/论文 | 学术出版、研究报告、专栏文章 |
| 2 | 播客/访谈 | 播客节目、视频访谈、公开演讲 |
| 3 | 社交媒体 | 小红书/B站/知乎/抖音/微博内容分析 |
| 4 | 批评者视角 | 争议、质疑、反驳观点 |
| 5 | 决策/成就记录 | 关键决策、重大事件、荣誉奖项 |
| 6 | 时间线 | 全量信息的时间排序 |

---

> 详细操作指引见 SKILL.md

Powered by OpenClaw