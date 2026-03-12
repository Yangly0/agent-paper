# Agent Paper

通过 AI 分析和总结论文的核心信息。

## 功能特性

- **多格式输入支持**：PDF 文件路径、文本内容或论文链接
- **智能内容总结**：自动提取论文的关键信息
- **结构化报告**：生成包含论文信息、问题、方法、创新点和实验结果的完整报告
- **自动保存**：报告自动保存到当前执行目录

## 使用方法

在 Claude Code 或 其他Agent Cli 中输入：

```
/agent-paper /path/to/paper.pdf
```

或

```
/agent-paper https://arxiv.org/abs/xxxx.xxxxx
```

## 输出格式

生成的报告文件命名格式：`{发表时间}-{作者}-{题目}.md`，保存到当前执行目录

报告包含以下部分：
- 论文基本信息（标题、作者、发表时间、来源）
- 研究问题
- 解决方法
- 创新点
- 实验结果

## 项目结构

```
agent-paper/
├── skills/agent-paper/SKILL.md  # Agent Skill 配置和提示词
├── README.md                    # 项目说明文档
└── AGENTS.md                    # Agent 操作指南
```

## 开发说明

这是一个纯配置型 Skill，不需要编译、构建或测试。所有逻辑都定义在 `SKILL.md` 文件的提示词中。

## 参考

- https://github.com/lijigang/ljg-skill-xray-paper
