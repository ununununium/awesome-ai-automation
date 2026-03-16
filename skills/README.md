# Skills & Agent Extensions

This directory contains reusable skill templates, CLAUDE.md examples, and agent config patterns for OpenClaw, Claude Code, and other AI platforms.

## Structure

```
skills/
├── openclaw/          # OpenClaw SKILL.md templates
├── claude-code/       # CLAUDE.md and MCP config templates
├── n8n/               # n8n workflow JSON exports
└── prompts/           # Reusable system prompt templates
```

## OpenClaw Skills

See the [ClawHub marketplace](https://clawhub.com) for installable skills.

Template structure for a new OpenClaw skill:

```
my-skill/
├── SKILL.md           # Required — skill instructions for the agent
├── references/        # Optional — reference docs, API schemas
└── scripts/           # Optional — helper scripts
```

### SKILL.md Minimal Template

```markdown
# My Skill

## When to use this skill
Describe when the agent should load and apply this skill.

## Setup
Any one-time setup steps (auth, install, config).

## Usage
How to invoke the skill. Key commands and patterns.

## Examples
Concrete examples of inputs and expected outputs.
```

## Claude Code

### CLAUDE.md Template

Place `CLAUDE.md` in your project root. Claude Code reads it automatically.

```markdown
# Project Context

## What this is
Brief description of the project.

## Architecture
Key files, entry points, and how they connect.

## Commands
- `npm run dev` — start dev server
- `npm run build` — production build
- `npm test` — run tests

## Conventions
- TypeScript strict mode
- Functional components only
- Co-locate tests with source files

## Do not
- Modify X without checking Y first
- Deploy without running tests
```

### MCP Config Template (`.mcp.json`)

```json
{
  "mcpServers": {
    "github": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-github"],
      "env": {
        "GITHUB_PERSONAL_ACCESS_TOKEN": "<your-token>"
      }
    },
    "supabase": {
      "command": "npx",
      "args": ["-y", "@supabase/mcp-server-supabase@latest"],
      "env": {
        "SUPABASE_ACCESS_TOKEN": "<your-token>"
      }
    }
  }
}
```

## n8n Workflows

See `n8n/` subdirectory for exportable workflow JSON files.

## Contributing

Add your skill template, CLAUDE.md pattern, or n8n workflow to the relevant subfolder and open a PR.
