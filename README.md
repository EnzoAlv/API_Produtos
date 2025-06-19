# 🛍️ API Produtos

API RESTful para gerenciar produtos de uma loja com MongoDB.

---

## 📌 POST `/produto` – Cadastrar produto

**Descrição:**  
Cadastra um novo produto no banco de dados.

**Body (JSON):**
```json
{
  "nome": "Notebook Gamer",
  "descricao": "RTX 3060, i7, 16GB RAM",
  "cor": "Preto",
  "peso": 2.3,
  "tipo": "Eletrônico",
  "preco": 7999.90
}
Resposta esperada (201):

json
Copiar
Editar
{
  "_id": "...",
  "nome": "...",
  "descricao": "...",
  ...
}
📌 GET /produto – Listar todos os produtos
Descrição:
Retorna todos os produtos cadastrados.

Resposta esperada (200):

json
Copiar
Editar
[
  {
    "_id": "...",
    "nome": "Notebook Gamer",
    ...
  },
  {
    "_id": "...",
    "nome": "Smartphone",
    ...
  }
]
📌 GET /produto/:valor – Buscar por ID ou Nome
Descrição:
Busca um produto pelo ID ou nome exato.

Exemplo de URL:

bash
Copiar
Editar
GET /produto/Notebook Gamer
GET /produto/665e3f9a23b9dbfa2d8d6d55
Resposta esperada:

json
Copiar
Editar
{
  "_id": "...",
  "nome": "Notebook Gamer",
  ...
}
📌 PUT /produto/:id – Atualizar produto
Descrição:
Atualiza os dados de um produto existente.

Exemplo de URL:

bash
Copiar
Editar
PUT /produto/665e3f9a23b9dbfa2d8d6d55
Body (JSON):

json
Copiar
Editar
{
  "preco": 7499.90,
  "cor": "Cinza"
}
Resposta esperada:

json
Copiar
Editar
{
  "_id": "...",
  "nome": "...",
  ...
}
📌 DELETE /produto/:id – Deletar produto
Descrição:
Remove um produto do banco de dados.

Exemplo de URL:

bash
Copiar
Editar
DELETE /produto/665e3f9a23b9dbfa2d8d6d55
Resposta esperada:

json
Copiar
Editar
{
  "message": "Produto deletado com sucesso."
}
