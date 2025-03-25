# 🎯 Checkpoint 1 - API de Pedidos

Este projeto é uma **API REST** para gerenciamento de pedidos, utilizando **Spring Boot**, **Spring Data JPA** e banco de dados **H2**.

---

## 🛠 Tecnologias Utilizadas
- 🚀 **Java 17**
- ⚙️ **Spring Boot 3.1.***
- 🌐 **Spring Web**
- 🔄 **Spring Boot DevTools**
- ✍️ **Lombok**
- 🗄 **Spring Data JPA**
- 🛢 **H2 Database**
- 📦 **Maven**

---

## 🚀 Como Rodar o Projeto

1. **Clone o repositório**:
   ```sh
   git clone https://github.com/Joaogdiass/SOA-CP1
   cd checkpoint1
   ```

2. **Compile e instale as dependências**:
   ```sh
   mvn clean install
   ```

3. **Execute a aplicação**:
   ```sh
   mvn spring-boot:run
   ```

4. **Acesse o console do H2 Database** (opcional):
   - 🔗 **URL:** `http://localhost:8080/h2-console`
   - 🛢 **JDBC URL:** `jdbc:h2:mem:testdb`
   - 👤 **User:** `sa`
   - 🔑 **Password:** *(deixe em branco)*

---

## 📌 Endpoints da API

### 📝 Criar um Pedido
- **URL:** `POST /pedidos`
- **Body (JSON):**
  ```json
  {
    "clienteNome": "João Silva",
    "valorTotal": 150.00
  }
  ```
- **Resposta:**
  ```json
  {
    "id": 1,
    "clienteNome": "João Silva",
    "dataPedido": "2025-03-25",
    "valorTotal": 150.00
  }
  ```

  ![alt text](image.png)
  ![alt text](image-1.png)

### 📋 Buscar Todos os Pedidos
- **URL:** `GET /pedidos`
- **Resposta:**
  ```json
  [
    {
      "id": 1,
      "clienteNome": "João Silva",
      "dataPedido": "2025-03-25",
      "valorTotal": 150.00
    }
  ]
  ```
  ![alt text](image-2.png)

### 🔍 Buscar Pedido por ID
- **URL:** `GET /pedidos/{id}`
- **Exemplo:** `GET /pedidos/1`

![alt text](image-3.png)


### ✏️ Atualizar um Pedido
- **URL:** `PUT /pedidos/{id}`
- **Body (JSON):**
  ```json
  {
    "clienteNome": "João Atualizado",
    "valorTotal": 200.00
  }
  ```
![alt text](image-5.png)
  

### ❌ Excluir um Pedido
- **URL:** `DELETE /pedidos/{id}`
- **Exemplo:** `DELETE /pedidos/1`

![alt text](image-4.png)
---


## 🔬 Testando a API
Para testar os endpoints, utilize:
- **📌 Postman**
- **📌 Insomnia**
- **📌 cURL**


