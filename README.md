# Investlink Backend

## Descrição

Este é o backend do projeto **Investlink**, reescrito em Java utilizando o framework **Spring Boot**. O objetivo deste backend é fornecer uma API REST robusta e escalável para gerenciar informações sobre ações e FIIs (Fundos de Investimento Imobiliário) da bolsa de valores. 

## Tecnologias Utilizadas

- **Java 17**: Linguagem principal utilizada no desenvolvimento.
- **Spring Boot**: Framework para facilitar a configuração e o desenvolvimento do backend.
- **Hibernate**: Framework ORM para mapeamento de entidades e interação com o banco de dados.
- **Spring Data JPA**: Para operações simplificadas de banco de dados.
- **JUnit**: Para testes unitários.
- **Mockito**: Para mockar dependências nos testes.
- **Docker**: Para conteinerização da aplicação.

## Estrutura do Projeto

O projeto está organizado da seguinte forma:

```
investlink-backend/
│
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── com/
│   │   │       └── investlink/
│   │   │           ├── controller/          # Controladores REST
│   │   │           ├── service/              # Lógica de negócio
│   │   │           ├── repository/           # Interação com o banco de dados
│   │   │           ├── model/                # Entidades JPA
│   │   │           ├── dto/                  # Data Transfer Objects
│   │   │           └── config/               # Configurações adicionais
│   │   │
│   │   ├── resources/
│   │   │   ├── application.properties        # Configurações da aplicação
│   │   │   └── static/                       # Arquivos estáticos
│   │   │
│   │   └── docker/
│   │       ├── Dockerfile                    # Dockerfile para build da imagem
│   │       └── docker-compose.yml            # Docker Compose
│   │
│   └── test/                                 # Testes unitários
│       └── java/
│           └── com/
│               └── investlink/
│
├── .gitignore                                # Arquivos e pastas a serem ignorados pelo Git
├── pom.xml                                   # Arquivo Maven para gerenciamento de dependências
├── README.md                                 # Descrição do projeto
└── mvnw, mvnw.cmd                            # Scripts do Maven Wrapper
```

## Como Executar

### Pré-requisitos

- **Java 17** ou superior
- **Maven 3.8+**
- **Docker** (opcional, para executar a aplicação em containers)

### Passos para Execução

1. **Clonar o repositório**:
   ```bash
   git clone https://github.com/jeffev/investlink_backend_java.git
   cd investlink-backend
   ```

2. **Build do projeto**:
   ```bash
   ./mvnw clean install
   ```

3. **Executar a aplicação**:
   ```bash
   ./mvnw spring-boot:run
   ```

4. **Executar a aplicação com Docker**:
   ```bash
   docker build -t investlink-backend .
   docker run -p 8080:8080 investlink-backend
   ```

### Endpoints Disponíveis

Os principais endpoints disponíveis são:

- **GET /api/v1/stocks**: Retorna a lista de ações disponíveis.
- **POST /api/v1/stocks**: Adiciona uma nova ação.
- **GET /api/v1/stocks/{id}**: Retorna detalhes de uma ação específica.
- **PUT /api/v1/stocks/{id}**: Atualiza os detalhes de uma ação.
- **DELETE /api/v1/stocks/{id}**: Remove uma ação.

## Testes

Para executar os testes unitários, use o seguinte comando:

```bash
./mvnw test
```

## Contribuição

Se desejar contribuir para este projeto:

1. Faça um fork do repositório.
2. Crie uma branch com a sua feature (`git checkout -b feature/sua-feature`).
3. Faça o commit das suas alterações (`git commit -am 'Adiciona nova feature'`).
4. Faça o push para a branch (`git push origin feature/sua-feature`).
5. Crie um novo Pull Request.

## Licença

Este projeto está licenciado sob os termos da licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.

## Contato

Para mais informações ou dúvidas, entre em contato pelo email: [jeffev123@gmail.com](mailto:jeffev123@gmail.com).
