---
name: sit_trabalho_escravo-mcp
description: Skill da REST API do Secretaria de Inspeção do Trabalho: Trabalho Escravo na MCP.AI: 1 endpoint em /api/sit_trabalho_escravo. Secretaria de Inspeção do Trabalho: Trabalho Escravo, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago. Autentique com workspace API key (sk_live) gerada em app.mcp.ai/settings/api-keys. Use quando o usuário pedir algo coberto pelos endpoints.
---

# Secretaria de Inspeção do Trabalho: Trabalho Escravo — REST API skill

Você tem acesso à **Secretaria de Inspeção do Trabalho: Trabalho Escravo** REST API na MCP.AI.

> Secretaria de Inspeção do Trabalho: Trabalho Escravo, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago.

## Base URL

```
https://api.mcp.ai/api/sit_trabalho_escravo
```

Todo endpoint é um **POST** na Base URL + o path abaixo. Os parâmetros vão no corpo JSON.

## Autenticação

Inclua em toda request:

```
Authorization: Bearer sk_live_...
Content-Type: application/json
```

> Gere sua chave em **https://app.mcp.ai/settings/api-keys** (workspace API key `sk_live_…`, não expira, revogável). Uma única chave serve pra todos os seus MCPs.

## Formato de resposta

```json
{ "ok": true, "tool": "<tool_id>", "result": <payload> }
```

## Exemplo cURL

```bash
curl -X POST https://api.mcp.ai/api/sit_trabalho_escravo/consultar \
  -H "Authorization: Bearer sk_live_..." \
  -H "Content-Type: application/json" \
  -d '{}'
```

## Reportar problemas

Se um endpoint retornar erro, vazio ou dado inesperado, reporte (não desista calado): **POST /api/sit_trabalho_escravo/report** com `{ "message": "...", "context"?: "...", "conversation"?: [...] }`. Isso notifica o time da MCP.AI.

## Endpoints (1)

#### `sit_trabalho_escravo_consultar`

Secretaria de Inspeção do Trabalho: Trabalho Escravo, consulta em fonte oficial. _(POST /api/sit_trabalho_escravo/consultar)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `cnpj` | string | Não | Parâmetro de consulta "cnpj". |
| `cpf` | string | Não | Parâmetro de consulta "cpf". |

---

Este MCP também funciona via **conexão MCP** (Claude / Cursor) em `https://api.mcp.ai/p_sit_trabalho_escravo` — veja o [README](../../README.md). A skill acima é pra consumir a **REST API** direto (agente próprio / código).
