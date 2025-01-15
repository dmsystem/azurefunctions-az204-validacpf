# Validação de CPF com Azure Functions

![C#](https://img.shields.io/badge/C%23-239120?style=for-the-badge&logo=c-sharp&logoColor=white)
![Azure Functions](https://img.shields.io/badge/Azure%20Functions-0062AD?style=for-the-badge&logo=azure-functions&logoColor=white)
![ASP.NET Core](https://img.shields.io/badge/ASP.NET%20Core-512BD4?style=for-the-badge&logo=dotnet&logoColor=white)
![Newtonsoft.Json](https://img.shields.io/badge/Newtonsoft.Json-000000?style=for-the-badge&logo=json&logoColor=white)

Este projeto tem como objetivo desenvolver um microsserviço eficiente, escalável e econômico para validação de CPFs, utilizando arquitetura serverless. A aplicação será construída com base em princípios modernos de computação em nuvem, garantindo alta disponibilidade, baixo custo operacional e facilidade de manutenção.

## Funcionalidades

- Recebe um CPF em formato JSON via requisição HTTP POST.
- Valida o CPF verificando seu formato e dígitos verificadores.
- Retorna uma resposta indicando se o CPF é válido ou inválido.

## Tecnologias Utilizadas

- C#
- Azure Functions
- ASP.NET Core
- Newtonsoft.Json

## Como Executar

1. Clone o repositório.
2. Configure seu ambiente de desenvolvimento para Azure Functions.
3. Execute a função localmente usando o Azure Functions Core Tools.
4. Envie uma requisição HTTP POST com um CPF para testar a validação.

**Observação:** Para rodar a função pela internet, é necessário criar previamente uma Function App no portal do Azure para hospedar este projeto. Caso contrário, a função só funcionará localmente.

## Exemplo de Requisição

```json
POST /api/fnvalidacpf
{
    "cpf": "12345678909"
}
```

## Exemplo de Resposta

```json
{
    "message": "CPF válido. Obrigado por utilizar a função de validação de CPF."
}
```

```json
{
    "message": "CPF inválido."
}
```


## Contribuição

Contribuições são bem-vindas! Sinta-se à vontade para abrir issues e pull requests.

## Licença

Este projeto está licenciado sob a licença MIT.
```