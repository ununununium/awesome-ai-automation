# n8n Workflow Templates

Exportable n8n workflow JSON files and setup guides.

## How to import

1. Open your n8n instance
2. Go to **Workflows** → **Import from file**
3. Select the `.json` file from this directory
4. Configure credentials as required
5. Activate the workflow

## Templates

| Template | Description | Requires |
|----------|-------------|---------|
| `openai-email-responder.json` | Reads Gmail, drafts AI responses with GPT-4 | Gmail, OpenAI |
| `slack-to-notion.json` | Saves starred Slack messages to a Notion DB | Slack, Notion |
| `rss-to-airtable.json` | Monitors RSS feeds and saves items to Airtable | Airtable |
| `webhook-to-slack.json` | Receives webhooks and posts formatted messages to Slack | Slack |

## Self-Hosted AI Starter Kit

For a complete local AI + n8n setup, use the official starter kit:

```bash
git clone https://github.com/n8n-io/self-hosted-ai-starter-kit
cd self-hosted-ai-starter-kit
docker compose up
```

This includes:
- n8n (workflow automation)
- Ollama (local LLM)
- Qdrant (vector database)
- PostgreSQL

## Useful n8n Resources

- [n8n Docs](https://docs.n8n.io)
- [Workflow Templates](https://n8n.io/workflows)
- [Community Forum](https://community.n8n.io)
- [AI-specific templates](https://n8n.io/workflows/?categories=AI)
- [Community nodes (npm)](https://www.npmjs.com/search?q=n8n-nodes)
