

# Projeto Course

## Descrição

Este projeto é uma demonstração de um aplicativo Spring Boot simples. Inicialmente, ele inclui funcionalidades básicas de desenvolvimento web e a possibilidade de se conectar a um banco de dados usando JPA.

## Pré-requisitos

* Java 11 ou superior
* Maven 3.x

## Configuração

1. Clone o repositório do projeto.
2. Execute `mvn install` para baixar e instalar as dependências.

## Executando o Projeto

1. Navegue para o diretório raiz do projeto.
2. Execute `mvn spring-boot:run` para iniciar a aplicação.
3. Acesse a aplicação em http://localhost:8080 (ou a porta especificada).

## Depêndências

Este projeto usa as seguintes dependências:

* `spring-boot-starter-web`: Fornece suporte para desenvolvimento web.
* `h2`: Banco de dados em memória para desenvolvimento e testes.
* `spring-boot-starter-data-jpa`: Permite acesso a dados JPA.
* `spring-boot-starter-test`: Fornece ferramentas para testes unitários e de integração.

  ## Exemplos de Uso

### Cadastro de Usuário

#### POST /users

Este exemplo demonstra como cadastrar um novo usuário enviando um objeto JSON no corpo da solicitação.

**Solicitação:**
```http
POST /users HTTP/1.1
Host: example.com
Content-Type: application/json

{
  "name": "Bob Brown",
  "email": "bob@gmail.com",
  "phone": "977557755",
  "password": "123456"
}
```
**Resposta:**
```http
HTTP/1.1 201 Created
Location: /users/1
Content-Type: application/json

{
"id": 1,
"name": "Bob Brown",
"email": "bob@gmail.com",
"phone": "977557755"
}
```
## Recuperação de Todos os Usuários

Este exemplo demonstra como recuperar todos os usuários cadastrados.

**Solicitação:**
```http
GET /users HTTP/1.1
Host: example.com
```
**Resposta:**
```http
HTTP/1.1 200 OK
Content-Type: application/json

[
  {
    "id": 1,
    "name": "Bob Brown",
    "email": "bob@gmail.com",
    "phone": "977557755"
  },
  {
    "id": 2,
    "name": "Alice Johnson",
    "email": "alice@gmail.com",
    "phone": "988889999"
  }
]


