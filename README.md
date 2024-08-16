Investlink backend

Descrição das Pastas e Arquivos:
InvestlinkApplication.java: Classe principal que contém o método main() para iniciar a aplicação Spring Boot.

controller/: Contém os controladores REST, responsáveis por expor os endpoints da API.

service/: Contém a lógica de negócios e orquestra chamadas para os repositórios.

repository/: Contém as interfaces que estendem JpaRepository ou CrudRepository, responsáveis por interagir com o banco de dados.

model/: Contém as classes de entidade que representam as tabelas do banco de dados, mapeadas usando Hibernate.

dto/: Contém os Data Transfer Objects (DTOs) usados para transferir dados entre as camadas da aplicação.

config/: Contém classes de configuração, como configurações de segurança, CORS, ou configurações específicas do Hibernate.

application.properties: Arquivo de configuração onde você define parâmetros como conexão com o banco de dados, configuração de portas, entre outros.

Dockerfile: Define como a imagem Docker da aplicação será construída.

docker-compose.yml: Utilizado para orquestrar múltiplos containers, como o backend, banco de dados, etc.

test/: Contém os testes unitários organizados de forma semelhante à estrutura principal.

pom.xml: Arquivo Maven que gerencia as dependências do projeto.

