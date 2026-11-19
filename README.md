<h1 align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:0d1117,100:1f6feb&height=170&section=header&text=Thiago%20Moreira&fontColor=ffffff&fontSize=52&animation=fadeIn" alt="Thiago Moreira" width="100%" />
</h1>

<p align="center">
  <strong>Tech Lead · Engenharia de Software com IA · TOTVS Protheus (ADVPL/TLPP)</strong>
</p>

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=18&duration=3200&pause=800&color=58A6FF&center=true&vCenter=true&width=560&lines=AI+Engineering+%7C+LLMs%2C+Agents+%26+MCP;TOTVS+Protheus+%7C+ADVPL+%26+TLPP;TypeScript%2C+Node.js%2C+Angular+%26+Python;Self-hosted+infra%3A+Docker%2C+PostgreSQL%2C+Redis" alt="AI Engineering com LLMs, agentes e MCP; TOTVS Protheus; TypeScript, Node.js, Angular, Python e infraestrutura self-hosted" />
</p>

> **EN TL;DR** — Tech Lead with 10+ years in software engineering, applying generative AI and LLM agents to software delivery with Claude Code and MCP. Background in TOTVS Protheus (ADVPL/TLPP), TypeScript/Node.js, Angular and Python, and I run the infrastructure myself.

---

## 👋 Sobre mim

Tech Lead na Apply System desde março de 2026, com mais de 10 anos em engenharia de software. Antes, TOTVS e Shoebiz (visão computacional com OpenCV). Trajetória completa no [LinkedIn](https://www.linkedin.com/in/tmmoreira93/).

- 🤖 **Engenharia de software com IA generativa** — agentes com LLM, MCP e Claude Code no fluxo de entrega do time (detalhe abaixo).
- 🧭 **Liderança técnica** — defino como o time entrega com agentes: padrão de issue, portões de revisão e CI obrigatório.
- 🔭 **TOTVS Protheus** — ADVPL, TLPP, APIs REST e integrações com o ERP.
- 👨‍💻 **Full-stack** — TypeScript/Node.js e Angular (PO UI) no produto, Python para automação e serviços.
- 🛠 Infra é parte do trabalho, não um detalhe: opero minhas aplicações e bancos em servidores próprios com **Docker, Linux, PostgreSQL, Redis e Caddy**, com Cloudflare na borda.
- 📍 São Paulo – SP · trabalho remoto.
- ⚡ Trilogia favorita: *O Senhor dos Anéis*.

---

## 🧠 IA na entrega, na prática

Um pipeline em que agentes fazem o trabalho repetitivo e as pessoas ficam com as decisões:

| Etapa | O agente faz | Portão |
|---|---|---|
| Issue | lê a issue e o código, com contexto via MCP | só entra na fila com critérios de aceite e label `ready-for-agent` |
| Implementação | trabalha numa worktree isolada, uma branch por issue | não toca a `main` nem outras issues |
| Pull request | abre o PR ligado à issue, com descrição e testes | proteção de branch: sem push direto, sem force push |
| CI | lint, build e testes a cada push | merge só com CI verde e revisão |

O ganho não é velocidade bruta: é chegar à revisão com o contexto montado e o diff pequeno.

Versão aberta e executável, com demo sem chave de API e os modos de falha que encontrei em uso real: **[agent-issue-pipeline](https://github.com/tmoreiradev/agent-issue-pipeline)**. Medi com um benchmark de 20 issues e testes de aceitação ocultos: o gate e o contrato `BLOCKED:` barraram ou escalaram 9 de 9 issues mal especificadas ou impossíveis; com a versão atual da revisão cruzada (Codex) foram 19/20 resultados corretos, 1 aprovação falsa e 0 bloqueios indevidos. A primeira versão do revisor tinha 0 aprovações falsas, mas 3 bloqueios indevidos: o benchmark mostrou que os dois prompts trocaram um tipo de erro pelo outro. Resultados, evidências e limites estão no repo.

---

## 🚀 Projetos

<p align="center">
  <img src="https://www.gitskins.com/api/section/projects?username=tmoreiradev&theme=github-dark&style=aura" alt="Repositórios públicos: protheus-docker, CRUD_rest-tlpp-api, discord-musicbot e pixoo-linear" width="100%" />
</p>

- [agent-issue-pipeline](https://github.com/tmoreiradev/agent-issue-pipeline) — pipeline de agentes de código: gate de especificação, worker isolado, revisão por outro fornecedor, deploy com rollback; benchmark de 20 issues com testes ocultos, demo e CI sem chave de API.
- [rtc-calculadora-mcp](https://github.com/tmoreiradev/rtc-calculadora-mcp) — servidor MCP que expõe a calculadora oficial da Reforma Tributária (CBS/IBS/IS, código aberto da Receita Federal) como ferramentas para agentes; avaliação com 30 cenários fictícios e a própria calculadora como gabarito: o mesmo modelo acertou 71% dos valores sozinho e 100% com o MCP.
- [fiscal-rag-br](https://github.com/tmoreiradev/fiscal-rag-br) — RAG sobre a LC 214/2025, a NT 2025.002-RTC e o manual da NF-e que cita documento, artigo/campo/regra, versão e página, e se abstém fora do corpus; golden set de 69 perguntas anotadas: o reranking leva o trecho certo à 1ª posição em 82% das perguntas (51% com BM25), e o LLM local (Qwen3-4B) cita o trecho certo em 92% das respostas e recusa todas as perguntas de teste fora do corpus; avaliação no CI sem chave de API.
- [protheus-docker](https://github.com/tmoreiradev/protheus-docker) — Protheus (AppServer, DBAccess e License Server) em Docker com PostgreSQL: ambiente de teste reproduzível, sem VM.
- [CRUD_rest-tlpp-api](https://github.com/tmoreiradev/CRUD_rest-tlpp-api) — API REST de clientes (SA1) em TLPP, em camadas.

---

## 🛠 Stack

**IA**

![Claude Code](https://img.shields.io/badge/Claude%20Code-D97757?style=for-the-badge&logo=anthropic&logoColor=white)
![MCP](https://img.shields.io/badge/MCP-000000?style=for-the-badge&logo=modelcontextprotocol&logoColor=white)
![LLM Agents](https://img.shields.io/badge/LLM%20Agents-6E40C9?style=for-the-badge&logoColor=white)

**TOTVS Protheus**

![ADVPL](https://img.shields.io/badge/ADVPL-323330?style=for-the-badge&logoColor=white)
![TLPP](https://img.shields.io/badge/TLPP-1e7a3b?style=for-the-badge&logoColor=white)
![REST API](https://img.shields.io/badge/REST%20API-005AA0?style=for-the-badge&logoColor=white)

**Web & Backend**

![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-5FA04E?style=for-the-badge&logo=nodedotjs&logoColor=white)
![Angular](https://img.shields.io/badge/Angular-DD0031?style=for-the-badge&logo=angular&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)

**Infra & DB**

![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-FF4438?style=for-the-badge&logo=redis&logoColor=white)
![Caddy](https://img.shields.io/badge/Caddy-1F88C0?style=for-the-badge&logo=caddy&logoColor=white)
![Cloudflare](https://img.shields.io/badge/Cloudflare-F38020?style=for-the-badge&logo=cloudflare&logoColor=white)

---

## 📊 Dashboard

<table align="center">
  <tr>
    <td>
      <img src="https://github-readme-stats-jet-three-92.vercel.app/api?username=tmoreiradev&theme=github_dark&show_icons=true&hide_rank=true&hide_border=true&count_private=true&include_all_commits=true" alt="Estatísticas do GitHub: commits, PRs, issues e estrelas" />
    </td>
    <td>
      <img src="https://streak-stats.demolab.com/?user=tmoreiradev&theme=github-dark-blue&hide_border=true" alt="Sequência de dias com contribuições no GitHub" />
    </td>
  </tr>
  <tr>
    <td colspan="2">
      <img src="https://github-readme-stats-jet-three-92.vercel.app/api/top-langs/?username=tmoreiradev&theme=github_dark&hide_border=true&layout=compact&langs_count=8&size_weight=0.5&count_weight=0.5" alt="Distribuição de linguagens nos repositórios analisados" />
    </td>
  </tr>
</table>

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="./profile-3d-contrib/profile-night-view.svg" />
    <img src="./profile-3d-contrib/profile-green.svg" alt="Contribution City: contribuições do último ano em 3D" width="100%" />
  </picture>
</p>

---

## 📬 Vamos conversar

Vamos conversar sobre engenharia de software com IA, agentes com LLM, liderança técnica e TOTVS Protheus. Me chama no LinkedIn ou manda um e-mail. Dúvida técnica: abre uma **[discussion](https://github.com/tmoreiradev/protheus-docker/discussions)** no repositório do projeto, fica registrado e ajuda quem chega depois.

<p>
  <a href="https://www.linkedin.com/in/tmmoreira93/"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
  <a href="mailto:tmmoreira93@gmail.com"><img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" /></a>
</p>

<p align="right">
  <img src="https://komarev.com/ghpvc/?username=tmoreiradev&color=58a6ff&style=flat-square&label=Visitors" alt="Contador de visualizações do perfil" />
</p>
