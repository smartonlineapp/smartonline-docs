# Autenticação

A autenticação funciona através de um token JWT.

### Exemplo

> **POST** https://login.smartonline.app/connect/token

No header da request os seguintes campos devem ser preenchidos.


- ClientId
- ClientSecret
- GrantType
- Scope

### Observações

- ***As credenciais são providas pelo administrador do seu grupo.***
- ***O token deve estar presente em todas as requisições***  
- ***O token se expira em 1 hora.***


