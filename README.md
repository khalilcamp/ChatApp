# Projeto de Chat em Tempo Real

Este projeto implementa uma aplicação de chat em tempo real com comunicação bidirecional entre cliente web e servidor usando WebSockets e STOMP.

---

## ✨ Funcionalidades Principais

- **Chat em Tempo Real:** Troca instantânea de mensagens.
- **Identificação do Remetente:** Usuário informa seu nome para identificação clara.
- **Ícones Personalizados:** Cada usuário recebe um emoji único como ícone.
- **Notificações de Conexão:** Informações visuais sobre o status da conexão.
- **Interface Responsiva:** Layout adaptável para diferentes dispositivos.
- **Ele é feio**

---

## 🛠 Tecnologias Utilizadas

### Frontend

- HTML5
- Tailwind CSS
- JavaScript
- SockJS
- STOMP.js

### Backend

- Java
- Spring Boot
- Spring WebSockets
- STOMP
- Lombok
- Jackson

---

## Estrutura do Código Backend

### Modelo `ChatMessage`

Classe Java que representa uma mensagem de chat com atributos `id`, `sender` e `content`.

### Controlador `ChatController`

Controlador Spring que recebe mensagens via STOMP no endpoint `/app/sendMessage` e retransmite para o tópico `/topic/messages`.

### Configuração `WebSocketConfig`

Configura endpoints WebSocket com SockJS e define prefixos para broker e aplicação.

---

## Como Executar

### Backend

```bash
mvn spring-boot:run
