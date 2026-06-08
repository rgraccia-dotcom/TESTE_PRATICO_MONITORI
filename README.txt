Projeto Monitori - Teste Prático
Tecnologias utilizadas

Front-end:
Angular v22.0.0
Angular CLI v22.0.0
TypeScript
HTML
SCSS

Back-end:
.NET 8
ASP.NET Core Web API
Entity Framework Core (ORM)
SQL Server

Banco de Dados

Na pasta /script_sql estão disponíveis os scripts necessários para:

Criação do banco de dados
Criação das tabelas
Inserção de dados iniciais

Observações importantes:

O projeto utiliza Entity Framework Core (ORM)
Não existem Stored Procedures na base de dados
Todo acesso ao banco é feito via ORM (Entity Framework)
Configuração do projeto

Connection String (Back-end)

A configuração deve ser feita no arquivo appsettings.json:

{
"ConnectionStrings": {
"DatabaseConnection": "Server=(LocalDB)\MSSQLLocalDB;Database=DB_MONITORI;Integrated Security=True;TrustServerCertificate=True;"
}
}

Execução do projeto

Back-end (.NET 8)

Acesse a pasta do projeto e execute:

dotnet restore
dotnet build
dotnet run

A API ficará disponível em:
https://localhost:xxxx

Front-end (Angular)

Acesse a pasta do front-end e execute:

npm install
ng serve

A aplicação ficará disponível em:
http://localhost:4200

Integração

O front-end consome a API do back-end via requisições HTTP.

Caso necessário, o CORS está configurado no back-end como:

policy.AllowAnyOrigin()
.AllowAnyMethod()
.AllowAnyHeader();

Observações finais
Projeto desenvolvido com foco em boas práticas de arquitetura
Separação em camadas:
Controllers (API)
Business (Regras de negócio)
Repository (Acesso a dados)
Uso de Entity Framework Core para abstração do banco de dados
Não há uso de Stored Procedures





