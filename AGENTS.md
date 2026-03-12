# AGENTS.md

## 项目概述

这是一个"Agent Skills"项目，通过AI分析和总结论文的核心信息。

## 核心功能

- 输入支持：PDF 路径、文本内容或论文链接
- 总结核心内容：论文信息，解决什么问题，采用什么方法，创新点是什么，实验结果

## 项目结构

```
agent-paper/
├── skills/agent-paper/SKILL.md  # Agent Skill 配置和提示词
├── README.md                    # 项目说明文档
└── AGENTS.md                    # Agent 操作指南
```

## Skill 执行流程

当用户调用 '/agent-paper' 命令时，Skill 按以下步骤执行
1. 接收论文输入：等待用户提供论文（PDF 路径、文本内容或论文链接）
2. 总结核心内容
3. 生成报告
4. 保存并打开：保存到当前执行目录并打开文件

## 开发说明

这是一个纯配置型 Skill，不需要编译、构建或测试。所有逻辑都定义在 `SKILL.md` 文件的提示词中。要修改 Skill 的行为，只需编辑 `SKILL.md` 文件。

## 使用示例

用户在 Claude Code 中输入：
```
/agent-paper /path/to/paper.pdf
```
或
```
/agent-paper https://arxiv.org/abs/xxxx.xxxxx
```

Skill 将分析论文并生成结构化报告。

