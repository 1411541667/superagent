# superagent

这个仓库由 **Super-agent**（dsh-superagent）托管：Router 轮询 GitHub 事件，Worker 在隔离的
worktree 里干活，产出分支 `agent/<ticket>` 并开 PR。

## 怎么给智能体派活

在本仓库新建 Issue 或发表评论，并 **@ 智能体的 GitHub 账号 `@UZyyk`**，例如：

```
@UZyyk 在 README 末尾加一节「主要特性」，列出三条，别改别的
```

- 只有许可名单里的账号（当前：`1411541667`）能发起明确请求；
- 智能体会以 `agent/<ticket>` 分支开 PR，**不会自动合并**，合并由人决定；
- 评估模式为 `observe`：不确定的需求只观察、不擅自动手。

## 主要特性

- **自动派活**：在 Issue 或评论里 @ 智能体账号即可提交任务。
- **隔离执行**：Worker 在独立 worktree 中完成改动，经 `agent/<ticket>` 分支提交 PR。
- **人工把关**：PR 不会自动合并，是否合并由人决定。
