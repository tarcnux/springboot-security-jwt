# [springboot-security-jwt](https://github.com/digitalinnovationone/dio-springboot/tree/main/dio-spring-security-jwt)
Um singelo exemplo de uso de Spring Securiyt com Token JWT com Springboot


### [JWT - JSON Web Token](https://glysns.gitbook.io/spring-framework/spring-security/spring-security-e-jwt)

### Estrutura do Projeto

| Pacote    | Descrição |
|-----------|-----------|
| model     | Camada que contém as entidades da aplicação |
| dto       | Camada que contém os dtos da aplicação |
|repository | Camada que contém os repositórios com base no Spring Data JPA |
|service    | Camada que detém da regra de negócio e comunicação com a base de dados via repositorys |
|controller | Camada que contém os recursos https expostos na API |
|security   | Camada responsável para toda configuração de segurança. |

### Classes Utilitárias

| Classe    | Descrição |
|-----------|-----------|
| SwaggerConfig | Classe responsável pela documentação da API |
| JWTObject     | Classe que representa um Objeto correspondente a estrutura JWT |
| JWTCreator    | Classe responsável por gerar o Token com base no Objeto e ou instanciar o Objeto JWT com base no Token |

## Cadastrar Usuário
POST http://localhost:8080/users

{
    "name":"Tarcísio Nunes", 
    "username":"tarcnux", 
    "password":"qwerty",
    "roles":["USERS","MANAGERS"]
}

### Consulta cadastro de usuário no BD
http://localhost:8080/h2-console/
