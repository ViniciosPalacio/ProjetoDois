<<<<<<< HEAD
# ProjetoDois
=======
# ⛩️ SRA - Sistema de Rastreamento de Animes

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=for-the-badge&logo=flask&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-07405E?style=for-the-badge&logo=sqlite&logoColor=white)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)

## 📌 Visão Geral do Sistema
O **SRA** é uma aplicação web *Full-Stack* desenvolvida para automatizar o rastreamento e o consumo de mídia de animação. O sistema substitui o controle manual em planilhas ou blocos de notas por uma interface gráfica conectada a um banco de dados relacional local, com enriquecimento de metadados em tempo real via consumo de API REST externa.

## 🏗️ Arquitetura e Stack Tecnológico
O projeto foi estruturado no padrão MVC (Model-View-Controller) simplificado para garantir a separação de responsabilidades:
* **Backend (Controller):** Python operando sob o micro-framework Flask. Lida com o roteamento, lógica de negócio e segurança.
* **Banco de Dados (Model):** SQLite3. Escolhido por ser nativo, *serverless* e garantir integridade de dados via operações ACID durante acessos simultâneos.
* **Integração de Dados (Data Ingestion):** Consumo da [Jikan API v4](https://jikan.moe/) para extração assíncrona de sinopses e capas oficiais.
* **Frontend (View):** HTML5 e CSS3 puro, garantindo uma interface leve e responsiva sem a sobrecarga de *frameworks* de terceiros.

## ⚙️ Funcionalidades Principais (Core Features)
* **Autenticação de Usuários:** Sistema de Login e Registro com isolamento de dados (Sessões). O banco de dados garante que a lista de um usuário não interfira na do outro.
* **CRUD de Mídia:** Criação, leitura, atualização (status de visualização) e exclusão de títulos no banco de dados.
* **Enriquecimento Assíncrono:** Ao cadastrar um título, o *backend* consulta a Jikan API e renderiza os ativos visuais (imagens e sinopse) dinamicamente na *dashboard* do usuário.
* **Tratamento de Rate Limit:** O motor Python possui *delays* estratégicos implementados para respeitar as políticas de requisição da API do MyAnimeList, evitando bloqueios (HTTP 429).

## 🗄️ Modelagem de Dados (MER Físico)
O banco de dados `banco.db` opera com relações bem definidas para evitar redundância:
* `tb_usuarios`: Armazena as credenciais de acesso (`id`, `username`, `senha_hash`).
* `tb_animes`: Armazena as obras monitoradas e o status de visualização, utilizando *Foreign Keys* para vincular a obra ao seu respectivo usuário.

## 🚀 Como Executar o Projeto Localmente

**Pré-requisitos:** No momento não liberarei para instalação
>>>>>>> c4a5a41dce8b9bab3c6b099c8162f1f3bf46653a
