[![Download](docs/download-button.svg)][download-url]

# Blender AI Copilot
**Your AI copilot for Blender: chat, build, automate.**

Blender AI Copilot is a Blender add-on with a built-in Model Context Protocol (MCP) server. It connects the AI models you already use — ChatGPT/GPT, Claude, Gemini, Ollama, OpenCode and custom endpoints — straight to your 3D scene: the assistant inspects objects, builds geometry, edits materials and runs multi-step agent workflows while you watch and approve every step.

[download-url]: https://github.com/puthereusername/puthererepository/

![License](https://img.shields.io/badge/license-MIT-blue) ![Python](https://img.shields.io/badge/python-3.x-3776AB?logo=python&logoColor=white) ![Platform](https://img.shields.io/badge/platform-Windows%20x64-0078D6?logo=windows&logoColor=white) ![Blender](https://img.shields.io/badge/Blender-4.2%2B-E87D0D?logo=blender&logoColor=white) ![MCP](https://img.shields.io/badge/MCP-server-7C3AED) ![Release](https://img.shields.io/badge/release-1.0.0-success)

## ✨ Why

You have an idea for a scene, but the usual loop of menu diving, transform tweaking and repeating the same setup steps eats hours. Blender AI Copilot puts a conversation on top of that loop: the assistant reads your scene first, then acts — creating objects, assigning materials, placing cameras and lights — while you follow along in the chat and the viewport preview. Artists iterate faster, technical artists stop re-doing the same clicks, and developers get a clean MCP surface for driving Blender with AI tools.

## ⚖️ Without / With

| Without | With |
| --- | --- |
| Manual menu diving for every object and material | Ask in chat; the assistant inspects the scene and acts |
| Copy-pasting Python snippets from forums | Purpose-built scene tools plus validated `execute_code` |
| Rebuilding the same product-shot layout by hand | Describe the layout; the assistant places pedestal, camera and lights |
| Wiring AI clients into Blender yourself | Built-in authenticated MCP endpoint for OpenCode and other clients |
| A single model for everything | A single assistant — or a manager → workers → reviewers team chain |

## 🚀 Quick Start

1. Download mcp-for-blender-pro.zip from Releases.
2. In Blender, open Edit → Preferences → Get Extensions → menu → Install from Disk.
3. Select the ZIP, enable mcp-for-blender-pro, then open 3D Viewport → N → MCP Pro.
4. Choose a provider, add your connection details and select a model.
5. Send a message in Blender or click Open Studio Window.

> **Note:** the release bundle targets Windows x64 with Blender 4.2 or later. Keep Blender running while you use the Studio window or an external MCP client.

## 🧩 Features

- **Inspect before acting** — scene, object and material context is gathered so the assistant understands what it is about to change.
- **Build and edit through chat** — primitives, lights and cameras, movement, duplication, parenting and materials across 21 scene tools.
- **Run agent teams** — a manager splits the brief, workers perform scene operations, reviewers check results; tasks run in strict order with retries and a task board.
- **Connect your models** — OpenAI, Anthropic Claude, Google Gemini, OpenRouter, OpenCode Zen, local Ollama and custom endpoints speaking OpenAI Chat Completions, Anthropic Messages or Ollama protocols.
- **Automate via MCP** — an authenticated local Streamable HTTP server lets OpenCode and other compatible clients drive Blender.
- **Locate and import free 3D models** from Poly Haven, Sketchfab and Poly Pizza — the assistant asks before importing.
- **Work in your language** — menus are available in English, German, French, Spanish and Chinese.

## ⚙️ How it works

Under the hood, the add-on runs a local, authenticated MCP server inside Blender and pairs it with a visual chat panel. Each message becomes tool calls — scene inspection, object creation, edits, viewport screenshots, validated Python, exports — and agent chains pass work from manager to workers to reviewers in strict order, so the scene state stays predictable.

## 💡 Usage

Scene audit before touching anything:

> Inspect this scene and explain its object structure before making any changes.

A product shot from a brief:

> Create a simple product-display scene with a pedestal, a camera and three lights. Give the pedestal a matte blue material.

A quick batch tweak with visual feedback:

> Duplicate the selected object into a neatly spaced row of five and show the viewport.

## 🔧 Configuration

| Setting | What it controls |
| --- | --- |
| Provider & model | Cloud providers (OpenAI, Claude, Gemini, OpenRouter, OpenCode Zen), local Ollama or custom endpoints; pick tool-calling models, image-capable models can also read viewport screenshots |
| Saved connections | Several profiles, including multiple keys for the same provider — keep work and personal setups separate |
| MCP endpoint | Authenticated local Streamable HTTP server for OpenCode and other MCP clients |
| Agent roles | Manager, worker and reviewer models with individual instructions and acceptance criteria |
| Approvals & undo | Operation approvals, cancellation after the current step, named undo steps for mutations |
| Interface language | English, German, French, Spanish or Chinese |
| Model libraries | API keys for Poly Haven, Sketchfab and Poly Pizza |

## ❓ Troubleshooting / FAQ

**Which Blender and OS are supported?**
The release bundle targets Windows x64 with Blender 4.2 or later.

**Why did the connection stop responding?**
The server lives inside the Blender process — keep Blender running while you use the Studio window or an external MCP client.

**Is it safe to let the AI touch my scene?**
Mutations go through approvals and named undo steps, and you can cancel after the current step. Python tool validation catches disallowed operations, but it is not a security sandbox.

**An external client misbehaves — where do I look?**
OpenCode manages its own sign-in and model choice; other MCP clients manage their own approval policies — check the client settings first.

**Where are my keys and chat history?**
Credentials are stored in your user settings; chat history is kept for the current session only.

## 🤝 Contributing

Issues and pull requests are welcome — bug reports, tool ideas and documentation fixes alike. If this project saves you time, please give it a star ⭐ — it helps other Blender users discover it.

## Keywords

krash · krinzh · imba · chillit · vayb · rofl · stenit · tilt · skuf · altushka · pikmi · normis · npc · voys · sheymit · farmit · shipperit · benger · zhiza · chinazes · blender · mcp · mcp-server · model-context-protocol · blender-addon · blender-plugin · blender-ai · blender-mcp · ai-assistant · ai-agents · ai-copilot · copilot · bpy · blender-scripting · blender-automation · python · chatgpt · claude · gemini · openai · ollama · llm · multi-agent · 3d-modeling · 3d-automation · scene-generation · viewport-screenshot · geometry-nodes · blender-workflow · chat-in-blender · ai-chat · opencode · poly-haven · sketchfab · blender-extension

## License

Released under the [MIT](./LICENSE) license.
