# Agente Inteligente de Pesquisa de Conteúdos AWS com IA

## Sobre o Projeto

Este projeto implementa um workflow automatizado no n8n que utiliza Inteligência Artificial para pesquisar e responder perguntas com base em conteúdos publicados no blog oficial de segurança da AWS.

O sistema coleta automaticamente novos artigos através de **RSS feeds**, organiza os dados e utiliza um **agente de IA** para gerar respostas baseadas nas informações encontradas.

---

## Problema

Acompanhar atualizações e boas práticas da AWS exige consultar frequentemente blogs técnicos e fontes oficiais.
Esse processo pode ser demorado e exigir a leitura manual de diversos artigos.
Este projeto automatiza esse processo, permitindo que o usuário faça perguntas diretamente e receba respostas baseadas nos conteúdos mais recentes e de fontes oficias AWS.

---

## Como Funciona

Fluxo do sistema:

1. O usuário envia uma pergunta no chat
2. O Chat Trigger inicia o workflow
3. O sistema consulta o RSS Feed do blog da AWS                    ![Workflow n8n](images/n8n-workflow.png)
4. Os artigos são filtrados e organizados
5. O Agente de IA analisa os conteúdos
6. Uma resposta é gerada e enviada ao usuário

---

## Workflow (Nodes Utilizados)

* **Chat Trigger**
  Inicia o workflow quando o usuário envia uma mensagem.

* **AI Agent**
  Interpreta a pergunta e gera respostas usando os dados coletados.

* **RSS Feed Reader**
  Busca automaticamente novos artigos publicados pela AWS.

* **Limit**
  Restringe a quantidade de artigos processados.

* **Aggregate**
  Organiza os dados coletados antes da análise da IA.

---

## Tecnologias Utilizadas

* **n8n** — Automação de workflows
* **RSS Feeds** — Coleta automática de conteúdos
* **LLM / Inteligência Artificial** — Interpretação de perguntas e geração de respostas
* **JSON Workflow** — Estrutura exportada do n8n

---

## Exemplo de Pergunta

Pergunta do usuário:
"Quais são as últimas boas práticas de segurança na AWS?"

O sistema consulta os artigos recentes no feed RSS da AWS e gera uma resposta baseada nesses conteúdos.

---

## Objetivo

Este projeto foi desenvolvido para estudo e portfólio, explorando:

* automação de workflows
* integração com inteligência artificial
* coleta automatizada de conteúdo
* construção de agentes inteligentes

## Arquitetura

![Arquitetura do Sistema](images/arquitetura-workflow.png)

## Workflow no n8n

![Workflow n8n](images/n8n-workflow.png)
