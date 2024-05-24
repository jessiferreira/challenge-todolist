<p align="center">
  <img src="https://github.com/jessiferreira/challenge-todolist/assets/121064773/673d1f5b-4a41-487c-92f8-d1dd60a11e83" width="1200px">
</p>

[![Generic badge](https://img.shields.io/badge/Tipo-Desafio-C2078F.svg)](https://shields.io/)&nbsp;
[![Generic badge](https://img.shields.io/badge/Status-Concluído-C2078F.svg)](https://shields.io/)&nbsp;

## 📖 DESCRIÇÃO
API para gestão de tarefas, desenvolvida como parte do desafio para candidatos a 
desenvolvedores back-end júnior na Simplify.
Repositório original [aqui](https://github.com/simplify-tec/desafio-junior-backend-simplify).


## 📑 ÍNDICE
- [Tecnologias](#-TECNOLOGIAS)
- [Metodologias](#-METODOLOGIAS)
- [Funcionalidades](#-FUNCIONALIDADES)
- [Como Utilizar](#-COMO-UTILIZAR)

## 🛠️ TECNOLOGIAS
- [IntelliJ IDEA](https://www.jetbrains.com/products/compare/?product=idea&product=idea-ce)
- [Java](https://www.java.com/pt-BR/download/ie_manual.jsp?locale=pt_BR)
- [MySQL](https://dev.mysql.com/downloads/)
- [Spring Boot](https://spring.io/projects/spring-boot)
- [Spring Data JPA](https://spring.io/projects/spring-data-jpa)
- [Spring MVC](https://docs.spring.io/spring-framework/reference/web/webmvc.html)
- [Spring Doc OpenAPI 3](https://springdoc.org/)

## ⚙️ METODOLOGIAS
- API REST
- Consultas com Spring Data JPA
- Geração automática do Swagger com a OpenAPI 3
- Injeção de dependências
- Tratamento de erros

## 🔧 FUNCIONALIDADES
- __Criar Tarefa:__ Capacidade de criar uma nova tarefa com nome, descrição e prioridade;
- __Listar Tarefas:__ Mostrar todas as tarefas existentes;
- __Atualizar Tarefa:__ Atualizar o nome, descrição ou prioridade de uma tarefa existente;
- __Excluir Tarefa:__ Remover uma tarefa existente.

## 🎮 COMO UTILIZAR
1. Clonar o repositório Git
2. Construir o projeto:
```

$ ./mvnw clean package

```
3. Executar a aplicação:
```

$ java -jar target/todolist-0.0.1-SNAPSHOT.jar

```
4. Acessar a API em [localhost:8080](http://localhost:8080/)
5. O Swagger poderá ser visualizado em [localhost:8080/swagger-ui.html](http://localhost:8080/swagger-ui/index.html)

## 🛣️ API ENDPOINTS
Para fazer as requisições HTTP abaixo, foi utilizada a ferramenta [httpie](https://httpie.io/).
1. Criar tarefas:
```
$ http POST :8080/todos name="Todo 1" description="Desc Todo 1" priority=1

[
  {
    "description": "Desc Todo 1",
    "id": 1,
    "name": "Todo 1",
    "priority": 1,
    "realized": false
  }
]
```
2. Listar tarefas:
```
$ http GET :8080/todos

[
  {
    "description": "Desc Todo 1",
    "id": 1,
    "name": "Todo 1",
    "priority": 1,
    "realized": false
  }
]
```
3. Atualizar tarefas:
```
$ http PUT :8080/todos/1 name="Todo 1 Up" description="Desc Todo 1 Up" priority=2

[
  {
    "description": "Desc Todo 1 Up",
    "id": 1,
    "name": "Todo 1 Up",
    "priority": 2,
    "realized": false
  }
]
```
4. Remover tarefas:
```
http DELETE :8080/todos/1

[ ]
```
