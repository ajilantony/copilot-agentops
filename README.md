# 🤖 Copilot AgentOps

Copilot AgentOps is a comprehensive framework and accelerator suite designed to maximize productivity when using GitHub Copilot. It is based on the GitHub Copilot best practices andcommunity created collection of custom agents, prompts, and instructions to supercharge your GitHub Copilot experience across different domains, languages, and use cases.

This repository provides a comprehensive toolkit for enhancing GitHub Copilot with specialized:

- **[Agents](docs/README.agents.md)** - Specialized GitHub Copilot agents that integrate with MCP servers to provide enhanced capabilities for specific workflows and tools
- **[Prompts](docs/README.prompts.md)** - Focused, task-specific prompts for generating code, documentation, and solving specific problems
- **[Instructions](docs/README.instructions.md)** - Comprehensive coding standards and best practices that apply to specific file patterns or entire projects
- **[Hooks](docs/README.hooks.md)** - Automated workflows triggered by specific events during development, testing, and deployment
- **[Skills](docs/README.skills.md)** - Self-contained folders with instructions and bundled resources that enhance AI capabilities for specialized tasks
- **[Collections](docs/README.collections.md)** - Curated collections of related prompts, instructions, agents, and skills organized around specific themes and workflows
- **[Cookbook Recipes](cookbook/README.md)** - Practical, copy-paste-ready code snippets and real-world examples for working with GitHub Copilot tools and features

## How to Install Customizations

To make it easy to add these customizations to your editor, created an MCP Server that provides a prompt for searching and installing prompts, instructions, agents, and skills directly from this repository. You'll need to have Docker installed and running to run the MCP server locally.

### Step 1: Open your Copilot settings

In VS Code, open the Command Palette (`Cmd+Shift+P` on macOS or `Ctrl+Shift+P` on Windows/Linux) and search for "Copilot: Open User Settings (JSON)".

### Step 2: Locate the MCP servers configuration

Find or create the `"mcpServers"` object in your settings file.

### Step 3: Add the copilot-agentops server

Add the following configuration block inside the `"mcpServers"` object:

```json
{
  "servers": {
      "copilot-agentops": {
   "command": "docker",
   "args": ["run", "-i", "--rm", "ajilantony/copilot-agentops:latest"]
  }  
  }
}
```

</details>

## 📄 llms.txt

An [`llms.txt`](https://github.github.io/copilot-agentops/llms.txt) file following the [llmstxt.org](https://llmstxt.org/) specification is available on the GitHub Pages site. This machine-readable file makes it easy for Large Language Models to discover and understand all available agents, prompts, instructions, and skills, providing a structured overview of the repository's resources with names and descriptions.

## 🔧 How to Use

### 🔌 Plugins

Plugins are installable packages generated from collections. Each plugin contains symlinked agents, commands (prompts), and skills from the source collection, making it easy to install a curated set of resources.

#### Installing Plugins

First, add the Copilot AgentOps marketplace to your Copilot CLI:

```bash
copilot plugin marketplace add github/copilot-agentops
```

Then install any plugin from the collection:

```bash
copilot plugin install <plugin-name>@copilot-agentops
```

Alternatively, you can use the `/plugin` command within a Copilot chat session to browse and install plugins interactively.

### 🤖 Custom Agents

Custom agents can be used in Copilot coding agent (CCA), VS Code, and Copilot CLI (coming soon). For CCA, when assigning an issue to Copilot, select the custom agent from the provided list. In VS Code, you can activate the custom agent in the agents session, alongside built-in agents like Plan and Agent.

### 🎯 Prompts

Use the `/` command in GitHub Copilot Chat to access prompts:

```plaintext
/copilot-agentops create-readme
```

### 📋 Instructions

Instructions automatically apply to files based on their patterns and provide contextual guidance for coding standards, frameworks, and best practices.

### 🪝 Hooks

Hooks enable automated workflows triggered by specific events during GitHub Copilot coding agent sessions (like sessionStart, sessionEnd, userPromptSubmitted). They can automate tasks like logging, auto-committing changes, or integrating with external services.

## 🎯 Why Use Copilot AgentOps?

- **Productivity**: Pre-built agents, prompts and instructions save time and provide consistent results.
- **Best Practices**: Benefit from community-curated coding standards and patterns.
- **Specialized Assistance**: Access expert-level guidance through specialized custom agents.
- **Continuous Learning**: Stay updated with the latest patterns and practices across technologies.

## 📖 Repository Structure

```plaintext
├── prompts/          # Task-specific prompts (.prompt.md)
├── instructions/     # Coding standards and best practices (.instructions.md)
├── agents/           # AI personas and specialized modes (.agent.md)
├── collections/      # Curated collections of related items (.collection.yml)
├── plugins/          # Installable plugins generated from collections
├── scripts/          # Utility scripts for maintenance
└── skills/           # AI capabilities for specialized tasks
```

## 📚 Additional Resources

- [VS Code Copilot Customization Documentation](https://code.visualstudio.com/docs/copilot/copilot-customization) - Official Microsoft documentation
- [GitHub Copilot Chat Documentation](https://code.visualstudio.com/docs/copilot/chat/copilot-chat) - Complete chat feature guide
- [VS Code Settings](https://code.visualstudio.com/docs/getstarted/settings) - General VS Code configuration guide
