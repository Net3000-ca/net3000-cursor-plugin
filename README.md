# Net3000 for Cursor

Connect Cursor to your [Net3000](https://www.net3000.ca) account. Your agent can read and, when you allow it, update the same websites, bookings, stores, courses, job boards and mailing lists you manage in Net3000 admin.

## Connect

1. Install the **Net3000** plugin from the Cursor marketplace, or add the server from [`mcp.json`](mcp.json) to your Cursor MCP settings.
2. Open a chat that uses the `net3000` server. Cursor opens your browser so you can sign in with your Net3000 admin login.
3. Choose the account, whether the agent may only read or may also make changes, and whether it may download bulk exports.
4. Ask the agent "who am I connected as?" to confirm the connection.

Server URL: `https://account-agents.net3000.ca/mcp`

One-click install: [Add to Cursor](cursor://anysphere.cursor-deeplink/mcp/install?name=net3000&config=eyJ1cmwiOiJodHRwczovL2FjY291bnQtYWdlbnRzLm5ldDMwMDAuY2EvbWNwIn0=)

## What the agent can do

The agent never does more than your own login. It sees only the applications your accounts use and only the screens your team permissions open in admin. Read-only is the default. Every change is recorded, and an administrator can require approval before changes run or pause every agent on an account at once.

## Personal tokens

If your Cursor build cannot complete the browser sign-in, create a personal token in Net3000 admin under **Settings → Connect Your Website → MCP tools**, then use:

```json
{
  "mcpServers": {
    "net3000": {
      "type": "http",
      "url": "https://account-agents.net3000.ca/mcp",
      "headers": { "Authorization": "Bearer YOUR_TOKEN" }
    }
  }
}
```

Never put a token in a prompt, a commit or a shared file.

## More

- Help: [Connect your AI agent to your Net3000 account](https://www.net3000.ca/docs)
- Privacy and terms: [AI Connector: Privacy and Terms](https://www.net3000.ca/ai-connector)
- Support: support@net3000.ca
