# A2A Agent Plugins

[![License](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](LICENSE)
[![Agent Plugins](https://img.shields.io/badge/Agent%20Plugins-1.0.0-blue.svg)](https://agent-plugins.org/specification)

<!-- markdownlint-disable no-inline-html -->

<div align="center">
   <img src="https://raw.githubusercontent.com/a2aproject/A2A/refs/heads/main/docs/assets/a2a-logo-black.svg" width="256" alt="A2A Logo"/>
   <h3>
      Teach your AI agent to work with <a href="https://a2a-protocol.org">Agent2Agent (A2A) Protocol</a> agents.
   </h3>
</div>

<!-- markdownlint-enable no-inline-html -->

---

**A2A Agent Plugins** are the official plugins for [A2A (Agent2Agent) agents](https://a2a-protocol.org/latest/), maintained by the **A2A Project Team**.

Each plugin is a portable [Agent Plugins](https://agent-plugins.org/) package, and this repository doubles as a plugin marketplace.

## Plugins

| Plugin | Description |
| --- | --- |
| **[a2a-cli](./plugins/a2a-cli)** | Drive A2A agents from the command line with the `a2a` CLI: fetch an agent card, send a message, stream or poll a task, and list, resume, or cancel tasks. Requires the [`a2a` binary](https://github.com/a2aproject/a2a-cli#installation). |

## Installation

Claude Code, GitHub Copilot CLI, Codex, and OpenClaw install the full plugin from this marketplace. Hermes Agent, Gemini CLI, OpenCode, and other agents install the skills it contains.

The examples below install `a2a-cli`. Substitute another plugin name from the [Plugins](#plugins) table.

### Claude Code

```bash
/plugin marketplace add a2aproject/agent-plugins
/plugin install a2a-cli@a2a-plugins
```

Turn on auto-update for `a2a-plugins` in the **Marketplaces** tab of `/plugin`, or update by hand with `claude plugin update a2a-cli@a2a-plugins`. See [Discover and install plugins](https://code.claude.com/docs/en/discover-plugins).

### GitHub Copilot CLI

```bash
copilot plugin marketplace add a2aproject/agent-plugins
copilot plugin install a2a-cli@a2a-plugins
```

The same commands work as `/plugin` slash commands inside a session. See the [Copilot CLI plugin reference](https://docs.github.com/en/copilot/reference/cli-plugin-reference).

### Codex

Add the marketplace, then install from the plugin browser:

```bash
codex plugin marketplace add a2aproject/agent-plugins
codex
/plugins
```

Pick the **A2A Agent Plugins** tab and install `a2a-cli`. The ChatGPT desktop app shows the same marketplace under **Plugins**. See [Codex plugins](https://developers.openai.com/codex/plugins).

### OpenClaw

OpenClaw installs Agent Plugins packages as bundles and reads Claude-compatible marketplaces:

```bash
openclaw plugins install a2a-cli --marketplace a2aproject/agent-plugins
openclaw plugins inspect a2a-cli
```

OpenClaw asks you to confirm the source on first install. Pass `--force` in non-interactive setups. See [Plugin bundles](https://docs.openclaw.ai/plugins/bundles).

### Hermes Agent

Hermes plugins are Python packages, so install the skill straight from GitHub:

```bash
hermes skills install a2aproject/agent-plugins/plugins/a2a-cli/skills/a2a-cli
```

Inside a session, use `/skills install` with the same identifier. Hermes scans the skill before installing it. See [Skills System](https://hermes-agent.nousresearch.com/docs/user-guide/features/skills).

### Gemini CLI

```bash
gemini skills install https://github.com/a2aproject/agent-plugins.git --path plugins/a2a-cli/skills/a2a-cli
```

Add `--scope workspace` to install for the current project only, and run `/skills reload` in an open session. See [Agent Skills](https://geminicli.com/docs/cli/skills/).

### OpenCode and other agents

OpenCode has no plugin marketplace, but it loads skills from `~/.config/opencode/skills/`, `~/.claude/skills/`, and `~/.agents/skills/`. The [`skills`](https://www.skills.sh) CLI installs into those directories for OpenCode and most other agents, including Cursor and Antigravity:

```bash
npx skills add https://github.com/a2aproject/agent-plugins/tree/main/plugins/a2a-cli/skills/a2a-cli -g
```

To install by hand, copy `plugins/a2a-cli/skills/a2a-cli/` into your agent's skills directory.

## How to Provide Feedback

Each plugin is developed in its own A2A repository, linked from the plugin's README. Open an issue or pull request there to share suggestions, questions, or bugs.

## License

A2A Agent Plugins are open-source and licensed under the [**Apache License 2.0**](LICENSE).
