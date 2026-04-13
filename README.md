<p align="center">
  <img src="/sarvisLogo.png" alt="Sarvis Logo" width="120"/>
</p>

<h1 align="center">Sarvis - AI Coding Assistant for VS Code</h1>

<p align="center">
  <strong>An intelligent AI coding assistant powered by Sarvam AI, built into VS Code.</strong><br/>
  Get instant completions, smart debugging, code explanations, and conversational AI — without leaving your editor.
</p>

<p align="center">
  <a href="https://sarvium.com">🌐 Website</a> &nbsp;|&nbsp;
  <a href="https://github.com/Sarvium/sarvis/issues">🐛 Report a Bug</a> &nbsp;|&nbsp;
  <a href="https://github.com/Sarvium/sarvis/issues/new?template=feature_request.md">💡 Feature Request</a> &nbsp;|&nbsp;
  <a href="https://github.com/Sarvium/sarvis/discussions">💬 Discussions</a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/version-1.0.0-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/license-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/VS%20Code-%5E1.109.0-blue?style=flat-square&logo=visualstudiocode"/>
  <img src="https://img.shields.io/badge/powered%20by-Sarvam%20AI-orange?style=flat-square"/>
  <img src="https://img.shields.io/badge/built%20by-Sarvium-purple?style=flat-square"/>
</p>

---

## 📋 Table of Contents

- [✨ Features](#-features)
- [🚀 Getting Started](#-getting-started)
- [🎯 Commands Reference](#-commands-reference)
  - [Core AI Commands](#core-ai-commands)
  - [Git & Version Control](#git--version-control)
  - [Code Quality & Analysis](#code-quality--analysis)
  - [Documentation](#documentation)
  - [Refactoring & Migration](#refactoring--migration)
  - [Testing](#testing)
  - [Security & Performance](#security--performance)
  - [Memory & Context](#memory--context)
  - [Diagrams & Architecture](#diagrams--architecture)
  - [Developer Productivity](#developer-productivity)
  - [Terminal Commands](#terminal-commands)
- [⌨️ Keyboard Shortcuts](#️-keyboard-shortcuts)
- [⚙️ Configuration](#️-configuration)
- [🛠️ Development Setup](#️-development-setup)
- [🗺️ Roadmap](#️-roadmap)
- [🐛 Reporting a Bug](#-reporting-a-bug)
- [📄 License](#-license)

---

## ✨ Features

| Feature | Description |
|---|---|
| 💬 **AI Chat Sidebar** | Ask anything about your code, get instant answers with full file context |
| ⚡ **Inline Completions** | Real-time code suggestions as you type (conservative / balanced / creative modes) |
| 🔧 **Fix with AI** | Select broken code, get an improved version shown as a diff |
| 🔐 **Secure Key Storage** | API key encrypted via VS Code's built-in secret storage |
| 🧠 **Session Memory** | Tracks bugs, features, goals, and notes across your coding session |
| 🧪 **Test Generation** | Auto-generate test cases for any file or selection |
| 🔒 **Security Scanning** | Detect vulnerabilities in a file or across the whole project |
| 📄 **Docs Generation** | Generate README, JSDoc, Swagger, and full API docs instantly |
| 🎤 **Voice Commands** | Control Sarvis hands-free with voice input |
| 🔀 **Git Intelligence** | Commit messages, diff reviews, PR creation, and risk detection |

---

## 🚀 Getting Started

### 1. Install

**Option A — Install from VSIX:**
```
Extensions panel (Ctrl+Shift+X) → ••• Menu → Install from VSIX → select sarvis-1.0.0.vsix
```

**Option B — Install from Marketplace:**
```
Extensions panel → Search "Sarvis" → Install
```

### 2. Set Your Sarvam API Key

Open the Command Palette and run:
```
Ctrl+Shift+P  →  "Sarvis: Set API Key"
```
Or click the **⚙** gear icon in the Sarvis sidebar panel.

> 🔑 Get your free API key at [sarvam.ai](https://dashboard.sarvam.ai/key-management)

### 3. Open the Sidebar

Click the **S** icon in the VS Code Activity Bar to open the Sarvis chat panel. Start asking questions about your code!

---

## 🎯 Commands Reference

All commands are accessible via the Command Palette (`Ctrl+Shift+P`) by typing `Sarvis:`.  
Many are also available in the **right-click context menu** in the editor and terminal.

---

### Core AI Commands

#### `Sarvis: Explain Selected Code`
**Shortcut:** `Ctrl+Shift+E` / `Cmd+Shift+E`  
**When:** Text selected in editor

Select any block of code, run this command, and Sarvis will explain what it does, line by line.

```
Example:
1. Select a complex function
2. Right-click → Sarvis: Explain Selected Code
3. Sarvis opens a panel with a plain-English breakdown
```

---

#### `Sarvis: Generate Code`
**Shortcut:** `Ctrl+Shift+G` / `Cmd+Shift+G`  
**When:** Editor is focused

Describe what you want to build in natural language and Sarvis generates the code inline.

```
Example prompt:
"Create a debounce function that accepts a callback and delay in milliseconds"

→ Sarvis inserts a ready-to-use debounce implementation at your cursor
```

---

#### `Sarvis: Debug Error`
**Shortcut:** `Ctrl+Shift+D` / `Cmd+Shift+D`  
**When:** Error text selected in editor

Select an error message or a broken code block and Sarvis diagnoses the issue and suggests a fix.

```
Example:
1. Select: TypeError: Cannot read properties of undefined (reading 'map')
2. Run Sarvis: Debug Error
3. Sarvis explains the root cause and shows a corrected code snippet
```

---

#### `Sarvis: Edit Code with Prompt`
**Shortcut:** `Ctrl+K Ctrl+E` / `Cmd+K Cmd+E`  
**When:** Editor focused

Opens an inline prompt bar. Describe how you want to change the current file and Sarvis edits it directly.

```
Example prompt: "Refactor all callbacks to use async/await"
→ Sarvis rewrites the file in place with a diff preview
```

---

#### `Sarvis: Pair Programmer`
**Shortcut:** `Ctrl+Shift+Space` / `Cmd+Shift+Space`  
**When:** Text selected in editor

Activates a live back-and-forth pair programming session around the selected code.

---

#### `Sarvis: Ask About Codebase`
**Shortcut:** `Ctrl+Shift+A` / `Cmd+Shift+A`

Ask a natural language question about your entire indexed codebase.

```
Example: "Where is the authentication middleware defined?"
→ Sarvis searches the index and points you to the exact file and line
```

---

#### `Sarvis: Index Codebase`
**Shortcut:** `Ctrl+Shift+I` / `Cmd+Shift+I`

Indexes your project so Sarvis can answer questions about the full codebase. Run this once when you open a new project.

---

### Git & Version Control

#### `Sarvis: Generate Commit Message`
**Shortcut:** `Ctrl+Shift+Alt+C` / `Cmd+Shift+Alt+C`  
**Also in:** Source Control panel title bar

Analyzes your staged changes and auto-generates a conventional commit message.

```
Example output:
feat(auth): add JWT refresh token rotation

- Implement token rotation on every refresh
- Store refresh token hash in DB instead of plaintext
- Add 7-day expiry policy
```

---

#### `Sarvis: Summarize Changes`
**Shortcut:** `Ctrl+Shift+Alt+S` / `Cmd+Shift+Alt+S`

Produces a human-readable summary of all current git changes — useful for standups or PR descriptions.

---

#### `Sarvis: Review Diff`
**Shortcut:** `Ctrl+Shift+Alt+R` / `Cmd+Shift+Alt+R`  
**Also in:** Source Control panel title bar

Reviews the current diff for logic issues, code quality, and potential bugs.

---

#### `Sarvis: Detect Risky Changes`
**Shortcut:** `Ctrl+Shift+Alt+K` / `Cmd+Shift+Alt+K`  
**Also in:** Source Control panel title bar

Scans the diff and flags changes that might break existing functionality or introduce regressions.

```
Example output:
⚠️ HIGH RISK: Removed null check on user.id in /src/routes/profile.js:42
⚠️ MEDIUM RISK: Changed default export signature in /lib/api.js
```

---

#### `Sarvis: Create PR`
**Shortcut:** `Ctrl+Shift+Alt+P` / `Cmd+Shift+Alt+P`

Generates a complete pull request description (title, summary, changes, testing notes) from your current branch diff.

---

#### `Sarvis: Review PR`

Fetches an open PR and performs a thorough review, highlighting issues, suggestions, and potential problems.

---

#### `Sarvis: Generate Changelog`
**Shortcut:** `Ctrl+Shift+Alt+L` / `Cmd+Shift+Alt+L`

Generates a structured changelog from your recent git commits, formatted for CHANGELOG.md.

---

### Code Quality & Analysis

#### `Sarvis: Review This File`
**Shortcut:** `Ctrl+Shift+Alt+V` / `Cmd+Shift+Alt+V`

Performs a comprehensive review of the current file — logic, style, best practices, and potential bugs.

---

#### `Sarvis: Fix This Issue`

Available in the **Problems panel** (lightbulb / quick fix). Fixes a specific diagnostic error flagged by VS Code.

---

#### `Sarvis: Fix All Problems in File`
**Shortcut:** `Ctrl+Shift+Alt+H` / `Cmd+Shift+Alt+H`

Scans all VS Code diagnostics in the current file and attempts to fix every problem at once.

---

#### `Sarvis: Fix All Problems in Workspace`
**Shortcut:** `Ctrl+Shift+Alt+Y` / `Cmd+Shift+Alt+Y`

Runs an AI-powered fix pass across every file in the workspace that has diagnostics.

---

#### `Sarvis: Find Root Cause`
**Shortcut:** `Ctrl+Shift+Alt+G` / `Cmd+Shift+Alt+G`

Traces an error back to its root cause by analyzing the call stack, related files, and recent changes.

---

#### `Sarvis: Detect Code Smells in File`
**Shortcut:** `Ctrl+Shift+Alt+O` / `Cmd+Shift+Alt+O`

Identifies anti-patterns, dead branches, overly complex logic, and other code smells in the current file.

---

#### `Sarvis: Detect Code Smells in Project`
**Shortcut:** `Ctrl+Shift+Alt+E` / `Cmd+Shift+Alt+E`

Runs code smell detection across the entire project and produces a consolidated report.

---

#### `Sarvis: Find Dead Code (File)`
**Shortcut:** `Ctrl+Shift+Alt+1` / `Cmd+Shift+Alt+1`

Identifies unreachable or unused code within the current file.

---

#### `Sarvis: Find Dead Code (Project)`
**Shortcut:** `Ctrl+Shift+Alt+2` / `Cmd+Shift+Alt+2`

Scans the entire project for dead code — unused functions, variables, exports, and imports.

---

#### `Sarvis: Code Complexity Map`
**Shortcut:** `Ctrl+K Ctrl+C` / `Cmd+K Cmd+C`

Generates a visual complexity map of the current file, highlighting the most complex functions by cyclomatic complexity.

---

#### `Sarvis: Analyze Dependencies`
**Shortcut:** `Ctrl+Shift+Alt+3` / `Cmd+Shift+Alt+3`

Analyzes your project's dependency graph, identifying circular dependencies, unused packages, and version conflicts.

---

#### `Sarvis: Workspace Health Dashboard`
**Shortcut:** `Ctrl+Shift+Alt+H` / `Cmd+Shift+Alt+H`

Opens an at-a-glance health dashboard for your workspace: errors, warnings, test coverage, complexity, and TODOs.

---

### Documentation

#### `Sarvis: Generate README`
**Shortcut:** `Ctrl+Shift+Alt+M` / `Cmd+Shift+Alt+M`

Analyzes your project structure and generates a comprehensive README.md.

```
Example output includes:
- Project title and description
- Installation instructions
- Usage examples
- API reference (if applicable)
- Contributing guidelines
```

---

#### `Sarvis: Add JSDoc Comments`
**Shortcut:** `Ctrl+Shift+Alt+J` / `Cmd+Shift+Alt+J`

Automatically adds JSDoc comments to all functions, classes, and exports in the current file.

```javascript
// Before
function calculateTax(price, rate) {
  return price * rate;
}

// After — Sarvis adds:
/**
 * Calculates the tax amount for a given price and rate.
 * @param {number} price - The base price before tax.
 * @param {number} rate - The tax rate as a decimal (e.g., 0.08 for 8%).
 * @returns {number} The calculated tax amount.
 */
function calculateTax(price, rate) {
  return price * rate;
}
```

---

#### `Sarvis: Generate Swagger Docs`
**Shortcut:** `Ctrl+Shift+Alt+W` / `Cmd+Shift+Alt+W`

Parses your Express/Fastify/NestJS routes and generates OpenAPI 3.0 (Swagger) documentation.

---

#### `Sarvis: Generate API Docs`
**Shortcut:** `Ctrl+Shift+Alt+D` / `Cmd+Shift+Alt+D`

Creates developer-friendly API documentation from your route handlers, including request/response shapes and examples.

---

### Refactoring & Migration

#### `Sarvis: Refactor This File`
**Shortcut:** `Ctrl+Shift+Alt+B` / `Cmd+Shift+Alt+B`

Refactors the current file: cleans up structure, applies consistent patterns, and removes redundancy — with a diff preview.

---

#### `Sarvis: Refactor Project (Multi-File)`
**Shortcut:** `Ctrl+Shift+Alt+Q` / `Cmd+Shift+Alt+Q`

Performs a project-wide refactor pass. Useful for renaming patterns, updating APIs, or enforcing a new convention.

---

#### `Sarvis: Migrate Code`
**Shortcut:** `Ctrl+K Ctrl+M` / `Cmd+K Cmd+M`

Migrates code to a different version, framework, or language.

```
Example prompts:
- "Migrate this from JavaScript to TypeScript"
- "Convert class components to React functional components with hooks"
- "Upgrade from Express 4 to Express 5 syntax"
```

---

### Testing

#### `Sarvis: Generate Test Cases`
**Shortcut:** `Ctrl+Shift+U` / `Cmd+Shift+U`

Generates comprehensive unit tests for the current file, covering happy paths, edge cases, and error cases.

```javascript
// Sarvis generates tests for your function using your project's existing test framework:
describe('calculateTax', () => {
  it('should calculate tax correctly', () => {
    expect(calculateTax(100, 0.08)).toBe(8);
  });
  it('should return 0 for zero rate', () => {
    expect(calculateTax(100, 0)).toBe(0);
  });
  it('should handle negative prices', () => {
    expect(calculateTax(-50, 0.1)).toBe(-5);
  });
});
```

---

#### `Sarvis: Run Tests`
**Shortcut:** `Ctrl+Shift+Alt+T` / `Cmd+Shift+Alt+T`

Runs the test suite for the current project and displays results in the Sarvis panel.

---

#### `Sarvis: Run Tests + Auto-Fix`
**Shortcut:** `Ctrl+Shift+Alt+F` / `Cmd+Shift+Alt+F`

Runs the test suite and automatically attempts to fix any failing tests using AI.

---

### Security & Performance

#### `Sarvis: Security Scan (File)`
**Shortcut:** `Ctrl+Shift+Alt+S` / `Cmd+Shift+Alt+S`

Scans the current file for security vulnerabilities: SQL injection, XSS, hardcoded secrets, insecure dependencies, etc.

```
Example output:
🔴 CRITICAL  Line 23: Possible SQL injection — user input concatenated into query
🟡 WARNING   Line 47: Hardcoded API key detected
🟡 WARNING   Line 89: eval() usage — potential code injection risk
```

---

#### `Sarvis: Security Scan (Project)`
**Shortcut:** `Ctrl+Shift+Alt+X` / `Cmd+Shift+Alt+X`

Runs a comprehensive security audit across all project files and exports a report.

---

#### `Sarvis: Analyze Performance (File)`
**Shortcut:** `Ctrl+Shift+Alt+8` / `Cmd+Shift+Alt+8`

Identifies performance bottlenecks in the current file: expensive loops, synchronous blocking calls, memory leaks, etc.

---

#### `Sarvis: Analyze Performance (Project)`
**Shortcut:** `Ctrl+Shift+Alt+9` / `Cmd+Shift+Alt+9`

Runs performance analysis across the entire project.

---

### Memory & Context

Sarvis maintains a **session memory** so it stays aware of what you're working on throughout your coding session.

#### `Sarvis: Set Current Bug`
**Shortcut:** `Ctrl+Shift+Alt+5` / `Cmd+Shift+Alt+5`

Tell Sarvis what bug you're currently investigating. It will keep this context across all subsequent commands.

```
Example: "Users are getting logged out randomly after about 10 minutes"
```

---

#### `Sarvis: Set Current Feature`
**Shortcut:** `Ctrl+Shift+Alt+6` / `Cmd+Shift+Alt+6`

Set the feature you're currently building so Sarvis can give more relevant suggestions.

```
Example: "Implementing OAuth2 with GitHub as a provider"
```

---

#### `Sarvis: Set Project Goal`

Define the high-level goal of your project for richer context in all AI responses.

---

#### `Sarvis: Add Memory Note`
**Shortcut:** `Ctrl+Shift+Alt+7` / `Cmd+Shift+Alt+7`

Add a freeform note to session memory.

```
Example: "The DB uses soft deletes — never hard-delete records"
```

---

#### `Sarvis: View Session Memory`
**Shortcut:** `Ctrl+Shift+Alt+4` / `Cmd+Shift+Alt+4`

Opens a panel showing everything Sarvis currently knows about your session context.

---

#### `Sarvis: Clear Session Memory`

Resets all session memory (bug, feature, goal, notes).

---

### Diagrams & Architecture

#### `Sarvis: Generate Architecture Diagram`
**Shortcut:** `Ctrl+K Ctrl+D` / `Cmd+K Cmd+D`

Analyzes your project structure and generates a visual architecture diagram (rendered as Mermaid or SVG).

```
Example output — a Mermaid diagram:
graph TD
  A[Client] --> B[API Gateway]
  B --> C[Auth Service]
  B --> D[User Service]
  D --> E[(PostgreSQL)]
```

---

#### `Sarvis: Generate Architecture`
**Shortcut:** `Ctrl+Shift+Alt+Z` / `Cmd+Shift+Alt+Z`

Suggests an architecture for a new feature or system based on your project context.

---

#### `Sarvis: Add Architecture Note`

Annotate a section of code with a high-level architecture note that persists in session memory.

---

### Developer Productivity

#### `Sarvis: Scan TODOs (Project)`
**Shortcut:** `Ctrl+Shift+Alt+0` / `Cmd+Shift+Alt+0`

Collects all TODO, FIXME, HACK, and NOTE comments across the project and presents them in a prioritized list.

---

#### `Sarvis: Scan TODOs (File)`
**Shortcut:** `Ctrl+Shift+Alt+\`` / `Cmd+Shift+Alt+\``

Same as above, scoped to the current file only.

---

#### `Sarvis: Generate Standup Report`
**Shortcut:** `Ctrl+Shift+Alt+=` / `Cmd+Shift+Alt+=`

Generates a daily standup summary based on your recent git commits and session memory.

```
Example output:
✅ Yesterday: Implemented JWT refresh rotation, fixed null-check bug in profile route
🔨 Today: Starting OAuth2 GitHub integration
🚧 Blockers: Need access to staging DB credentials
```

---

#### `Sarvis: Insert Smart Snippet`
**Shortcut:** `Ctrl+Shift+Alt+J` / `Cmd+Shift+Alt+J`

Inserts a context-aware code snippet at your cursor based on surrounding code and your session context.

---

#### `Sarvis: Add Custom Snippet Trigger`

Define your own snippet shortcuts. Type a trigger word and Sarvis expands it into full code.

```
Example: Trigger "apiroute" → Sarvis inserts your standard Express route boilerplate
```

---

#### `Sarvis: Prompt Templates`
**Shortcut:** `Ctrl+Shift+Alt+T` / `Cmd+Shift+Alt+T`

Opens a library of pre-built prompt templates for common tasks (review, refactor, document, etc.).

---

#### `Sarvis: Learn From This File`
**Shortcut:** `Ctrl+Shift+Alt+N` / `Cmd+Shift+Alt+N`

Sarvis analyzes the current file and updates your coding profile with patterns, libraries, and conventions you use.

---

#### `Sarvis: View My Coding Profile`
**Shortcut:** `Ctrl+Shift+Alt+L` / `Cmd+Shift+Alt+L`

Displays your personalized coding profile: preferred languages, frameworks, patterns, and skill areas.

---

#### `Sarvis: Practice Interview`
**Shortcut:** `Ctrl+Shift+Alt+I` / `Cmd+Shift+Alt+I`

Starts an interactive coding interview practice session tailored to your skill profile.

---

#### `Sarvis: Voice Command`
**Shortcut:** `Ctrl+Shift+Alt+V` / `Cmd+Shift+Alt+V`

Activates voice input — speak your command or code request and Sarvis executes it.

---

#### `Sarvis: Toggle Live Error Explainer`

Toggles AI-powered hover explanations for VS Code diagnostic errors. When enabled, hovering over a red underline shows a plain-English explanation and suggested fix.

---

#### `Sarvis: Toggle Review on Save`

Toggles automatic code review every time you save a file.

---

### Terminal Commands

#### `Sarvis: Generate Terminal Command`
**Shortcut:** `Ctrl+Shift+X` / `Cmd+Shift+X` *(when terminal is focused)*  
**Also in:** Terminal right-click menu

Describe what you want to do in plain English and Sarvis generates the shell command.

```
Example: "Find all .log files larger than 100MB and delete them"
→ find . -name "*.log" -size +100M -delete
```

---

#### `Sarvis: Fix Terminal Error`
**Shortcut:** `Ctrl+Shift+F` / `Cmd+Shift+F` *(when terminal is focused)*  
**Also in:** Terminal right-click menu

Copy a terminal error, run this command, and Sarvis diagnoses the error and provides a fix.

```
Example terminal error:
Error: Cannot find module 'express'

→ Sarvis: Run `npm install express` — the package is missing from node_modules
```

---

## ⌨️ Keyboard Shortcuts

### Quick Reference

| Command | Windows/Linux | macOS |
|---|---|---|
| Explain Selected Code | `Ctrl+Shift+E` | `Cmd+Shift+E` |
| Generate Code | `Ctrl+Shift+G` | `Cmd+Shift+G` |
| Debug Error | `Ctrl+Shift+D` | `Cmd+Shift+D` |
| Generate Tests | `Ctrl+Shift+U` | `Cmd+Shift+U` |
| Ask About Codebase | `Ctrl+Shift+A` | `Cmd+Shift+A` |
| Index Codebase | `Ctrl+Shift+I` | `Cmd+Shift+I` |
| Edit Code with Prompt | `Ctrl+K Ctrl+E` | `Cmd+K Cmd+E` |
| Pair Programmer | `Ctrl+Shift+Space` | `Cmd+Shift+Space` |
| Git Commit Message | `Ctrl+Shift+Alt+C` | `Cmd+Shift+Alt+C` |
| Git Review Diff | `Ctrl+Shift+Alt+R` | `Cmd+Shift+Alt+R` |
| Detect Risky Changes | `Ctrl+Shift+Alt+K` | `Cmd+Shift+Alt+K` |
| Security Scan (File) | `Ctrl+Shift+Alt+S` | `Cmd+Shift+Alt+S` |
| Security Scan (Project) | `Ctrl+Shift+Alt+X` | `Cmd+Shift+Alt+X` |
| Refactor File | `Ctrl+Shift+Alt+B` | `Cmd+Shift+Alt+B` |
| Generate README | `Ctrl+Shift+Alt+M` | `Cmd+Shift+Alt+M` |
| Add JSDoc | `Ctrl+Shift+Alt+J` | `Cmd+Shift+Alt+J` |
| Generate Swagger | `Ctrl+Shift+Alt+W` | `Cmd+Shift+Alt+W` |
| Complexity Map | `Ctrl+K Ctrl+C` | `Cmd+K Cmd+C` |
| Architecture Diagram | `Ctrl+K Ctrl+D` | `Cmd+K Cmd+D` |
| Find Dead Code (File) | `Ctrl+Shift+Alt+1` | `Cmd+Shift+Alt+1` |
| Find Dead Code (Project) | `Ctrl+Shift+Alt+2` | `Cmd+Shift+Alt+2` |
| Analyze Dependencies | `Ctrl+Shift+Alt+3` | `Cmd+Shift+Alt+3` |
| View Session Memory | `Ctrl+Shift+Alt+4` | `Cmd+Shift+Alt+4` |
| Set Current Bug | `Ctrl+Shift+Alt+5` | `Cmd+Shift+Alt+5` |
| Set Current Feature | `Ctrl+Shift+Alt+6` | `Cmd+Shift+Alt+6` |
| Add Memory Note | `Ctrl+Shift+Alt+7` | `Cmd+Shift+Alt+7` |
| Analyze Performance (File) | `Ctrl+Shift+Alt+8` | `Cmd+Shift+Alt+8` |
| Analyze Performance (Project) | `Ctrl+Shift+Alt+9` | `Cmd+Shift+Alt+9` |
| Scan TODOs (Project) | `Ctrl+Shift+Alt+0` | `Cmd+Shift+Alt+0` |
| Run Tests | `Ctrl+Shift+Alt+T` | `Cmd+Shift+Alt+T` |
| Run Tests + Auto-Fix | `Ctrl+Shift+Alt+F` | `Cmd+Shift+Alt+F` |
| Health Dashboard | `Ctrl+Shift+Alt+H` | `Cmd+Shift+Alt+H` |
| Standup Report | `Ctrl+Shift+Alt+=` | `Cmd+Shift+Alt+=` |
| Generate Changelog | `Ctrl+Shift+Alt+L` | `Cmd+Shift+Alt+L` |
| Create PR | `Ctrl+Shift+Alt+P` | `Cmd+Shift+Alt+P` |
| Voice Command | `Ctrl+Shift+Alt+V` | `Cmd+Shift+Alt+V` |
| Practice Interview | `Ctrl+Shift+Alt+I` | `Cmd+Shift+Alt+I` |
| Fix Terminal Error | `Ctrl+Shift+F` *(terminal)* | `Cmd+Shift+F` *(terminal)* |
| Generate Terminal Command | `Ctrl+Shift+X` *(terminal)* | `Cmd+Shift+X` *(terminal)* |

---

## ⚙️ Configuration

Open VS Code Settings (`Ctrl+,`) and search for **Sarvis** to configure the following:

| Setting | Type | Default | Description |
|---|---|---|---|
| `sarvis.reviewOnSave` | boolean | `true` | Automatically review code when saving a file |
| `sarvis.errorExplainer` | boolean | `true` | Show AI-powered error explanations on hover |
| `sarvis.errorExplainerDelay` | number | `500` | Delay (ms) before fetching error explanation on hover |
| `sarvis.completionMode` | string | `"balanced"` | Inline completion aggressiveness: `conservative`, `balanced`, or `creative` |
| `sarvis.customSnippetTriggers` | object | `{}` | Custom snippet triggers — key = trigger word, value = description |
| `sarvis.showBranding` | boolean | `true` | Show Sarvis branding when a suggestion is accepted |

### Example `settings.json`

```json
{
  "sarvis.completionMode": "creative",
  "sarvis.reviewOnSave": false,
  "sarvis.errorExplainerDelay": 300,
  "sarvis.customSnippetTriggers": {
    "apiroute": "Express GET route with error handling and async/await",
    "mongoose": "Mongoose schema with timestamps and validation"
  }
}
```

---

## 🛠️ Development Setup

Want to contribute or run Sarvis locally?

```bash
# 1. Clone the repository
git clone https://github.com/Sarvium/sarvis.git
cd sarvis

# 2. Install dependencies
npm install

# 3. Build the extension
node esbuild.js

# 4. Open in VS Code
code .

# 5. Press F5 to launch the Extension Development Host
```

### Watch Mode (auto-rebuild on changes)

```bash
node esbuild.js --watch
```

### Project Structure

```
sarvis/
├── src/               # TypeScript source files
├── media/             # Icons and assets
├── out/               # Compiled output (generated)
├── esbuild.js         # Build configuration
└── package.json       # Extension manifest
```

### Commit Message Convention

```
feat:      New feature
fix:       Bug fix
docs:      Documentation changes
style:     Formatting, no logic change
refactor:  Code restructure
chore:     Build / config changes
test:      Adding or updating tests
```

---

## 🗺️ Roadmap

- [ ] Multi-language support (Hindi, Tamil, Telugu via Sarvam)
- [ ] Chat history persistence across sessions
- [ ] Custom system prompt configuration
- [ ] Support for multiple AI models
- [ ] Workspace-level context awareness
- [ ] Inline diff editor for AI suggestions
- [ ] GitHub Copilot–style ghost text completions

---

## 🐛 Reporting a Bug

Found something broken? We want to fix it fast.

**Before reporting:**
- Check [open issues](https://github.com/Sarvium/sarvis/issues) to avoid duplicates
- Make sure you're on the latest version
- Try reloading VS Code: `Ctrl+Shift+P` → `Reload Window`

👉 [**Open a Bug Report**](https://github.com/Sarvium/sarvis/issues/new?template=bug_report.md&labels=bug)

Please include:
```
VS Code Version:   Help → About
Sarvis Version:    Extensions panel → Sarvis
OS:                Windows / macOS / Linux

What happened:     Clear description of the bug
Steps to reproduce:
  1. ...
  2. ...
Expected behavior: What you expected
Logs:              View → Output → "Extension Host"
```

---

## 💡 Requesting a Feature

👉 [**Open a Feature Request**](https://github.com/Sarvium/sarvis/issues/new?template=feature_request.md&labels=enhancement)

Include: what problem it solves, how you'd like it to work, and any examples or references.

---

## 📋 Issue Labels

| Label | Description |
|---|---|
| `bug` | Something isn't working |
| `enhancement` | New feature request |
| `question` | General question |
| `good first issue` | Great for new contributors |
| `help wanted` | Extra attention needed |
| `wontfix` | Will not be addressed |
| `duplicate` | Already reported |

---

## 📄 License

MIT License © 2024 [Sarvium](https://sarvium.com)

See [LICENSE](LICENSE) for full text.

---

## 👨‍💻 Credits

<table>
  <tr>
    <td align="center"><strong>Created by</strong><br/><a href="https://sarvium.com">Sarvium</a></td>
    <td align="center"><strong>Developed by</strong><br/><a href="https://github.com/AkashKobal">Akash Kobal</a></td>
    <td align="center"><strong>Powered by</strong><br/><a href="https://sarvam.ai">Sarvam AI</a></td>
  </tr>
</table>

---

<p align="center">
  Built with ❤️ by <a href="https://sarvium.com">Sarvium</a> &nbsp;·&nbsp; Developed by <a href="https://github.com/AkashKobal">Akash Kobal</a>
</p>
