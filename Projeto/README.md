# Projeto Python com PostgreSQL (AWS RDS)

Este projeto é um exemplo básico de como conectar uma aplicação Python a um banco de dados PostgreSQL hospedado na AWS RDS utilizando a biblioteca psycopg2.

---

## 📌 Pré-requisitos

Antes de rodar o projeto, você precisa ter:

- Python 3.8+
- psycopg2 instalado
- Uma instância do PostgreSQL no AWS RDS (ou localmente)
- Permissões de acesso ao banco (IP liberado no grupo de segurança)

---

## 🔌 Conexão com o Banco de Dados

A conexão com o PostgreSQL é feita utilizando a biblioteca psycopg2.

📄 Arquivo: db_connect.py

```python
import psycopg2

# Conectando ao banco de dados PostgreSQL hospedado na AWS
conn = psycopg2.connect(
    host="seu-endpoint-rds.amazonaws.com",  # Endereço do RDS
    port=5432,                              # Porta padrão do PostgreSQL
    database="nome_do_banco",              # Nome do seu banco
    user="seu_usuario",                    # Usuário do PostgreSQL
    password="sua_senha"                   # Senha do PostgreSQL
)

print("Conexão estabelecida com sucesso!")
