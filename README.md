# Foco Financeiro - Ambiente de Desenvolvimento

Bem-vindo ao ambiente de desenvolvimento do projeto **Foco Financeiro**. Este repositório contém a configuração do Docker Compose necessária para orquestrar e executar o backend, o frontend e o banco de dados do projeto de forma integrada.

## 🚀 Sobre o Projeto

O **Foco Financeiro** é uma aplicação full-stack para gestão de finanças pessoais, permitindo aos usuários registrar e categorizar seus ganhos e custos. Este repositório é o ponto de partida para qualquer desenvolvedor que queira executar o ambiente completo localmente.

## 🛠️ Pré-requisitos

Antes de começar, garanta que você tenha as seguintes ferramentas instaladas na sua máquina:

* [**Git**](https://git-scm.com/)
* [**Docker**](https://www.docker.com/products/docker-desktop/)
* [**Docker Compose**](https://docs.docker.com/compose/install/) (geralmente já vem com o Docker Desktop)

## ⚙️ Configuração do Ambiente

Para configurar o ambiente de desenvolvimento, siga estes passos:

1. **Crie uma pasta de trabalho:**
   ```bash
   mkdir foco-financeiro-workspace
   cd foco-financeiro-workspace
   ```

2. **Clone os três repositórios do projeto:**
   ```bash
   # Clone este repositório (o orquestrador)
   git clone [https://github.com/IgorRocha22/foco-financeiro.git](https://github.com/IgorRocha22/foco-financeiro.git)
   
   # Clone o repositório do Backend
   git clone [https://github.com/IgorRocha22/foco-financeiro-backend.git](https://github.com/IgorRocha22/foco-financeiro-backend.git)
   
   # Clone o repositório do Frontend
   git clone [https://github.com/IgorRocha22/foco-financeiro-frontend.git](https://github.com/IgorRocha22/foco-financeiro-frontend.git)
   ```

3. **Verifique a estrutura de pastas:**
   Ao final, sua pasta `foco-financeiro-workspace` deve ter a seguinte estrutura:
   ```
   foco-financeiro-workspace/
   ├── foco-financeiro/   <-- Você está aqui
   ├── foco-financeiro-backend/
   └── foco-financeiro-frontend/
   ```

## ▶️ Executando a Aplicação

Com a estrutura de pastas correta, o processo é muito simples.

1. **Acesse a pasta do orquestrador:**
   ```bash
   cd foco-financeiro
   ```

2. **Suba os contêineres com o Docker Compose:**
   ```bash
   docker-compose up --build
   ```
   O comando `--build` garante que as imagens Docker serão construídas a partir dos `Dockerfiles` na primeira execução.

## 🔗 Acessando os Serviços

Após os contêineres iniciarem com sucesso, os serviços estarão disponíveis nos seguintes endereços:

* **Frontend (Aplicação Web):** http://localhost:3000
* **Backend (API):** http://localhost:8080/api
* **Banco de Dados (PostgreSQL):** Acessível internamente pelos outros contêineres no host `database` e porta `5432`.

## 📂 Estrutura do Projeto

* **`foco-financeiro`**: Contém este `README` e o `docker-compose.yml`, responsável por unificar os serviços.
* **`foco-financeiro-backend`**: Repositório da API RESTful construída com Java e Spring Boot.
* **`foco-financeiro-frontend`**: Repositório da interface de usuário construída com React.
