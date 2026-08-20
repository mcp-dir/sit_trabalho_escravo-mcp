# Instalação detalhada

Secretaria de Inspeção do Trabalho: Trabalho Escravo é um servidor MCP remoto. Aponte seu cliente pra `https://api.mcp.ai/p_sit_trabalho_escravo`. Snippets rápidos: [INSTALL.md](../INSTALL.md).

| Cliente | URL | Auth |
|---|---|---|
| Claude Desktop | `https://api.mcp.ai/p_sit_trabalho_escravo` | OAuth 2.1 ou agent-auth |
| Cursor | `https://api.mcp.ai/p_sit_trabalho_escravo` | OAuth 2.1 ou agent-auth |
| VS Code (Copilot) | `https://api.mcp.ai/p_sit_trabalho_escravo` | OAuth 2.1 ou agent-auth |

A config JSON é a mesma em todos: só a URL, sem headers.

## Desinstalar

Remova o bloco `mcpServers.sit_trabalho_escravo` (ou `servers.sit_trabalho_escravo` no VS Code) do config do cliente e reinicie.
