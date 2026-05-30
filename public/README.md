# Mini Ecommerce com JSON Server

Nome: Victhor Gabriel Freire de Oliveira  
Matrícula: 918963

## Resumo do projeto

Este projeto é um mini ecommerce de produtos de tecnologia. A Home exibe cards de produtos consumidos de uma API fake criada com JSON Server. Cada produto possui uma página de detalhes acessada por QueryString.

## Estrutura do db.json

O arquivo `db.json` possui as seguintes coleções:

- `produtos`: guarda os produtos exibidos nos cards da Home.
- `categorias`: guarda as categorias disponíveis para organização dos produtos.
- `avaliacoes`: guarda avaliações relacionadas aos produtos.

## Modelo de produto

```json
{
  "id": 1,
  "nome": "Notebook Dell Inspiron",
  "descricaoCurta": "Notebook para estudos e trabalho.",
  "descricaoCompleta": "Notebook Dell Inspiron com ótimo desempenho para tarefas do dia a dia.",
  "imagem": "https://picsum.photos/400/250?random=1",
  "categoria": "Notebooks",
  "preco": 3500,
  "tags": ["notebook", "trabalho", "estudos"],
  "destaque": true,
  "emEstoque": true
}
```

## Como executar

Instale o JSON Server:

```bash
npm install -g json-server
```

Execute o servidor:

```bash
json-server --watch db.json --port 3000
```

Depois abra o arquivo `index.html` no navegador.

## Rotas principais

- `http://localhost:3000/produtos`
- `http://localhost:3000/produtos/1`
- `http://localhost:3000/categorias`
- `http://localhost:3000/avaliacoes`

## Funcionalidades

- Buscar produtos no JSON Server com Fetch API.
- Renderizar cards dinamicamente na Home.
- Filtrar produtos por nome e categoria.
- Acessar página de detalhes usando `details.html?id=ID`.
- Ler o ID com `URLSearchParams`.
- Cadastrar novos produtos usando requisição POST.
