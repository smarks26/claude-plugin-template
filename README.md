# Claude Code Plugin Template

Create and distribute Claude Code plugins for your team or community. This GitHub template provides everything you need to build a plugin — from scaffolding and validation to CI/CD automation.

[![GitHub stars](https://img.shields.io/github/stars/smarks26/claude-plugin-template?style=social)](https://github.com/smarks26/claude-plugin-template/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/smarks26/claude-plugin-template?style=social)](https://github.com/smarks26/claude-plugin-template/network/members)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## Why Use This Template?

- **Skip the boilerplate** — Pre-configured marketplace structure, plugin manifests, and GitHub Actions validation
- **Full plugin development toolkit** — Commands for scaffolding plugins, adding components (commands, skills, agents, hooks), and validating before release
- **Best practices built-in** — Comprehensive documentation, examples, and guided workflows

## What's Included

| Component | Description |
|-----------|-------------|
| **Marketplace Configuration** | `.claude-plugin/marketplace.json` following the [official schema](https://code.claude.com/docs/en/plugin-marketplaces#marketplace-schema) |
| **Plugin Development Toolkit** | `plugin-development` plugin with 7 slash commands, a `plugin-authoring` skill for ambient guidance, and a reviewer agent |
| **Example Plugin** | `hello-world` plugin demonstrating proper structure and best practices |
| **CI/CD Workflows** | GitHub Actions for automated plugin validation on every push and PR |
| **Documentation** | Complete guides for plugins, hooks, settings, commands, skills, and sub-agents |

## Quick Start

### 1. Create Your Marketplace

Click **"Use this template"** on GitHub, then clone your new repository:

```bash
git clone [https://github.com/your-org/your-marketplace-name.git](https://github.com/your-org/your-marketplace-name.git)
cd your-marketplace-name
```

### 2. Customize the Marketplace

Update `.claude-plugin/marketplace.json` with your organization details:

```json
{
  "name": "my-team-marketplace",
  "owner": {
    "name": "Your Organization",
    "email": "team@your-org.com"
  },
  "metadata": {
    "description": "A curated collection of Claude Code plugins for our team",
    "version": "1.0.0"
  },
  "plugins": []
}
```

### 3. Install the Plugin Development Toolkit

```bash
# Start Claude Code
claude

# Add your local marketplace
/plugin marketplace add .

# Install the development toolkit
/plugin install plugin-development@my-team-marketplace

```

### 4. Create Your First Plugin

1. **Plan your plugin structure:**
* Ask: "What's the best directory structure for a plugin with commands and MCP integration?"
* The plugin-structure skill will guide you


2. **Add MCP integration (if needed):**
* Ask: "How do I add an MCP server for database access?"
* The mcp-integration skill provides examples and patterns


3. **Implement hooks (if needed):**
* Ask: "Create a PreToolUse hook that validates file writes"
* The hook-development skill gives working examples and utilities



## Development Workflow

The plugin-development toolkit supports your entire plugin development lifecycle:

```
┌─────────────────────┐
│  Design Structure   │ ──> plugin-structure skill
│  (manifest, layout) │
└──────────┬──────────┘
           │
┌──────────▼──────────┐
│    Add Components   │ ──> All skills provide guidance
│ (commands, agents,  │
│    skills, hooks)   │
└──────────┬──────────┘
           │
┌──────────▼──────────┐
│ Integrate Services  │ ──> mcp-integration skill
│    (MCP servers)    │
└──────────┬──────────┘
           │
┌──────────▼──────────┐
│   Add Automation    │ ──> hook-development skill
│ (hooks, validation) │     + utility scripts
└──────────┬──────────┘
           │
┌──────────▼──────────┐
│   Test & Validate   │ ──> hook-development utilities:
│                     │     - validate-hook-schema.sh
└─────────────────────┘     - test-hook.sh
                            - hook-linter.sh
```

## Documentation Standards

All skills follow consistent standards:

* Third-person descriptions ("This skill should be used when...")
* Strong trigger phrases for reliable loading
* Imperative/infinitive form throughout
* Based on official Claude Code documentation
* Security-first approach with best practices

## Use Cases

### Building a Database Plugin

```
1. "What's the structure for a plugin with MCP integration?"
   → plugin-structure skill provides layout

2. "How do I configure an stdio MCP server for PostgreSQL?"
   → mcp-integration skill shows configuration

3. "Add a Stop hook to ensure connections close properly"
   → hook-development skill provides pattern
```

### Creating a Validation Plugin

```
1. "Create hooks that validate all file writes for security"
   → hook-development skill with examples

2. "Test my hooks before deploying"
   → Use validate-hook-schema.sh and test-hook.sh

3. "Organize my hooks and configuration files"
   → plugin-structure skill shows best practices
```

### Integrating External Services

```
1. "Add Asana MCP server with OAuth"
   → mcp-integration skill covers SSE servers

2. "Use Asana tools in my commands"
   → mcp-integration tool-usage reference

3. "Structure my plugin with commands and MCP"
   → plugin-structure skill provides patterns
```

## Best Practices

### ✅ Security First

* Input validation in hooks
* HTTPS/WSS for MCP servers
* Environment variables for credentials
* Principle of least privilege

### ✅ Portability

* Use `${CLAUDE_PLUGIN_ROOT}` everywhere
* Relative paths only
* Environment variable substitution

### ✅ Testing

* Validate configurations before deployment
* Test hooks with sample inputs
* Use debug mode (`claude --debug`)

### ✅ Documentation

* Clear README files
* Documented environment variables
* Usage examples

## Official Claude Code Documentation

* [Plugins Overview](https://code.claude.com/docs/en/plugins) — Plugin development guide
* [Plugin Marketplaces](https://code.claude.com/docs/en/plugin-marketplaces) — Marketplace management
* [Plugins Reference](https://code.claude.com/docs/en/plugins-reference) — Technical specifications
* [Slash Commands](https://code.claude.com/docs/en/slash-commands) — Command development

## Acknowledgments

Built for [Claude Code](https://claude.com/claude-code) by [Anthropic](https://www.anthropic.com/).

## License

MIT License — see [LICENSE](/LICENSE) for details.

## Resources

* [Claude Code Documentation](https://code.claude.com/docs)
* [Anthropic Discord](https://discord.com/invite/anthropic) — Community support
* [Claude Code GitHub](https://github.com/anthropics/claude-code) — Official repository

```

```
