# 🍇 Web Site Desfruto - BackEnd

![NodeJS](https://img.shields.io/badge/Node.js-43853D?style=for-the-badge&logo=node.js&logoColor=white)
![Express.js](https://img.shields.io/badge/Express.js-404D59?style=for-the-badge)
![MySQL](https://img.shields.io/badge/mysql-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![Sequelize](https://img.shields.io/badge/Sequelize-52B0E7?style=for-the-badge&logo=Sequelize&logoColor=white)
![JWT](https://img.shields.io/badge/JWT-000000?style=for-the-badge&logo=JSON%20web%20tokens&logoColor=white)


> Servidor e API responsável por gerenciar os dados do sistema de pedidos de açaí "Desfruto".

Este projeto lida com as regras de negócio, persistência de dados e autenticação, servindo como a espinha dorsal para a aplicação de pedidos.

---

## 🔌 Integração com Front-End

Este back-end foi projetado para funcionar em conjunto com a interface do usuário.

🍓 **[Acesse o Repositório do Front-End](https://github.com/stellahada/acaiFrontEnd)**

---

## 🚀 Funcionalidades

- **Gerenciamento de Cardápio:** Operações de CRUD para itens e acompanhamentos.
- **Autenticação:** Sistema de registro e login de usuários.
- **Controle de Pedidos:** Processamento de pedidos recebidos e atualização de status (Ex: Em Preparo).
- **Persistência de Dados:** Integração robusta com MySQL via Sequelize.

---

## 🛠️ Tecnologias Utilizadas

O projeto utiliza uma stack moderna e eficiente para APIs REST.

- **Ambiente:** Node.js
- **Framework:** Express.js
- **Banco de Dados:** MySQL (Relacional)
- **ORM:** Sequelize (Abstração e modelagem de dados)
- **Autenticação:** JSON Web Token (JWT)
- **Integração:** Axios 


---

## 📂 Estrutura do Banco de Dados

Para o funcionamento correto, o sistema espera a seguinte estrutura de tabelas. Você pode executar o script SQL abaixo no seu cliente MySQL:

```sql
-- Tabela de Pedidos
CREATE TABLE pedido (
  id_pedido int primary key auto_increment,
  ds_estado varchar(400)
);

-- Tabela de Itens do Pedido
CREATE TABLE itens (
  id_item int primary key auto_increment,
  id_pedido int,
  ds_url varchar(200),
  dp_preco float,
  ds_nome varchar(100),
  ds_tamanho varchar (100),
  ds_acompanhamentos varchar(200),
  FOREIGN KEY (id_pedido) REFERENCES pedido(id_pedido) 
);

-- Tabela de Login/Usuários
CREATE TABLE login(
  id_login int primary key auto_increment, 
  ds_email varchar(200),
  ds_senha varchar(200)
);

-- Inserção de Estado Inicial
INSERT INTO pedido(ds_estado) VALUES('Em Preparo');
```

---

## ⚙️ Instalação e Execução
Pré-requisitos: Node.js e MySQL instalados.

Clone o repositório

```Bash
git clone [https://github.com/stellahada/acaiBackEnd.git](https://github.com/stellahada/acaiBackEnd.git)
cd acaiBackEnd
```
Instale as dependências

```Bash
npm install
```
Configuração do Banco Certifique-se de que seu serviço MySQL esteja rodando e que as tabelas acima tenham sido criadas. Verifique também o arquivo de configuração do Sequelize (geralmente em /config ou .env) para ajustar usuário e senha do banco.

Execute o Servidor

```Bash
npm start
# ou
node index.js
```

---

## Contribuidores 🧑‍💻👩‍💻🧑‍💻
| [<img src="https://avatars.githubusercontent.com/u/95144250?s=400&u=149cf20f52f4c096721d16967b22655f18e5c7f5&v=4" width=115><br><sub>Samuel Victor</sub>](https://github.com/Samuel-045) | [<img src="https://avatars.githubusercontent.com/u/138524660?v=4" width=115><br><sub>Erick Bernat</sub>](https://github.com/ErickBernat) | [<img src="https://avatars.githubusercontent.com/u/91349698?v=4" width=115><br><sub>Stella Hada</sub>](https://github.com/stellahada) | 
| :---: | :---: | :---: |
