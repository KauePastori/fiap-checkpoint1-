# ✅ FIAP - Checkpoint 1: API de Pedidos

**Disciplina:** Arquitetura SOA e Web Services  
**Professor:** João Baptista Moreira Junior  
**Integrantes:** Kauê Pastori Teixeira | RM98501 | Felipe Bressane| RM97688
---

## 📋 Descrição

API REST em Spring Boot desenvolvida para cadastrar, listar, buscar, atualizar e deletar pedidos de clientes. Este projeto tem como objetivo aplicar os conceitos de arquitetura orientada a serviços (SOA).

---

## 🚀 Tecnologias Utilizadas

- Java 17  
- Spring Boot 3.1.x  
- Spring Web  
- Spring Data JPA  
- H2 Database  
- Maven

---

## ⚙️ Como Executar

1. Clone o repositório:
```bash
git clone https://github.com/KauePastori/fiap-checkpoint1
```

2. Abra o projeto no IntelliJ

3. Execute a classe:
```java
Checkpoint1Application.java
```

4. Acesse a API no navegador ou via Postman:  
[http://localhost:8080/pedidos](http://localhost:8080/pedidos)

5. Acesse o banco de dados H2:  
[http://localhost:8080/h2-console](http://localhost:8080/h2-console)  

---

## 🧪 Endpoints da API

| Método | Endpoint              | Descrição                       |
|--------|------------------------|----------------------------------|
| POST   | `/pedidos`            | Cria um novo pedido              |
| GET    | `/pedidos`            | Lista todos os pedidos           |
| GET    | `/pedidos/{id}`       | Busca pedido por ID              |
| PUT    | `/pedidos/{id}`       | Atualiza um pedido existente     |
| DELETE | `/pedidos/{id}`       | Remove um pedido por ID          |

---

## 📦 Exemplos de Requisições e Respostas

### ▶️ Criar um pedido (POST `/pedidos`)

**Requisição:**
```json
{
  "clienteNome": "João Silva",
  "valorTotal": 150.00
}
```

**Resposta:**
```json
{
  "id": 1,
  "clienteNome": "João Silva",
  "dataPedido": "2025-03-28",
  "valorTotal": 150.0
}
```

---

### 🔎 Buscar todos os pedidos (GET `/pedidos`)

**Resposta:**
```json
[
  {
    "id": 1,
    "clienteNome": "João Silva",
    "dataPedido": "2025-03-28",
    "valorTotal": 150.0
  }
]
```

---

### 🔍 Buscar pedido por ID (GET `/pedidos/1`)

**Resposta:**
```json
{
  "id": 1,
  "clienteNome": "João Silva",
  "dataPedido": "2025-03-28",
  "valorTotal": 150.0
}
```

---

### ✏️ Atualizar pedido (PUT `/pedidos/1`)

**Requisição:**
```json
{
  "clienteNome": "João P. Silva",
  "valorTotal": 200.00
}
```

**Resposta:**
```json
{
  "id": 1,
  "clienteNome": "João P. Silva",
  "dataPedido": "2025-03-28",
  "valorTotal": 200.0
}
```

---

### ❌ Deletar pedido (DELETE `/pedidos/1`)

**Resposta:** `204 No Content`

---

## 🖼️ Prints dos Testes (Postman)

1. ✅ Criar pedido (POST)
   ![Imagem do WhatsApp de 2025-03-28 à(s) 16 07 52_e5da4f6b](https://github.com/user-attachments/assets/47785ad6-5b08-465d-8074-5de5f70bae0a)

3. ✅ Buscar todos (GET)
   
   ![Imagem do WhatsApp de 2025-03-28 à(s) 16 08 51_6e01b9fb](https://github.com/user-attachments/assets/3dcc45bb-5322-40aa-9d5e-5e9b638e4573)

5. ✅ Buscar por ID (GET)
   ![Imagem do WhatsApp de 2025-03-28 à(s) 16 09 24_e6d94418](https://github.com/user-attachments/assets/be296643-558c-4043-a32b-483d7415f35d)

7. ✅ Atualizar pedido (PUT)
   ![Imagem do WhatsApp de 2025-03-28 à(s) 16 11 00_d5eccdb8](https://github.com/user-attachments/assets/ce70d4ef-aa95-4b27-b52c-a2c7e80a600a)

9. ✅ Deletar pedido (DELETE)
![Imagem do WhatsApp de 2025-03-28 à(s) 16 11 32_b0e22a54](https://github.com/user-attachments/assets/589f1362-2c61-4ac2-8ec7-c64981bb116b)

