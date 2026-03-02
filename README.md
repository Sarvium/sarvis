# Sarvis — VS Code Extension

<p align="center">
  <img src="media/icon.png" alt="Sarvis AI Logo" width="100"/>
</p>

<p align="center">
  <strong>An intelligent AI coding assistant powered by Sarvam AI, built into VS Code.</strong>
</p>

<p align="center">
  <a href="https://sarvium.com">🌐 Website</a> &nbsp;|&nbsp;
  <a href="https://github.com/AkashKobal/sarvis/issues">🐛 Report a Bug</a> &nbsp;|&nbsp;
  <a href="https://github.com/AkashKobal/sarvis/issues/new?template=feature_request.md">💡 Request a Feature</a> &nbsp;|&nbsp;
  <a href="https://github.com/AkashKobal/sarvis/discussions">💬 Discussions</a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/version-1.0.4-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/license-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/VS%20Code-%5E1.85.0-blue?style=flat-square&logo=visualstudiocode"/>
  <img src="https://img.shields.io/badge/powered%20by-Sarvam%20AI-orange?style=flat-square"/>
  <img src="https://img.shields.io/badge/built%20by-Sarvium-purple?style=flat-square"/>
</p>

---

## ✨ Features

- 💬 **AI Chat Sidebar** — Ask anything about your code, get instant answers with full file context
- ⚡ **Inline Code Completions** — Real-time suggestions as you type
- 🔧 **Fix with Sarvis AI** — Select broken code, get an improved version shown as a diff
- 🔐 **Secure API Key Storage** — Encrypted via VS Code's built-in secret storage

---

## 🚀 Getting Started

### 1. Install
Install from `.vsix`:
```
Extensions panel (Ctrl+Shift+X) → ••• Menu → Install from VSIX
```

### 2. Set Your Sarvam API Key
```
Ctrl+Shift+P → "Sarvis: Set API Key"
```
Or click **⚙** in the Sarvis sidebar panel.

> Get your API key at [sarvam.ai](https://sarvam.ai)

### 3. Open the Sidebar
Click the **S** icon in the VS Code Activity Bar and start chatting!

---

## 🐛 Reporting a Bug

Found something broken? We want to fix it fast.

### Before Reporting
- [ ] Check if the issue already exists in [open issues](https://github.com/AkashKobal/sarvis/issues)
- [ ] Make sure you're on the latest version
- [ ] Try reloading VS Code (`Ctrl+Shift+P` → `Reload Window`)

### How to Report

👉 [**Click here to open a Bug Report**](https://github.com/AkashKobal/sarvis/issues/new?template=bug_report.md&labels=bug)

Please include:

```
**VS Code Version:** (Help → About)
**Sarvis Version:** (Extensions panel → Sarvis AI)
**OS:** Windows / macOS / Linux

**What happened:**
A clear description of the bug.

**Steps to reproduce:**
1. Go to '...'
2. Click on '...'
3. See error

**Expected behavior:**
What you expected to happen.

**Screenshots / Logs:**
Attach any screenshots or paste the Output panel logs.
(View → Output → select "Extension Host" from dropdown)
```

---

## 💡 Requesting a Feature

Have an idea to make Sarvis better?

👉 [**Click here to open a Feature Request**](https://github.com/AkashKobal/sarvis/issues/new?template=feature_request.md&labels=enhancement)

Please include:
- What problem does this solve?
- How would you like it to work?
- Any examples or references?

---

## 💬 Discussions

For questions, ideas, or general feedback that isn't a bug:

👉 [**Join the Discussions**](https://github.com/AkashKobal/sarvis/discussions)

---

## 🛠️ Development Setup

Want to contribute or run locally?

```bash
# 1. Clone the repo
git clone https://github.com/AkashKobal/sarvis.git
cd sarvis

# 2. Install dependencies
npm install

# 3. Build
node esbuild.js

# 4. Open in VS Code
code .

# 5. Press F5 to launch Extension Development Host
```

### Project Structure

```
sarvis/
├── src/
│   ├── extension.ts              # Entry point
│   ├── providers/
│   │   ├── ChatViewProvider.ts   # Sidebar webview
│   │   ├── CodeActionProvider.ts # Fix with Sarvis
│   │   ├── DiffManager.ts        # Diff preview
│   │   └── InlineCompletionProvider.ts
│   ├── services/
│   │   └── AiService.ts          # Sarvam API calls
│   ├── commands/
│   │   └── setApiKey.ts
│   └── utils/
│       └── errorHandler.ts
├── media/
│   ├── chat.css                  # Sidebar UI styles
│   ├── chat.js                   # Sidebar UI logic
│   └── icon.svg
├── out/                          # Compiled output
├── esbuild.js
└── package.json
```

---

## 🤝 Contributing

Contributions are welcome! Here's how:

1. **Fork** the repository
2. **Create** a branch: `git checkout -b feature/your-feature-name`
3. **Commit** your changes: `git commit -m "feat: add your feature"`
4. **Push** to your branch: `git push origin feature/your-feature-name`
5. **Open a Pull Request** and describe what you changed

### Commit Message Convention
```
feat:     New feature
fix:      Bug fix
docs:     Documentation changes
style:    Formatting, no logic change
refactor: Code restructure
chore:    Build / config changes
```

---

## 📋 Issue Labels

| Label | Description |
|---|---|
| `bug` | Something isn't working |
| `enhancement` | New feature request |
| `question` | General question |
| `good first issue` | Great for new contributors |
| `help wanted` | Extra attention needed |
| `wontfix` | This will not be worked on |
| `duplicate` | Already reported |

---

## 🗺️ Roadmap

- [ ] Multi-language support (Hindi, Tamil, Telugu via Sarvam)
- [ ] Chat history persistence across sessions
- [ ] Custom system prompt configuration
- [ ] Voice input support
- [ ] Support for multiple AI models
- [ ] Workspace-level context awareness

---

## 📄 License

MIT License © 2024 [Sarvium](https://sarvium.com)

See [LICENSE](LICENSE) for full text.

---

## 👨‍💻 Credits

<table>
  <tr>
    <td align="center">
      <strong>Created by</strong><br/>
      <a href="https://sarvium.com">Sarvium</a>
    </td>
    <td align="center">
      <strong>Developed by</strong><br/>
      <a href="https://github.com/AkashKobal">Akash Kobal</a>
    </td>
    <td align="center">
      <strong>Powered by</strong><br/>
      <a href="https://sarvam.ai">Sarvam AI</a>
    </td>
  </tr>
</table>

---

<p align="center">
  Built with ❤️ by <a href="https://sarvium.com">Sarvium</a> &nbsp;·&nbsp; Developed by <a href="https://github.com/AkashKobal">Akash Kobal</a>
</p>
