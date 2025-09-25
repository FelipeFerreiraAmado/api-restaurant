# 🍽️ API de Gerenciamento de Pedidos de Restaurante

Este projeto é uma API robusta e funcional para o gerenciamento de pedidos em um restaurante, desenvolvida com foco em performance, segurança de tipos e tratamento de erros.

## ✨ Visão Geral

Esta API foi criada para simular um sistema completo de gerenciamento de pedidos de restaurante. Ela permite controlar produtos, mesas e pedidos de forma eficiente. O projeto explora a criação e utilização de APIs RESTful, integração com banco de dados e a implementação de validações rigorosas para garantir a integridade dos dados e a robustez do sistema. A utilização de TypeScript garante uma tipagem segura e consistente em todo o código.

## 🛠️ Tecnologias Utilizadas

[![My Skills](https://skillicons.dev/icons?i=ts,nodejs,express,sqlite )](https://skillicons.dev )

-   **TypeScript**: Linguagem de programação que adiciona tipagem estática ao JavaScript, proporcionando maior segurança e consistência ao código.
-   **Node.js**: Ambiente de execução JavaScript server-side.
-   **Express**: Framework web para Node.js, utilizado para construir a API de forma rápida e eficiente.
-   **Knex.js**: Construtor de queries SQL flexível e poderoso, utilizado para interagir com o banco de dados.
-   **Zod**: Biblioteca de validação de esquemas TypeScript-first, garantindo que os dados de entrada e saída da API estejam sempre no formato esperado.
-   **SQLite**: Banco de dados leve e serverless, utilizado para persistir os dados da aplicação.

## 🚀 Como Usar

Para configurar e executar a API localmente, siga os passos abaixo:

1.  **Clone o repositório:**
    ```bash
    git clone https://github.com/FelipeFerreiraAmado/api-restaurant.git
    ```
2.  **Navegue até o diretório do projeto:**
    ```bash
    cd api-restaurant
    ```
3.  **Instale as dependências:**
    ```bash
    npm install
    ```
4.  **Execute as migrações do banco de dados:**
    ```bash
    npm run knex migrate:latest
    ```
5.  **Inicie o servidor:**
    ```bash
    npm run dev
    ```

A API estará rodando em `http://localhost:3333`.

## 💡 Funcionalidades e Validações

### Produtos

-   **Listar Produtos**: Retorna todos os produtos disponíveis no cardápio.
-   **Criar Produto**: Adiciona um novo produto ao cardápio.
-   **Atualizar Produto**: Modifica as informações de um produto existente.

### Mesas

-   **Listar Mesas**: Retorna todas as mesas do restaurante.
-   **Listar Mesas Abertas**: Exibe as mesas que estão atualmente em uso.
-   **Listar Mesas Fechadas**: Exibe as mesas que estão disponíveis.
-   **Abrir Mesa**: Altera o status de uma mesa para "aberta".
    -   **Validações**: Impede a abertura de mesas já abertas ou inexistentes.
-   **Fechar Mesa**: Altera o status de uma mesa para "fechada".
    -   **Validações**: Impede o fechamento de mesas já fechadas ou inexistentes.

### Pedidos

-   **Criar Pedido por Mesa**: Adiciona um novo pedido a uma mesa específica.
    -   **Validações**: Impede a criação de pedidos em mesas inexistentes ou fechadas.
-   **Listar Pedidos por Mesa**: Retorna todos os pedidos associados a uma mesa.
-   **Ver Total por Mesa**: Calcula e exibe o valor total dos pedidos de uma mesa.

### Tratamento de Erros

A API foi projetada para lidar com diversos cenários de erro, fornecendo mensagens claras e status HTTP apropriados para situações como:

-   Tentativa de abrir uma mesa já aberta.
-   Tentativa de fechar uma mesa já fechada.
-   Tentativa de operar em uma mesa inexistente.
-   Dados de entrada inválidos (validação com Zod ).

## 🌐 Endpoints da API

*Todos endpoints estão disponíveis para exportação no insomnia pelo arquivo 'requests_insomnia.yaml'*

## 🔮 Melhorias Futuras

-   Implementação de autenticação e autorização (JWT).
-   Adição de um painel administrativo para gerenciamento de produtos, mesas e usuários.
-   Integração com sistemas de pagamento.
-   Testes unitários e de integração mais abrangentes.
-   Documentação da API com Swagger/OpenAPI.

## 🤝 Contribuição

Contribuições são sempre bem-vindas! Se você tem ideias para melhorar este projeto, sinta-se à vontade para:

1.  Fazer um fork do repositório.
2.  Criar uma nova branch (`git checkout -b feature/sua-feature`).
3.  Fazer suas alterações e commit (`git commit -m \'Adiciona nova feature\'`).
4.  Enviar para a branch (`git push origin feature/sua-feature`).
5.  Abrir um Pull Request.

## 📄 Licença

Este projeto está licenciado sob a licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.
