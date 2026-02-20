# 🎵 AI00-X 开源社区招募 | 一起打造下一代AI桌面助手

<p align="center">
  <img src="https://img.shields.io/github/stars/ai00-x/ai00-x?style=flat&color=ff69b4" alt="stars">
  <img src="https://img.shields.io/github/forks/ai00-x/ai00-x?style=flat&color=ff69b4" alt="forks">
  <img src="https://img.shields.io/github/license/ai00-x/ai00-x?style=flat&color=ff69b4" alt="license">
</p>

<p align="center">
  <strong>English version below</strong>
</p>

---

## 🌟 关于 AI00-X

**AI00-X** 是一个开源的桌面 AI 助手项目，采用 Tauri + React 技术栈构建。我们正在打造一个**有情感、有能力、能干活**的AI伙伴，而不仅仅是一个聊天窗口。

### 核心特性

- 🤖 **AI助手** - 本地 RWKV 模型，实时对话，情感陪伴
- 🎨 **桌面美化** - 动态场景、主题切换、VRM虚拟形象
- 🎵 **AI音乐** - Lofi 音乐生成，环境音效
- 🐾 **桌面宠物** - 物理引擎驱动的互动宠物
- 🔌 **插件系统** - 强大的扩展能力

---

## 🔥 正在开发的核心功能

### 1. 🎤 Qwen3 TTS - 本地语音合成

**已实现！** 使用 Rust 驱动 GGUF 推理加速，实现本地化的语音合成。

```rust
// 高效的 GGUF 模型推理
let model = GGUFModel::load("qwen3-tts.gguf")?;
let audio = model.synthesize("你好，我是AI00-X").await?;
```

**技术亮点**:
- ✅ GGUF 格式支持
- ✅ 本地推理，保护隐私
- ✅ 低延迟实时合成

---

### 2. 🦞 OpenClaw - AI Agent 框架

**正在开发** - 使用 Rust 开发类似 [OpenClaw](https://github.com/openclaw/openclaw) 的 AI Agent 框架，让 AI 能够真正"干活"。

**架构设计**:

| 组件 | 功能 |
|------|------|
| Agent Core | 任务规划与执行 |
| Browser Control | 浏览器自动化 |
| File System | 文件操作 |
| Shell Executor | 系统命令执行 |
| Remote LLM | 调用 OpenAI/Anthropic 等强大模型 |

**任务分流机制**:

```
轻量任务 → 本地 RWKV (实时响应)
    │
    └── 情感陪伴、桌面控制、主题切换

复杂任务 → OpenClaw + 远程LLM (强大能力)
    └── 浏览器自动化、复杂推理、文件操作
```

---

### 3. 🎵 AI 音乐生成平台

**现有能力**:
- ✅ Lofi 音乐生成 (Magenta.js)
- ✅ 多乐器编排
- ✅ 环境音效/白噪音
- ✅ 12种乐器采样

**正在开发** - 🎤 **有人声歌词的歌曲生成**

**技术路线**:

```
┌─────────────────┐     ┌─────────────────┐     ┌─────────────────┐
│   歌词生成      │ ──▶ │   旋律生成       │ ──▶ │   人声合成      │
│  (LLM/RWKV)    │     │  (MusicGen/     │     │  (Vocaloid/     │
│                │     │   ACEStep)      │     │   Diffusion)     │
└─────────────────┘     └─────────────────┘     └─────────────────┘
```

**ACOStep 1.5 优化**:
- 🎯 Rust 驱动 GGUF 推理加速
- 🎵 多轨道音乐生成
- 🎤 人声/伴奏分离
- 📦 轻量本地运行

**愿景**: 建立一个 **AI 音乐制作与分享的小平台**

- 🎹 在线 AI 音乐创作
- 🎧 社区分享与发现
- 🎤 人声合成预览
- 📀 导出多种格式

---

### 4. 🔌 插件体系

AI00-X 拥有强大的插件系统，支持：

| 插件类型 | 说明 |
|----------|------|
| Widget | 桌面挂件 |
| Popup | 弹窗应用 |
| Skill | AI 技能 |
| Backend | 后端服务 |

**已有插件示例**:
- 社交媒体数据监控
- 系统监控
- 音乐播放板
- 时钟挂件

**我们期待**:

```
┌─────────────────────────────────────────────┐
│              AI00-X 插件市场                 │
├─────────────────────────────────────────────┤
│  🎮 游戏辅助    📊 数据看板    🌐 浏览器工具 │
│  📝 笔记工具    🔧 开发工具    🎨 创意工具  │
│  🤖 AI 技能    📺 影音娱乐    🛠️ 系统工具  │
└─────────────────────────────────────────────┘
```

---

## 💻 技术栈

| 层级 | 技术 |
|------|------|
| 前端 | React 19, TypeScript, Tailwind CSS |
| 3D/图形 | Three.js, Pixi.js, Spine |
| 后端 | Rust, Tauri 2.x |
| AI/ML | RWKV, ONNX, GGUF, Magenta.js |
| 音频 | Tone.js, Web Audio API |
| 物理 | Matter.js |

---

## 🤝 如何参与

### 贡献方式

1. **🌟 Star** - 给项目点个 Star
2. **🐛 提交 Bug** - 发现问题提 Issue
3. **💡 功能建议** - 分享你的想法
4. **📝 文档完善** - 帮助完善文档
5. **💻 代码贡献** - 提交 PR

### 需要帮助的方向

| 方向 | 描述 | 需求 |
|------|------|------|
| 🎵 音乐AI | ACEStep/Vocaloid 优化 | Rust + ML |
| 🦞 Agent | OpenClaw 框架开发 | Rust |
| 🎤 TTS | Qwen3 TTS 改进 | Rust + ONNX |
| 🎨 UI/UX | 界面设计与动画 | React + CSS |
| 📖 文档 | 中文/英文文档 | 技术写作 |

---

## 📱 联系方式

- 💬 Discord: [加入讨论](https://discord.gg/ai00-x)
- � GitHub: [github.com/ai00-x](https://github.com/ai00-x/ai00-x)
- 📧 Email: hello@ai00-x.dev

---

## 📄 License

MIT License - 欢迎商业使用！

---

<p align="center">
  <strong>让我们一起打造下一代 AI 桌面助手！</strong><br>
  <em>Build the future of AI desktop assistant together!</em>
</p>

---

# 🎵 AI00-X Open Source Community Recruitment

Join us in building the next generation AI desktop assistant!

### What We're Building

1. **Qwen3 TTS** - Local speech synthesis with Rust + GGUF
2. **OpenClaw-style Agent** - AI that actually does work
3. **AI Music Platform** - Generate songs with lyrics + vocals
4. **Plugin Ecosystem** - Powerful extensibility

### Tech Stack

Rust, Tauri, React 19, TypeScript, RWKV, ONNX, GGUF

### Get Involved

- ⭐ Star us on GitHub
- 🐛 Report bugs
- 💡 Share ideas
- 📝 Contribute code

**Discord**: [Join our community](https://discord.gg/ai00-x)

---

*Let's create something amazing together! 🦞*
