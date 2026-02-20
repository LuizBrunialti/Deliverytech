ddDeliveryTech API

API RESTful desenvolvida com Spring Boot 3 e Java 21 para gerenciar um sistema de delivery completo. Este projeto simula as funcionalidades principais de plataformas como iFood e Uber Eats, incluindo autenticação JWT, cache, monitoramento, CI/CD e muito mais.

---

## 1. Como instalar e executar o projeto

### Pré-requisitos

- JAVA JDK-21
- MAVEN 3.9.12
- GIT
- Docker e Docker container (opcional)
- VS Code

### Instalação e execução

1. Clone o repositório via CMD:
```
git clone https://github.com/LuizBrunialti/Deliverytech.git
cd Deliverytech
```
2. Abra o VS Code
3. Clique em abrir pasta
4. Selecione o projeto em:   
```
C:\Users\SeuNome\ProjetoDeliveryTech
```
5. Clique no em qualquer arquivo .java e aperte o play no canto superior direito do VS Code
6. Acesse as Endpoints via swagger em:
```
http://localhost:8080/swagger-ui.html

```
## Funcionalidades

- Cadastro e login de usuários com JWT
- Controle de acesso por perfis (CLIENTE, RESTAURANTE, ADMIN)
- Cadastro de clientes, restaurantes, produtos e pedidos
- Listagem de produtos por restaurante
- Criação de pedidos com itens e cálculo do total
- Atualização de status de pedido
- Cache com Spring Cache
- Testes automatizados com JUnit e Mockito
- Documentação com Swagger/OpenAPI
- Banco de dados em memória com H2
- Containerização com Docker e orquestração com Docker Compose
- Pipeline CI/CD com GitHub Actions

---

## Tecnologias Utilizadas

- Java 21
- Spring Boot 3.2.x
- Spring Data JPA
- Spring Security + JWT
- Spring Validation
- H2 Database
- SpringDoc OpenAPI (Swagger)
- Docker + Docker Compose
- JUnit 5 + Mockito

---
## 2. Estrutura de pastas e organização

```
DELIVERY/
├── 📂 .vscode/                  # Configurações do editor (settings.json)
├── 📂 Projeto DeliveryTech/      # Pasta raiz do projeto Java
│   └── 📂 deliverytech/         # Módulo principal da aplicação
│       ├── 📂 src/
│       │   ├── 📂 main/
│       │   │   ├── 📂 java/com/deliverytech/
│       │   │   │   ├── 📂 config/      # Configurações (ex: OpenAPI/Swagger)
│       │   │   │   ├── 📂 controller/  # Endpoints da API (Ex: ClienteController)
│       │   │   │   ├── 📂 dto/         # Objetos de Transferência de Dados
│       │   │   │   ├── 📂 exception/   # Tratamento de erros personalizado
│       │   │   │   ├── 📂 model/       # Entidades JPA (Cliente, Pedido, etc.)
│       │   │   │   ├── 📂 repository/  # Interfaces de acesso ao banco (Spring Data JPA)
│       │   │   │   ├── 📂 security/    # Filtros e configurações de segurança (JWT)
│       │   │   │   ├── 📂 service/     # Lógica de negócio da aplicação
│       │   │   │   └── 📄 DeliveryTechApiApplication.java # Classe principal (Play)
│       │   │   └── 📂 resources/    # application.properties e arquivos estáticos
│       │   └── 📂 test/
│       │       └── 📂 java/com/deliverytech/
│       │           ├── 📂 config/     # Configurações específicas para testes
│       │           └── 📂 controller/ # Testes de integração de API
│       │               └── 📄 ClienteControllerTest.java # Testes unitários/integração
│       ├── 📂 target/           # Arquivos compilados (.class e .jar)
│       ├── 📄 pom.xml           # Gerenciador de dependências Maven
│       ├── 📄 Dockerfile        # Instruções para criação da imagem Docker
│       └── 📄 docker-compose.yml # Orquestração de containers (Banco/App)
└── 📄 README.md                 # Documentação do projeto
```

---
## 3. Bibliotecas e dependências utilizadas

1. Framework Base (Core)
-Spring Boot (v3.2.5): É o "cérebro" do projeto, responsável por orquestrar todas as outras ferramentas com configuração mínima.

-Spring MVC: Gerencia a camada de controle (controllers), definindo os endpoints da API de delivery.

2. Persistência e Dados
-Spring Data JPA / Hibernate: Facilita a comunicação com o banco de dados, transformando suas classes Java (model) em tabelas automaticamente.

-Banco de Dados H2: Um banco de dados em memória, ideal para desenvolvimento e testes rápidos, pois não exige instalação externa.

3. Segurança e Documentação
-Spring Security & JWT: Camada de proteção que gerencia quem pode acessar o quê (Roles como CLIENTE ou ADMIN) via tokens de autenticação.

-SpringDoc OpenAPI (Swagger): A ferramenta que você abriu recentemente para testar e visualizar seus endpoints de forma interativa.

4. Monitoramento e Observabilidade
-Spring Boot Actuator: Fornece os endpoints de saúde e métricas da aplicação.

-Micrometer (Tracing & Observation): Coleta dados detalhados sobre o desempenho das requisições.

-Zipkin Reporter: Permite enviar esses dados de rastreamento para uma interface visual externa, ajudando a identificar lentidão no sistema.

5. Qualidade e Infraestrutura
-JUnit 5 & MockMvc: Utilizados nos seus testes (ClienteControllerTest) para garantir que as alterações no código não quebrem as funcionalidades existentes.

-Docker & Docker Compose: Preparam o ambiente para que o projeto rode da mesma forma em qualquer computador ou servidor.

-Maven: O maestro que baixa e organiza todas essas dependências citadas acima.

---


---

