# Validação de CPF com Azure Functions

![C#](https://img.shields.io/badge/C%23-239120?style=for-the-badge&logo=c-sharp&logoColor=white)
![Azure Functions](https://img.shields.io/badge/Azure%20Functions-0062AD?style=for-the-badge&logo=azure-functions&logoColor=white)
![ASP.NET Core](https://img.shields.io/badge/ASP.NET%20Core-512BD4?style=for-the-badge&logo=dotnet&logoColor=white)
![Newtonsoft.Json](https://img.shields.io/badge/Newtonsoft.Json-000000?style=for-the-badge&logo=json&logoColor=white)

Este projeto tem como objetivo desenvolver um microsserviço eficiente, escalável e econômico para validação de CPFs, utilizando arquitetura serverless. A aplicação foi criada para garantir alta disponibilidade, baixo custo operacional e facilidade de manutenção, baseando-se em princípios modernos de computação em nuvem.

![Azure Functions Workflow](https://user-images.githubusercontent.com/12345678/azure-functions-workflow.png)

## Funcionalidades

- **Entrada JSON via HTTP POST:** Recebe um CPF no formato JSON por meio de uma requisição HTTP POST.
- **Validação de CPF:** Verifica o formato e os dígitos verificadores do CPF.
- **Resposta clara:** Retorna uma mensagem indicando se o CPF é válido ou inválido.

## Tecnologias Utilizadas

- **Linguagem:** C#
- **Plataforma:** Azure Functions
- **Framework:** ASP.NET Core
- **Serialização JSON:** Newtonsoft.Json

## Configuração do Ambiente

1. Clone este repositório:

   ```bash
   git clone <URL_DO_REPOSITORIO>
   ```

2. Configure seu ambiente de desenvolvimento para Azure Functions.

   - Instale o [Azure Functions Core Tools](https://learn.microsoft.com/azure/azure-functions/functions-run-local).
   - Configure o Visual Studio ou Visual Studio Code com as extensões para Azure Functions.

3. Execute a função localmente:

   ```bash
   func start
   ```

4. Envie uma requisição HTTP POST para testar a validação:

   ```bash
   curl -X POST http://localhost:7071/api/fnvalidacpf \
   -H "Content-Type: application/json" \
   -d '{"cpf": "12345678909"}'
   ```

5. Para disponibilizar a função online, crie uma Function App no portal do Azure e faça o deploy do código.

## Exemplo de Requisição

```json
POST /api/fnvalidacpf
{
    "cpf": "12345678909"
}
```

## Exemplo de Resposta

### CPF Válido:

```json
{
    "message": "CPF válido. Obrigado por utilizar a função de validação de CPF."
}
```

### CPF Inválido:

```json
{
    "message": "CPF inválido."
}
```

## Autor

Este projeto foi desenvolvido por **Décio Faustino Morais Neto**:

- **[LinkedIn](https://www.linkedin.com/in/decio-morais/)**
- **[Cloud Skills Boost](https://www.cloudskillsboost.google/public_profiles/5470aeca-088d-4358-ad63-b2530cd433d7)**
- **Estudante de Data Science pela UNIVESP**
- **Formado em Engenharia de Dados (Koru) e Análise de Dados (Soul Code)**
- **Habilidades em computação em nuvem: AWS, Azure, GCP**

## Contribuição

Contribuições são bem-vindas! Sinta-se à vontade para abrir issues e pull requests.

## Licença

Este projeto está licenciado sob a licença MIT. Consulte o arquivo `LICENSE` para mais detalhes.

![Project Preview](https://user-images.githubusercontent.com/12345678/project-preview.png)

