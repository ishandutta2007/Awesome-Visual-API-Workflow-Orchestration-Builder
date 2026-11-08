# Awesome-Visual-API-Workflow-Orchestration-Builder

# Awesome Visual API Workflow & Orchestration Builder

> A curated list of top Visual API Workflow and Orchestration Builder platforms — both SaaS/Hosted commercial solutions and open-source alternatives for designing, automating, and orchestrating API-driven workflows with visual canvases.  
> 🌟 Star this repo if you find it useful! 🌟

---

## 📋 Table of Contents

- [SaaS / Hosted Platforms](#-saas--hosted-platforms)
  - [Postman Flows](#postman-flows)
  - [Zapier](#zapier)
  - [Make](#make)
  - [Tray.io](#trayio)
  - [Workato](#workato)
  - [Pipedream](#pipedream)
- [Open-Source Software](#-open-source-software)
  - [n8n](#n8n)
  - [Activepieces](#activepieces)
  - [Node-RED](#node-red)
  - [Flowise](#flowise)
  - [Windmill](#windmill)
  - [Fluxify](#fluxify)
  - [Open Flow](#open-flow)
  - [napflow](#napflow)
  - [MEL Agent](#mel-agent)
- [Comparison at a Glance](#-comparison-at-a-glance)
- [Contributing](#-contributing)

---

## 🟦 SaaS / Hosted Platforms

Commercial, cloud-hosted Visual API Workflow and Orchestration Builder platforms. These are not open-source but are included as reference points for feature comparison.

### Postman Flows
**Type:** API-centric visual workflow builder  
Postman Flows provides a visual canvas for chaining API requests, transforming data, and orchestrating multi-step API workflows. It is tightly integrated with Postman collections and environments, making it a natural choice for teams already using Postman for API testing. The platform focuses on API request/response orchestration rather than general-purpose automation, with visual debugging and run logs.

### Zapier
**Type:** No-code automation with API connectivity  
Zapier connects 7,000+ apps with trigger-action workflows, including Webhooks by Zapier for custom API calls. Multi-step Zaps support filters, formatters, and Paths for branching. While not purpose-built for complex API orchestration, it is widely used for lightweight API-driven automations without code.

### Make
**Type:** Visual automation with granular data control  
Make's scenario builder shows data flowing between modules, with powerful data transformation, iteration, and error handling. Its HTTP module allows arbitrary API calls, and the visual canvas makes complex API workflows easier to reason about than linear automation tools. Pricing scales per operation, which can become expensive at volume.

### Tray.io
**Type:** Enterprise iPaaS with API orchestration  
Tray.io provides a visual workflow canvas with 650+ connectors, JSONata data mapping, and a Connector SDK for custom API integrations. Its **Headless** offering allows building workflows from AI coding agents (Claude Code, Cursor, MCP clients) against the hosted platform, with everything opening in the visual builder [citation:12]. Features include callable workflows for reusable logic and Insights for health monitoring. Managed cloud only.

### Workato
**Type:** Enterprise automation with governance  
Workato combines enterprise-grade security with a consumer-grade design interface, targeting both IT and business users. Recipes can orchestrate complex API-driven processes across cloud and on-premises systems, with cross-enterprise visibility for IT governance. The Connector SDK enables custom API integrations.

### Pipedream
**Type:** Developer-focused event source platform  
Pipedream provides HTTP webhook triggers and API integrations with code-first Node.js/Python steps, built-in auth handling, and event history. Suited for developers wanting programmatic control over API workflows without a visual-only constraint. **Note:** Pipedream Workflows is closing, according to a 2026 report [citation:12].

---

## 🟩 Open-Source Software

Self-hosted, community-driven Visual API Workflow and Orchestration Builder tools. All listed projects offer source code you can deploy on your own infrastructure.

### n8n
**Stack:** TypeScript / Node.js | **License:** Sustainable Use License (source-available, not OSI)  
n8n is the most widely adopted source-available workflow automation platform, with a visual canvas and 500+ native integrations. Any API can be called via HTTP, and any agent via MCP. Workflows can mix visual building with custom code (JavaScript/Python) where needed. Key differentiators include full visibility into agent decisions, human-in-the-loop approval steps, and replay of past runs for debugging. **Important:** The license restricts certain commercial resale; self-hosting for internal use is permitted.

### Activepieces
**Stack:** TypeScript | **License:** MIT (Community Edition)  
Activepieces is a genuinely MIT-licensed open-source automation platform positioned as a permissively licensed alternative to n8n [citation:5]. The Community Edition is free to self-host with a visual builder, AI-ready pieces, human-in-the-loop approval pieces, and 200+ integrations. Features include loops, branches, auto retries, HTTP, and code with NPM. Self-hosted and network-gapped for maximum security.  
**Best for:** Teams wanting an MIT-licensed, self-hostable automation platform without the source-available restrictions of n8n.

### Node-RED
**Stack:** Node.js | **License:** Apache 2.0  
Node-RED is a long-running open-source flow editor under the OpenJS Foundation, with a large community and no vendor pricing [citation:12]. It is built for **event-driven automation, IoT, and workloads close to the hardware** — its node catalogue reflects event routing rather than business system integration. The project itself has no SSO, access control, or audit trail; those must be built or added via third-party support (e.g., FlowFuse) [citation:12].  
**Best for:** IoT, edge computing, and event-driven data flows where visual wiring of devices and services is the priority.

### Flowise
**Stack:** TypeScript / Node.js | **License:** Apache 2.0 (Open Source)  
Flowise is an open-source generative AI development platform for building AI Agents and LLM workflows with three visual builders: Assistant (beginner-friendly), Chatflow (single-agent systems), and Agentflow (multi-agent orchestration) [citation:6]. Connects to 100+ sources, tools, vector databases, and memories. Features include execution logs, visual debugging, self-hosted/air-gapped deployment, API/SDK/CLI access, and RBAC/SSO on enterprise tiers.  
**Best for:** Teams building AI agent and LLM-powered workflows who want a visual builder specifically designed for generative AI orchestration.

### Windmill
**Stack:** Rust / Svelte / PostgreSQL | **License:** AGPL-3.0 (Community Edition)  
Windmill is a code-first developer platform that turns scripts (Python, TypeScript, Go, Bash, SQL) into workflows, webhooks, and UIs. Every script auto-generates a UI form from its parameters, enabling rapid internal tool creation without frontend development. Flows can include an AI agent step that uses your scripts as tools, and an MCP server exposes scripts and flows to AI assistants [citation:12]. Claims 13x faster than Airflow for job execution.  
**Best for:** Engineering teams that would rather write code than assemble nodes, while still wanting visual flow orchestration and auto-generated UIs.

### Fluxify
**Stack:** Bun / TypeScript | **License:** Apache 2.0 (open-source core)  
Fluxify is a production-grade, low-code agentic backend platform that turns a visual workflow into a **real, compiled API** . You draw the flow, and it is translated into JavaScript once when you save; requests run that code directly, with no graph walking. Supports databases, key-value stores, message queues, AI models, and observability integrations. Custom blocks are supported. Enterprise features are gated under a separate license .  
**Best for:** Teams wanting the performance of compiled code with the convenience of a visual workflow builder, particularly for backend API orchestration.

### Open Flow
**Stack:** TypeScript / Node.js | **License:** Open Source (per repository)  
Open Flow is an open-source workflow platform designed for **AI-assisted building with visual verification** [citation:2]. You can ask Codex, Claude Code, or another agent to build a Flow, open it in the Workbench, and refine it together. Combines JavaScript, connected apps, AI, branching, and human approval in one canvas. Features include explicit input sources, branches and reusable subflows, LLM/Agent tasks with approval policies, and versioned publishing. Connects apps via OpenConnector without putting credentials in the graph. Self-hosted via Docker or Fly.io [citation:2].  
**Best for:** Teams wanting AI agents to help build workflows while keeping every step visible, inspectable, and version-controlled.

### napflow
**Stack:** Python / YAML | **License:** Open Source (per PyPI)  
napflow is a local-first, git-friendly, node-based flow editor and engine for **API request/response processing** — explicitly positioned as "Postman Flows, but open, file-based, Python-powered, and composable" [citation:4]. A flow is one YAML file + one `nodes.py` in one folder, making diffs small and reviewable. Features include headless `napf run` with assert-driven exit codes for CI, full observability (headers, bodies, timing, retries), and a visual canvas. Flows are composable: any flow is usable as a node inside another flow. Python-native logic testable with pytest. **Status:** v0.2 developer preview; formats experimental before v1.0 [citation:4].  
**Best for:** QA and dev teams testing APIs who want their flows reviewed, diffed, and run in CI like any other code.

### MEL Agent
**Stack:** Go / React / PostgreSQL | **License:** Open Source (per package)  
MEL Agent is an AI-first workflow automation platform with a visual builder inspired by n8n, Make.com, and Node-RED [citation:3]. Built from the ground up for LLM orchestration and AI agent workflows. Features include real-time debugging with step-by-step execution traces, live data preview for every node, AI nodes (LLM chat, embeddings), integration nodes (Slack, Baserow, webhooks, HTTP), logic nodes, and a dual worker model (embedded + distributed). API-first design with everything available via REST API. Docker Compose deployment [citation:3].  
**Best for:** Teams building AI-powered workflows who want a visual builder designed for LLM orchestration rather than retrofitted automation.

---

## 📊 Comparison at a Glance

| Software | License | Type | Visual Canvas | Code Support | Self-Hosted | Best For |
|----------|---------|------|---------------|--------------|-------------|----------|
| **Postman Flows** | Proprietary | API workflow builder | ✅ | Limited | ❌ | Postman ecosystem |
| **Zapier** | Proprietary | No-code automation | ✅ | Limited | ❌ | Broadest app coverage |
| **Make** | Proprietary | Visual automation | ✅ | Limited | ❌ | Granular data shaping |
| **Tray.io** | Proprietary | Enterprise iPaaS | ✅ | JSONata | ❌ | Governed enterprise automation |
| **Workato** | Proprietary | Enterprise automation | ✅ | SDK | ❌ | Citizen integrators |
| **n8n** | Sustainable Use | Source-available automation | ✅ | JS/Python | ✅ | Powerful self-hosted + AI |
| **Activepieces** | MIT | Open-source automation | ✅ | NPM | ✅ | MIT-licensed self-hosted |
| **Node-RED** | Apache 2.0 | Event-driven flows | ✅ | JS | ✅ | IoT + edge automation |
| **Flowise** | Apache 2.0 | AI/LLM workflows | ✅ | Custom code | ✅ | AI agent orchestration |
| **Windmill** | AGPL-3.0 | Code-first platform | ✅ | Python/TS/Go | ✅ | Scripts-to-workflow |
| **Fluxify** | Apache 2.0 (core) | Compiled API workflows | ✅ | JS (compiled) | ✅ | Performance + visual builder |
| **Open Flow** | Open Source | AI-assisted workflows | ✅ | TypeScript | ✅ | Agent-built + inspectable |
| **napflow** | Open Source | API request/response flows | ✅ | Python | ✅ | Git-friendly API testing |
| **MEL Agent** | Open Source | AI-native workflows | ✅ | Go SDK | ✅ | LLM orchestration |

---

## 🤝 Contributing

Contributions are welcome! If you know of an open-source Visual API Workflow or Orchestration Builder that should be listed here, please open a pull request with:

- Project name and URL
- Brief description (1–2 sentences)
- Stack and license
- Why it stands out

Please ensure the project is actively maintained (releases within the last 12 months) and genuinely open-source (or clearly note the license if source-available but not OSI-approved, as with n8n).

---

## 📄 License

This list is released under CC0 1.0 Universal (Public Domain). The software projects listed retain their respective licenses.

---

⭐ **If this list helped you discover a useful tool, please star the repo!** ⭐
