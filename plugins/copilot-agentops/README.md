# Copilot AgentOps Plugin

Meta prompts that help you discover and generate curated GitHub Copilot agents, collections, instructions, prompts, and skills.

## Installation

```bash
# Using Copilot CLI
copilot plugin install copilot-agentops@copilot-agentops
```

## What's Included

### Commands (Slash Commands)

| Command | Description |
|---------|-------------|
| `/copilot-agentops:suggest-awesome-github-copilot-collections` | Suggest relevant GitHub Copilot collections from the copilot-agentops repository based on current repository context and chat history, providing automatic download and installation of collection assets, and identifying outdated collection assets that need updates. |
| `/copilot-agentops:suggest-awesome-github-copilot-instructions` | Suggest relevant GitHub Copilot instruction files from the copilot-agentops repository based on current repository context and chat history, avoiding duplicates with existing instructions in this repository, and identifying outdated instructions that need updates. |
| `/copilot-agentops:suggest-awesome-github-copilot-prompts` | Suggest relevant GitHub Copilot prompt files from the copilot-agentops repository based on current repository context and chat history, avoiding duplicates with existing prompts in this repository, and identifying outdated prompts that need updates. |
| `/copilot-agentops:suggest-awesome-github-copilot-agents` | Suggest relevant GitHub Copilot Custom Agents files from the copilot-agentops repository based on current repository context and chat history, avoiding duplicates with existing custom agents in this repository, and identifying outdated agents that need updates. |

### Agents

| Agent | Description |
|-------|-------------|
| `meta-agentic-project-scaffold` | Meta agentic project creation assistant to help users create and manage project workflows effectively. |

## Source

This plugin is part of [Copilot AgentOps](https://github.com/github/copilot-agentops), a community-driven collection of GitHub Copilot extensions.

## License

MIT

