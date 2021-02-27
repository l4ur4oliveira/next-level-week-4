# Next Level Week #4 :rocket:

Projeto desenvolvido durante a trilha **[Elixir](https://nextlevelweek.com/)** com as principais noções sobre a tecnologia.

## Links

- [Instalação do Elixir, Phoenix e Postgres](https://www.notion.so/Configura-es-do-ambiente-Elixir-f823443de76840cbbcb8ab1db8aa4667)

## Rocketpay API

Iniciando um Phoenix server:

- Instalar dependências com `mix deps.get`
- Criação de DB com `mix ecto.setup`
- Start Phoenix com `mix phx.server`

Acesso em [`localhost:4000`](http://localhost:4000).

## Tools

- Visual Studio Code
- Google Chrome

## Endpoints

<br>

### POST
- /api/**users** (cria um usuário com uma conta zerada)
```
BODY:
{
    "name": "nome_do_usuario",
    "nickname": "nickname_do_usuario",  // unique
    "email": "email@usuario.com",       // unique
    "age": 30,                          // >=18
    "password": "123456"                // min 6 characters
}
```
- /api/**accounts/:id/deposit** (realiza um depósito em uma conta)
- /api/**accounts/:id/withdraw** (realiza um saque em uma conta)
```
BODY:
{
    "value": "5.0"
}
```
- /api/**accounts/transaction** (realiza uma transferência entre contas)
```
BODY:
{
    "value": "5.0",
    "from": "from_account_id",
    "to": "to_account_id"
}
```