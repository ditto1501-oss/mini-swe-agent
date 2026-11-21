# Mini SWE Agent

一个以学习为目的、从零逐步实现的 Mini SWE Agent 项目。重点是理解 SWE Agent 的底层原理、系统架构和运行机制，并保留学习者自主思考与编程实践的空间。

## 当前状态

- 当前阶段：建立跨设备开发与上下文同步机制。
- 仓库尚无 Mini SWE Agent 核心代码，也没有可运行入口、依赖清单或自动化测试。
- 编程语言、模型服务、依赖管理、工具执行方式和整体架构均待讨论确认。
- 最新任务与待确认事项见 [PROGRESS.md](PROGRESS.md)。

## 跨设备协作

Windows 和 macOS 上的 Codex 对话彼此独立。GitHub 仓库是共享代码、开发进度和已记录决策的唯一事实来源，不依赖 Codex 原生 Handoff 或聊天记录同步。

本地尚未提交、推送的内容不代表另一台设备已经收到。同步时需同时确认本地文件、提交记录和远程分支状态。

| 文件 | 用途 |
| --- | --- |
| [AGENTS.md](AGENTS.md) | 两端 Codex 共同遵守的开发与同步规则 |
| [PROGRESS.md](PROGRESS.md) | 当前阶段、已完成事项、待办、问题与下一步 |
| [docs/DEVLOG.md](docs/DEVLOG.md) | 按时间追加的讨论、决策、实验和交接记录 |

## 开始使用

在本机项目目录中先检查工作区与关联信息。以下 Git 命令适用于 macOS 终端、Windows PowerShell 和 Git Bash：

```text
git status --short --branch
git branch -vv
git remote -v
git log -5 --oneline
```

工作区干净、分支及上游正确、没有冲突时，再执行：

```text
git pull --ff-only
```

随后阅读 `AGENTS.md`、`README.md`、`PROGRESS.md` 和相关开发日志，再决定下一步。遇到未提交修改、分支分叉或记录不一致时，先告知用户并处理，不能覆盖已有成果。

当前没有安装或运行 Agent 的命令；待首个可运行模块经讨论并实现后，再补充实际验证过的说明。

## 结束或切换设备

更新进度与日志，检查变更及敏感信息，展示变更摘要并准备 commit message。只有获得用户明确授权后，才执行 `git commit` 与 `git push`。

远程同步完成后，另一端在工作区干净时执行 `git pull --ff-only`，并通过仓库文档恢复上下文。完整规则见 `AGENTS.md`。
