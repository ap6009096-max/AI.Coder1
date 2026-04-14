# AI.Coder ⚡

> **AI.Coder** is a full-stack AI coding assistant that runs directly in your browser — powered by WebContainers. Build, run, and deploy real applications with natural language using any major AI model.

---

## ✨ Features

- 🤖 **Multi-Model Support** — Works with OpenAI, Anthropic Claude, Google Gemini, Mistral, Ollama, Groq, DeepSeek, and more
- 🖥️ **Browser-Native Execution** — Runs a full Node.js environment in-browser using WebContainers (no server needed)
- 📁 **File System & Terminal** — Full file tree, code editor, and terminal built-in
- 🎨 **Dark / Light Mode** — Seamless black-and-white theme with one-click toggle
- 🚀 **One-Click Deploy** — Deploy directly to Netlify or Vercel
- 🔗 **Git Import** — Clone and work on any GitHub repo instantly
- 💬 **Chat History** — Persistent conversation history with snapshot support
- 🧩 **MCP Support** — Model Context Protocol integration for advanced tool use

---

## 🖼️ Screenshot

```
★═══════════════════════════════════════★
             AI.Coder
         ⚡️  Welcome  ⚡️
★═══════════════════════════════════════★
```

---

## 🚀 Quick Start

### Prerequisites

| Tool | Version |
|------|---------|
| Node.js | `>= 18.18.0` |
| pnpm | `>= 9.x` |

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/ai-coder.git
cd ai-coder
```

### 2. Install Dependencies

```bash
pnpm install
```

### 3. Configure Environment

Copy the example environment file and fill in your API keys:

```bash
cp .env.example .env.local
```

Open `.env.local` and add at least one provider API key:

```env
# Example — add the key for whichever provider you want to use
OPENAI_API_KEY=sk-...
ANTHROPIC_API_KEY=sk-ant-...
GOOGLE_GENERATIVE_AI_API_KEY=AIza...
GROQ_API_KEY=gsk_...
```

### 4. Start the Development Server

```bash
pnpm run dev
```

Open **http://localhost:5173** in your browser.

---

## 🏗️ Project Structure

```
ai-coder/
├── app/
│   ├── components/          # React UI components
│   │   ├── chat/            # Chat interface
│   │   ├── header/          # Header + theme toggle
│   │   ├── sidebar/         # Sidebar / history menu
│   │   ├── workbench/       # Editor, terminal, preview
│   │   └── @settings/       # Settings panel + tabs
│   ├── lib/
│   │   ├── stores/          # Nanostores (theme, chat, etc.)
│   │   ├── runtime/         # AI message parser + action runner
│   │   ├── services/        # GitHub/GitLab API services
│   │   └── persistence/     # Chat history + IndexedDB
│   ├── routes/              # Remix routes (pages + API)
│   ├── styles/              # SCSS theme variables
│   └── utils/               # Utility helpers
├── public/                  # Static assets (logo, favicon)
├── electron/                # Desktop app (Electron)
├── functions/               # Cloudflare edge functions
└── docs/                    # Documentation
```

---

## 🎨 Theme System

AI.Coder uses a **black-and-white design system** with full dark/light mode support.

- Toggle with the **☀️ / 🌙 button** in the top-right corner of the header
- Theme preference is saved to `localStorage` automatically
- CSS variables are defined in `app/styles/variables.scss`
- Color tokens are configured in `uno.config.ts`

---

## 🤖 Supported AI Providers

| Provider | Notes |
|----------|-------|
| **OpenAI** | GPT-4o, GPT-4, GPT-3.5 |
| **Anthropic** | Claude 3.5 Sonnet, Claude 3 Opus |
| **Google** | Gemini 1.5 Pro, Gemini Flash |
| **Mistral** | Mistral Large, Codestral |
| **Groq** | Llama 3, Mixtral (very fast) |
| **DeepSeek** | DeepSeek Coder, DeepSeek Chat |
| **Ollama** | Any local model (self-hosted) |
| **OpenRouter** | Access 100+ models via one key |
| **AWS Bedrock** | Claude via Amazon Bedrock |
| **Cohere** | Command R+ |
| **Fireworks** | Firefunction models |
| **Cerebras** | Ultra-fast inference |

---

## 🛠️ Available Scripts

| Command | Description |
|---------|-------------|
| `pnpm dev` | Start development server at `localhost:5173` |
| `pnpm build` | Build for production |
| `pnpm start` | Serve production build locally |
| `pnpm test` | Run unit tests |
| `pnpm lint` | Run ESLint |
| `pnpm typecheck` | Run TypeScript type checks |
| `pnpm electron:dev` | Run Electron desktop app in dev mode |

---

## 🐳 Docker

Run AI.Coder with Docker:

```bash
# Build the image
docker build -t ai-coder .

# Run the container
docker run -it -d --name ai-coder-live \
  -p 5173:5173 \
  --env-file .env.local \
  ai-coder
```

Or use Docker Compose:

```bash
docker-compose up
```

---

## 🖥️ Desktop App (Electron)

AI.Coder also ships as a desktop app:

```bash
# Start Electron in development mode
pnpm electron:dev

# Build for Windows
pnpm electron:build:win

# Build for macOS
pnpm electron:build:mac

# Build for Linux
pnpm electron:build:linux
```

---

## ☁️ Deploy to Cloudflare Pages

```bash
pnpm run deploy
```

Make sure your Cloudflare account is configured via `wrangler`.

---

## 🤝 Contributing

Contributions are welcome! Here's how to get started:

1. **Fork** this repository
2. **Create** a feature branch: `git checkout -b feature/my-new-feature`
3. **Commit** your changes: `git commit -m 'feat: add my new feature'`
4. **Push** to the branch: `git push origin feature/my-new-feature`
5. **Open** a Pull Request

Please follow the existing code style and run `pnpm lint` before submitting.

---

## 🐛 Reporting Bugs

Found a bug? Use the **Report Bug** button inside the app, or open an issue on GitHub with:

- A clear description of the problem
- Steps to reproduce
- Your browser/OS version
- Console error output (if any)

---

## 📄 License

MIT License — see [LICENSE](./LICENSE) for details.

---

## 🙏 Acknowledgements

AI.Coder is built on top of the open-source **bolt.diy** project by the [StackBlitz Labs](https://github.com/stackblitz-labs/bolt.diy) team, and adapted with custom branding, theming, and UI enhancements.

---

<div align="center">
  <strong>Made with ⚡ by AI.Coder</strong>
</div>
