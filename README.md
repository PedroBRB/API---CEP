📌 API de Consulta de CEP com Spring Boot
🔍 Uma API robusta e eficiente para busca de endereços a partir de CEPs, desenvolvida em Spring Boot com integração à ViaCEP, documentação via Swagger e um toque de inteligência artificial com OpenAI.

🚀 Tecnologias Utilizadas
Java 17

Spring Boot 3 (Web, Lombok, Validation)

Swagger (OpenAPI 3) – Documentação interativa da API

Integração com APIs externas:

ViaCEP – Para consulta de endereços

OpenAI API – Para respostas inteligentes (ex: sugestões de CEPs próximos)

Maven – Gerenciamento de dependências

Git & GitHub – Versionamento de código

⚡ Funcionalidades
✅ Consulta de CEP – Retorna logradouro, bairro, cidade e UF.
✅ Validação de CEP – Verifica se o formato é válido antes da consulta.
✅ Documentação Automatizada – Acessível via Swagger UI (/swagger-ui.html).
✅ Respostas Inteligentes – Integração com OpenAI para sugestões de CEPs similares (ex: "Você quis dizer [CEP]?").
✅ Tratamento de Erros – Mensagens claras para CEPs inválidos ou não encontrados.

📌 Como Usar?
🔧 Pré-requisitos
JDK 17+

Maven 3.8+

Conta na OpenAI (se quiser usar a integração com IA)

🚀 Executando Localmente
Clone o repositório:

bash
git clone https://github.com/PedroBRB/API---CEP.git
Entre na pasta do projeto:

bash
cd API---CEP
Execute o projeto com Maven:

bash
mvn spring-boot:run
Acesse a API em:

bash
http://localhost:8080
Documentação Swagger:
Acesse http://localhost:8080/swagger-ui.html para testar os endpoints.

🔗 Endpoints
1. GET /api/cep/{cep}
Descrição: Retorna os dados do endereço correspondente ao CEP.
Exemplo de Requisição:

bash
GET http://localhost:8080/api/cep/01001000
Resposta de Sucesso (200 OK):

json
{
  "cep": "01001-000",
  "logradouro": "Praça da Sé",
  "bairro": "Sé",
  "localidade": "São Paulo",
  "uf": "SP"
}
Resposta de Erro (400/404):

json
{
  "mensagem": "CEP inválido ou não encontrado."
}
🎯 Melhorias Futuras
🔹 Cache de consultas (Redis) para melhor desempenho.
🔹 Deploy em nuvem (AWS/Heroku) com Docker.
🔹 Autenticação JWT para uso em produção.

👨‍💻 Contribuições
Contribuições são bem-vindas! Sinta-se à vontade para abrir issues ou pull requests.

📄 Licença
Este projeto está sob a licença MIT.
