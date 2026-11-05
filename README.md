# HANRIA agent mandate check

Before an AI agent acts, ask whether the action fits what its operator wrote down. The hosted check answers permit, deny or escalate, and names the clause that decided it. You can log the answer or show it to your operator.

The check is free, needs no account or API key, and is advisory. It cannot stop an action. It keeps no request content.

## Use it

Remote MCP server (streamable HTTP, no auth): `https://check.hanria.ai/v1/mcp`

Tools:
- `check_action`: check one proposed action against a mandate.
- `validate_mandate`: check that a written mandate is well formed.

Other doors:
- HTTP: `https://check.hanria.ai/v1/check` (OpenAPI 3.1 in [openapi.json](openapi.json))
- A2A agent card: [agent-card.json](agent-card.json), also at https://hanria.ai/.well-known/agent-card.json
- Docs for agents: [llms.txt](llms.txt)
- Official MCP Registry name: `ai.hanria/agent-mandate-check` ([server.json](server.json))
- Privacy: https://check.hanria.ai/privacy

Five mandate templates are served as MCP resources: payments ceiling, file sandbox, outbound email, deploy gate, read-only research.

## What this is not

- Not a guard. A permit does not make an action safe, and a deny does not block it. Your agent or its harness has to honor the answer.
- Not the HANRIA review or payment system. That system is not released and has not been independently audited.
- Not a source of mandates. You write the mandate; the check evaluates against it.

## This repository

Public copies of the files that describe the hosted service. The service itself is hosted at check.hanria.ai. The files here mirror what is already published at hanria.ai and check.hanria.ai; if they differ, the hosted versions govern.

Maintained by HANRIA. Site: https://hanria.ai
