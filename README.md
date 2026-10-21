<p align="center">
<a href="assets/banner.png"><img src="assets/banner.png" alt="把不顺手的部分，做成能交付的工具 — SHANGHAI · TOOLS & AGENT SKILLS" width="100%"></a>
</p>

<p align="center">
我在上海。造工具的人 —— 桌面应用、Windows 原生、以及把生产踩过的坑固化成 Agent Skill。<br>
共同的底线是<b>本地优先</b>、<b>规则可机检</b>、<b>失败可复现</b>。
</p>

<p align="center">
<code>14 public repos</code> · <code>1 PyPI package</code> · <code>2 MCP servers</code> · <code>since 2021-10</code> · <code>Shanghai / Zenico</code>
</p>

<p align="center">
<a href="assets/strip-skills.png"><img src="assets/strip-skills.png" alt="四个 Agent Skill 的规格索引：仓库 / 规模 / 门禁 / 解决什么问题" width="100%"></a>
</p>

<table>
<tr>
<td width="50%" valign="top"><a href="assets/card-afm.png"><img src="assets/card-afm.png" alt="alpha-file-manager 规格卡与真实界面截图" width="100%"></a></td>
<td width="50%" valign="top"><a href="assets/card-fluxing.png"><img src="assets/card-fluxing.png" alt="fluxing 火流猩输入法 规格卡、官方 logo 与真实设置面板" width="100%"></a></td>
</tr>
<tr>
<td width="50%" valign="top"><a href="assets/card-weavepage.png"><img src="assets/card-weavepage.png" alt="weavepage 织页 官方海报" width="100%"></a></td>
<td width="50%" valign="top"><a href="assets/card-mtd.png"><img src="assets/card-mtd.png" alt="media-to-doc 11 阶段流水线编号表" width="100%"></a></td>
</tr>
</table>

<h2 align="center">做工具的人</h2>

| `location` | `company` | `since` | `repos` | `pypi` | `mcp` |
|---|---|---|---|---|---|
| Shanghai | Zenico | 2021-10 | 14 public | `media_to_doc` | 2 servers |

日常某个环节不顺手，就自己造一个工具；工具要**本地优先**、**规则可机检**、**失败可复现**；做完沉淀成别人能直接用的东西。

这不是四件无关的事，是同一件事的**四次重演**：

- **桌面应用**（`alpha-file-manager`、`weavepage`）—— 操作系统那一层不顺手
- **Windows 原生**（`fluxing`）—— 输入法那一层不顺手
- **音视频流水线**（`media-to-doc`、`ad-cut`、`long-doc-processor`）—— 内容加工那一层不顺手
- **Agent Skills**（`sql-skill`、`evidence-skill`、`skill-forge`、`loop-engineering`）—— 让 AI 别再犯同样的错

最后一条是这套东西里比较特别的一条：这些 skill 不是玩具 demo，是把**生产事故**（nginx patch、postgres_fdw 跨库、postmortem）固化成**可机检的契约**。`sql-skill` 10 章 + 4 辅助文件 + 4 通道动态同步；`evidence-skill` 20 章 + 168 页 docs 镜像；`skill-forge` 6 阶段、确定性 + LLM 评分双门禁、SHA 基线竞态检查；`loop-engineering` 5 道项目级 guard rails hook。

<h2 align="center">仓库索引</h2>

| 仓库 | 语言 | 一句话 |
|---|---|---|
| [`alpha-file-manager`](https://github.com/kizemo/alpha-file-manager) | TypeScript | 基于 Sigma File Manager 二次开发，新增目录双击、快速切换、批量重命名等实用能力，并对大量细节做了优化的开源文件管理器。 |
| [`fluxing`](https://github.com/kizemo/fluxing) | C++ | Fluxing IME（火流猩输入法）：RIME 引擎的 Windows 原生前端 fork，保留 RIME 全部可定制性，同时提供原生 TSF 集成、系统托盘、自动部署。 |
| [`weavepage`](https://github.com/kizemo/weavepage) | TypeScript | 所见即所得的本地网页编辑器（Tauri + Tiptap）：打开任意 HTML 文件，立即呈现完整 CSS 样式与 JS 动态效果，编辑界面就是最终效果。 |
| [`media-to-doc`](https://github.com/kizemo/media-to-doc) | Python | 把本地音视频一键转化为带 AI 配图、可独立分发的 Markdown + HTML 讲义；11 阶段流水线，全栈本地推理。 |
| [`sql-skill`](https://github.com/kizemo/sql-skill) | HTML | 企业 PostgreSQL 视角的通用 SQL 专业度 Skill：10 章 + 4 辅助文件 + 4 通道动态同步 + gbrain 语义召回/全文检索双模式。 |
| [`evidence-skill`](https://github.com/kizemo/evidence-skill) | — | Evidence BI (Core 2026) 生产切换经验蒸馏：connection.yaml、nginx patch、SQL 反模式、postgres_fdw 跨库、postmortem。 |
| [`skill-forge`](https://github.com/kizemo/skill-forge) | Python | 六阶段元技能：审计 → 定范围 → 引导 → 前向 → 验证 → 物化，确定性 + LLM 评分双门禁，SHA 基线竞态检查，绝不覆盖 marketplace 安装。 |
| [`long-doc-processor`](https://github.com/kizemo/long-doc-processor) | Python | 音视频 / 多份 docx / XMind 等异构输入 → 可独立打开的 HTML 讲义；30 条规约可机检，531 tests passed。 |
| [`ad-cut`](https://github.com/kizemo/ad-cut) | Python | 去除讲师课程录像中的赞助口播：LLM 关键词扩展 + faster-whisper 转写 + LLM 二次裁判 + ffmpeg 剪辑。 |
| [`loop-engineering`](https://github.com/kizemo/loop-engineering) | Shell | 把「AI Agent 的持续运行」当软件工程问题解：5 道项目级 guard rails hook + LoopX 控制面 + 3 种 Playbook。 |
| [`shgb-keepalive`](https://github.com/kizemo/shgb-keepalive) | JavaScript | 上海干部在线学习视频自动循环播放工具，Playwright + Edge CDP，打包双 exe 免 Node 环境。 |
| [`focus-sync`](https://github.com/kizemo/focus-sync) | PowerShell | Sigma File Manager 插件，文件对话框路径焦点同步（源码已并入 Alpha File Manager）。 |
| [`media-to-doc-ui`](https://github.com/kizemo/media-to-doc-ui) | Rust | media-to-doc 的 Tauri 2 桌面外壳。 |
| [`kizemo`](https://github.com/kizemo/kizemo) | — | 本仓库（个人主页）。 |

<details open>
<summary>协议与统计</summary>

- 公开仓库 **14** 个，其中 4 个精选呈现
- 协议分布：GPL-3.0 ×1 · MIT ×4 · NOASSERTION ×5 · 无声明 ×4
- 语言谱：TypeScript · Rust · C++ · Python · PowerShell · JavaScript · Shell · HTML
- 技术栈关键词：Tauri · Rust · Vue · React · Tiptap · RIME / weasel · WTL · TSF · Playwright · Edge CDP · MCP server · ffmpeg · faster-whisper · Ollama · SDXL · RapidOCR · Postgres FDW
- 1 个 PyPI 包（`media_to_doc`）· 2 个 MCP server（`alpha-file-manager`、`media-to-doc`）
- 2021-10 起持续产出，最近更新 2026-10-21

</details>

<hr/>

<p align="center">
<img src="https://img.shields.io/badge/repos-14-16150f" alt="14 public repos">
<img src="https://img.shields.io/badge/since-2021--10-16150f" alt="since 2021-10">
<img src="https://img.shields.io/badge/location-Shanghai-16150f" alt="Shanghai">
<img src="https://img.shields.io/badge/company-Zenico-16150f" alt="Zenico">
<img src="https://img.shields.io/badge/pypi-media__to__doc-c8452b" alt="PyPI media_to_doc">
<img src="https://img.shields.io/badge/mcp-2%20servers-c8452b" alt="2 MCP servers">
<img src="https://img.shields.io/badge/languages-8-6b6a63" alt="8 languages">
<img src="https://img.shields.io/badge/license-GPL--3.0%20%C2%B7%20MIT-6b6a63" alt="license GPL-3.0 / MIT">
<img src="https://img.shields.io/badge/stack-tauri%20%C2%B7%20rust%20%C2%B7%20vue%20%C2%B7%20C%2B%2B-6b6a63" alt="stack tauri / rust / vue / C++">
<img src="https://img.shields.io/badge/pipeline-11%20stages-6b6a63" alt="11 stage pipeline">
</p>

<p align="center">
<code>kizemo</code> · <a href="https://github.com/kizemo">github.com/kizemo</a>
</p>
