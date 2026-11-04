# a2a-cli

An [Agent Plugin](https://agent-plugins.org/) that teaches an AI agent to drive the [`a2a` CLI](https://github.com/a2aproject/a2a-cli): fetch an agent's card, send it a message, stream or poll a task, and list, resume, or cancel tasks on any A2A (Agent2Agent) agent.

> [!NOTE]
> This plugin is generated from [a2aproject/a2a-cli](https://github.com/a2aproject/a2a-cli/tree/main/agent-plugin) on every a2a-cli release. Send changes there.

## Requires the `a2a` binary

The plugin carries the agent-facing skill only. Install `a2a` separately:

- **Homebrew (macOS / Linux):** `brew tap a2aproject/a2a-cli https://github.com/a2aproject/a2a-cli && brew install a2a`
- **WinGet (Windows):** `winget install a2aproject.a2acli`
- **Prebuilt binary:** download from the [latest release](https://github.com/a2aproject/a2a-cli/releases/latest) and put `a2a` on your `PATH`.

Check it with `a2a version`. The skill runs the same preflight check.

## Install

**Claude Code**

```bash
/plugin marketplace add a2aproject/agent-plugins
/plugin install a2a-cli@a2a-plugins
```

**Any Agent Plugins client:** load the `plugins/a2a-cli` directory of [a2aproject/agent-plugins](https://github.com/a2aproject/agent-plugins).

**Skill only**, with the [`skills`](https://www.skills.sh) CLI:

```bash
npx skills add https://github.com/a2aproject/agent-plugins/tree/main/plugins/a2a-cli/skills/a2a-cli -g
```

## Contents

```text
a2a-cli/
├── plugin.json          # Agent Plugins 1.0.0 manifest
├── LICENSE
└── skills/
    └── a2a-cli/
        └── SKILL.md
```

## Usage

Ask your agent for A2A work and it loads the skill on its own, for example:

> Fetch the agent card at `http://localhost:8080` and send it "summarize this repo".

## Versioning

The plugin `version` matches the a2a-cli release it was built from. The bundled skill keeps its own date-based `metadata.version`.
