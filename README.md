# Skills

Claude Code 日常技能合集 — URL 阅读、图表绘制、LLM 测试、3D 场景、对话 Demo 等。

## 标准规范

本项目遵循 [Agent Skills 规范](https://agentskills.io/specification)，确保技能格式标准化和互操作性：

- ✅ **标准 YAML Frontmatter** - 每个技能包含 `name`、`description` 和 `metadata.version`
- ✅ **语义化版本** - 遵循 [semver](https://semver.org/) 进行版本管理
- ✅ **兼容性字段** - 个人技能声明环境要求
- ✅ **结构化组织** - 通用技能与个人技能明确分离

## 安装

### 通过 `npx skills`（推荐）

```bash
# 安装全部技能
npx skills add zhuguibiao/skills

# 列出可用技能（不安装）
npx skills add zhuguibiao/skills --list

# 安装单个技能
npx skills add zhuguibiao/skills --skill ink-reader
```

### 手动安装

将单个技能目录复制到 `~/.claude/skills/` 即可使用。

## 更新

```bash
# 检查可用更新
npx skills check

# 更新所有已安装技能到最新版本
npx skills update
```

## 技能列表

### 通用技能 (`zhuguibiao:`)

| 技能                | 命令                            | 描述                                       |
| ------------------- | ------------------------------- | ------------------------------------------ |
| cc-features         | `/zhuguibiao:cc-features`         | 查看 Claude Code 功能级更新速览（中文）    |
| nano-banana-builder | `/zhuguibiao:nano-banana-builder` | 基于 Google Gemini API 构建图像生成应用    |
| gh-star-list        | `/zhuguibiao:gh-star-list`        | 用 AI 自动将 GitHub Stars 分类整理到 Lists |
| openclash-merger    | `/zhuguibiao:openclash-merger`    | 合并 OpenClash 订阅配置并生成分流规则      |
| threejs-builder     | `/zhuguibiao:threejs-builder`     | 创建 Three.js 3D Web 应用                  |


## 项目结构

```
oh-my-daily-skills/
├── .claude-plugin/
│   └── plugin.json
├── skills/
│   ├── cc-features/
│   ├── nano-banana-builder/
│   ├── openclash-merger/
│   └── threejs-builder/
├── CLAUDE.md
└── README.md
```

## 命名规范

| 类型     | 目录                   | 示例                   |
| -------- | ---------------------- | ---------------------- |
| 通用技能 | `skills/skill-name/`   | `skills/ink-reader/`   |

## 版本规范

遵循 [Semantic Versioning](https://semver.org/) 规范：

| 版本号        | 变更类型   | 示例                      |
| ------------- | ---------- | ------------------------- |
| x.0.0 (MAJOR) | 破坏性变更 | 重构 skill 结构、移除功能 |
| 0.x.0 (MINOR) | 新增功能   | 添加新命令、新章节        |
| 0.0.x (PATCH) | 修复/优化  | 文档修正、格式调整        |

## 开源协议

MIT
