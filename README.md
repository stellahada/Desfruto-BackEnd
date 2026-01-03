# 🍇 Web Site Desfruto - backend
O AçaíBackEnd é o servidor e sistema de API responsável por gerenciar os dados do sistema de pedidos de açaí. Ele lida com as operações no banco de dados, autenticação e funcionalidades relacionadas ao gerenciamento de pedidos.

🍓FrontEnd: https://github.com/stellahada/acaiFrontEnd
## 📦 Tecnologias Utilizadas
Node.js: Ambiente de execução para JavaScript no servidor.

Express.js: Framework para construção de APIs.

MySQL: Banco de dados relacional para armazenar informações.

Sequelize: ORM para interação com o banco de dados.
## 🖥️ Funcionalidades

Gerenciamento de cardápio (CRUD).

Registro e autenticação de usuários.

Processamento de pedidos e controle de status.
## 🚀 Como Executar o Projeto
1. Acesse o projeto: 
``` bash
git clone https://github.com/stellahada/acaiBackEnd.git
cd acaiBackEnd
npm install

```
2. Database Schema
```sql
CREATE TABLE pedido (
  id_pedido int primary key auto_increment,
  ds_estado varchar(400)
);

Create table itens (
  id_item int primary key auto_increment,
  id_pedido int,
  ds_url varchar(200),
  dp_preco float,
  ds_nome varchar(100),
  ds_tamanho varchar (100),
  ds_acompanhamentos varchar(200),
  FOREIGN KEY (id_pedido) REFERENCES pedido(id_pedido) 
);

create table login(
  id_login int primary key auto_increment, 
  ds_email varchar(200),
  ds_senha varchar(200)
);

insert into pedido(ds_estado) values('Em Preparo');
```

## Contribuidores 🧑‍💻👩‍💻🧑‍💻
| [<img src="https://avatars.githubusercontent.com/u/95144250?s=400&u=149cf20f52f4c096721d16967b22655f18e5c7f5&v=4" width=115><br><sub>Samuel Victor</sub>](https://github.com/Samuel-045) | [<img src="https://avatars.githubusercontent.com/u/138524660?v=4" width=115><br><sub>Erick Bernat</sub>](https://github.com/ErickBernat) | [<img src="https://avatars.githubusercontent.com/u/91349698?v=4" width=115><br><sub>Stella Hada</sub>](https://github.com/stellahada) | 
| :---: | :---: | :---: |
