# Banco de Dados Vetorizado para IA (PostgreSQL + pgvector)

## Autor

**Athos Lial**  
**Matrícula: 2320071**

## Objetivo

Este repositório disponibiliza uma infraestrutura Plug & Play utilizando PostgreSQL com a extensão pgvector para armazenamento de embeddings e implementação de buscas semânticas em aplicações de Inteligência Artificial e RAG (Retrieval-Augmented Generation).

## Tecnologias Utilizadas

- Docker
- Docker Compose
- PostgreSQL 16
- pgvector

## Como subir a infraestrutura

```bash
docker-compose up -d
```

## Verificar se a extensão foi instalada

```bash
docker exec ia-vector-db psql -U admin -d vector_db -c "\dx"
```

## Derrubar a infraestrutura

```bash
docker-compose down -v
```

## Credenciais padrão

- Usuário: admin
- Senha: senha123
- Banco: vector_db
- Porta: 5432

## Estrutura do Projeto

- docker-compose.yml
- init.sql
- README.md

## Observações

Caso a porta 5432 esteja ocupada, altere para:

```yaml
ports:
  - "5433:5432"
```

Caso o init.sql não execute:

```bash
docker-compose down -v
docker-compose up -d
```

---

Atividade desenvolvida para a APS 16 – Arquitetura em Nuvem e Sistemas Cloud Native.
