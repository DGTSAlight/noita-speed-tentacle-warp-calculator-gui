# ✦ NOITA 速度触手跃迁计算器 GUI ✦

**Noita Speed Tentacle Warp Calculator GUI** — 单文件 HTML 工具，用于计算 Noita 中「速度触手跃迁」的 α_other 分解方案。无需任何环境，双击即可运行，支持离线使用。

> 🌐 **Language / 切换语言**：[English](#english) · [中文](#中文)

---

<a name="english"></a>

## English

### Overview

**Noita Speed Tentacle Warp Calculator** is a single-file HTML/CSS/JavaScript application that solves the speed-tentacle warp (跃迁) break-down problem in the game *Noita*.

### Features

- 🎯 **Distance presets** — `NG+0` (35,840 px / 1 world) and `NG+1` (32,768 px), or a fully custom distance.
- ⚡ **Exponential multipliers** — configurable up/down-flight count and arbitrary extra exponential chips (e.g. 1.3²).
- 🧩 **α_other decomposition** — combines 9 normal speed modifiers plus the optional "start ×20" step:
  | Value | Modifier                                     |
  | ----- | -------------------------------------------- |
  | 0.33  | Phasing Body (相位)                          |
  | 0.32  | Gradual Acceleration (逐渐加速)              |
  | 0.3   | Heavy Shot (沉重一击)                        |
  | 0.75  | Explosive (易爆)                             |
  | 1.2   | Mucus/Flash (闪灭)                           |
  | 1.68  | Gradual Deceleration (逐渐减速)              |
  | 7.5   | Light Shot (轻盈一击)                        |
  | 2.5   | Accelerating Shot (加速)                     |
  | 2     | Worm Detector / Chaotic Path (蛇形/混沌轨迹) |
- 🪄 **Staff & slime** — staff speed bonus fixed `×1.0` or auto-choose among `1 / 1.25 / 1.5`; slime pellet `×1.1` is the only source of a 1.1 multiplier inside α_other and does not count toward the modifier count limit.
- 📐 **Tolerance & sorting** — relative percentage or absolute-pixel error mode, sort by error or by fewest modifiers, page size 10/20/30, up to 12 modifiers with a configurable cap (default 5).
- 🔁 **Copy ordinary factors (v0.6)** — each normal factor may be used once or copied `1..N` times (N ≤ 800, default 100). The search is protected by per-step clamping at `20`, saturation pruning (e.g. `7.5²` already clamps to 20), plus node/time limits (8M nodes / 8 s); a warning badge appears when deep searching may take a while.
- 🛡️ **Built-in regression self-test** — 12 checks (T1–T12) covering constants (`v₁ = 7.92`), per-step clamp `≤ 20`, NG+0 classic scenario, absolute-pixel error mode, least-modifier sorting, regular-number validation, exact `0.3¹⁰` hit, saturation pruning, mixed copy like `0.3³ × 2`, and copy-count regular-number enforcement.
- 🖼️ **Fully self-contained** — all spell icons are embedded as base64 data URIs; no external resources, no network access, works offline. Double-click the file and it runs.

### Usage

1. Download (or clone) `触手跃迁计算器GUI_v0.6.html`.
2. Double-click the HTML file — it opens directly in any modern browser (Chrome / Edge / Firefox).
3. Pick a distance preset (or enter a custom one), configure the search parameters.
4. Click **“✦ 开始计算 ✦”** — the solution list shows the factor stacks, per-solution deviation in pixels, and (optional) icons.
5. The collapsible **self-test** panel runs all T1–T12 regression checks with one click.

### File

- `触手跃迁计算器GUI_v0.6.html` — the entire application in a single file (~100 KB).

### Note on AI Generation

The main content of this project was **generated with the assistance of an AI large language model** based on the Noita warp-tutorial mechanics, then reviewed and validated (via in-page self-tests against known in-game scenarios). If you find any issue, please adjust expectations accordingly and feel free to report feedback.

---

<a name="中文"></a>

## 中文

### 项目简介

**NOITA 速度触手跃迁计算器 GUI** 是一个单文件 HTML/CSS/JavaScript 应用，用于解决《Noita》游戏中「速度触手跃迁」的 α_other 分解问题。无需安装任何环境，双击即可运行，可完全离线使用。

### 功能特性

- 🎯 **预设距离** —— `NG+0`（35,840 像素 / 1 世界）与 `NG+1`（32,768 像素），或自定义任意距离。
- ⚡ **指数级乘数** —— 可配置上/下飞数量，并支持任意“底数/指数”附加条目（例如 1.3²）。
- 🧩 **α_other 分解** —— 组合 9 种普通速度修正法术及可选的“起始 20 倍”：
  | 数值 | 修正          |
  | ---- | ------------- |
  | 0.33 | 相位          |
  | 0.32 | 逐渐加速      |
  | 0.3  | 沉重一击      |
  | 0.75 | 易爆          |
  | 1.2  | 闪灭          |
  | 1.68 | 逐渐减速      |
  | 7.5  | 轻盈一击      |
  | 2.5  | 加速          |
  | 2    | 蛇形/混沌轨迹 |
- 🪄 **法杖与粘液弹** —— 法杖自带倍率可固定 `×1.0`，或在 `1 / 1.25 / 1.5` 中自动选择；粘液弹 `×1.1` 是 α_other 中 1.1 倍乘数的唯一来源，且不计入修正个数上限。
- 📐 **误差与排序** —— 支持相对百分比 / 绝对像素两种误差模式，按“误差优先”或“因子最少优先”排序，每页显示 10/20/30 条方案；普通修正个数上限可调（默认 5，最大 12）。
- 🔁 **复制普通因子（v0.6）** —— 每个普通因子可使用 1 次或复制 `1..N` 次（N ≤ 800，默认 100）。搜索受每步钳制 ≤ 20、饱和剪枝（如 `7.5²` 已被钳制到 20）以及节点/时间上限（800 万节点 / 8 秒）保护；当深度搜索可能较久时会出现提示徽标。
- 🛡️ **内置回归自检** —— 共 12 项（T1–T12），覆盖常量（`v₁ = 7.92`）、每步钳制 ≤ 20、NG+0 经典场景、绝对像素误差模式、因子最少排序、正则数校验、`0.3¹⁰` 精确命中、饱和剪枝、`0.3³ × 2` 混合复制、复制次数正则数强制等。
- 🖼️ **完全自包含** —— 全部法术图标以 base64 内嵌，无外部资源、无需联网，离线可用。双击文件即运行。

### 使用方法

1. 下载（或克隆）`触手跃迁计算器GUI_v0.6.html`。
2. 双击该 HTML 文件，即可在现代浏览器（Chrome / Edge / Firefox）中直接打开。
3. 选择距离预设（或输入自定义距离），配置分解参数。
4. 点击 **「✦ 开始计算 ✦」** —— 结果列表展示因子组合方案、每方案的偏差像素，并可显示对应图标。
5. 可折叠的 **自检** 面板一键运行全部 T1–T12 回归测试。

### 文件说明

- `触手跃迁计算器GUI_v0.6.html` —— 整个应用仅此一个文件（约 100 KB）。

### 关于 AI 生成

本项目的主要内容由 **AI 大语言模型辅助生成**；生成后对照 Noita 跃迁教程机制与已知游戏场景进行了人工复核与在线自检验证。如发现问题，欢迎提出反馈。

---

> **License / 授权**：仅供学习与娱乐用途。Noita 是 Nolla Games 的商标，本工具与 Nolla Games 无关联。
