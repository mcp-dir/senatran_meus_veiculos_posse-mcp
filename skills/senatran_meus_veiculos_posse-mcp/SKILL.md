---
name: senatran_meus_veiculos_posse-mcp
description: Skill da REST API do SENATRAN: Meus Veículos - Possuidor (Listagem) na MCP.AI: 1 endpoint em /api/senatran_meus_veiculos_posse. SENATRAN: Meus Veículos - Possuidor (Listagem), consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago. Autentique com workspace API key (sk_live) gerada em app.mcp.ai/settings/api-keys. Use quando o usuário pedir algo coberto pelos endpoints.
---

# SENATRAN: Meus Veículos - Possuidor (Listagem) — REST API skill

Você tem acesso à **SENATRAN: Meus Veículos - Possuidor (Listagem)** REST API na MCP.AI.

> SENATRAN: Meus Veículos - Possuidor (Listagem), consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago.

## Base URL

```
https://api.mcp.ai/api/senatran_meus_veiculos_posse
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
curl -X POST https://api.mcp.ai/api/senatran_meus_veiculos_posse/consultar \
  -H "Authorization: Bearer sk_live_..." \
  -H "Content-Type: application/json" \
  -d '{}'
```

## Reportar problemas

Se um endpoint retornar erro, vazio ou dado inesperado, reporte (não desista calado): **POST /api/senatran_meus_veiculos_posse/report** com `{ "message": "...", "context"?: "...", "conversation"?: [...] }`. Isso notifica o time da MCP.AI.

## Endpoints (1)

#### `senatran_meus_veiculos_posse_consultar`

SENATRAN: Meus Veículos - Possuidor (Listagem), consulta em fonte oficial. _(POST /api/senatran_meus_veiculos_posse/consultar)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `cnpj` | string | Não | Parâmetro de consulta "cnpj". |
| `pagina` | string | Não | Parâmetro de consulta "pagina". |
| `login_cpf` | string | Não | Parâmetro de consulta "login_cpf". |
| `login_senha` | string | Não | Parâmetro de consulta "login_senha". |
| `pkcs12_cert` | string | Não | Parâmetro de consulta "pkcs12_cert". |
| `pkcs12_pass` | string | Não | Parâmetro de consulta "pkcs12_pass". |

---

Este MCP também funciona via **conexão MCP** (Claude / Cursor) em `https://api.mcp.ai/p_senatran_meus_veiculos_posse` — veja o [README](../../README.md). A skill acima é pra consumir a **REST API** direto (agente próprio / código).
