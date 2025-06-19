API Produtos
StartFragment

<p >API RESTful para gerenciar produtos de uma loja com MongoDB.</p> 

📌 POST /produto – Cadastrar produto
Descrição:

Cadastra um novo produto no banco de dados.

Body (JSON):

Plain Text
jsonCopiarEditar{
  "nome": "Notebook Gamer",
  "descricao": "RTX 3060, i7, 16GB RAM",
  "cor": "Preto",
  "peso": 2.3,
  "tipo": "Eletrônico",
  "preco": 7999.90
}
Resposta esperada (201):

Plain Text
jsonCopiarEditar{
  "_id": "...",
  "nome": "...",
  "descricao": "...",
  ...
}
📌 GET /produto – Listar todos os produtos
Descrição:

Retorna todos os produtos cadastrados.

Resposta esperada (200):

View More
Plain Text
jsonCopiarEditar[
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

Plain Text
bashCopiarEditarGET /produto/Notebook Gamer
GET /produto/665e3f9a23b9dbfa2d8d6d55
Resposta esperada:

Plain Text
jsonCopiarEditar{
  "_id": "...",
  "nome": "Notebook Gamer",
  ...
}
📌 PUT /produto/:id – Atualizar produto
Descrição:

Atualiza os dados de um produto existente.

Exemplo de URL:

Plain Text
bashCopiarEditarPUT /produto/665e3f9a23b9dbfa2d8d6d55
Body (JSON):

Plain Text
jsonCopiarEditar{
  "preco": 7499.90,
  "cor": "Cinza"
}
Resposta esperada:

Plain Text
jsonCopiarEditar{
  "_id": "...",
  "nome": "...",
  ...
}
📌 DELETE /produto/:id – Deletar produto
Descrição:

Remove um produto do banco de dados.

Exemplo de URL:

Plain Text
bashCopiarEditarDELETE /produto/665e3f9a23b9dbfa2d8d6d55
Resposta esperada:

Plain Text
jsonCopiarEditar{
  "message": "Produto deletado com sucesso."
}
EndFragment
