# json-server-base

Esse é o repositório com a base de JSON-Server + JSON-Server-Auth já configurada, feita para ser usada no desenvolvimento das API's nos Projetos Front-end.

## Endpoints

Assim como a documentação do JSON-Server-Auth traz (https://www.npmjs.com/package/json-server-auth), existem 3 endpoints que podem ser utilizados para cadastro e 2 endpoints que podem ser usados para login.

### Cadastro

POST /register <br/>

POST /signup <br/>

POST /users

Precisa ter os dados:

{
"name": string,
"email": string,
"password": string,
"CPF": number,
}

Qualquer um desses 3 endpoints irá cadastrar o usuário na lista de "Users", sendo que os campos obrigatórios são os de email e password.
Você pode ficar a vontade para adicionar qualquer outra propriedade no corpo do cadastro dos usuários.

### Login

POST /login <br/>
POST /signin

Qualquer um desses 2 endpoints pode ser usado para realizar login com um dos usuários cadastrados na lista de "Users"

---

API criada para gerenciar dados sobre animais silvestres resgatados.

# GET

/users/{id} - vizualizar lista de usuarios cadastrados

/animals - vizualizar lista de animais cadastrados

# POST - ambas rotas necessitam de autorização (token)

/animals - registar animais resgatados

Precisa ter os dados:

{
"rescued": boolean,
"petname": string,
"gender": string,
"specie": string,
"identification": number,
}

/ransoms - registrar funcionarios

Precisa ter os dados:

{
"state": string,
"city": string,
"employees": [
{
"name": string,
"CPF": string
}
],
"animals-rescued": [
{
"name": string,
"specie": string,
"identification": string
}
]
}
