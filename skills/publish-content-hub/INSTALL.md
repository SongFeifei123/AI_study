# publish-content-hub Skill

这个 Skill 用于把图片、PDF、文档、技术笔记等资料发布到固定的
[`AI_study`](https://github.com/SongFeifei123/AI_study) Git 仓库。

## 包含文件

```text
publish-content-hub/
|-- SKILL.md
`-- agents/
    `-- openai.yaml
```

旧版网站发布脚本没有包含在此包中，因为当前 Skill 只操作 Git 仓库，不负责构建或部署网站。

## 安装到多个 Agent

每个需要使用该能力的 Agent 环境，都把整个 `publish-content-hub` 文件夹复制到其 Codex skills 目录：

```text
<CODEX_HOME>/skills/publish-content-hub/
```

Windows 默认位置通常是：

```text
%USERPROFILE%\.codex\skills\publish-content-hub\
```

macOS/Linux 默认位置通常是：

```text
~/.codex/skills/publish-content-hub/
```

如果多个 Agent 共用同一个 `CODEX_HOME`，只需安装一次；如果各 Agent 使用隔离的 Home 或运行主机，则分别复制一次。安装后新建任务，或重启需要重新发现 Skill 的 Agent 会话。

## 运行前提

- 本机已有仓库检出目录 `D:\00CodexWarkSpace\publish`。
- 仓库的 `origin` 指向 `git@github.com:SongFeifei123/AI_study.git`。
- 工作分支为 `main`，并且运行 Agent 具备 Git push 权限。
- 如果目标 Agent 使用其他操作系统或仓库路径，需要先修改 `SKILL.md` 中的本地检出路径。

## 调用示例

```text
使用 $publish-content-hub，把这份 vLLM 分析笔记发布到 AI_study 仓库。
```

Skill 默认允许自动发现；也可以通过 `$publish-content-hub` 显式调用。
