## 🎮 API REST - Game Collection

Este projeto é uma API REST desenvolvida em Spring Boot para gerenciar uma coleção de jogos.
A aplicação permite listar, consultar e gerenciar games organizados em listas personalizadas.  

## 📌 Funcionalidades
- Listar todos os jogos
- Listar todos os tipos de jogos (listas)
- Buscar jogo por ID
- Trocar a posição de um jogo em uma lista (endpoint POST)

## 🛠️ Tecnologias Utilizadas

- Java 21+
- Spring Boot
- Spring Data JPA
- H2 Database (testes locais)
- PostgreSQL (homologação com container Docker)
- Maven

## 🗂️ Estrutura do Projeto

- entities → mapeamento das entidades (Game, GameList, Belonging, BelongingPK)
- repositories → acesso ao banco de dados
- services → regras de negócio
- dto → transferência de dados
- projections → consultas específicas ao banco
- controllers → endpoints da API

## Endpoints
🔹 Listar todos os games GET /games  
🔹 Listar todos os tipos de games (listas) GET /lists  
🔹 Buscar game por ID GET /games/{id}  
  
🔹 Trocar posição de um game em uma lista POST /lists/{listId}/replacement  
  
Body (JSON exemplo):  
  
{  
  "sourceIndex": 2,  
  "destinationIndex": 0  
}  


## 🗄️ Banco de Dados

- H2 Database utilizado para desenvolvimento e testes.
- PostgreSQL em container Docker utilizado para homologação.
