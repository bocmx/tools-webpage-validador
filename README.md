# ✅ Validador Simples com n8n

Este é um exemplo de workflow do [n8n](https://n8n.io) para validar se um **e-mail informado** está presente em uma tabela PostgreSQL (ou Supabase), retornando o status HTTP adequado.

---

## ⚙️ Funcionamento

1. Um webhook do tipo `POST` recebe uma requisição com o campo `email`.
2. O workflow busca esse e-mail na tabela `usuarios` do banco.
3. Se encontrado, retorna `200 OK`.
4. Se **não** encontrado, retorna `404 Not Found`.

---

## 🔧 Requisitos

- Instância do [n8n](https://n8n.io)
- Banco de dados PostgreSQL (pode ser Supabase)
- Tabela `usuarios` com a coluna `email`

---

## 📥 Como usar

1. Importe o arquivo `validador-simples.json` no seu n8n
2. Configure as **credenciais PostgreSQL** no nó `Verificar E-mail1`
3. Atualize o caminho do webhook (`/validador`) se necessário
4. Conecte sua página ou serviço ao endpoint gerado

---

## 🧪 Exemplo de Requisição

```bash
curl -X POST https://SEU-N8N.com/webhook/validador \
  -H 'Content-Type: application/json' \
  -d '{ "email": "teste@exemplo.com" }'
