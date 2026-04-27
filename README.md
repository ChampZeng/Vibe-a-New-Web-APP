这份 README 是我们这套 **AI 驱动开发流** 的说明书。基于确立的“大脑（Gemini）与手脚（Cursor）解耦”的开发哲学形成。
***

```markdown
# Vibe-a-New-Web-APP 🚀

本项目展示了一种极致高效的 **AI 驱动全栈开发工作流 (AI-Driven Full-Stack Workflow)**。通过将“系统架构设计”与“代码编写”严格解耦，实现由单人（产品经理）协同 AI 完成从 0 到 1 的产品研发、测试与部署。

## 🧠 核心开发哲学：解耦与防呆

传统的“直接对话写代码 (Vibe Coding)”容易导致大型模型在长上下文中遗忘需求、逻辑崩盘。本工作流坚持以下核心原则：

1. **大脑与手脚分离**：使用大语言模型（如 Gemini）作为“大脑”，负责需求拆解、UI 设计规划和技术架构输出；使用智能代码编辑器（如 Cursor 的 Plan 模式）作为“手脚”，严格按照既定文档执行构建。
2. **文档驱动开发 (DDD)**：在写第一行代码前，必须先确立标准化的产品需求文档（PRD）、UI 设计文档和技术架构文档。
3. **稳定性与容器化优先**：默认选择成熟的开源组件避免重复造轮子，所有前后端服务均在本地 Docker 中运行隔离。

## 📂 推荐目录结构

```text
Vibe-a-New-Web-APP/
├── AI_Workflows/               # 存放核心的 AI 提示词与 SOP 资产
│   ├── WebApp_Architect_Skill.md     # Gemini 架构师设定指令
│   └── Cursor_Execution_SOP.md       # Cursor 执行标准作业流
├── Docs/                       # 驱动 Cursor 开发的核心基石文档
│   ├── 1_PRD.md                # 产品需求文档
│   ├── 2_UI_Design.md          # UI 规范与布局定义
│   └── 3_Development.md        # 技术架构、API规范与数据表结构
├── src/                        # 源代码目录（由 Cursor 自动生成）
├── docker-compose.yml          # 本地容器化编排文件
└── README.md
```

## ⚙️ 标准作业流 (SOP)

### Phase 1: 架构设计 (在 Gemini 中完成)
1. **注入灵魂**：将 `WebApp_Architect_Skill.md` 作为 System Prompt 发送给大模型。
2. **需求对齐**：输入愿望清单与 UI 草图，经过多轮对话确认，最终输出标准化、Markdown 格式的 `1_PRD.md`、`2_UI_Design.md` 和 `3_Development.md`。
3. **获取密钥**：大模型将输出一段专用于唤醒 Cursor 的“交接指令”。

### Phase 2: 代码构建 (在 Cursor 中完成)
1. **挂载文档**：在 Cursor 中打开项目根目录，按 `Ctrl+I` / `Cmd+I` 呼出 Composer（推荐 Agent/Plan 模式）。
2. **下达指令**：粘贴 Phase 1 获取的交接指令，强制 Cursor 读取 `Docs/` 目录下的三份文档。
3. **生成计划与执行**：Cursor 理解并复述无误后，生成 Step-by-Step 的开发计划。点击 `Build` 逐个节点推进，遇到问题直接让 Cursor 结合文档进行修正。

## 🛠️ 环境准备与快速上手

**前置依赖：**
* [Git](https://git-scm.com/) (版本控制与推送)
* [Docker Desktop](https://www.docker.com/) (本地容器运行环境)
* [Cursor](https://www.cursor.com/) (AI 代码编辑器)

**克隆与运行：**
```bash
# 1. 克隆仓库
git clone [https://github.com/ChampZeng/Vibe-a-New-Web-APP.git](https://github.com/ChampZeng/Vibe-a-New-Web-APP.git)

# 2. 进入目录
cd "Vibe-a-New-Web-APP"

# 3. 开始你的 AI 构建之旅...
```

---
*Developed with Systematic AI Workflow.*
```
