## Products - API

Esta é uma API, para ser utilizada no armazenamento de dados de qualquer tipo de produto, com isso é possível utilizar para os mais diversos tipo de ecommerce.

## Endpoints

Essa API, possui 7 endpoints.
É possível cadastrar usuário, realizar o login. E cadastrar os produtos que serão necessário para sua aplicação.
Além disso também possui um endpoint de exemplo, para mostrar como que pode ser utilizado.

#### Rotas que não precisam de autenticação

Verificando exemplo de como se utilizar a API <br/>

GET /typeProducts

#### Criação de usuário

POST /register <br/>
POST /signup <br/>
POST /users

Qualquer um desses 3 endpoints irá cadastrar o usuário na lista de "Users", sendo que os campos obrigatórios são os de email e password.
Você pode ficar a vontade para adicionar qualquer outra propriedade no corpo do cadastro dos usuários.

#### Login

POST /login <br/>
POST /signin

Qualquer um desses 2 endpoints pode ser usado para realizar login com um dos usuários cadastrados na lista de "Users".

#### Criando produtos

POST /product - Formato da requisição

    {
        "name": "televisao",
        "category": "eletronico",
        "userId": 2,

    }

No primeiro campo, temos de enviar o nome da categoria (STRING), no segundo a categoria do produto (STRING) e no terceiro o userId (NUMBER) que o usuário recebe esse ID ao realizar o cadastro.

#### Rotas relacionadas

Esta é uma rota relacionada com os produtos, onde é possível coletar as características dos produtos cadastrados.
Utilizando o queryParams abaixo um exemplo:

Neste caso o usuário possuo o id: 3

"localhost:3001/users/3_embed=product"
