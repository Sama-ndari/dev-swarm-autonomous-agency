# DevSwarm: The Self-Evolving AI Software Agency

**DevSwarm** is an autonomous, event-driven multi-agent system that doesn't just write code—it **architects its own workforce**. Unlike static AI agents, DevSwarm performs a "Discovery Phase" to research modern best practices and dynamically hires specialized agents and creates custom tasks at runtime to build complex, multi-module software systems.

## 🧠 The "God Mode" Logic

DevSwarm operates on a recursive intelligence loop:

1. **Reconnaissance:** The Architect researches the user requirement via Google/Serper.
2. **Self-Assembly:** The system identifies gaps in its own "team" and dynamically instantiates new Agents (e.g., "Stripe Expert") and Tasks.
3. **Sandboxed Execution:** Code is written and then verified in a safe execution environment.
4. **Self-Healing:** If the QA agent detects a crash, the error log is fed back for an automatic refactor.

## 🚀 Key Features

* **Dynamic Workforce Injection:** Programmatically "hires" specialized agents based on project complexity.
* **Hierarchical Supervision:** Uses a **Manager LLM** (GPT-4o) to oversee **Worker LLMs** (GPT-4o-mini).
* **Structured Output (Pydantic):** All architectural blueprints are enforced via strict data models.
* **Automated Testing:** Includes a `CodeExecutionTool` to verify generated scripts before finalization.
* **Cost Guardrails:** Hard-coded logic limits the number of dynamic agents to prevent token-drain loops.

---

## 🛠️ Installation

### 1. Prerequisites

* **Python 3.11+**
* **OpenAI API Key**
* **Serper API Key** (for web research)

### 2. Setup

```bash
# Clone the repository
git clone https://github.com/Sama-ndari/dev-swarm-autonomous-agency.git
cd dev-swarm-autonomous-agency

# Install dependencies using uv
uv sync

```

### 3. Environment Configuration (`.env`)

Create a `.env` file in the root directory:

```ini
# Primary model for coding and documentation
MODEL=gpt-4o-mini
# High-reasoning model for management and architecture
MANAGER_MODEL=gpt-4o

OPENAI_API_KEY=sk-proj-xxxx
SERPER_API_KEY=xxxx

```

---

## 📂 Project Structure

```text
dev_swarm/
├── src/
│   └── dev_swarm/
│       ├── tools/            # Custom logic: File Writers & QA Runners
│       ├── config/           # Agent & Task YAML templates
│       ├── crew.py           # The "Engine" (Agent Factory)
│       └── main.py           # The "Orchestrator" (Dynamic Loop)
├── project_output/           # THE FINAL PRODUCT: 
│   └── src/                  # Generated Source Code
│   └── README.md             # Generated Documentation

```

## 🎮 Usage

Run the swarm with a single command:

```bash
uv run crewai run

```

The agents will begin the discovery phase, create a `blueprint.json`, hire specialized agents, and build your project inside the `project_output` folder.

---

## 🛡️ Security & Guardrails

* **Safe Execution:** Code is executed in a subprocess/sandbox environment to protect the host machine.
* **Resource Limits:** The orchestrator enforces `MAX_AGENTS` and `MAX_TASKS` limits.
* **Security Audit:** A dedicated Sentinel agent scans for OWASP vulnerabilities in the generated output.

---

*Created by Samandari - Advancing the frontier of Agentic Workflows.*

---
