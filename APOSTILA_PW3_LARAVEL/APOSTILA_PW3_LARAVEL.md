# Apostila PW3 — Laravel

> **Programação Web III (PW3)** • 2º Ano • Técnico em Desenvolvimento de Sistemas  
> Projeto integrador: **Sistema Web para uma Lanchonete**  
> Aulas de **100 minutos/semana** • **4 bimestres** • **16 capítulos**

Esta apostila organiza o aprendizado em 4 bimestres (16 capítulos), com aulas semanais de 100 minutos, combinando teoria essencial e prática guiada. O projeto integrador será um Sistema Web para uma Lanchonete.

- Semana A: conceitos + iniciar passo a passo
- Semana B: concluir + atividades + revisão
- Git + VS Code + Linux
- MySQL + Migrations/Seeds
- Postman + APIs

> Os capítulos terão: teoria objetiva, passo a passo, atividades propostas, pesquisas e questionário interativo.

## Visão Geral Didática

- Competências: MVC, frameworks, serviços Web, integração mobile.
- Bases: CRUD, validação, auth, i18n, segurança, REST/JSON, SOAP/XML.
- Entregas: 1 por bimestre + entrega final completa.
- Ferramentas: Laravel, Composer, Node/Vite, Docker (opcional), Postman.

## Competências e Habilidades (ao longo do curso)

Desenvolvimento de sistemas multicamadas com framework MVC, construção de serviços Web e integração com recursos de dispositivos (quando aplicável).

- MVC: Models, Views (Blade) e Controllers.
- ORM (Eloquent): mapeamento objeto-relacional e relacionamentos.
- Roteamento: URLs, rotas web e API.
- Templates: layout, partials, componentes Blade.
- Scaffolding: Artisan, geração de estruturas, produtividade.
- Validação e Formulários: Form Requests, UX e mensagens.
- Auth / Autorização: Breeze, middleware, policies e gates.
- Integrações: AJAX, consumo de API pública, Postman.
- Serviços: REST/JSON, XML e SOAP/WSDL.
- Segurança: CSRF/XSS, tokens, rate limit, upload seguro.
- i18n: internacionalização e acessibilidade básica.

## Projeto Integrador: Sistema de Lanchonete

O projeto evolui durante o ano: catálogo → pedidos → APIs → segurança/qualidade.

- **Catálogo** — Categorias e produtos (CRUD, validação, imagens, busca/paginação).
- **Pedidos** — Fluxo de pedido e itens (relacionamentos, status, total, regras).
- **Integrações e Serviços** — AJAX, consumo de API pública (ex.: ViaCEP), REST/JSON, XML, SOAP.
- **Segurança e Qualidade** — Sanctum, policies, rate limit, logs, i18n, performance e deploy.

## Sumário

- [Visão Geral Didática](#visão-geral-didática)
- [Competências e Habilidades (ao longo do curso)](#competências-e-habilidades-ao-longo-do-curso)
- [Projeto Integrador: Sistema de Lanchonete](#projeto-integrador-sistema-de-lanchonete)
- [Planejamento por Bimestre (entregas)](#planejamento-por-bimestre-entregas)
  - [1º Bimestre — Fundamentos de MVC (Laravel) e CRUD com Validação](#1º-bimestre--fundamentos-de-mvc-laravel-e-crud-com-validação)
  - [2º Bimestre — Autenticação/Autorização, Relacionamentos e Integração AJAX & API Pública](#2º-bimestre--autenticaçãoautorização-relacionamentos-e-integração-ajax--api-pública)
  - [3º Bimestre — Serviços para Web: REST/JSON, SOAP/WSDL/XML e Segurança de API](#3º-bimestre--serviços-para-web-restjson-soapwsdlxml-e-segurança-de-api)
  - [4º Bimestre — i18n, Autorização Avançada, Qualidade/Desempenho e Empacotamento](#4º-bimestre--i18n-autorização-avançada-qualidadedesempenho-e-empacotamento)
- [Capítulo 01 — Arquitetura Web (HTTP & MVC) e Setup do Projeto Laravel (Lanchonete)](#capítulo-01--arquitetura-web-http--mvc-e-setup-do-projeto-laravel-lanchonete)
  - [1) Objetivos de aprendizagem](#1-objetivos-de-aprendizagem)
  - [2) Pré-requisitos e ferramentas](#2-pré-requisitos-e-ferramentas)
  - [3) Conteúdo teórico](#3-conteúdo-teórico)
    - [3.1. HTTP em linhas claras](#31-http-em-linhas-claras)
    - [3.2. MVC (Model–View–Controller) na prática](#32-mvc-modelviewcontroller-na-prática)
    - [3.3. O que o Laravel organiza para você](#33-o-que-o-laravel-organiza-para-você)
  - [4) Passo a passo guiado (Projeto Lanchonete)](#4-passo-a-passo-guiado-projeto-lanchonete)
    - [4.1. Preparar o banco de dados (MySQL)](#41-preparar-o-banco-de-dados-mysql)
    - [4.2. Criar o projeto Laravel](#42-criar-o-projeto-laravel)
    - [4.3. Configurar o .env](#43-configurar-o-env)
    - [4.4. Subir o servidor de desenvolvimento](#44-subir-o-servidor-de-desenvolvimento)
    - [4.5. Rotas, Controller e View iniciais](#45-rotas-controller-e-view-iniciais)
    - [4.6. Iniciar controle de versão (Git)](#46-iniciar-controle-de-versão-git)
  - [5) Atividades correlatas (para a Semana B)](#5-atividades-correlatas-para-a-semana-b)
  - [6) Pesquisas complementares (para aprofundar)](#6-pesquisas-complementares-para-aprofundar)
  - [9) Entregáveis do capítulo](#9-entregáveis-do-capítulo)
- [Capítulo 02 — Modelagem, Migrations, Seeders & Eloquent (CRUD de Categoria)](#capítulo-02--modelagem-migrations-seeders--eloquent-crud-de-categoria)
  - [1) Objetivos de aprendizagem](#1-objetivos-de-aprendizagem-1)
  - [2) Pré-requisitos e ferramentas](#2-pré-requisitos-e-ferramentas-1)
  - [3) Conteúdo teórico](#3-conteúdo-teórico-1)
    - [3.1. Modelagem de dados (visão prática)](#31-modelagem-de-dados-visão-prática)
    - [3.2. Migrations, Seeders e Factories](#32-migrations-seeders-e-factories)
    - [3.3. Eloquent ORM](#33-eloquent-orm)
    - [3.4. Resource Controllers & Views](#34-resource-controllers--views)
  - [4) Passo a passo guiado — CRUD de Categoria](#4-passo-a-passo-guiado--crud-de-categoria)
    - [4.1. Criar Models, Migration, Factory, Seeder e Controller](#41-criar-models-migration-factory-seeder-e-controller)
    - [4.2. Definir migrations](#42-definir-migrations)
    - [4.3. Modelos Eloquent](#43-modelos-eloquent)
    - [4.4. Factories e Seeders](#44-factories-e-seeders)
    - [4.5. Rotas (resource) e Controller](#45-rotas-resource-e-controller)
    - [4.6. Views Blade (index, create, edit e parcial _form)](#46-views-blade-index-create-edit-e-parcial-_form)
  - [5) Atividades correlatas (para a Semana B)](#5-atividades-correlatas-para-a-semana-b-1)
  - [6) Pesquisas complementares (para aprofundar)](#6-pesquisas-complementares-para-aprofundar-1)
  - [9) Entregáveis do capítulo](#9-entregáveis-do-capítulo-1)
- [Capítulo 03 — Blade, Formulários, Validação e Mensagens](#capítulo-03--blade-formulários-validação-e-mensagens)
  - [1) Objetivos de aprendizagem](#1-objetivos-de-aprendizagem-2)
  - [2) Pré-requisitos e ferramentas](#2-pré-requisitos-e-ferramentas-2)
  - [3) Conteúdo teórico](#3-conteúdo-teórico-2)
    - [3.1. CSRF (Cross-Site Request Forgery)](#31-csrf-cross-site-request-forgery)
    - [3.2. Validação no Laravel (inline vs Form Request)](#32-validação-no-laravel-inline-vs-form-request)
    - [3.3. Mensagens ao usuário (sucesso/erro) e UX](#33-mensagens-ao-usuário-sucessoerro-e-ux)
    - [3.4. Blade na prática (diretivas e partials)](#34-blade-na-prática-diretivas-e-partials)
  - [4) Passo a passo guiado (Projeto Lanchonete)](#4-passo-a-passo-guiado-projeto-lanchonete-1)
    - [4.1. Criar o Form Request (CategoriaRequest)](#41-criar-o-form-request-categoriarequest)
    - [4.2. Atualizar o Controller para usar Form Request](#42-atualizar-o-controller-para-usar-form-request)
    - [4.3. Melhorar o partial de alertas (sucesso/erro/validação)](#43-melhorar-o-partial-de-alertas-sucessoerrovalidação)
    - [4.4. Preservar valores e exibir erros por campo (old() e @error)](#44-preservar-valores-e-exibir-erros-por-campo-old-e-error)
    - [4.5. Teste de validação (erros e sucesso)](#45-teste-de-validação-erros-e-sucesso)
    - [4.6. Commit no Git](#46-commit-no-git)
  - [5) Atividades correlatas (para a Semana B)](#5-atividades-correlatas-para-a-semana-b-2)
  - [6) Pesquisas complementares (para aprofundar)](#6-pesquisas-complementares-para-aprofundar-2)
  - [9) Entregáveis do capítulo](#9-entregáveis-do-capítulo-2)
- [Capítulo 04 — Listagens, Paginação, Busca e Segurança Básica (CSRF/XSS)](#capítulo-04--listagens-paginação-busca-e-segurança-básica-csrfxss)
  - [1) Objetivos de aprendizagem](#1-objetivos-de-aprendizagem-3)
  - [2) Pré-requisitos e ferramentas](#2-pré-requisitos-e-ferramentas-3)
  - [3) Conteúdo teórico](#3-conteúdo-teórico-3)
    - [3.1. Paginação (por que e como)](#31-paginação-por-que-e-como)
    - [3.2. Busca e filtros por query string](#32-busca-e-filtros-por-query-string)
    - [3.3. Segurança básica na entrada e na saída](#33-segurança-básica-na-entrada-e-na-saída)
  - [4) Passo a passo guiado (Projeto Lanchonete)](#4-passo-a-passo-guiado-projeto-lanchonete-2)
    - [4.1. Ajustar o Controller de Categorias para paginar e buscar](#41-ajustar-o-controller-de-categorias-para-paginar-e-buscar)
    - [4.2. Ajustar a View de Categorias: formulário de busca + links de paginação](#42-ajustar-a-view-de-categorias-formulário-de-busca--links-de-paginação)
    - [4.3. Preparar Produtos: paginação + busca + filtro por categoria (base)](#43-preparar-produtos-paginação--busca--filtro-por-categoria-base)
    - [4.4. Segurança básica: revisar CSRF e escaping no Blade](#44-segurança-básica-revisar-csrf-e-escaping-no-blade)
    - [4.5. Commit no Git](#45-commit-no-git)
  - [5) Atividades correlatas (para a Semana B)](#5-atividades-correlatas-para-a-semana-b-3)
  - [6) Pesquisas complementares (para aprofundar)](#6-pesquisas-complementares-para-aprofundar-3)
  - [9) Entregáveis do capítulo](#9-entregáveis-do-capítulo-3)
  - [Entrega Bimestral (B1) — Catálogo da Lanchonete](#entrega-bimestral-b1--catálogo-da-lanchonete)
- [Capítulo 05 — Autenticação manual, Sessão e Perfis](#capítulo-05--autenticação-manual-sessão-e-perfis)
  - [1) Objetivos de aprendizagem](#1-objetivos-de-aprendizagem-4)
  - [2) Pré-requisitos e ferramentas](#2-pré-requisitos-e-ferramentas-4)
  - [3) Conteúdo teórico](#3-conteúdo-teórico-4)
    - [3.1. Autenticação x autorização](#31-autenticação-x-autorização)
    - [3.2. Sessão e middlewares](#32-sessão-e-middlewares)
    - [3.3. Autenticação manual com Laravel + Blade](#33-autenticação-manual-com-laravel--blade)
    - [3.4. Perfis (roles) e controle de acesso](#34-perfis-roles-e-controle-de-acesso)
  - [4) Passo a passo guiado (Projeto Lanchonete)](#4-passo-a-passo-guiado-projeto-lanchonete-3)
    - [4.1. Preparar o banco e a tabela de sessão (se necessário)](#41-preparar-o-banco-e-a-tabela-de-sessão-se-necessário)
    - [4.2. Criar a coluna role (perfil) na tabela users](#42-criar-a-coluna-role-perfil-na-tabela-users)
    - [4.3. Atualizar o Model User](#43-atualizar-o-model-user)
    - [4.4. Criar o controller da autenticação manual](#44-criar-o-controller-da-autenticação-manual)
    - [4.5. Criar as rotas de registro, login e logout](#45-criar-as-rotas-de-registro-login-e-logout)
    - [4.6. Criar as views Blade de autenticação](#46-criar-as-views-blade-de-autenticação)
    - [4.7. Criar uma dashboard simples e testar o fluxo](#47-criar-uma-dashboard-simples-e-testar-o-fluxo)
    - [4.8. Ajustar a navbar com @auth, @guest e logout](#48-ajustar-a-navbar-com-auth-guest-e-logout)
    - [4.9. Definir um usuário gerente e restringir Categorias](#49-definir-um-usuário-gerente-e-restringir-categorias)
    - [4.10. Commit no Git](#410-commit-no-git)
  - [5) Atividades correlatas (para a Semana B)](#5-atividades-correlatas-para-a-semana-b-4)
  - [6) Pesquisas complementares (para aprofundar)](#6-pesquisas-complementares-para-aprofundar-4)
  - [9) Entregáveis do capítulo](#9-entregáveis-do-capítulo-4)
- [Capítulo 06 — Relacionamentos Eloquent e Fluxo de Pedido](#capítulo-06--relacionamentos-eloquent-e-fluxo-de-pedido)
  - [1) Objetivos de aprendizagem](#1-objetivos-de-aprendizagem-5)
  - [2) Pré-requisitos e ferramentas](#2-pré-requisitos-e-ferramentas-5)
  - [3) Conteúdo teórico](#3-conteúdo-teórico-5)
    - [3.1. Relacionamentos Eloquent (1:N na prática)](#31-relacionamentos-eloquent-1n-na-prática)
    - [3.2. Regras de negócio e consistência](#32-regras-de-negócio-e-consistência)
    - [3.3. Eager loading e o problema N+1](#33-eager-loading-e-o-problema-n1)
  - [4) Passo a passo guiado — Fluxo de Pedido (sem AJAX ainda)](#4-passo-a-passo-guiado--fluxo-de-pedido-sem-ajax-ainda)
    - [4.1. Criar Models e Migrations](#41-criar-models-e-migrations)
    - [4.2. Migrations: pedidos e itens_pedido](#42-migrations-pedidos-e-itens_pedido)
    - [4.3. Models Eloquent: relações](#43-models-eloquent-relações)
    - [4.4. Rotas: Pedido resource + rotas para itens](#44-rotas-pedido-resource--rotas-para-itens)
    - [4.5. PedidoController: criar pedido e editar para adicionar itens](#45-pedidocontroller-criar-pedido-e-editar-para-adicionar-itens)
    - [4.6. ItemPedidoController: adicionar e remover itens + recalcular total](#46-itempedidocontroller-adicionar-e-remover-itens--recalcular-total)
    - [4.7. Views Blade (index, create, edit)](#47-views-blade-index-create-edit)
    - [4.8. Link no menu para Pedidos](#48-link-no-menu-para-pedidos)
    - [4.9. Commit no Git](#49-commit-no-git)
  - [5) Atividades correlatas (para a Semana B)](#5-atividades-correlatas-para-a-semana-b-5)
  - [6) Pesquisas complementares (para aprofundar)](#6-pesquisas-complementares-para-aprofundar-5)
  - [9) Entregáveis do capítulo](#9-entregáveis-do-capítulo-5)
- [Capítulo 07 — Requisições Assíncronas (AJAX) no Laravel/Blade](#capítulo-07--requisições-assíncronas-ajax-no-laravelblade)
  - [1) Objetivos de aprendizagem](#1-objetivos-de-aprendizagem-6)
  - [2) Pré-requisitos e ferramentas](#2-pré-requisitos-e-ferramentas-6)
  - [3) Conteúdo teórico](#3-conteúdo-teórico-6)
    - [3.1. O que é AJAX (moderno)](#31-o-que-é-ajax-moderno)
    - [3.2. JSON, headers e códigos de status](#32-json-headers-e-códigos-de-status)
    - [3.3. CSRF em requisições AJAX](#33-csrf-em-requisições-ajax)
  - [4) Passo a passo guiado — Pedido com AJAX (fetch + JSON)](#4-passo-a-passo-guiado--pedido-com-ajax-fetch--json)
    - [4.1. Inserir CSRF token no layout (meta)](#41-inserir-csrf-token-no-layout-meta)
    - [4.2. Criar rotas JSON para itens do pedido](#42-criar-rotas-json-para-itens-do-pedido)
    - [4.3. Implementar métodos JSON no ItemPedidoController](#43-implementar-métodos-json-no-itempedidocontroller)
    - [4.4. Atualizar a view do pedido para enviar via fetch](#44-atualizar-a-view-do-pedido-para-enviar-via-fetch)
    - [4.5. Ajuste mínimo na tabela para suportar atualização dinâmica](#45-ajuste-mínimo-na-tabela-para-suportar-atualização-dinâmica)
    - [4.6. Commit no Git](#46-commit-no-git-1)
  - [5) Atividades correlatas (para a Semana B)](#5-atividades-correlatas-para-a-semana-b-6)
  - [6) Pesquisas complementares (para aprofundar)](#6-pesquisas-complementares-para-aprofundar-6)
  - [9) Entregáveis do capítulo](#9-entregáveis-do-capítulo-6)
- [Capítulo 08 — Consumindo APIs Públicas + Postman](#capítulo-08--consumindo-apis-públicas--postman)
  - [1) Objetivos de aprendizagem](#1-objetivos-de-aprendizagem-7)
  - [2) Pré-requisitos e ferramentas](#2-pré-requisitos-e-ferramentas-7)
  - [3) Conteúdo teórico](#3-conteúdo-teórico-7)
    - [3.1. Consumindo APIs públicas com responsabilidade](#31-consumindo-apis-públicas-com-responsabilidade)
    - [3.2. Timeouts e tratamento de erro](#32-timeouts-e-tratamento-de-erro)
    - [3.3. Cache: reduzindo chamadas repetidas](#33-cache-reduzindo-chamadas-repetidas)
    - [3.4. Postman: testar, documentar e automatizar](#34-postman-testar-documentar-e-automatizar)
  - [4) Passo a passo guiado — ViaCEP + Cache + Postman](#4-passo-a-passo-guiado--viacep--cache--postman)
    - [4.1. Criar rota e controller para consulta de CEP](#41-criar-rota-e-controller-para-consulta-de-cep)
    - [4.2. Implementar consumo da API ViaCEP com Http + timeout + cache](#42-implementar-consumo-da-api-viacep-com-http--timeout--cache)
    - [4.3. Criar campos de entrega no pedido (exemplo simples)](#43-criar-campos-de-entrega-no-pedido-exemplo-simples)
    - [4.4. Front-end: buscar CEP via fetch e autopreencher](#44-front-end-buscar-cep-via-fetch-e-autopreencher)
    - [4.5. Testar com Postman (coleção e ambiente)](#45-testar-com-postman-coleção-e-ambiente)
    - [4.6. Commit no Git](#46-commit-no-git-2)
  - [5) Atividades correlatas (para a Semana B)](#5-atividades-correlatas-para-a-semana-b-7)
  - [6) Pesquisas complementares (para aprofundar)](#6-pesquisas-complementares-para-aprofundar-7)
  - [9) Entregáveis do capítulo](#9-entregáveis-do-capítulo-7)
- [Capítulo 09 — API REST (api.php), Resources e Autenticação por Token (Sanctum)](#capítulo-09--api-rest-apiphp-resources-e-autenticação-por-token-sanctum)
  - [1) Objetivos de aprendizagem](#1-objetivos-de-aprendizagem-8)
  - [2) Pré-requisitos e ferramentas](#2-pré-requisitos-e-ferramentas-8)
  - [3) Conteúdo teórico](#3-conteúdo-teórico-8)
    - [3.1. REST: recursos e verbos HTTP](#31-rest-recursos-e-verbos-http)
    - [3.2. Status HTTP e “contratos” de API](#32-status-http-e-contratos-de-api)
    - [3.3. Versionamento e padronização de respostas](#33-versionamento-e-padronização-de-respostas)
  - [4) Passo a passo — API de Produtos + Token (Sanctum)](#4-passo-a-passo--api-de-produtos--token-sanctum)
    - [4.1. Instalar e configurar Sanctum](#41-instalar-e-configurar-sanctum)
    - [4.2. Criar um endpoint de login para gerar token](#42-criar-um-endpoint-de-login-para-gerar-token)
    - [4.3. Criar ApiResource para Produto](#43-criar-apiresource-para-produto)
    - [4.4. Criar controlador de API para Produtos](#44-criar-controlador-de-api-para-produtos)
    - [4.5. Rotas em routes/api.php (protegidas por Sanctum)](#45-rotas-em-routesapiphp-protegidas-por-sanctum)
    - [4.6. Testes no Postman (passo a passo)](#46-testes-no-postman-passo-a-passo)
    - [4.7. Commit no Git](#47-commit-no-git)
  - [5) Atividades correlatas](#5-atividades-correlatas)
  - [6) Pesquisas complementares](#6-pesquisas-complementares)
  - [9) Entregáveis](#9-entregáveis)
- [Capítulo 10 — Padronização de API: filtros, ordenação, paginação, rate limit e documentação](#capítulo-10--padronização-de-api-filtros-ordenação-paginação-rate-limit-e-documentação)
  - [1) Objetivos de aprendizagem](#1-objetivos-de-aprendizagem-9)
  - [2) Pré-requisitos e ferramentas](#2-pré-requisitos-e-ferramentas-9)
  - [3) Conteúdo teórico](#3-conteúdo-teórico-9)
    - [3.1. Contrato de API e compatibilidade](#31-contrato-de-api-e-compatibilidade)
    - [3.2. Filtros, ordenação e segurança](#32-filtros-ordenação-e-segurança)
    - [3.3. Paginação e performance](#33-paginação-e-performance)
    - [3.4. Rate limiting e proteção contra abuso](#34-rate-limiting-e-proteção-contra-abuso)
    - [3.5. Documentação (OpenAPI/Swagger) e coleções Postman](#35-documentação-openapiswagger-e-coleções-postman)
  - [4) Passo a passo guiado](#4-passo-a-passo-guiado)
    - [4.1. Adicionar filtros e busca no endpoint GET /api/produtos](#41-adicionar-filtros-e-busca-no-endpoint-get-apiprodutos)
    - [4.2. Documentar parâmetros aceitos (exemplo rápido)](#42-documentar-parâmetros-aceitos-exemplo-rápido)
    - [4.3. Adicionar rate limit (throttle) nas rotas de API](#43-adicionar-rate-limit-throttle-nas-rotas-de-api)
    - [4.4. Criar uma especificação OpenAPI mínima (arquivo YAML)](#44-criar-uma-especificação-openapi-mínima-arquivo-yaml)
    - [4.5. Testar no Postman](#45-testar-no-postman)
    - [4.6. Commit no Git](#46-commit-no-git-3)
  - [5) Atividades correlatas](#5-atividades-correlatas-1)
  - [6) Pesquisas complementares](#6-pesquisas-complementares-1)
  - [9) Entregáveis](#9-entregáveis-1)
- [Capítulo 11 — Testes Automatizados (PHPUnit/Pest), Factories/Seeders e Qualidade](#capítulo-11--testes-automatizados-phpunitpest-factoriesseeders-e-qualidade)
  - [1) Objetivos de aprendizagem](#1-objetivos-de-aprendizagem-10)
  - [2) Pré-requisitos e ferramentas](#2-pré-requisitos-e-ferramentas-10)
  - [3) Conteúdo teórico](#3-conteúdo-teórico-10)
    - [3.1. Testes Unit x Feature (e onde cada um faz sentido)](#31-testes-unit-x-feature-e-onde-cada-um-faz-sentido)
    - [3.2. Por que testar? (valor prático e “documentação viva”)](#32-por-que-testar-valor-prático-e-documentação-viva)
    - [3.3. Dados de teste: Factories, Seeders e RefreshDatabase](#33-dados-de-teste-factories-seeders-e-refreshdatabase)
    - [3.4. Testando APIs protegidas com Sanctum (Sanctum::actingAs)](#34-testando-apis-protegidas-com-sanctum-sanctumactingas)
  - [4) Passo a passo guiado](#4-passo-a-passo-guiado-1)
    - [4.1. Rodar testes no Laravel](#41-rodar-testes-no-laravel)
    - [4.2. Criar factories (Categoria e Produto)](#42-criar-factories-categoria-e-produto)
    - [4.3. Criar teste Feature para a API de Produtos](#43-criar-teste-feature-para-a-api-de-produtos)
    - [4.4. (Opcional) Instalar Pest](#44-opcional-instalar-pest)
    - [4.5. Seed de dados para demo (não confundir com testes)](#45-seed-de-dados-para-demo-não-confundir-com-testes)
    - [4.6. Rodar testes e commitar](#46-rodar-testes-e-commitar)
  - [5) Atividades correlatas (Semana B)](#5-atividades-correlatas-semana-b)
  - [6) Pesquisas complementares](#6-pesquisas-complementares-2)
  - [9) Entregáveis do capítulo](#9-entregáveis-do-capítulo-8)
- [Capítulo 12 — Consumindo sua própria API: Cliente JS, CORS e tokens (Sanctum)](#capítulo-12--consumindo-sua-própria-api-cliente-js-cors-e-tokens-sanctum)
  - [1) Objetivos](#1-objetivos)
  - [2) Pré-requisitos](#2-pré-requisitos)
  - [3) Teoria (CORS e Tokens)](#3-teoria-cors-e-tokens)
    - [3.1. O que é CORS? (origem, navegador e preflight)](#31-o-que-é-cors-origem-navegador-e-preflight)
    - [3.2. Tokens Bearer (Sanctum) e diferença para sessão](#32-tokens-bearer-sanctum-e-diferença-para-sessão)
    - [3.3. Armazenamento do token (localStorage, riscos e alternativas)](#33-armazenamento-do-token-localstorage-riscos-e-alternativas)
    - [3.4. Boas práticas de cliente JS (fetch): headers, erros e UX](#34-boas-práticas-de-cliente-js-fetch-headers-erros-e-ux)
  - [4) Passo a passo — Mini cliente consumindo a API](#4-passo-a-passo--mini-cliente-consumindo-a-api)
    - [4.1. Configurar CORS no Laravel](#41-configurar-cors-no-laravel)
    - [4.2. Criar um mini cliente (arquivo HTML)](#42-criar-um-mini-cliente-arquivo-html)
    - [4.3. Implementar app.js (fetch + Bearer)](#43-implementar-appjs-fetch--bearer)
    - [4.4. Testar no navegador](#44-testar-no-navegador)
    - [4.5. Commit no Git](#45-commit-no-git-1)
  - [5) Atividades correlatas](#5-atividades-correlatas-2)
  - [6) Pesquisas complementares](#6-pesquisas-complementares-3)
  - [9) Entregáveis](#9-entregáveis-2)
- [Capítulo 13 — Deploy de Aplicação Laravel (Produção)](#capítulo-13--deploy-de-aplicação-laravel-produção)
  - [1) Objetivos](#1-objetivos-1)
  - [2) Pré-requisitos](#2-pré-requisitos-1)
  - [3) Teoria (produção)](#3-teoria-produção)
    - [3.1. O que muda em produção? (mentalidade e configurações essenciais)](#31-o-que-muda-em-produção-mentalidade-e-configurações-essenciais)
    - [3.2. Erros comuns de deploy (e por que eles acontecem)](#32-erros-comuns-de-deploy-e-por-que-eles-acontecem)
    - [3.3. Operação em produção: logs, filas, cache e tarefas agendadas](#33-operação-em-produção-logs-filas-cache-e-tarefas-agendadas)
    - [3.4. Segurança básica em produção (o que não pode faltar)](#34-segurança-básica-em-produção-o-que-não-pode-faltar)
  - [4) Passo a passo — Deploy (VPS com Nginx)](#4-passo-a-passo--deploy-vps-com-nginx)
    - [4.1. Preparar servidor (pacotes essenciais)](#41-preparar-servidor-pacotes-essenciais)
    - [4.2. Clonar o projeto e instalar dependências](#42-clonar-o-projeto-e-instalar-dependências)
    - [4.3. Configurar .env de produção](#43-configurar-env-de-produção)
    - [4.4. Migrations, storage e caches](#44-migrations-storage-e-caches)
    - [4.5. Permissões (storage e cache)](#45-permissões-storage-e-cache)
    - [4.6. Configurar Nginx (server block)](#46-configurar-nginx-server-block)
    - [4.7. Filas/cron (opcional, mas recomendado)](#47-filascron-opcional-mas-recomendado)
    - [4.8. Checklist de “deploy” rápido (script mental)](#48-checklist-de-deploy-rápido-script-mental)
    - [4.9. Commit no Git](#49-commit-no-git-1)
  - [5) Atividades correlatas](#5-atividades-correlatas-3)
  - [6) Pesquisas complementares](#6-pesquisas-complementares-4)
  - [9) Entregáveis](#9-entregáveis-3)
- [Capítulo 14 — Observabilidade e Segurança em Produção](#capítulo-14--observabilidade-e-segurança-em-produção)
  - [1) Objetivos de aprendizagem](#1-objetivos-de-aprendizagem-11)
  - [2) Pré-requisitos](#2-pré-requisitos-2)
  - [3) Conteúdo teórico — Observabilidade](#3-conteúdo-teórico--observabilidade)
    - [3.1. O que é observabilidade? (logs, métricas e traces na prática)](#31-o-que-é-observabilidade-logs-métricas-e-traces-na-prática)
    - [3.2. Logs úteis: o que registrar (e o que NÃO registrar)](#32-logs-úteis-o-que-registrar-e-o-que-não-registrar)
    - [3.3. Health-check e monitoramento: detectar queda antes do usuário reclamar](#33-health-check-e-monitoramento-detectar-queda-antes-do-usuário-reclamar)
    - [3.4. Segurança em produção (mínimo essencial) e hardening](#34-segurança-em-produção-mínimo-essencial-e-hardening)
  - [4) Passo a passo — Logs, Health-check, HTTPS e Backups](#4-passo-a-passo--logs-health-check-https-e-backups)
    - [4.1. Criar rota de health-check](#41-criar-rota-de-health-check)
    - [4.2. Logs: onde olhar e como configurar](#42-logs-onde-olhar-e-como-configurar)
    - [4.3. Monitoramento básico (uptime) com health-check](#43-monitoramento-básico-uptime-com-health-check)
    - [4.4. HTTPS com Certbot (Nginx)](#44-https-com-certbot-nginx)
    - [4.5. Hardening: headers básicos no Nginx](#45-hardening-headers-básicos-no-nginx)
    - [4.6. Backup do banco + storage (rotina simples)](#46-backup-do-banco--storage-rotina-simples)
    - [4.7. Testar restore (muito importante)](#47-testar-restore-muito-importante)
    - [4.8. Commit no Git](#48-commit-no-git)
  - [5) Atividades correlatas](#5-atividades-correlatas-4)
  - [6) Pesquisas complementares](#6-pesquisas-complementares-5)
  - [9) Entregáveis](#9-entregáveis-4)
- [Capítulo 15 — CI/CD e Automação (GitHub Actions): testes, qualidade e deploy (opcional)](#capítulo-15--cicd-e-automação-github-actions-testes-qualidade-e-deploy-opcional)
  - [1) Objetivos](#1-objetivos-2)
  - [2) Pré-requisitos](#2-pré-requisitos-3)
  - [3) Teoria (CI x CD, branches e secrets)](#3-teoria-ci-x-cd-branches-e-secrets)
    - [3.1. CI vs CD (e por que isso reduz erro humano)](#31-ci-vs-cd-e-por-que-isso-reduz-erro-humano)
    - [3.2. Branches, Pull Requests e “branch protection”](#32-branches-pull-requests-e-branch-protection)
    - [3.3. Secrets e princípio do menor privilégio (segurança no pipeline)](#33-secrets-e-princípio-do-menor-privilégio-segurança-no-pipeline)
    - [3.4. O que vale automatizar no pipeline (qualidade e saúde do projeto)](#34-o-que-vale-automatizar-no-pipeline-qualidade-e-saúde-do-projeto)
  - [4) Passo a passo — Workflow de CI + Deploy (opcional)](#4-passo-a-passo--workflow-de-ci--deploy-opcional)
    - [4.1. Criar workflow de CI (GitHub Actions)](#41-criar-workflow-de-ci-github-actions)
    - [4.2. Proteger a branch main (recomendado)](#42-proteger-a-branch-main-recomendado)
    - [4.3. (Opcional) Workflow de deploy via SSH](#43-opcional-workflow-de-deploy-via-ssh)
    - [4.4. Salvar Secrets no GitHub](#44-salvar-secrets-no-github)
    - [4.5. Commit no Git](#45-commit-no-git-2)
  - [5) Atividades correlatas](#5-atividades-correlatas-5)
  - [6) Pesquisas complementares](#6-pesquisas-complementares-6)
  - [9) Entregáveis](#9-entregáveis-5)
- [Capítulo 16 — Projeto Final e Apresentação](#capítulo-16--projeto-final-e-apresentação)
  - [1) Objetivos do projeto final](#1-objetivos-do-projeto-final)
  - [2) Escopo mínimo obrigatório](#2-escopo-mínimo-obrigatório)
  - [3) Critérios de avaliação (rubrica sugerida)](#3-critérios-de-avaliação-rubrica-sugerida)
  - [4) Roteiro de apresentação (5–8 minutos)](#4-roteiro-de-apresentação-58-minutos)
  - [5) Validação final (plano rápido de testes)](#5-validação-final-plano-rápido-de-testes)
  - [6) Entregáveis e evidências](#6-entregáveis-e-evidências)
  - [9) Encerramento e próximos passos](#9-encerramento-e-próximos-passos)

## Planejamento por Bimestre (entregas)

### 1º Bimestre — Fundamentos de MVC (Laravel) e CRUD com Validação

- **01. Visão Geral da Arquitetura Web e Setup do Projeto** — HTTP, request/response, estado vs stateless, MVC, setup Laravel + MySQL, layout base com Blade.
- **02. Modelagem, Migrations, Seeders & Eloquent (CRUD Categoria)** — Entidades, migrations/seeders, Eloquent básico, relacionamento (visão) e primeiro CRUD completo.
- **03. Blade, Formulários, Validação e Mensagens** — CSRF, Form Requests, mensagens amigáveis, UX básica e preservação de dados (old()).
- **04. Listagens, Paginação, Busca e Segurança Básica** — Paginação, filtros, busca, escaping no Blade, CSRF/XSS e noções de SQLi.

- **Entrega Bimestral (B1):** Catálogo da Lanchonete com CRUDs de Categoria/Produto, validação, imagem, paginação/busca e README.

### 2º Bimestre — Autenticação/Autorização, Relacionamentos e Integração AJAX & API Pública

- **05. Autenticação (Breeze), Sessão e Perfis** — Login/registro, middleware auth, sessão e roles (Gerente/Atendente).
- **06. Relacionamentos Eloquent e Fluxo de Pedido** — 1:N e N:N, pedidos e itens, regras iniciais e persistência completa.
- **07. Requisições Assíncronas (AJAX) no Laravel/Blade** — fetch/Axios, respostas JSON, atualização sem recarregar, códigos de status.
- **08. Consumindo APIs Públicas + Postman** — Integração com API pública (ex.: ViaCEP), tratamento de erros e coleção no Postman.

- **Entrega Bimestral (B2):** Fluxo de pedidos com AJAX + integração com API pública + coleção Postman com exemplos.

### 3º Bimestre — Serviços para Web: REST/JSON, SOAP/WSDL/XML e Segurança de API

- **09. Expondo uma REST API (stateless) para a Lanchonete** — REST, rotas api.php, API Resources, versionamento e CORS.
- **10. Padrões de Transferência: JSON e XML** — JSON vs XML, content negotiation (Accept), serialização e exportações.
- **11. SOAP/WSDL — Consumo e Exposição (com estado)** — SOAP, WSDL, SoapClient/SoapServer, diferenças para REST e sessão.
- **12. Segurança de API e Observabilidade** — Sanctum (tokens), rate limiting, padrão de erros e logs com contexto.

- **Entrega Bimestral (B3):** API v1 segura com tokens, rate limit, logs e documentação (coleção Postman atualizada).

### 4º Bimestre — i18n, Autorização Avançada, Qualidade/Desempenho e Empacotamento

- **13. Internacionalização (i18n) e Acessibilidade Básica** — resources/lang, locale, pluralização, boas práticas e acessibilidade essencial.
- **14. Autorização Fina (Policies/Gates) e Segurança** — Policies, gates, defesa em camadas, mass assignment e upload seguro.
- **15. Qualidade, Desempenho e Manutenção** — N+1, eager loading, cache simples, organização em serviços e comandos Artisan.
- **16. Empacotamento, Deploy e Fechamento (opcional PWA)** — .env, build Vite, scripts de migração/seed, Docker (opcional), backup e PWA leve.

- **Entrega Final do Curso:** Sistema completo da Lanchonete com catálogo, pedidos, autorização, API v1 (JSON/XML) segura, i18n e documentação (README + Postman + manual do usuário).

---

## Capítulo 01 — Arquitetura Web (HTTP & MVC) e Setup do Projeto Laravel (Lanchonete)

**Carga horária:** 2 semanas (100 min/semana)

**Formato das aulas:**

- Semana A (100 min): Conceitos + demonstração do professor + início do passo a passo.
- Semana B (100 min): Conclusão do passo a passo pelos alunos + atividades correlatas + revisão.

### 1) Objetivos de aprendizagem

Ao final deste capítulo, o(a) aluno(a) será capaz de:

- Explicar o ciclo requisição–resposta HTTP, diferenciação stateless vs. stateful, métodos HTTP e códigos de status mais comuns.
- Descrever a arquitetura MVC e o fluxo de uma requisição dentro do Laravel (roteamento → controller → model → view).
- Preparar um projeto Laravel conectado ao MySQL e executar migrações.
- Criar rotas, controllers e views Blade com layouts e parciais (navbar/footer).
- Organizar o repositório com Git e documentar instruções iniciais no README.
### 2) Pré-requisitos e ferramentas

- Conhecimentos prévios: HTML, CSS, introdução a JavaScript; PHP OO e conexão com banco (2º ano); noções básicas de banco de dados.
- Ferramentas:
    - VS Code, Git, MySQL, Postman (instalados no laboratório).
    - Laravel (PHP 8.2+) + Composer (para este capítulo).
    - Observação: caso PHP/Composer não estejam disponíveis nas máquinas, o professor pode disponibilizar um ambiente preparado (ex.: máquina de laboratório ou VM) para o desenvolvimento com Laravel. (Manteremos o passo a passo no modo nativo com Composer para reduzir dependências.)
### 3) Conteúdo teórico

#### 3.1. HTTP em linhas claras

HTTP (HyperText Transfer Protocol) é o “idioma” padrão da Web. Ele define como um cliente (normalmente o navegador) solicita algo a um servidor (uma aplicação) e como o servidor responde. Pense em HTTP como uma conversa em que o cliente pede um recurso (“quero ver a página inicial”) e o servidor entrega uma resposta (“aqui está o HTML dessa página”). Esse ciclo é chamado de requisição–resposta e acontece o tempo todo: ao carregar uma página, ao enviar um formulário, ao buscar dados via API, ao baixar um arquivo, etc.

Uma requisição HTTP possui três partes principais: (1) a linha inicial, com o método e a rota (por exemplo, GET /); (2) os cabeçalhos (headers), que são metadados como o tipo de conteúdo que o cliente aceita (Accept) e o tipo de conteúdo que está sendo enviado (Content-Type); e (3) opcionalmente um corpo (body), que contém dados enviados pelo cliente — muito comum em POST/PUT/PATCH. A resposta também segue um padrão: um código de status (ex.: 200), cabeçalhos e um corpo (HTML, JSON, etc.). Quando você entende essas partes, fica muito mais fácil diagnosticar problemas, como “por que meu formulário não chegou?” ou “por que a aplicação está respondendo com erro?”.

Dizemos que o HTTP é stateless (“sem estado”) porque cada requisição é independente: o servidor não é obrigado a lembrar o que aconteceu antes. Se o usuário está logado, por exemplo, essa informação precisa ser “transportada” de alguma forma em cada requisição — normalmente por cookies de sessão ou por tokens. Isso não significa que não exista login; significa apenas que o estado não é mantido automaticamente pelo protocolo. O Laravel facilita esse processo ao usar sessões e middlewares, mas o conceito fundamental continua sendo o mesmo.

Os métodos (verbos) HTTP indicam a intenção da requisição. Em aplicações web e APIs, os mais comuns são:

- `GET` — Ler/obter informações (ex.: abrir a Home ou listar produtos).
- `POST` — Enviar dados para criar um recurso (ex.: cadastrar um produto).
- `PUT/PATCH` — Enviar dados para atualizar um recurso (ex.: editar um produto).
- `DELETE` — Remover um recurso (ex.: apagar um produto).

Os códigos de status são a forma padrão do servidor dizer “o que aconteceu”. Eles são agrupados em classes: 2xx (sucesso), 3xx (redirecionamento), 4xx (erro do cliente) e 5xx (erro do servidor). Um erro 4xx geralmente indica que o cliente pediu algo inválido (rota inexistente, dados errados, falta de login), enquanto um erro 5xx aponta falhas internas (ex.: bug, configuração incorreta, indisponibilidade do banco).

- `200 OK` — Sucesso na leitura/retorno do recurso.
- `201 Created` — Recurso criado com sucesso (muito comum em APIs).
- `302 Found` — Redirecionamento temporário (muito usado em login).
- `400 Bad Request` — Requisição inválida (dados malformados).
- `401 Unauthorized` — Não autenticado (precisa login/token).
- `404 Not Found` — Rota ou item não encontrado.
- `500 Internal Server Error` — Erro inesperado no servidor.

> **Exemplo aplicado no passo a passo (Cap. 1)**
>
> Quando você executar “php artisan serve” (seção 4.4) e abrir http://127.0.0.1:8000, o navegador faz uma requisição GET /. O Laravel encontra a rota definida em routes/web.php (seção 4.5) e responde com status 200 e o HTML renderizado. Se você acessar uma rota que não existe, o Laravel responderá 404. Se o banco estiver configurado incorretamente no .env e você rodar “php artisan migrate” (seção 4.3), a aplicação pode registrar um erro e você verá mensagens indicando falha de conexão — um exemplo típico de problema que aparece como 500 quando ocorre durante uma requisição web.

#### 3.2. MVC (Model–View–Controller) na prática

MVC é um padrão de arquitetura que separa uma aplicação em três responsabilidades principais: Model (dados e regras), View (interface) e Controller (coordenação). Essa separação existe para evitar “bagunça” no código. Quando tudo fica misturado — HTML, SQL e regras de negócio no mesmo arquivo — o projeto cresce e rapidamente fica difícil de manter. Com MVC, cada parte tem um lugar claro, e isso reduz erros e facilita evolução.

O Model representa o domínio do seu sistema: conceitos como Produto, Categoria e Pedido. No Laravel, ele normalmente é um Model Eloquent, que se conecta a uma tabela do banco. Além de consultar e salvar dados, o Model pode conter regras e relacionamentos (por exemplo, um produto pertence a uma categoria). Isso evita repetição de código em várias telas e mantém a regra de negócio centralizada.

A View é a camada de apresentação. Em Laravel, usamos o Blade (templates) para montar HTML de forma organizada, reaproveitando layouts e parciais. A View não deveria conter regra de negócio pesada: o ideal é receber dados já prontos do Controller e apenas exibi-los (com loops e condições simples). Assim, você consegue trocar o visual sem reescrever a lógica do sistema.

O Controller é o “orquestrador”. Ele recebe a requisição da rota, decide o que precisa ser feito, valida dados de entrada, chama o Model para buscar/salvar informações e escolhe qual View deve ser retornada. Em muitos casos, o Controller também define qual resposta será enviada (HTML, JSON, redirecionamento). Um bom Controller é claro, pequeno e objetivo: ele coordena, mas não concentra tudo.

Em resumo, o fluxo típico MVC no Laravel é: (1) o usuário acessa uma URL, (2) a rota aponta para um método de Controller, (3) o Controller interage com Models, (4) o Controller retorna uma View (ou JSON). Se você memorizar esse fluxo, consegue entender praticamente qualquer parte do Laravel com facilidade.

> **Exemplo aplicado no passo a passo (Cap. 1)**
>
> Na seção 4.5, você cria o HomeController e define o método index(). A rota GET / aponta para esse método. Dentro do index(), você prepara o dado ($titulo) e retorna a view home.blade.php. A view renderiza o HTML usando o layout base e parciais (navbar/footer). Mesmo sem banco de dados nessa tela inicial, você já enxerga claramente o MVC funcionando: a rota direciona, o Controller prepara os dados, e a View apresenta. Nos próximos capítulos, quando você criar Models e migrations, o Controller passará a buscar dados no banco (Model) antes de enviar para a View.

#### 3.3. O que o Laravel organiza para você

Laravel é um framework que padroniza a forma como aplicações web são construídas. Em vez de começar “do zero” com dezenas de decisões (onde colocar arquivos, como rotear, como validar, como acessar banco), você ganha uma estrutura pronta e convenções bem definidas. Isso é especialmente útil em projetos didáticos: todos os alunos trabalham com o mesmo padrão, o que facilita estudar, revisar e corrigir.

A primeira grande ajuda do Laravel é a organização de pastas. Quando você aprende a localizar rapidamente rotas, controllers, models, views e migrations, você economiza tempo e evita erros. Essa organização também incentiva a separação de responsabilidades (MVC). Veja os diretórios mais importantes:

- `routes/web.php` — Define as rotas de páginas web (normalmente retornam HTML).
- `app/Http/Controllers` — Onde ficam os Controllers (lógica de coordenação).
- `app/Models` — Onde ficam os Models Eloquent (dados e regras).
- `resources/views` — Views Blade (layouts, páginas e parciais).
- `database/migrations` — Arquivos que versionam a estrutura do banco (tabelas/colunas).
- `database/seeders` — Dados iniciais ou de demonstração (povoar banco).

A segunda grande ajuda é o Artisan, a linha de comando do Laravel. Ele automatiza tarefas repetitivas e cria arquivos “do jeito certo”, com namespace e estrutura corretos. Isso diminui erros comuns de iniciantes (por exemplo, criar um controller na pasta errada). Além disso, o Artisan executa tarefas essenciais como migrations e caches.

Migrations merecem destaque: elas são como “histórico” do banco. Em vez de cada pessoa criar tabelas manualmente e acabar com bancos diferentes, as migrations garantem que todos tenham o mesmo esquema. Quando você roda “php artisan migrate”, o Laravel aplica as alterações de forma controlada. Esse padrão é fundamental para trabalhar em equipe, usar Git e manter consistência entre ambientes (desenvolvimento, testes e produção).

Por fim, o Laravel já vem com recursos de segurança e produtividade integrados: proteção CSRF para formulários, validação de dados, middlewares, suporte a autenticação e muito mais. Você não precisa dominar tudo agora, mas é importante saber que o framework oferece essas ferramentas — e que você vai ativá-las conforme o projeto evolui.

> **Exemplo aplicado no passo a passo (Cap. 1)**
>
> Na seção 4.5, o comando “php artisan make:controller HomeController” cria o controller no lugar certo e com o namespace correto. Já na seção 4.3, “php artisan migrate” aplica as migrations padrão no seu MySQL, criando tabelas essenciais (como a de migrations). Esse mesmo processo será usado nos próximos capítulos para criar as tabelas do sistema da Lanchonete (categorias, produtos, pedidos). Ao seguir a estrutura do Laravel, você sabe exatamente onde colocar cada arquivo do passo a passo.

### 4) Passo a passo guiado (Projeto Lanchonete)

Meta do capítulo: Criar o esqueleto do projeto Laravel conectado ao MySQL, com página inicial, layout base (Blade), navbar/footer e rotas/controladores mínimos.

#### 4.1. Preparar o banco de dados (MySQL)

Crie um banco para o projeto. Se usar o CLI do MySQL:

```sql
# Acesse o MySQL (ajuste usuário/senha conforme seu ambiente)
-- Dentro do console SQL:
CREATE DATABASE lanchonete CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;

-- Opcional: criar usuário com permissões restritas ao banco
-- CREATE USER 'aluno'@'localhost' IDENTIFIED BY 'senha_segura';
-- GRANT ALL PRIVILEGES ON lanchonete.* TO 'aluno'@'localhost';
-- FLUSH PRIVILEGES;
EXIT;
```

> **Dica:** Use um usuário não-root do MySQL para desenvolver.

#### 4.2. Criar o projeto Laravel

Pré-requisitos: PHP 8.2+ e Composer instalados.

Sem usar root: execute tudo no seu diretório de usuário.

**Shell**

```bash
# No terminal, navegue até a pasta onde deseja criar o projeto
composer create-project laravel/laravel lanchonete-web3
cd lanchonete-web3
```

#### 4.3. Configurar o .env

Duplique o arquivo .env.example para .env (se necessário) e ajuste o MySQL:

```ini
APP_NAME="Lanchonete"
APP_ENV=local
APP_KEY=base64:... # (gerado pelo artisan)
APP_DEBUG=true
APP_URL=http://localhost

LOG_CHANNEL=stack
LOG_LEVEL=debug

DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=lanchonete
DB_USERNAME=aula
DB_PASSWORD=aula
```

Atualize a chave depois de modificar o arquivo .env

**Shell**

```bash
# Gere a chave da aplicação (normalmente já vem gerada)
php artisan key:generate
```

Teste a conexão executando as migrações padrão:

**Shell**

```bash
# teste de conexão com o banco de dados
php artisan migrate
```

Se aparecer “Migration table created successfully”, a conexão está correta.

#### 4.4. Subir o servidor de desenvolvimento

**Shell**

```bash
# iniciar o servidor
php artisan serve
```

Acesse: http://127.0.0.1:8000

Dica: Não usaremos o bootstrap para css agora, mas se preferir não usar npm por enquanto, você pode incluir um CSS via CDN no layout (ex.: Bootstrap). No capítulo 3 veremos validação e no 4 paginar/buscar; o build de assets via Vite/Node pode ficar para depois.

#### 4.5. Rotas, Controller e View iniciais

Crie um HomeController:

**Shell**

```bash
# Crie um HomeController:
php artisan make:controller HomeController
```

Crie ou Edite app/Http/Controllers/HomeController.php:

**PHP**

```php
<?php
namespace App\Http\Controllers;
use Illuminate\Http\Request;
class HomeController extends Controller
{
    public function index()
    {
        $titulo = 'Bem-vindo à Lanchonete';
        return view('home', compact('titulo'));
    }
}
```

Defina rotas em routes/web.php:

**PHP**

```php
<?php
use Illuminate\Support\Facades\Route;
use App\Http\Controllers\HomeController;
Route::get('/', [HomeController::class, 'index'])->name('home');
```

Crie o layout base em resources/views/layouts/app.blade.php:

**PHP**

```php
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>@yield('title', config('app.name'))</title>

    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet"
      integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.11.3/font/bootstrap-icons.min.css">    
    
</head>
<body class="bg-light">

    @include('partials.navbar')
    <main class="container py-4">
        @yield('content')
    </main>
    @include('partials.footer')
</body>
</html>
```

Crie parciais resources/views/partials/navbar.blade.php e resources/views/partials/footer.blade.php:

**PHP**

```php
{{-- resources/views/partials/navbar.blade.php --}}
<nav class="navbar navbar-expand-lg navbar-dark bg-dark">
    <div class="container">
        <a href="{{ route('home') }}">{{ config('app.name') }}</a>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarConteudo">
            <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarConteudo">
            <ul class="navbar-nav ms-auto">
                <li class="nav-item"><a href="#cardapio">Cardápio</a></li>
                <li class="nav-item"><a href="#pedidos">Pedidos</a></li>
                <li class="nav-item"><a href="#contato">Contato</a></li>
            </ul>
        </div>
    </div>
</nav>
```

**PHP**

```php
{{-- resources/views/partials/footer.blade.php --}}
<footer class="py-4 mt-5 border-top">
    <div class="container text-center text-muted">
        <small>&copy; {{ date('Y') }} {{ config('app.name') }} — Todos os direitos reservados.</small>
    </div>
</footer>
```

Crie a view resources/views/home.blade.php:

**PHP**

```php
@extends('layouts.app')

@section('title', 'Início')

@section('content')
    <div class="p-5 mb-4 bg-white rounded-3 shadow-sm">
        <div class="container-fluid py-5">
            <h1 class="display-5 fw-bold">{{ $titulo }}</h1>
            <p class="col-md-8 fs-5">
                Este é o início do sistema da Lanchonete. Nas próximas aulas,
                vamos construir o catálogo (categorias e produtos), pedidos e relatórios.
            </p>
            #Ver Cardápio</a>
        </div>
    </div>
@endsection
```

Atualize o nome do app em config/app.php (opcional), ou mantenha o valor de APP_NAME no .env.

#### 4.6. Iniciar controle de versão (Git)

**Shell**

```bash
#iniciar controle de versão
git init
git add .
git config --global user.email "you@example.com"
git config --global user.name "Your Name"
git commit -m "Capítulo 1: setup do projeto Lanchonete (Laravel + Blade)"
```

Crie um README.md com instruções mínimas:

**Markdown**

```markdown
# Lanchonete

## Requisitos
- PHP 8.2+, Composer
- MySQL

## Como rodar
1. Copie `.env.example` para `.env` e ajuste DB_*
2. `composer install` (se necessário)
3. `php artisan key:generate`
4. `php artisan migrate`
5. `php artisan serve`
```

### 5) Atividades correlatas (para a Semana B)

O professor acompanha e tira dúvidas. Os(as) alunos(as) entregam via repositório (branch ou PR).

1. Página “Sobre”
    - Crie a rota /sobre, um SobreController com método index e a view sobre.blade.php usando o layout base.
    - Conteúdo: breve descrição da lanchonete e missão/valores.
2. Página “Contato” (form estático)
    - Crie rota /contato, controller e view com um formulário (nome, e-mail, mensagem).
    - Sem backend ainda: apenas a interface, reutilizando componentes do layout.
3. Parcial de alertas reutilizável
    - Crie resources/views/partials/alerts.blade.php que exibe mensagens fictícias de sucesso/erro.
    - Inclua @include('partials.alerts') em home.blade.php e em outras páginas.

Critérios: usar layout, partials, rotas nomeadas, controller e view em Blade. Organização e padronização contam.

### 6) Pesquisas complementares (para aprofundar)

- HTTP: Como o navegador monta requisições? Diferenças entre GET e POST no envio de formulários.
- Status HTTP: Quando retornar 201 Created? O que significam 422 Unprocessable Entity e 409 Conflict?
- MVC: Vantagens de separar responsabilidades. Exemplos de antipadrões quando não se usa MVC.
- Laravel: O que são middlewares? Exemplos práticos (auth, logging, throttle).
- Blade: Diferenças entre @include, @yield e @section. Quando criar componentes vs partials?

Sugestão de estudo prático: Faça um diagrama simples do fluxo Rota → Controller → Model → View no seu projeto, com setas e exemplos reais de arquivos.

### 9) Entregáveis do capítulo

1. Link do repositório Git com o projeto inicial (Laravel + Blade) e README.
2. Aplicação executando Home/Sobre/Contato com layout e partials.
3. Captura de tela da Home e da Página Sobre (salvas no repositório em docs/).

---

## Capítulo 02 — Modelagem, Migrations, Seeders & Eloquent (CRUD de Categoria)

**Carga horária:** 2 semanas (100 min/semana)

**Formato das aulas:**

- Semana A (100 min): Teoria + demonstração + início do passo a passo.
- Semana B (100 min): Conclusão do passo a passo pelos alunos + atividades correlatas + revisão.

> Contexto do projeto: continuação do Sistema da Lanchonete iniciado no Capítulo 1 (Laravel + Blade + MySQL).

### 1) Objetivos de aprendizagem

Ao final deste capítulo, o(a) aluno(a) será capaz de:

- Modelar entidades simples (Categoria/Produto) para um sistema de lanchonete.
- Criar e executar migrations e seeders no Laravel.
- Usar Eloquent ORM para operações CRUD.
- Construir um CRUD completo para Categoria com Resource Controller e Views Blade.
- Estruturar rotas REST com Route::resource.
### 2) Pré-requisitos e ferramentas

- Pré-requisitos: Capítulo 1 concluído (projeto Laravel rodando com MySQL e layout base).
- Ferramentas: VS Code, Git, MySQL, Postman (opcional neste capítulo).
- Sem root: tudo via composer/artisan local e permissões do seu usuário.
### 3) Conteúdo teórico

#### 3.1. Modelagem de dados (visão prática)

Modelagem de dados é a etapa em que você transforma uma necessidade do mundo real (por exemplo, “uma lanchonete precisa organizar itens do cardápio”) em uma estrutura que o banco de dados consegue armazenar. Nessa etapa, você decide quais “entidades” existem (por exemplo, Categoria e Produto), quais informações cada entidade guarda (atributos) e como elas se relacionam. Em termos práticos, isso vira tabelas, colunas e chaves no banco.

No sistema da Lanchonete, Categoria e Produto são entidades centrais porque o cardápio precisa ser organizado e consultável. Uma categoria agrupa vários produtos (ex.: “Bebidas” contém “Suco”, “Refrigerante”, “Água”). Esse relacionamento é chamado de 1:N (um para muitos): uma Categoria possui muitos Produtos, e cada Produto pertence a uma Categoria. Quando você modela isso corretamente, o sistema ganha consistência: você evita produtos “soltos” sem categoria e facilita consultas como “listar produtos de uma categoria”.

Além de escolher entidades e relacionamentos, você define tipos de dados adequados. Preço deve ser decimal (não float) para evitar erros de precisão; campos de texto com tamanho previsível devem ter limites (ex.: nome até 100 caracteres); e valores booleanos (ativa/ativo) permitem desativar itens sem apagar do banco. Esses detalhes fazem diferença na qualidade do sistema: aumentam a integridade, melhoram a performance e reduzem bugs no CRUD.

Atributos sugeridos para este capítulo (e o motivo de cada um):

- `Categoria: nome` — Identifica a categoria; usar unique evita duplicidade como “Bebidas” repetido.
- `Categoria: descricao` — Texto opcional para explicar a categoria.
- `Categoria: ativa` — Permite ativar/desativar sem apagar registros.
- `Produto: categoria_id` — Chave estrangeira que liga o produto à sua categoria (integridade referencial).
- `Produto: preco` — Decimal para valores monetários; evita arredondamentos incorretos.
- `timestamps` — created_at e updated_at ajudam auditoria e ordenação.

> **Exemplo aplicado no passo a passo (Cap. 2)**
>
> No passo a passo (seção 4.2) você transforma essa modelagem em migrations: cria a tabela categorias com nome único e a tabela produtos com categoria_id como chave estrangeira. O trecho foreignId("categoria_id")->constrained("categorias") materializa o relacionamento 1:N definido na teoria e garante que não exista produto apontando para categoria inexistente.

#### 3.2. Migrations, Seeders e Factories

Depois de modelar, precisamos “materializar” o banco. No Laravel, isso é feito com migrations: arquivos PHP que descrevem a estrutura do banco (tabelas, colunas, índices, chaves estrangeiras). A grande vantagem é que o banco passa a ser versionado como código. Isso significa que, ao clonar o projeto, qualquer pessoa consegue criar o mesmo banco apenas rodando um comando, sem depender de scripts SQL espalhados ou de passos manuais.

Seeders entram em seguida: são classes que inserem dados iniciais ou de demonstração no banco. Em um sistema real, seeders podem criar perfis, permissões, categorias padrão etc. No contexto didático, seeders ajudam a povoar o banco rapidamente para testar telas, listagens e relacionamentos. Isso evita que você tenha que cadastrar tudo manualmente antes de ver o sistema funcionando.

Factories complementam seeders com dados fake gerados automaticamente (usando Faker). A diferença é que a factory define “como gerar” um registro realista (nome, descrição, preço), e o seeder decide “quantos” registros criar e quais registros fixos são necessários. Com factories, você cria massa de dados em segundos — essencial para treinar paginação, busca e UX.

Resumo rápido das funções:

- `Migration` — cria/alterar tabelas e colunas de forma rastreável.
- `Seeder` — insere dados iniciais ou de teste automaticamente.
- `Factory` — gera dados fake realistas (muitas vezes usados pelos seeders).

> **Exemplo aplicado no passo a passo (Cap. 2)**
>
> Na seção 4.1 você cria arquivos com Artisan usando o atalho -mfs (migration + factory + seeder). Na seção 4.4 você configura CategoriaSeeder com dados fixos (Bebidas, Lanches, Doces) e depois usa Categoria::factory()->count(5)->create() para gerar mais categorias. Por fim, rodando php artisan db:seed (seção 4.4) você popula o banco automaticamente e já consegue ver a listagem no index do CRUD.

#### 3.3. Eloquent ORM

Eloquent é o ORM (Object-Relational Mapping) do Laravel. A ideia do ORM é permitir que você trabalhe com o banco usando objetos e métodos, em vez de escrever SQL manualmente para tudo. No Eloquent, cada Model representa uma tabela e cada instância do Model representa uma linha. Por exemplo, Categoria (Model) representa a tabela categorias, e uma instância $categoria representa um registro específico dessa tabela.

O Eloquent facilita muito as operações CRUD: criar, listar, atualizar e excluir. Ele também facilita relacionamentos: uma categoria “tem muitos” produtos, e um produto “pertence a” uma categoria. Com relacionamentos bem definidos, você consegue acessar $categoria->produtos para obter os produtos daquela categoria, ou $produto->categoria para obter a categoria de um produto. Isso melhora a legibilidade do código e reduz repetição.

Um ponto importante de segurança no Eloquent é o “mass assignment” (atribuição em massa), usado em create() e update(). Para evitar que o usuário envie campos indevidos (por exemplo, tentando alterar um campo sensível), o Laravel exige que você liste explicitamente quais campos podem ser preenchidos em massa. Isso é feito com $fillable (permitidos) ou $guarded (bloqueados). Em um CRUD, essa configuração é essencial para segurança e previsibilidade.

Métodos de consulta e escrita mais usados no dia a dia:

- `all()` — retorna todos os registros (cuidado com tabelas grandes).
- `orderBy()` — ordena resultados (ex.: por nome).
- `get()` — executa a consulta e retorna coleção.
- `paginate()` — retorna resultados paginados (veremos melhor no Cap. 4).
- `findOrFail()` — busca por id e lança erro 404 se não achar.
- `create()` — cria registro usando mass assignment (requer $fillable).
- `update()` — atualiza registro usando mass assignment (requer $fillable).
- `delete()` — remove registro.

> **Exemplo aplicado no passo a passo (Cap. 2)**
>
> Na seção 4.5, o CategoriaController usa Categoria::orderBy("nome")->get() para listar, Categoria::create($dados) para criar e $categoria->update($dados) para atualizar. Esses métodos só funcionam corretamente porque, na seção 4.3, você configurou $fillable no Model Categoria. Sem $fillable, o Laravel bloquearia create/update para proteger contra mass assignment.

#### 3.4. Resource Controllers & Views

Quando construímos um CRUD, repetimos sempre o mesmo conjunto de ações: listar (index), mostrar formulário (create/edit), salvar (store/update) e excluir (destroy). No Laravel, um Resource Controller organiza essas ações em métodos padronizados, o que cria consistência no projeto e reduz improviso. A grande vantagem é que você e qualquer colega conseguem “adivinhar” onde está cada lógica, porque a convenção é sempre a mesma.

O Route::resource complementa isso criando automaticamente as rotas REST para essas ações. Em vez de declarar manualmente todas as rotas, você escreve uma linha e ganha o conjunto completo. Isso melhora produtividade e reduz erros de digitação. Além disso, o Route::resource combina com as views Blade: você cria index.blade.php, create.blade.php, edit.blade.php e um partial de formulário, e reaproveita layout e partials do Capítulo 1 para manter consistência visual.

Nas views, uma boa prática é evitar duplicação. O formulário de criar e editar normalmente tem os mesmos campos; por isso usamos um partial (_form.blade.php). Assim, se você precisar mudar um campo, muda uma vez só. Outra boa prática é sempre mostrar feedback ao usuário (mensagens de sucesso/erro) e manter navegação clara (botão cancelar, voltar ao index).

Ações padrão em um Resource Controller e o que cada uma faz:

- `index` — lista registros
- `create` — mostra formulário de criação
- `store` — processa criação (salva no banco)
- `show` — mostra um registro (opcional neste capítulo)
- `edit` — mostra formulário de edição
- `update` — processa edição (atualiza no banco)
- `destroy` — exclui registro

> **Exemplo aplicado no passo a passo (Cap. 2)**
>
> Na seção 4.5, você registra Route::resource("categorias", CategoriaController::class). Isso cria automaticamente rotas como /categorias (index) e /categorias/create (create). Na seção 4.6, você cria as views index/create/edit e o partial _form para reutilizar o formulário. Assim, quando o usuário clica em “Nova Categoria”, ele cai na rota create, vê o formulário (view create) e ao enviar o POST, o método store valida e chama Categoria::create.

### 4) Passo a passo guiado — CRUD de Categoria

Meta do capítulo: Modelar Categoria e Produto, implementar CRUD completo de Categoria, deixar Produto preparado para a próxima atividade (Cap. 3 terá validação com Form Requests e upload de imagem do produto).

#### 4.1. Criar Models, Migration, Factory, Seeder e Controller

No terminal, dentro do projeto:

**Shell**

```bash
# Categoria: model + migration + factory + seeder + controller (resource)
php artisan make:model Categoria -mfs
php artisan make:controller CategoriaController --resource

# Produto (vamos modelar e migrar agora; o CRUD completo ficará como atividade correlata):
php artisan make:model Produto -mf
```

O atalho -mfs cria Migration, Factory e Seeder junto com o Model. O Controller foi criado à parte, como resource.

#### 4.2. Definir migrations

Edite database/migrations/xxxx_xx_xx_xxxxxx_create_categorias_table.php:

**PHP**

```php
public function up(): void
{
    Schema::create('categorias', function (Blueprint $table) {
        $table->id();
        $table->string('nome')->unique();
        $table->text('descricao')->nullable();
        $table->boolean('ativa')->default(true);
        $table->timestamps();
    });
}
```

Edite database/migrations/xxxx_xx_xx_xxxxxx_create_produtos_table.php:

**PHP**

```php
public function up(): void
{
    Schema::create('produtos', function (Blueprint $table) {
        $table->id();
        $table->foreignId('categoria_id')->constrained('categorias')->cascadeOnDelete();
        $table->string('nome');
        $table->text('descricao')->nullable();
        $table->decimal('preco', 10, 2)->default(0);
        $table->boolean('ativo')->default(true);
        $table->timestamps();
    });
}
```

Execute as migrations:

**Shell**

```bash
php artisan migrate
```

#### 4.3. Modelos Eloquent

app/Models/Categoria.php:

**PHP**

```php
<?php
namespace App\Models;
use Illuminate\Database\Eloquent\Model;
use Illuminate\Database\Eloquent\Factories\HasFactory;
class Categoria extends Model
{
    use HasFactory;
    protected $table = 'categorias';
    protected $fillable = [
        'nome',
        'descricao',
        'ativa',
    ];
    public function produtos()
    {
        return $this->hasMany(Produto::class, 'categoria_id');
    }
}
```

app/Models/Produto.php:

**PHP**

```php
<?php
namespace App\Models;
use Illuminate\Database\Eloquent\Model;
use Illuminate\Database\Eloquent\Factories\HasFactory;
class Produto extends Model
{
    use HasFactory;
    protected $table = 'produtos';
    protected $fillable = [
        'categoria_id',
        'nome',
        'descricao',
        'preco',
        'ativo',
    ];

    public function categoria()
    {
        return $this->belongsTo(Categoria::class, 'categoria_id');
    }
}
```

#### 4.4. Factories e Seeders

database/factories/CategoriaFactory.php:

**PHP**

```php
<?php
namespace Database\Factories;
use Illuminate\Database\Eloquent\Factories\Factory;
class CategoriaFactory extends Factory
{
    public function definition(): array
    {
        return [
            'nome' => $this->faker->unique()->word(),
            'descricao' => $this->faker->optional()->sentence(8),
            'ativa' => $this->faker->boolean(85),
        ];
    }
}
```

database/factories/ProdutoFactory.php:

**PHP**

```php
<?php
namespace Database\Factories;
use App\Models\Categoria;
use Illuminate\Database\Eloquent\Factories\Factory;

class ProdutoFactory extends Factory
{
    public function definition(): array
    {
        return [
            'categoria_id' => Categoria::factory(),
            'nome' => $this->faker->unique()->words(2, true),
            'descricao' => $this->faker->optional()->sentence(12),
            'preco' => $this->faker->randomFloat(2, 5, 60), // R$ 5,00 a R$ 60,00
            'ativo' => $this->faker->boolean(90),
        ];
    }
}
```

Abra o Seeder de Categoria criado automaticamente (ex.: database/seeders/CategoriaSeeder.php):

**PHP**

```php
<?php
namespace Database\Seeders;
use App\Models\Categoria;
use Illuminate\Database\Seeder;
class CategoriaSeeder extends Seeder
{
    public function run(): void
    {
        // Exemplos fixos (úteis para desenvolvimento)
        $fixas = [
            ['nome' => 'Bebidas', 'descricao' => 'Sucos, refrigerantes e água', 'ativa' => true],
            ['nome' => 'Lanches', 'descricao' => 'Sanduíches e porções', 'ativa' => true],
            ['nome' => 'Doces',   'descricao' => 'Sobremesas e guloseimas', 'ativa' => true],
        ];

        foreach ($fixas as $c) {
            Categoria::firstOrCreate(['nome' => $c['nome']], $c);
        }

        // Complemento com dados fake
        Categoria::factory()->count(5)->create();
    }
}
```

Crie um DatabaseSeeder que chama o de Categoria (e, se quiser, Produtos):

database/seeders/DatabaseSeeder.php:

**PHP**

```php
public function run(): void
{
    $this->call(CategoriaSeeder::class);

    // Opcional: produtos de exemplo (por ora podemos deixar para a atividade do aluno)
    // \App\Models\Produto::factory()->count(15)->create();
}
```

Popule o banco:

**Shell**

```bash
php artisan db:seed
```

#### 4.5. Rotas (resource) e Controller

routes/web.php:

**PHP**

```php
use App\Http\Controllers\CategoriaController;

Route::resource('categorias', CategoriaController::class);
// Isso cria as rotas: index, create, store, show, edit, update, destroy
```

app/Http/Controllers/CategoriaController.php (versão inicial, sem Form Request ainda):

**PHP**

```php
<?php
namespace App\Http\Controllers;
use App\Models\Categoria;
use Illuminate\Http\Request;
class CategoriaController extends Controller
{
    public function index()
    {
        $categorias = Categoria::orderBy('nome')->get(); // Paginação entra no Cap. 4
        return view('categorias.index', compact('categorias'));
    }

    public function create()
    {
        return view('categorias.create');
    }

    public function store(Request $request)
    {
        // Validação simples por enquanto (Form Request no Cap. 3)
        $dados = $request->validate([
            'nome' => 'required|string|max:100|unique:categorias,nome',
            'descricao' => 'nullable|string|max:500',
            'ativa' => 'nullable|boolean',
        ]);

        $dados['ativa'] = $request->boolean('ativa');

        Categoria::create($dados);

        return redirect()->route('categorias.index')
            ->with('sucesso', 'Categoria criada com sucesso!');
    }

    public function edit(Categoria $categoria)
    {
        return view('categorias.edit', compact('categoria'));
    }

    public function update(Request $request, Categoria $categoria)
    {
        $dados = $request->validate([
            'nome' => 'required|string|max:100|unique:categorias,nome,' . $categoria->id,
            'descricao' => 'nullable|string|max:500',
            'ativa' => 'nullable|boolean',
        ]);

        // Converter checkbox para boolean
        $dados['ativa'] = $request->boolean('ativa');

        $categoria->update($dados);

        return redirect()->route('categorias.index')
            ->with('sucesso', 'Categoria atualizada com sucesso!');
    }

    public function destroy(Categoria $categoria)
    {
        $categoria->delete();

        return redirect()->route('categorias.index')
            ->with('sucesso', 'Categoria excluída com sucesso!');
    }
}
```

#### 4.6. Views Blade (index, create, edit e parcial _form)

Crie a pasta resources/views/categorias/

resources/views/categorias/index.blade.php:

**PHP**

```php
@extends('layouts.app')
@section('title', 'Categorias')
@section('content')
@include('partials.alerts')
    <div class="d-flex justify-content-between align-items-center mb-3">
        <h2>Categorias</h2>
        <a href="{{ route('categorias.create') }}" class="btn btn-sm btn-primary">Nova Categoria </a>
    </div>
    <div class="card">
        <div class="card-body p-0">
            <table class="table table-striped table-hover mb-0">
                <thead class="table-light">
                    <tr>
                        <th>Nome</th>
                        <th>Ativa</th>
                        <th>Atualizado em</th>
                        <th class="text-end">Ações</th>
                    </tr>
                </thead>
                <tbody>
                    @forelse ($categorias as $categoria)
                        <tr>
                            <td>{{ $categoria->nome }}</td>
                            <td>
                                @if ($categoria->ativa)
                                    <span class="badge text-bg-success">Sim</span>
                                @else
                                    <span class="badge text-bg-secondary">Não</span>
                                @endif
                            </td>
                            <td>{{ $categoria->updated_at->format('d/m/Y H:i') }}</td>
                            <td class="text-end">
                                <a href="{{ route('categorias.edit', $categoria) }}" class="btn btn-sm btn-outline-secondary">
                                    Editar
                                </a>

                                <form action="{{ route('categorias.destroy', $categoria) }}" method="POST" class="d-inline">
                                    @csrf
                                    @method('DELETE')
                                    <button class="btn btn-sm btn-outline-danger">Excluir</button>
                                </form>
                            </td>
                        </tr>
                    @empty
                        <tr><td colspan="4" class="text-center p-4 text-muted">Nenhuma categoria cadastrada.</td></tr>
                    @endforelse
                </tbody>
            </table>
        </div>
    </div>
@endsection
```

resources/views/categorias/_form.blade.php:

**PHP**

```php
@php
    $isEdit = isset($categoria);
@endphp
<div class="mb-3">
    <label for="nome" class="form-label">Nome</label>
    <input type="text" class="form-control @error('nome') is-invalid @enderror"
           id="nome" name="nome" value="{{ old('nome', $categoria->nome ?? '') }}" maxlength="100" required>
    @error('nome')
        <div class="invalid-feedback">{{ $message }}</div>
    @enderror
</div>
<div class="mb-3">
    <label for="descricao" class="form-label">Descrição</label>
    <textarea class="form-control @error('descricao') is-invalid @enderror"
              id="descricao" name="descricao" rows="3" maxlength="500">{{ old('descricao', $categoria->descricao ?? '') }}</textarea>
    @error('descricao')
        <div class="invalid-feedback">{{ $message }}</div>
    @enderror
</div>
<div class="form-check form-switch mb-3">
    <input class="form-check-input" type="checkbox" role="switch" id="ativa" name="ativa" value = "1"
           {{ old('ativa', $categoria->ativa ?? true) ? 'checked' : '' }}>
    <label class="form-check-label" for="ativa">Ativa</label>
</div>
<div class="d-flex gap-2">
    <button type="submit" class="btn btn-primary">{{ $isEdit ? 'Atualizar' : 'Salvar' }}</button>
    <a href="{{ route('categorias.index') }}" class="btn btn-secondary">Cancelarv/a>

</div>
```

resources/views/categorias/create.blade.php:

**PHP**

```php
@extends('layouts.app')
@section('title', 'Nova Categoria')
@section('content')
    <h2 class="mb-3">Nova Categoria</h2>
     <form action="{{ route('categorias.store') }}" method="POST">
        @csrf
        @include('categorias._form')
    
    </form>
@endsection
```

resources/views/categorias/edit.blade.php:

**PHP**

```php
@extends('layouts.app')
@section('title', 'Editar Categoria')
@section('content')
    <h2 class="mb-3">Editar Categoria</h2>
    &ltform action="{{ route('categorias.update', $categoria) }}" method="POST">
        @csrf
        @method('PUT')
        @include('categorias._form', ['categoria' => $categoria])
    </form>
@endsection
```

Link no menu (navbar) para Categorias:

**PHP**

```php
<li><a href ="/categorias">Categorias</a></li>
```

Pronto! Você tem o CRUD de Categoria funcionando, com migrations, seeders, model e resource controller.

### 5) Atividades correlatas (para a Semana B)

Objetivo: consolidar Eloquent, migrations/seeders e prática de CRUD.

Entrega: commit + push no repositório.

1. CRUD de Produto
- Crie o ProdutoController como resource.
- Implemente index/create/store/edit/update/destroy (sem upload ainda).
- Campos: categoria_id, nome, descricao (opcional), preco (decimal, ≥ 0), ativo (bool).
- Nas telas, liste e selecione a Categoria (select com Categoria::orderBy('nome')->get()).
2. Seeders/Factories complementares
- Ative no DatabaseSeeder a geração de Produtos (ProdutoFactory) em quantidade suficiente para testar as telas.
- Geração coerente (nome, preço, ativo).
3. UX básica
- Adicione mensagens de sucesso/erro no partial partials/alerts.
- Voltar para o index após salvar/excluir.
- Tornar o botão de excluir com confirm() (já ilustrado em Categoria).

Plus (opcional): ajustar máscara de preço no front (JS simples) — o valor salvo no banco deve ser decimal válido.

### 6) Pesquisas complementares (para aprofundar)

- Migrations: diferenças entre Schema::table() e Schema::create(); como alterar colunas em migrações posteriores.
- Factories: como usar states (ex.: state(\['ativo' => false\])) para gerar cenários específicos.
- Seeders: boas práticas para popular dados fixos (ex.: perfis iniciais).
- Eloquent: diferenças entre fillable e guarded; riscos de mass assignment.
- Relacionamentos: hasMany, belongsTo, with() para eager loading (evitar N+1).
### 9) Entregáveis do capítulo

1. Repositório com migrations, models, seeder e CRUD de Categoria.
2. Capturas de tela da listagem e do formulário de Categoria (pasta docs/).
3. (Atividade) Rascunho inicial do CRUD de Produto (controller, views, rotas), mesmo sem upload/validação avançada.

---

## Capítulo 03 — Blade, Formulários, Validação e Mensagens

**Carga horária:** 2 semanas (100 min/semana)

**Formato das aulas:**

- Semana A (100 min): Conceitos + demonstração do professor + início do passo a passo.
- Semana B (100 min): Conclusão do passo a passo pelos alunos + atividades correlatas + revisão.

> Contexto do projeto: continuação do Sistema da Lanchonete (CRUD de Categoria e base de Produto criados no Cap. 2).

### 1) Objetivos de aprendizagem

Ao final deste capítulo, o(a) aluno(a) será capaz de:

- Explicar o que é CSRF e por que frameworks exigem token em formulários.
- Diferenciar validação “inline” (no controller) de validação com Form Requests.
- Criar Form Requests no Laravel, definindo regras e mensagens amigáveis.
- Exibir mensagens de erro e sucesso com melhor UX (alerts) e preservar campos com old().
- Aplicar boas práticas de Blade: herança de layout, diretivas (@error, @csrf, @method) e partials reutilizáveis.
### 2) Pré-requisitos e ferramentas

- Pré-requisitos: Capítulos 1 e 2 concluídos (projeto Laravel rodando com MySQL; CRUD de Categoria funcionando).
- Ferramentas: VS Code, Git, MySQL e navegador. (Postman opcional neste capítulo.)
- Recomendado: terminal do Linux com PHP/Composer configurados para o usuário (sem root).
### 3) Conteúdo teórico

#### 3.1. CSRF (Cross-Site Request Forgery)

CSRF é um tipo de ataque em que um site malicioso tenta fazer o navegador de um usuário autenticado executar ações em outro site sem que ele perceba. O ponto crítico é que o navegador “leva junto” cookies de sessão automaticamente. Se você estiver logado em um sistema e visitar uma página maliciosa, essa página pode tentar disparar uma requisição para o seu sistema (por exemplo, um POST para excluir um registro). Se o servidor aceitar a requisição apenas porque o cookie de sessão está presente, o ataque funciona.

Para impedir isso, a defesa mais comum é exigir um “segredo” adicional que um site externo não consegue adivinhar: o token CSRF. Em frameworks como o Laravel, esse token é gerado para a sessão do usuário e precisa estar presente em requisições que alteram estado (normalmente POST, PUT, PATCH, DELETE). Se o token não estiver presente ou estiver inválido, o Laravel bloqueia a requisição. Assim, mesmo que um site malicioso force o navegador a enviar o formulário, ele não terá o token correto e a ação será negada.

No Laravel com Blade, inserir o token é fácil porque a diretiva @csrf gera automaticamente um campo hidden com o token. Essa convenção reduz erros: você não precisa lembrar de criar o input manualmente em cada formulário. Além disso, ao trabalhar com métodos PUT/DELETE em HTML (que não existem nativamente), o Laravel usa a técnica de “method spoofing” com @method("PUT") ou @method("DELETE"). Isso também depende de um formulário POST por baixo, e por isso o token CSRF continua sendo necessário.

- `Quando usar` — Em formulários e requisições que criam/atualizam/excluem dados.
- `Quando não usar` — Em requisições somente de leitura (GET), que não alteram dados.
- `Erro comum` — Esquecer @csrf e receber erro 419 (Page Expired) no Laravel.

> **Exemplo aplicado no passo a passo (Cap. 3)**
>
> Na seção 4.3 você cria/edita o partial partials/alerts e garante que as views usem @include(...). Já nas views do CRUD (Cap. 2) e no fluxo de edição/exclusão (seção 4.2), os formulários devem conter @csrf. Se você testar o formulário de exclusão (DELETE) sem @csrf, o Laravel bloqueará a requisição. Portanto, ao validar o CRUD no item 4.5, um dos sinais de que o CSRF está correto é conseguir criar/editar/excluir sem erro 419.

#### 3.2. Validação no Laravel (inline vs Form Request)

Validação é o processo de garantir que os dados enviados pelo usuário fazem sentido antes de salvar no banco. Em um CRUD, isso evita registros incompletos (por exemplo, categoria sem nome), valores inválidos (preço negativo) e inconsistências (nome duplicado quando deveria ser único). Além disso, validação reduz riscos de segurança e melhora a experiência do usuário ao fornecer mensagens claras do que precisa ser corrigido.

No Laravel, a forma mais simples é validar “inline” no controller usando $request->validate(\[...\]). Isso é útil para ações pequenas e rápidas, porque você coloca as regras no mesmo lugar onde salva o registro. O problema é que, conforme o projeto cresce, os controllers ficam grandes e difíceis de manter: as regras se repetem entre store e update, as mensagens ficam espalhadas e a leitura do controller fica confusa.

O Form Request resolve isso criando uma classe dedicada para validação. Ele separa responsabilidades: o controller passa a focar no fluxo (salvar, redirecionar) e a classe de request cuida das regras e mensagens. Além disso, o Form Request pode ter authorize(), que permite negar a ação por perfil (por exemplo, somente gerente pode cadastrar). Mesmo que você deixe authorize() como true agora, a estrutura já fica pronta para evoluir mais tarde.

Outra vantagem importante é a reutilização e consistência: o mesmo Form Request pode ser usado tanto em store quanto em update, e a regra de unique pode ser adaptada para ignorar o registro atual quando estiver editando. Isso evita um erro clássico: ao editar uma categoria sem mudar o nome, a validação unique não deve bloquear. A solução é “ignorar” o id da categoria atual — exatamente o que é feito com Rule::unique(...)->ignore($categoriaId).

Em resumo, quando usar cada abordagem:

- `Inline no controller` — Projetos pequenos ou validações pontuais e rápidas.
- `Form Request` — CRUDs completos, projetos que crescem, necessidade de mensagens amigáveis e organização.

> **Exemplo aplicado no passo a passo (Cap. 3)**
>
> Na seção 4.1 você cria CategoriaRequest e define rules() e messages(). Na seção 4.2, o controller passa a receber CategoriaRequest $request em store/update e usa $request->validated(). Isso deixa o controller mais limpo e centraliza as regras. Quando você testar o cenário de nome duplicado (seção 4.5), a mensagem “Já existe uma categoria...” vem do messages() do Form Request.

#### 3.3. Mensagens ao usuário (sucesso/erro) e UX

Uma aplicação profissional sempre dá retorno ao usuário. Se o usuário clica em “Salvar” e nada acontece, ele fica inseguro e pode repetir a ação (gerando duplicidade). Se ocorre um erro e ele não sabe o motivo, ele não consegue corrigir. Por isso, mensagens de sucesso e erro não são “detalhe”: são parte essencial da qualidade do sistema.

No Laravel, é comum usar flash messages, que são mensagens gravadas na sessão por apenas uma requisição. Isso combina com o padrão Post/Redirect/Get: depois de salvar, o controller redireciona para a listagem e, nessa nova requisição, a mensagem aparece no topo. Esse padrão evita reenvio de formulário ao atualizar a página e mantém o fluxo mais estável.

Além disso, quando a validação falha, o Laravel redireciona de volta para o formulário com um conjunto de erros (bag $errors) e com os valores anteriores (old()). O usuário vê a mensagem do que está errado e não precisa digitar tudo de novo. Para uma boa UX, o ideal é: (1) mostrar um aviso geral no topo (“verifique os campos”), (2) mostrar o erro específico ao lado do campo, (3) manter os valores preenchidos e (4) manter a navegação clara (botão cancelar/voltar).

Boas práticas simples que melhoram muito a experiência:

- `Mensagens claras` — Dizer o que falta e como corrigir (ex.: “Informe o nome da categoria”).
- `Evitar repetir digitação` — Usar old() para preservar valores.
- `Erros perto do campo` — Usar @error para exibir a mensagem no input certo.
- `Feedback de sucesso` — Mostrar confirmação após criar/editar/excluir.

> **Exemplo aplicado no passo a passo (Cap. 3)**
>
> Na seção 4.3 você cria o partial partials/alerts.blade.php para exibir session("sucesso"), session("erro") e um aviso quando $errors->any(). Na seção 4.4 você garante que os inputs usam old() e @error para mostrar a mensagem específica. Em 4.5, ao tentar salvar uma categoria sem nome, o formulário deve voltar com o campo preservado e uma mensagem visível; ao salvar com sucesso, o index deve exibir o alerta verde “Categoria criada com sucesso!”.

#### 3.4. Blade na prática (diretivas e partials)

Blade é o mecanismo de templates do Laravel. Ele permite construir HTML de forma organizada, usando herança de layout e reaproveitamento de componentes. A grande ideia é evitar repetição: em vez de copiar e colar a mesma navbar e footer em todas as páginas, você cria um layout base e inclui partes comuns. Isso reduz trabalho, melhora consistência visual e facilita manutenção.

As diretivas @extends, @section e @yield implementam herança: a página “filha” diz qual layout ela usa e quais seções preenche. Já @include injeta um arquivo parcial dentro da view. Com isso, você pode ter um partial de alerts, um partial de formulário, e reaproveitar em create e edit. Esse padrão é muito usado em CRUDs porque mantém as telas uniformes.

Outras diretivas do Blade são fundamentais para formulários: @csrf (token CSRF), @method (simular PUT/DELETE), @error (mostrar erro do campo) e old() (recuperar valor antigo). Quando você combina @error com classes do Bootstrap (como is-invalid) você cria uma interface que destaca imediatamente o campo errado. Isso é didaticamente importante: o aluno aprende a associar validação com feedback visual.

Diretivas e seus usos mais comuns no capítulo:

- `@extends / @section / @yield` — Herança de layout: define estrutura e encaixa conteúdo.
- `@include` — Reutiliza pedaços: alerts, navbar, footer, formulário.
- `@csrf` — Proteção CSRF em formulários.
- `@method` — Simula PUT/DELETE em formulários HTML.
- `@error` — Exibe mensagem do campo e permite estilizar input com erro.
- `old()` — Reutiliza valores digitados após erro de validação.

> **Exemplo aplicado no passo a passo (Cap. 3)**
>
> Na seção 4.3 você centraliza mensagens em um único partial (partials/alerts). Depois, todas as telas do CRUD apenas fazem @include("partials.alerts"), evitando duplicação. Na seção 4.4, o input usa old("nome", ...) e @error("nome") para mostrar feedback. Isso conecta diretamente a teoria: Blade fornece as ferramentas para criar layouts reutilizáveis e formulários com validação amigável.

### 4) Passo a passo guiado (Projeto Lanchonete)

Meta do capítulo: **converter a validação do CRUD de Categoria para Form Requests**, **exibir mensagens de sucesso/erro** e **preservar valores com old()**.

#### 4.1. Criar o Form Request (CategoriaRequest)

No terminal (dentro do projeto):

**Shell**

```bash
php artisan make:request CategoriaRequest
```

Edite `app/Http/Requests/CategoriaRequest.php`:

**PHP**

```php
<?php

namespace App\Http\Requests;

use Illuminate\Foundation\Http\FormRequest;
use Illuminate\Validation\Rule;

class CategoriaRequest extends FormRequest
{
    public function authorize(): bool
    {
        return true; // por enquanto qualquer usuário pode; autorização entra mais adiante
    }

    public function rules(): array
    {
        // Se estiver editando, o model vem pela rota (route model binding)
        $categoriaId = $this->route('categoria')?->id;

        return [
            'nome' => [
                'required',
                'string',
                'max:100',
                Rule::unique('categorias', 'nome')->ignore($categoriaId),
            ],
            'descricao' => 'nullable|string|max:500',
            'ativa' => 'nullable|boolean',
        ];
    }

    public function messages(): array
    {
        return [
            'nome.required' => 'Informe o nome da categoria.',
            'nome.max' => 'O nome deve ter no máximo :max caracteres.',
            'nome.unique' => 'Já existe uma categoria com este nome.',
            'descricao.max' => 'A descrição deve ter no máximo :max caracteres.',
        ];
    }
}
```

#### 4.2. Atualizar o Controller para usar Form Request

No `CategoriaController`, troque `Request` por `CategoriaRequest` em store/update.

**PHP**

```php
<?php

namespace App\Http\Controllers;

use App\Models\Categoria;
use App\Http\Requests\CategoriaRequest;

class CategoriaController extends Controller
{
    public function index()
    {
        $categorias = Categoria::orderBy('nome')->get();
        return view('categorias.index', compact('categorias'));
    }

    public function create()
    {
        return view('categorias.create');
    }

    public function store(CategoriaRequest $request)
    {
        $dados = $request->validated();
        $dados['ativa'] = $request->boolean('ativa');

        Categoria::create($dados);

        return redirect()->route('categorias.index')
            ->with('sucesso', 'Categoria criada com sucesso!');
    }

    public function edit(Categoria $categoria)
    {
        return view('categorias.edit', compact('categoria'));
    }

    public function update(CategoriaRequest $request, Categoria $categoria)
    {
        $dados = $request->validated();
        $dados['ativa'] = $request->boolean('ativa');

        $categoria->update($dados);

        return redirect()->route('categorias.index')
            ->with('sucesso', 'Categoria atualizada com sucesso!');
    }

    public function destroy(Categoria $categoria)
    {
        $categoria->delete();

        return redirect()->route('categorias.index')
            ->with('sucesso', 'Categoria excluída com sucesso!');
    }
}
```

#### 4.3. Melhorar o partial de alertas (sucesso/erro/validação)

Crie (ou edite) `resources/views/partials/alerts.blade.php`:

**PHP**

```php
{{-- resources/views/partials/alerts.blade.php --}}

@if (session('sucesso'))
    <div class="alert alert-success alert-dismissible fade show" role="alert">
        {{ session('sucesso') }}
        <button type="button" class="btn-close" data-bs-dismiss="alert" aria-label="Fechar"></button>
    </div>
@endif

@if (session('erro'))
    <div class="alert alert-danger alert-dismissible fade show" role="alert">
        {{ session('erro') }}
        <button type="button" class="btn-close" data-bs-dismiss="alert" aria-label="Fechar"></button>
    </div>
@endif

@if ($errors->any())
    <div class="alert alert-warning" role="alert">
        <strong>Atenção:</strong> verifique os campos do formulário.
    </div>
@endif
```

Garanta que suas views chamam:

**PHP**

```php
@include('partials.alerts')
```

#### 4.4. Preservar valores e exibir erros por campo (old() e @error)

No Cap. 2, o `_form.blade.php` já usava `old()` e `@error`. Confira se está assim (ou ajuste se necessário):

**PHP**

```php
<input type="text" class="form-control @error('nome') is-invalid @enderror"
       id="nome" name="nome" value="{{ old('nome', $categoria->nome ?? '') }}" maxlength="100" required>

@error('nome')
    <div class="invalid-feedback">{{ $message }}</div>
@enderror
```

#### 4.5. Teste de validação (erros e sucesso)

Teste cenários:

- Tentar criar categoria sem nome → deve aparecer erro e manter campos.
- Tentar criar categoria com nome já existente → mensagem de “Já existe uma categoria...”.
- Criar/editar/excluir → deve aparecer mensagem de sucesso no topo.
#### 4.6. Commit no Git

**Shell**

```bash
git add .
git commit -m "Capítulo 3: Form Request para Categoria + alerts + mensagens e old()"
git push
```

### 5) Atividades correlatas (para a Semana B)

O professor acompanha e tira dúvidas. Entrega via repositório (commit + push).

1. **Aplicar Form Requests ao CRUD de Produto**
    - Criar `ProdutoRequest` com regras: nome obrigatório, preço numérico ≥ 0, categoria_id obrigatório, ativo boolean.
    - Atualizar `ProdutoController` para usar `ProdutoRequest` em store/update.
2. **Upload de imagem do produto (Storage local) + exibição**
    - Adicionar campo `imagem` (string/nullable) na tabela de produtos via migration.
    - Validar: arquivo de imagem, tamanho máximo e extensões (jpg, png, webp).
    - Salvar em `storage/app/public` e exibir na listagem usando `Storage::url()`.
3. **Regras de validação adicionais**
    - Validar preço: `numeric|min:0`.
    - Validar imagem: `image|mimes:jpg,jpeg,png,webp|max:2048` (exemplo).
    - Mensagens amigáveis (custom messages) para as regras.
### 6) Pesquisas complementares (para aprofundar)

- CSRF: como cookies e sessões participam do mecanismo de proteção em frameworks.
- Form Request: como usar `authorize()` para restringir ações por perfil (ex.: gerente).
- Mensagens de validação: como personalizar atributos (ex.: “nome do produto” em vez de “nome”).
- Blade: diferença entre partials e components; quando criar um componente.
- Upload seguro: validação de MIME, nomes de arquivo e cuidados com diretório público.
### 9) Entregáveis do capítulo

1. Repositório atualizado com CategoriaRequest e controller revisado.
2. Partial de alerts funcionando (sucesso/erro/validação) em todas as páginas do CRUD.
3. Capturas de tela do formulário com erro de validação e do sucesso após salvar (salvar em docs/).

---

## Capítulo 04 — Listagens, Paginação, Busca e Segurança Básica (CSRF/XSS)

**Carga horária:** 2 semanas (100 min/semana)

**Formato das aulas:**

- Semana A (100 min): Conceitos + demonstração do professor + início do passo a passo.
- Semana B (100 min): Conclusão do passo a passo pelos alunos + atividades correlatas + revisão + entrega bimestral.

> Contexto do projeto: continuação do Sistema da Lanchonete (CRUDs e validação básica já existentes).

### 1) Objetivos de aprendizagem

Ao final deste capítulo, o(a) aluno(a) será capaz de:

- Implementar paginação em listagens usando Eloquent e Blade.
- Criar uma busca simples por nome usando query string (ex.: ?q=...).
- Aplicar filtros em listagens por parâmetros (ex.: categoria_id).
- Explicar e aplicar práticas básicas de segurança em formulários e views (CSRF, escaping, noções de XSS e SQL Injection).
- Manter a navegação consistente (rotas nomeadas, preservação de filtros na paginação).
### 2) Pré-requisitos e ferramentas

- Pré-requisitos: Capítulos 1 a 3 concluídos (CRUD de Categoria funcional; validação e alerts configurados).
- Ferramentas: VS Code, Git, MySQL, navegador. Postman opcional.
- Recomendado: ter alguns registros no banco (seeders) para visualizar paginação e busca.
### 3) Conteúdo teórico

#### 3.1. Paginação (por que e como)

Paginação é a técnica de dividir uma lista grande em “fatias” (páginas) menores, em vez de carregar tudo de uma vez. Em sistemas reais, tabelas podem ter centenas ou milhares de registros. Se você buscar tudo com get(), sua aplicação pode ficar lenta, gastar muita memória e gerar páginas enormes. Além disso, a experiência do usuário piora: uma lista infinita dificulta encontrar itens, aumenta o tempo de carregamento e deixa a navegação cansativa.

No Laravel, a paginação é simples porque o Eloquent já oferece métodos prontos. Ao trocar get() por paginate(10), o framework faz duas coisas importantes: (1) limita a consulta para trazer apenas os itens daquela página, e (2) cria um objeto paginador com informações como página atual, total de itens, total de páginas e links. Na view, você renderiza os links com $itens->links(). Isso padroniza a navegação e evita que você tenha que construir links manualmente.

Uma armadilha comum aparece quando você combina paginação com filtros (por exemplo, busca por nome). Se você clicar em “Próximo” e o sistema esquecer os parâmetros de filtro, o usuário “perde” a busca e vê a lista completa de novo. Para evitar isso, usamos withQueryString() na query paginada. Esse método preserva todos os parâmetros GET atuais (como q, categoria_id, sort, dir) e os adiciona automaticamente aos links da paginação.

Boas práticas para paginação em CRUDs:

- `Prefira paginate()` — Quando você quer saber total de páginas/itens e renderizar links completos.
- `Use simplePaginate()` — Quando quer performance máxima e não precisa do total (menos consultas).
- `Preserve filtros` — Use withQueryString() para manter parâmetros ao paginar.
- `Mostre contexto` — Exibir algo como “Mostrando 1–10 de 53” ajuda o usuário a entender onde está.

> **Exemplo aplicado no passo a passo (Cap. 4)**
>
> Na seção 4.1, você troca a listagem de Categorias para ->paginate(10)->withQueryString(). Depois, na seção 4.2, adiciona {{ $categorias->links() }} na view. O resultado prático é que a página /categorias passa a carregar apenas 10 registros por vez e exibir botões de navegação. Quando houver busca (?q=...), o withQueryString() garante que ao clicar em “Próximo” você continue filtrando pelo mesmo termo.

#### 3.2. Busca e filtros por query string

Busca e filtros servem para reduzir o conjunto de dados exibido e ajudar o usuário a encontrar rapidamente o que precisa. Em aplicações web, o padrão mais simples e comum é usar query string (parâmetros na URL), por exemplo: /categorias?q=bebidas. A vantagem é que a URL fica compartilhável (você pode copiar/colar), e o navegador consegue manter histórico (voltar/avançar) naturalmente. Além disso, buscas via GET combinam bem com paginação, porque os parâmetros são apenas leitura (não alteram dados).

No controller, você lê o parâmetro com request("q") e monta a consulta. O Eloquent ajuda com when(): ele aplica um trecho de query apenas se o parâmetro existir. Isso deixa o código mais limpo do que vários ifs. Para buscar parte de um texto, normalmente usamos where + LIKE ("%texto%"). Em bancos como MySQL, essa busca funciona bem para listas pequenas e médias, mas pode ficar lenta em tabelas muito grandes. Por isso, mais adiante você pode estudar índices, FULLTEXT ou mecanismos de busca — por enquanto, o importante é entender o padrão.

Filtros seguem a mesma lógica: você pode filtrar produtos por categoria_id, por ativo, ou por faixa de preço. Cada filtro é apenas mais um parâmetro GET. A boa prática é manter a interface clara: mostrar o valor atual do filtro (ex.: campo de busca preenchido), oferecer botão “Limpar”, e garantir que o filtro continue ativo ao paginar (withQueryString).

Boas práticas para parâmetros de busca e filtro:

- `Normalize entrada` — Remover espaços extras e limitar tamanho do termo de busca evita problemas e melhora UX.
- `Evite SQL manual` — Use Query Builder/Eloquent para binding seguro.
- `Mantenha estado na UI` — Inputs devem refletir o filtro atual (value="{{ request(...) }}").
- `Permita limpar` — Link/ação para remover parâmetros e voltar à lista completa.

> **Exemplo aplicado no passo a passo (Cap. 4)**
>
> Na seção 4.2, você cria um formulário GET com um input name="q" e preenche o value com {{ request("q") }}. Isso faz o termo continuar visível na caixa após buscar. No controller (seção 4.1), o when($q, ...) adiciona where("nome", "like", "%{$q}%"). Assim, ao acessar /categorias?q=lanche, a listagem exibirá somente categorias contendo “lanche”. O botão “Limpar” simplesmente aponta para a rota sem parâmetros, removendo o filtro.

#### 3.3. Segurança básica na entrada e na saída

Quando você começa a aceitar dados do usuário (formulários, buscas, filtros), segurança deixa de ser opcional. As três preocupações mais comuns em CRUDs iniciais são: CSRF, XSS e SQL Injection. A boa notícia é que o Laravel e o Blade já oferecem proteções fortes por padrão — desde que você use as ferramentas do jeito correto.

CSRF (Cross-Site Request Forgery) acontece quando um site externo tenta induzir o navegador do usuário a executar uma ação no seu sistema (como excluir um item) usando a sessão do usuário. A proteção no Laravel é o token CSRF: todo formulário que envia POST/PUT/PATCH/DELETE deve incluir @csrf. Se faltar, a requisição é negada (erro 419). Portanto, “CSRF ok” significa: qualquer ação de escrita (criar/editar/excluir) deve estar protegida por token.

XSS (Cross-Site Scripting) ocorre quando conteúdo malicioso (HTML/JavaScript) é armazenado ou refletido e depois exibido no navegador, executando código no contexto do seu site. A defesa principal é escapar a saída: no Blade, {{ }} faz escaping automático, transformando `<script>` em texto visível. Já {!! !!} imprime “cru”, sem escapar — por isso deve ser evitado para dados vindos do usuário. Em outras palavras: nunca confie que o usuário vai digitar apenas “Bebidas”. Ele pode tentar inserir marcação ou script.

SQL Injection acontece quando a aplicação constrói SQL por concatenação de strings com entrada do usuário (por exemplo, "... WHERE nome = $q"). O Eloquent/Query Builder protege disso ao usar binding de parâmetros: mesmo que o usuário tente inserir caracteres maliciosos, o framework trata aquilo como dado, não como parte do comando SQL. Apesar disso, ainda existe risco se você aceitar valores dinâmicos para coisas que não são parâmetros (como nomes de colunas em orderBy). Por isso, quando fizer ordenação dinâmica, use whitelist: uma lista de colunas permitidas e direções válidas.

> **Regra de ouro (nível técnico)**
>
> Valide a entrada (Request) e escape a saída (View). Isso resolve grande parte dos problemas comuns. Para parâmetros dinâmicos (como sort/dir), use whitelist. Para ações de escrita, use CSRF.

> **Exemplo aplicado no passo a passo (Cap. 4)**
>
> Na seção 4.4, você revisa que todos os forms de POST/PUT/DELETE têm @csrf e, quando necessário, @method("DELETE"). Isso garante proteção CSRF. No mesmo item, você verifica que as views exibem dados com {{ }} (escapado). O exemplo didático mostra que {{ $categoria->nome }} é seguro mesmo se o usuário tentar cadastrar `<script>`..., enquanto {!! $categoria->nome !!} seria perigoso. Já na busca (seções 4.1 e 4.3), você usa where("nome", "like", ...) via Eloquent, evitando concatenação de SQL manual — reduzindo risco de SQL Injection.

### 4) Passo a passo guiado (Projeto Lanchonete)

Meta do capítulo: adicionar **paginação** e **busca por nome** em Categorias e Produtos, reforçando **segurança básica** (CSRF e escaping).

#### 4.1. Ajustar o Controller de Categorias para paginar e buscar

Edite `app/Http/Controllers/CategoriaController.php` (método index):

**PHP**

```php
public function index()
{
    $q = request('q');

    $categorias = Categoria::query()
        ->when($q, function ($query) use ($q) {
            $query->where('nome', 'like', "%{$q}%");
        })
        ->orderBy('nome')
        ->paginate(10)
        ->withQueryString();

    return view('categorias.index', compact('categorias', 'q'));
}
```

> **Por que withQueryString()?**
>
> Ele preserva `?q=...` (e outros filtros) ao navegar nas páginas.

#### 4.2. Ajustar a View de Categorias: formulário de busca + links de paginação

Edite `resources/views/categorias/index.blade.php` e adicione um formulário de busca no topo:

**PHP**

```php
@include('partials.alerts')

<div class="d-flex flex-wrap justify-content-between align-items-center gap-2 mb-3">
    <h2 class="mb-0">Categorias</h2>

    <form method="GET" action="{{ route('categorias.index') }}" class="d-flex gap-2">
        <input type="text" name="q" value="{{ request('q') }}" class="form-control" placeholder="Buscar por nome...">
        <button class="btn btn-outline-secondary" type="submit">Buscar</button>
        <a class="btn btn-outline-secondary" href="{{ route('categorias.index') }}">Limpar</a>
    </form>

    <a class="btn btn-primary" href="{{ route('categorias.create') }}">Nova Categoria</a>
</div>
```

Troque a lista `get()` por paginação na renderização e adicione os links ao final da tabela:

**PHP**

```php
{{-- ... sua tabela aqui ... --}}

<div class="mt-3">
    {{ $categorias->links() }}
</div>
```

Edite o arquivo /app/Providers/AppServiceProvider.php :

**PHP**

```php
{{-- ... No início ... --}}
use Illuminate\Pagination\Paginator; // 1. IMPORTANTE: Importe esta linha

{{-- ... Dentro da Função boot ... --}}
Paginator::useBootstrapFive(); 
```

#### 4.3. Preparar Produtos: paginação + busca + filtro por categoria (base)

Se você já fez o CRUD de Produto (atividade do Cap. 2/3), aplique o mesmo padrão. Se ainda não fez, implemente pelo menos a listagem de Produto com filtro por categoria.

Exemplo para `ProdutoController@index` (paginação, busca e filtro):

**PHP**

```php
public function index()
{
    $q = request('q');
    $categoriaId = request('categoria_id');

    $produtos = Produto::query()
        ->with('categoria')
        ->when($q, function ($query) use ($q) {
            $query->where('nome', 'like', "%{$q}%");
        })
        ->when($categoriaId, function ($query) use ($categoriaId) {
            $query->where('categoria_id', $categoriaId);
        })
        ->orderBy('nome')
        ->paginate(10)
        ->withQueryString();

    $categorias = Categoria::orderBy('nome')->get();

    return view('produtos.index', compact('produtos', 'categorias'));
}
```

#### 4.4. Segurança básica: revisar CSRF e escaping no Blade

Checklist rápido (confira no seu projeto):

- Todo `<form>` que faz POST/PUT/DELETE tem `@csrf`.
- Para PUT/DELETE: usar `@method('PUT')` / `@method('DELETE')`.
- Em views: preferir `{{ $variavel }}` (escapa) e evitar `{!! $variavel !!}` quando for dado do usuário.

Exemplo de exclusão com CSRF (já parecido com o que você tem):

**PHP**

```php
<form method="POST" action="{{ route('categorias.destroy', $categoria) }}" class="d-inline"
      onsubmit="return confirm('Tem certeza que deseja excluir?')">
    @csrf
    @method('DELETE')
    <button class="btn btn-sm btn-outline-danger">Excluir</button>
</form>
```

> **XSS (exemplo didático)**
>
> Se alguém cadastrar o nome como `<script>alert('XSS')</script>`, então `{{ $categoria->nome }}` exibirá como texto (seguro), mas `{!! $categoria->nome !!}` poderia executar o script (perigoso).

#### 4.5. Commit no Git

**Shell**

```bash
git add .
git commit -m "Capítulo 4: paginação + busca + segurança básica (CSRF/escaping)"
git push
```

### 5) Atividades correlatas (para a Semana B)

Objetivo: consolidar listagens, filtros e segurança básica. Entrega via repositório (commit + push).

1. **Filtro por Categoria na listagem de Produtos**
    - Criar um `<select>` com as categorias, enviando `categoria_id` por GET.
    - Manter filtros ao paginar usando `withQueryString()`.
2. **Ordenação por preço (asc/desc)**
    - Implementar `?sort=preco&dir=asc` e `?dir=desc` na listagem de produtos.
    - Validar `sort` e `dir` para permitir apenas valores esperados (segurança e consistência).
3. **Relatório simples exportável para CSV**
    - Criar rota `/relatorios/categorias.csv` que gera CSV com nome/ativa/updated_at.
    - Garantir que o endpoint usa headers corretos e não imprime HTML.

> **Plus (opcional)**
>
> Criar uma página “Relatórios” com botões para baixar CSV de Categorias e Produtos.

### 6) Pesquisas complementares (para aprofundar)

- Paginação: diferença entre `paginate()` e `simplePaginate()` e quando usar cada uma.
- Busca: como indexar colunas no MySQL e como isso afeta performance de LIKE.
- Segurança: diferença entre XSS refletido e armazenado; exemplos reais e prevenção.
- SQL Injection: por que query builder ajuda e onde ainda pode haver risco (ex.: orderBy dinâmico sem whitelist).
- Blade: quando usar `@isset`, `@empty`, `@csrf`, `@method` e cuidados com `{!! !!}`.
### 9) Entregáveis do capítulo

1. Repositório atualizado com paginação e busca em Categorias (e Produtos, se implementado).
2. Capturas de tela: listagem paginada e resultado de busca (salvar em `docs/`).
3. Evidências de segurança básica: forms com CSRF e views com escaping (printscreen do código ou descrição no README).
### Entrega Bimestral (B1) — Catálogo da Lanchonete

**Objetivo:** consolidar o 1º bimestre em uma entrega prática completa e organizada.

**Escopo mínimo**

- CRUD de Categoria completo (create/edit/delete) com validação (Form Request) e mensagens (alerts).
- CRUD de Produto completo (se feito) ou, no mínimo, listagem com relação Categoria (belongsTo) e criação/edição simples.
- Listagens com paginação + busca por nome.
- Segurança básica: CSRF em formulários e escaping no Blade.

**Entrega**

1. Link do repositório Git (commit final com mensagem: *"Entrega B1"*).
2. README com: como rodar, como migrar/seed, e rotas principais.
3. Pasta `docs/` com: 3 prints (Home, Listagem de Categorias com paginação, Form de Categoria com erro e sucesso).

**Critérios (resumo)**

- Funciona localmente (serve + migrate + seed) sem ajustes manuais além do .env.
- Código organizado (controllers enxutos, requests para validação, partials reutilizados).
- Interface consistente (layout, navbar, alerts).

---

## Capítulo 05 — Autenticação manual, Sessão e Perfis

**Carga horária:** 2 semanas (100 min/semana)

**Formato das aulas:**

- Semana A (100 min): Conceitos + demonstração do professor + início do passo a passo.
- Semana B (100 min): Conclusão do passo a passo + atividades correlatas + revisão.

> Contexto do projeto: continuação do Sistema da Lanchonete (catálogo com categorias/produtos, login manual e perfis com controle de acesso básico).

### 1) Objetivos de aprendizagem

Ao final deste capítulo, o(a) aluno(a) será capaz de:

- Implementar autenticação manual (registro, login e logout) usando Laravel + Blade + sessão.
- Explicar como o Laravel usa sessão para manter o usuário autenticado entre requisições.
- Proteger rotas com middleware `auth` e separar áreas públicas e privadas.
- Criar perfis simples (Gerente/Atendente) e exibir menu condicional no Blade.
- Aplicar uma restrição básica de acesso por perfil (ex.: categorias somente Gerente).
### 2) Pré-requisitos e ferramentas

- Pré-requisitos: projeto Laravel funcionando (Cap. 1) + CRUDs do catálogo (Cap. 2) + validação/mensagens (Cap. 3) + paginação/busca (Cap. 4).
- Ferramentas: VS Code, Git, MySQL, Composer, PHP CLI e navegador.
- Observação: neste capítulo, a autenticação será implementada manualmente com recursos nativos do Laravel, sem depender de Node.js/NPM.
### 3) Conteúdo teórico

#### 3.1. Autenticação x autorização

Em sistemas web, autenticação e autorização resolvem problemas diferentes. Autenticação responde “quem é você?”: é a etapa em que o sistema verifica a identidade do usuário, normalmente por e-mail e senha. Autorização responde “o que você pode fazer?”: depois de logado, o sistema verifica se esse usuário pode acessar determinada rota, recurso ou ação.

No sistema da Lanchonete, por exemplo, um atendente pode estar autenticado para lançar pedidos, mas isso não significa que ele tenha autorização para administrar categorias e produtos. Já o gerente, além de estar logado, possui permissões extras. Separar esses conceitos ajuda a manter o projeto organizado e evita erros de segurança.

No Laravel, é comum começar exigindo login com o middleware `auth`. Depois, você acrescenta regras de autorização com base no perfil do usuário, como uma coluna `role` na tabela `users`. Mais adiante, projetos maiores podem evoluir para Gates e Policies.

- `Autenticação` — comprova a identidade do usuário.
- `Autorização` — define o que o usuário pode acessar ou executar.
- `Segurança real fica no servidor` — esconder link no menu não substitui proteção de rota.

> **Exemplo aplicado no passo a passo (Cap. 5)**
>
> Na seção 4, você criará rotas e formulários de registro/login manualmente (autenticação). Depois, usará a coluna `role` e o middleware `auth` para limitar acesso ao catálogo e exibir menu diferente para Gerente e Atendente (autorização).

#### 3.2. Sessão e middlewares

HTTP é stateless: cada requisição é independente. Isso significa que, sem um mecanismo adicional, o servidor não “lembraria” quem acabou de fazer login. A sessão resolve esse problema. No Laravel, quando o login é aceito, o framework guarda na sessão as informações necessárias para identificar o usuário nas próximas páginas.

Na prática, o navegador mantém um cookie com o identificador da sessão e, a cada requisição, o Laravel recupera esse estado. É por isso que funções como `auth()->user()`, `Auth::check()` e diretivas como `@auth` funcionam depois que o usuário entra no sistema.

Middleware é um filtro executado antes da rota. O middleware `auth` verifica se existe um usuário autenticado na sessão; se não existir, o Laravel redireciona para a tela de login. Assim, a rota fica realmente protegida no servidor.

- `auth` — exige que o usuário esteja logado.
- `guest` — exige que o usuário NÃO esteja logado.
- `middleware customizado` — pode validar perfil, token, auditoria etc.

> **Exemplo aplicado no passo a passo (Cap. 5)**
>
> Quando você agrupa as rotas do catálogo em `Route::middleware(['auth'])`, qualquer usuário não autenticado é redirecionado para `/login`. Depois do login, a sessão passa a identificar o usuário em cada nova requisição.

#### 3.3. Autenticação manual com Laravel + Blade

Autenticação manual significa que você mesmo cria as rotas, controllers e telas de registro/login/logout, usando os recursos nativos do Laravel. Em vez de depender de scaffolding pronto, você entende cada parte do fluxo: validação, criação do usuário, hash da senha, tentativa de login, regeneração da sessão e logout seguro.

No cadastro, a senha nunca é salva em texto puro: ela deve ser convertida com `Hash::make()`. No login, o método `Auth::attempt()` recebe as credenciais e verifica se o usuário existe e se a senha informada corresponde ao hash armazenado no banco. Se o login der certo, é boa prática regenerar a sessão para evitar ataques de fixação de sessão.

Com Blade, você pode criar formulários simples para `/register` e `/login`, exibir mensagens de erro e montar uma navbar que muda conforme o usuário está logado ou não. Essa abordagem é excelente para fins didáticos porque torna visíveis as peças que, em outras soluções, já vêm prontas.

- `Hash::make()` — gera hash seguro da senha antes de salvar no banco.
- `Auth::attempt()` — tenta autenticar o usuário com e-mail e senha.
- `$request->session()->regenerate()` — renova o ID da sessão após login.
- `Auth::logout()` + invalidação da sessão — encerra o login com segurança.

> **Exemplo aplicado no passo a passo (Cap. 5)**
>
> Você criará um `AuthController` com métodos para exibir formulários, cadastrar usuário, autenticar e encerrar sessão. Em seguida, ligará esse controller às rotas `/register`, `/login` e `/logout`.

#### 3.4. Perfis (roles) e controle de acesso

Depois de autenticar, surge a necessidade de diferenciar o que cada tipo de usuário pode fazer. Uma forma simples e didática é adicionar um campo `role` na tabela `users`, com valores como `gerente` e `atendente`. Esse campo permite criar menus diferentes e restringir rotas.

É importante lembrar: menu condicional é experiência do usuário, não segurança. Mesmo que um link não apareça, a pessoa ainda pode tentar digitar a URL manualmente. Por isso, o controle real deve ficar no servidor, com middleware, `abort_unless()`, Gate ou Policy.

Neste capítulo, seguiremos uma abordagem simples: usuários novos entram com perfil `atendente` e um usuário de teste será promovido para `gerente`. Assim, você conseguirá observar na prática a diferença entre autenticação e autorização.

- `Default seguro` — usuário novo entra como `atendente`.
- `Menu condicional` — melhora a navegação, mas não protege sozinho.
- `Proteção no servidor` — a rota precisa validar o perfil antes de responder.

> **Exemplo aplicado no passo a passo (Cap. 5)**
>
> Na seção 4.8, a navbar será ajustada com `@auth`, `@guest` e verificação do `role`. Na seção 4.9, uma rota de categorias será limitada para usuários com `role = 'gerente'`.

### 4) Passo a passo guiado (Projeto Lanchonete)

Meta do capítulo: implementar autenticação manual com Laravel, Blade e sessão; proteger rotas; criar perfis simples e exibir menu condicional.

#### 4.1. Preparar o banco e a tabela de sessão (se necessário)

Confirme que a tabela `users` existe e, se seu projeto estiver usando sessão em banco, gere a tabela de sessões:

**Shell**

```bash
php artisan make:session-table
php artisan migrate
```

> **Observação**
>
> Se o seu projeto já possui a migration de sessões ou usa outro driver configurado em `config/session.php`, basta garantir que o ambiente está funcionando e seguir para as próximas etapas.

#### 4.2. Criar a coluna role (perfil) na tabela users

Crie uma migration para adicionar o perfil do usuário:

**Shell**

```bash
php artisan make:migration add_role_to_users_table --table=users
```

Edite a migration gerada em `database/migrations/xxxx_add_role_to_users_table.php`:

**PHP**

```php
public function up(): void
{
    Schema::table('users', function (Blueprint $table) {
        $table->string('role')->default('atendente')->after('email');
    });
}

public function down(): void
{
    Schema::table('users', function (Blueprint $table) {
        $table->dropColumn('role');
    });
}
```

Depois, execute:

**Shell**

```bash
php artisan migrate
```

#### 4.3. Atualizar o Model User

Edite `app/Models/User.php` para permitir preenchimento do `role` e garantir que a senha continue protegida:

**PHP**

```php
protected $fillable = [
    'name',
    'email',
    'password',
    'role',
];
```

#### 4.4. Criar o controller da autenticação manual

No terminal:

**Shell**

```bash
php artisan make:controller AuthController
```

Em `app/Http/Controllers/AuthController.php`, implemente o fluxo básico:

**PHP**

```php
<?php

namespace App\Http\Controllers;

use App\Models\User;
use Illuminate\Http\Request;
use Illuminate\Support\Facades\Auth;
use Illuminate\Support\Facades\Hash;

class AuthController extends Controller
{
    public function showRegisterForm()
    {
        return view('auth.register');
    }

    public function register(Request $request)
    {
        $data = $request->validate([
            'name' => ['required', 'string', 'max:255'],
            'email' => ['required', 'email', 'max:255', 'unique:users,email'],
            'password' => ['required', 'min:6', 'confirmed'],
        ]);

        $user = User::create([
            'name' => $data['name'],
            'email' => $data['email'],
            'password' => Hash::make($data['password']),
            'role' => 'atendente',
        ]);

        Auth::login($user);
        $request->session()->regenerate();

        return redirect()->route('dashboard')->with('success', 'Conta criada com sucesso.');
    }

    public function showLoginForm()
    {
        return view('auth.login');
    }

    public function login(Request $request)
    {
        $credentials = $request->validate([
            'email' => ['required', 'email'],
            'password' => ['required'],
        ]);

        if (Auth::attempt($credentials)) {
            $request->session()->regenerate();
            return redirect()->intended(route('dashboard'));
        }

        return back()
            ->withErrors(['email' => 'Credenciais inválidas.'])
            ->onlyInput('email');
    }

    public function logout(Request $request)
    {
        Auth::logout();
        $request->session()->invalidate();
        $request->session()->regenerateToken();

        return redirect()->route('login.form');
    }
}
```

#### 4.5. Criar as rotas de registro, login e logout

Em `routes/web.php`, adicione rotas públicas para formulários e rotas protegidas para logout e área autenticada:

**PHP**

```php
use App\Http\Controllers\AuthController;
use App\Http\Controllers\CategoriaController;
use App\Http\Controllers\ProdutoController;
use Illuminate\Support\Facades\Route;

Route::get('/register', [AuthController::class, 'showRegisterForm'])->name('register.form')->middleware('guest');
Route::post('/register', [AuthController::class, 'register'])->name('register')->middleware('guest');

Route::get('/login', [AuthController::class, 'showLoginForm'])->name('login.form')->middleware('guest');
Route::post('/login', [AuthController::class, 'login'])->name('login')->middleware('guest');

Route::post('/logout', [AuthController::class, 'logout'])->name('logout')->middleware('auth');

Route::middleware(['auth'])->group(function () {
    Route::view('/dashboard', 'dashboard')->name('dashboard');
    Route::resource('produtos', ProdutoController::class);
});
```

> Depois, você acrescentará uma restrição adicional para categorias, permitindo acesso somente ao gerente.

#### 4.6. Criar as views Blade de autenticação

Crie a pasta `resources/views/auth` e adicione os formulários. Exemplo do cadastro em `resources/views/auth/register.blade.php`:

**PHP**

```php
@extends('layouts.app')

@section('content')
<div class="container mt-4">
    <h1>Criar conta</h1>

    <form action="{{ route('register') }}" method="POST" class="mt-3">
        @csrf

        <div class="mb-3">
            <label class="form-label">Nome</label>
            <input type="text" name="name" class="form-control" value="{{ old('name') }}" required>
            @error('name') <div class="text-danger small">{{ $message }}</div> @enderror
        </div>

        <div class="mb-3">
            <label class="form-label">E-mail</label>
            <input type="email" name="email" class="form-control" value="{{ old('email') }}" required>
            @error('email') <div class="text-danger small">{{ $message }}</div> @enderror
        </div>

        <div class="mb-3">
            <label class="form-label">Senha</label>
            <input type="password" name="password" class="form-control" required>
            @error('password') <div class="text-danger small">{{ $message }}</div> @enderror
        </div>

        <div class="mb-3">
            <label class="form-label">Confirmar senha</label>
            <input type="password" name="password_confirmation" class="form-control" required>
        </div>

        <button class="btn btn-primary" type="submit">Cadastrar</button>
    </form>
</div>
@endsection
```

Exemplo do login em `resources/views/auth/login.blade.php`:

**PHP**

```php
@extends('layouts.app')

@section('content')
<div class="container mt-4">
    <h1>Entrar</h1>

    <form action="{{ route('login') }}" method="POST" class="mt-3">
        @csrf

        <div class="mb-3">
            <label class="form-label">E-mail</label>
            <input type="email" name="email" class="form-control" value="{{ old('email') }}" required>
        </div>

        <div class="mb-3">
            <label class="form-label">Senha</label>
            <input type="password" name="password" class="form-control" required>
        </div>

        @error('email')
            <div class="text-danger small mb-3">{{ $message }}</div>
        @enderror

        <button class="btn btn-primary" type="submit">Entrar</button>
    </form>
</div>
@endsection
```

#### 4.7. Criar uma dashboard simples e testar o fluxo

Crie a view `resources/views/dashboard.blade.php` para testar se o usuário permanece autenticado:

**PHP**

```php
@extends('layouts.app')

@section('content')
<div class="container mt-4">
    <h1>Dashboard</h1>
    <p>Olá, {{ auth()->user()->name }}! Você está autenticado(a).</p>
</div>
@endsection
```

Suba o servidor e teste o fluxo:

**Shell**

```bash
php artisan serve
```

Acesse:

- `/register` para criar usuário
- `/login` para entrar
- `/dashboard` para validar a sessão e a proteção por `auth`
#### 4.8. Ajustar a navbar com @auth, @guest e logout

Edite sua navbar em `resources/views/partials/navbar.blade.php`:

**PHP**

```php
@guest
    <li class="nav-item"><a class="nav-link" href="{{ route('login.form') }}">Entrar</a></li>
    <li class="nav-item"><a class="nav-link" href="{{ route('register.form') }}">Criar conta</a></li>
@endguest

@auth
    <li class="nav-item"><a class="nav-link" href="{{ route('dashboard') }}">Dashboard</a></li>

    @if (auth()->user()->role === 'gerente')
        <li class="nav-item"><a class="nav-link" href="{{ route('categorias.index') }}">Categorias</a></li>
    @endif

    <li class="nav-item"><a class="nav-link" href="{{ route('produtos.index') }}">Produtos</a></li>
    <li class="nav-item">{{ auth()->user()->name }} ({{ auth()->user()->role }})</li>
    <li class="nav-item">
        <form action="{{ route('logout') }}" method="POST" class="d-inline">
            @csrf
            <button class="btn btn-link nav-link p-0" type="submit">Sair</button>
        </form>
    </li>
@endauth
```

#### 4.9. Definir um usuário gerente e restringir Categorias

Depois de registrar um usuário, promova-o a gerente com o tinker:

**Shell**

```bash
php artisan tinker
>>> $u = App\Models\User::where('email', 'seuemail@exemplo.com')->first();
>>> $u->role = 'gerente';
>>> $u->save();
>>> exit
```

Agora proteja as rotas de categorias para que apenas gerente acesse:

**PHP**

```php
Route::middleware(['auth'])->group(function () {
    Route::group(['middleware' => [
        function ($request, $next) {
            abort_unless(auth()->user()?->role == 'gerente', 403);
            return $next($request);
        }
    ]], function () {
        Route::resource('categorias', CategoriaController::class);
    });
});
```

> **Nota didática**
>
> Em projetos maiores, o ideal é criar um middleware próprio (por exemplo, `role:gerente`) ou usar Gates/Policies. Aqui usamos uma abordagem simples para fixar o conceito.

#### 4.10. Commit no Git

**Shell**

```bash
git add .
git commit -m "Capítulo 5: autenticação manual + sessão + perfis (role)"
git push
```

### 5) Atividades correlatas (para a Semana B)

Objetivo: consolidar autenticação manual, sessão e autorização básica. Entrega via repositório (commit + push).

1. **Criar middleware próprio para perfil**
    - Crie um middleware `RoleMiddleware` que recebe o papel esperado.
    - Aplique esse middleware em todas as rotas de `categorias`.
2. **Página “Minha Conta”**
    - Crie uma página para exibir e alterar dados do usuário autenticado (nome e e-mail).
    - Proteja com middleware `auth`.
3. **Melhorar feedback de autenticação**
    - Exiba mensagens flash para cadastro concluído, login realizado e logout efetuado.
    - Dica: use `session()->flash()` ou `with()` nos redirecionamentos.

> **Plus (opcional)**
>
> Implementar uma tela “Acesso negado” personalizada para respostas 403 quando o usuário não possuir o perfil exigido.

### 6) Pesquisas complementares (para aprofundar)

- O que é *hashing* de senha e por que `Hash::make()` deve ser usado antes de salvar?
- O que acontece se você esquecer de regenerar a sessão após o login?
- Como funcionam cookies e sessões em aplicações PHP/Laravel?
- Diferença entre middleware `auth`, middleware customizado, Gates e Policies.
- Quando vale a pena sair da autenticação manual e evoluir para uma solução mais automatizada?
### 9) Entregáveis do capítulo

1. Repositório com autenticação manual funcionando: cadastro, login e logout.
2. Rotas protegidas com middleware `auth` (dashboard e catálogo acessíveis apenas logado).
3. Perfis (`role`) implementados e menu condicional no Blade.
4. Capturas de tela em `docs/`: tela de cadastro, tela de login, dashboard e menu exibindo opção do Gerente.

---

## Capítulo 06 — Relacionamentos Eloquent e Fluxo de Pedido

**Carga horária:** 2 semanas (100 min/semana)

**Formato das aulas:**

- Semana A (100 min): Teoria + demonstração + início do passo a passo.
- Semana B (100 min): Conclusão do passo a passo + atividades correlatas + revisão.

> Contexto do projeto: Sistema da Lanchonete com autenticação e perfis (Cap. 5). Agora criaremos o fluxo de pedidos.

### 1) Objetivos de aprendizagem

Ao final deste capítulo, o(a) aluno(a) será capaz de:

- Explicar e implementar relacionamentos Eloquent **hasMany** e **belongsTo**.
- Modelar tabelas de **Pedido** e **ItemPedido** com integridade referencial (FK).
- Criar um fluxo de pedido: iniciar pedido, adicionar itens e visualizar resumo.
- Aplicar eager loading (`with()`) para evitar problema N+1 em listagens de pedidos.
- Implementar regras iniciais de negócio (status do pedido, total calculado).
### 2) Pré-requisitos e ferramentas

- Pré-requisitos: autenticação pronta (Cap. 5), catálogo com Produto/Categoria e banco migrado/seedado.
- Ferramentas: VS Code, Git, MySQL, navegador. (Postman ainda é opcional.)
- Sugestão: tenha produtos cadastrados para conseguir adicionar itens ao pedido.
### 3) Conteúdo teórico

#### 3.1. Relacionamentos Eloquent (1:N na prática)

Relacionamentos são a forma de representar, no banco e no código, como entidades do sistema se conectam. Em um sistema de lanchonete, um pedido não é um “registro isolado”: ele precisa ter itens (produtos e quantidades). Esse cenário é clássico de relacionamento 1:N (um para muitos): um Pedido (pai) possui muitos ItemPedido (filhos).

No banco, o relacionamento 1:N acontece quando a tabela “filha” guarda uma chave estrangeira apontando para a tabela “pai”. No nosso caso, a tabela item_pedidos tem pedido_id. Isso garante que cada item sempre pertence a um pedido válido. Em Eloquent, esse relacionamento vira métodos que deixam o código expressivo: em Pedido, você define hasMany para itens; em ItemPedido, você define belongsTo para pedido. Com isso, acessar os itens de um pedido vira algo simples como $pedido->itens.

Além disso, o ItemPedido também pertence a um Produto. Isso cria um encadeamento: Pedido -> itens -> produto. Quando esse encadeamento existe, você consegue montar telas de resumo muito facilmente, mostrando nome do produto, quantidade, preço e subtotal. Em termos de modelagem, estamos criando uma “tabela de itens” que funciona como detalhe do pedido.

Relações importantes deste capítulo (tanto no banco quanto no Eloquent):

- `Pedido hasMany ItemPedido` — Um pedido pode ter vários itens.
- `ItemPedido belongsTo Pedido` — Cada item pertence a um pedido específico.
- `ItemPedido belongsTo Produto` — Cada item referencia qual produto foi vendido.

> **Exemplo aplicado no passo a passo (Cap. 6)**
>
> Na seção 4.3, você cria os métodos user() e itens() no model Pedido e os métodos pedido() e produto() no model ItemPedido. Na seção 4.5, o método edit() faz $pedido->load("itens.produto"). Isso só funciona porque os relacionamentos foram definidos corretamente. Já na view pedidos/edit.blade.php (seção 4.7), o loop @forelse($pedido->itens as $item) acessa $item->produto->nome, mostrando o encadeamento do relacionamento.

#### 3.2. Regras de negócio e consistência

Regras de negócio são as decisões que fazem o sistema refletir a realidade do processo da lanchonete. Por exemplo: um pedido pode estar “aberto”, “em preparo”, “pronto”, “entregue” ou “fechado”; e um pedido fechado não deveria receber novos itens. Essas regras não são “detalhes técnicos”; elas definem como o sistema deve se comportar para evitar erros (por exemplo, alguém alterar um pedido já encerrado).

Outra regra central é o cálculo do total. O total do pedido normalmente é a soma dos subtotais de seus itens, e cada subtotal é quantidade × preço unitário. Parece simples, mas existe um detalhe importante: o preço do produto pode mudar no futuro. Se você sempre buscar o preço atual do produto para recalcular pedidos antigos, você altera o histórico de vendas. Por isso, é uma boa prática registrar, no item, o preço unitário no momento da venda (preco_unitario) e o subtotal calculado naquele momento. Assim, mesmo que o produto seja reajustado, o pedido antigo continua correto.

Existem duas estratégias comuns: (1) calcular o total “na hora” (somando subtotais toda vez que exibir) ou (2) armazenar o total no pedido e recalcular sempre que itens mudarem. Neste capítulo, adotamos a segunda estratégia para simplificar telas e consultas, mas garantindo que sempre que um item é adicionado ou removido o total seja recalculado imediatamente. Em aplicações reais, isso costuma ser feito com eventos/model observers ou transações, mas aqui faremos no controller para ficar didático.

Boas práticas iniciais para regras de pedido:

- `Status como enum lógico` — Definir lista de status permitidos e evitar valores livres.
- `Imutabilidade de histórico` — Salvar preco_unitario no item mantém histórico fiel.
- `Recalcular total sempre que item mudar` — Evita total divergente do somatório.
- `Bloquear edição quando fechado` — Regra de negócio evita alterações indevidas.

> **Exemplo aplicado no passo a passo (Cap. 6)**
>
> Na migration de itens (seção 4.2), você cria as colunas preco_unitario e subtotal para registrar histórico. No ItemPedidoController (seção 4.6), após criar/atualizar o item, o código faz $pedido->total = sum("subtotal") e salva. Isso aplica diretamente a regra “total = soma dos subtotais”. Nas atividades correlatas (seção 5), você evolui a regra para impedir alteração quando status for “fechado”.

#### 3.3. Eager loading e o problema N+1

O problema N+1 é um dos principais motivos de lentidão em aplicações com ORM quando o desenvolvedor não percebe o que está acontecendo. Ele ocorre assim: você executa uma consulta para buscar N registros (por exemplo, N pedidos). Em seguida, ao renderizar a view, para cada pedido você acessa uma relação (por exemplo, $pedido->user). Se o relacionamento não estiver carregado, o Eloquent faz uma nova consulta para cada pedido. Resultado: 1 consulta para a lista + N consultas para o usuário = N+1 consultas.

Quando N é pequeno, isso passa despercebido. Mas com dezenas ou centenas de registros, o sistema fica muito lento. A solução é eager loading: carregar relacionamentos antecipadamente com with() (ou load() em um model já carregado). Assim, o Eloquent faz poucas consultas maiores, em vez de muitas consultas pequenas. Além de performance, isso ajuda na previsibilidade do sistema e reduz carga no banco.

No nosso fluxo de pedidos, eager loading é especialmente importante porque temos relações encadeadas: um pedido tem itens e cada item tem produto. Se você listar pedidos com seus itens sem eager loading, pode acabar com N+1+M consultas. Por isso, usar Pedido::with("user", "itens.produto") é uma prática essencial. Você verá isso em duas situações: (1) listagens (index) e (2) telas de edição/resumo (edit/show).

Formas comuns de eager loading no Laravel:

- `with()` — Usado na query antes de executar (ex.: Pedido::with(...)->paginate()).
- `load()` — Usado após já ter um model (ex.: $pedido->load(...)).
- `Relação aninhada` — Carregar itens e produto junto: with("itens.produto").

> **Exemplo aplicado no passo a passo (Cap. 6)**
>
> No PedidoController@index (seção 4.5), você usa Pedido::with("user") para não fazer uma consulta de usuário para cada pedido. No PedidoController@edit, você faz $pedido->load("itens.produto") para carregar itens e seus produtos antes de renderizar a view. Isso evita consultas extras dentro do loop @forelse($pedido->itens as $item) em pedidos/edit.blade.php (seção 4.7).

### 4) Passo a passo guiado — Fluxo de Pedido (sem AJAX ainda)

Meta: criar tabelas/models de Pedido e ItemPedido, iniciar pedido e adicionar itens com formulário normal.

#### 4.1. Criar Models e Migrations

No terminal, dentro do projeto:

**Shell**

```bash
php artisan make:model Pedido -m
php artisan make:model ItemPedido -m
php artisan make:controller PedidoController --resource
php artisan make:controller ItemPedidoController
```

#### 4.2. Migrations: pedidos e itens_pedido

Edite a migration de pedidos (`create_pedidos_table`):

**PHP**

```php
public function up(): void
{
    Schema::create('pedidos', function (Blueprint $table) {
        $table->id();
        $table->foreignId('user_id')->constrained('users');
        $table->string('status')->default('aberto'); // aberto, em_preparo, pronto, entregue, fechado
        $table->decimal('total', 10, 2)->default(0);
        $table->text('observacoes')->nullable();
        $table->timestamps();
    });
}
```

Edite a migration de itens (`create_item_pedidos_table`):

**PHP**

```php
public function up(): void
{
    Schema::create('item_pedidos', function (Blueprint $table) {
        $table->id();
        $table->foreignId('pedido_id')->constrained('pedidos')->cascadeOnDelete();
        $table->foreignId('produto_id')->constrained('produtos');
        $table->unsignedInteger('quantidade')->default(1);
        $table->decimal('preco_unitario', 10, 2)->default(0);
        $table->decimal('subtotal', 10, 2)->default(0);
        $table->timestamps();

        // Evita o mesmo produto duplicado no mesmo pedido (opcional)
        $table->unique(['pedido_id', 'produto_id']);
    });
}
```

Execute as migrations:

**Shell**

```bash
php artisan migrate
```

#### 4.3. Models Eloquent: relações

`app/Models/Pedido.php`:

**PHP**

```php
<?php

namespace App\Models;

use Illuminate\Database\Eloquent\Model;
use Illuminate\Database\Eloquent\Factories\HasFactory;

class Pedido extends Model
{
    use HasFactory;

    protected $table = 'pedidos';

    protected $fillable = [
        'user_id',
        'status',
        'total',
        'observacoes',
    ];

    public function user()
    {
        return $this->belongsTo(User::class);
    }

    public function itens()
    {
        return $this->hasMany(ItemPedido::class, 'pedido_id');
    }
}
```

`app/Models/ItemPedido.php`:

**PHP**

```php
<?php

namespace App\Models;

use Illuminate\Database\Eloquent\Model;
use Illuminate\Database\Eloquent\Factories\HasFactory;

class ItemPedido extends Model
{
    use HasFactory;

    protected $table = 'item_pedidos';

    protected $fillable = [
        'pedido_id',
        'produto_id',
        'quantidade',
        'preco_unitario',
        'subtotal',
    ];

    public function pedido()
    {
        return $this->belongsTo(Pedido::class, 'pedido_id');
    }

    public function produto()
    {
        return $this->belongsTo(Produto::class, 'produto_id');
    }
}
```

#### 4.4. Rotas: Pedido resource + rotas para itens

Em `routes/web.php` (dentro do grupo `auth`):

**PHP**

```php
use App\Http\Controllers\PedidoController;
use App\Http\Controllers\ItemPedidoController;

Route::middleware(['auth'])->group(function () {
    Route::resource('pedidos', PedidoController::class);

    // rotas para itens de um pedido
    Route::post('pedidos/{pedido}/itens', [ItemPedidoController::class, 'store'])->name('pedidos.itens.store');
    Route::delete('pedidos/{pedido}/itens/{itemPedido}', [ItemPedidoController::class, 'destroy'])->name('pedidos.itens.destroy');
});
```

#### 4.5. PedidoController: criar pedido e editar para adicionar itens

Implementação mínima (sem Form Request por enquanto):

**PHP**

```php
<?php

namespace App\Http\Controllers;

use App\Models\Pedido;
use Illuminate\Http\Request;

class PedidoController extends Controller
{
    public function index()
    {
        $pedidos = Pedido::with('user')
            ->orderByDesc('id')
            ->paginate(10);

        return view('pedidos.index', compact('pedidos'));
    }

    public function create()
    {
        return view('pedidos.create');
    }

    public function store(Request $request)
    {
        $pedido = Pedido::create([
            'user_id' => auth()->id(),
            'status' => 'aberto',
            'total' => 0,
            'observacoes' => $request->input('observacoes'),
        ]);

        return redirect()->route('pedidos.edit', $pedido)
            ->with('sucesso', 'Pedido iniciado! Agora adicione itens.');
    }

    public function edit(Pedido $pedido)
    {
        $pedido->load('itens.produto');
        $produtos = \App\Models\Produto::orderBy('nome')->get();

        return view('pedidos.edit', compact('pedido', 'produtos'));
    }

    // update e destroy podem ser evoluídos nas atividades
}
```

#### 4.6. ItemPedidoController: adicionar e remover itens + recalcular total

Regra: subtotal = quantidade × preco_unitario (do produto no momento), e total do pedido = soma dos subtotais.

**PHP**

```php
<?php

namespace App\Http\Controllers;

use App\Models\Pedido;
use App\Models\ItemPedido;
use App\Models\Produto;
use Illuminate\Http\Request;

class ItemPedidoController extends Controller
{
    public function store(Request $request, Pedido $pedido)
    {
        $dados = $request->validate([
            'produto_id' => 'required|exists:produtos,id',
            'quantidade' => 'required|integer|min:1|max:99',
        ]);

        $produto = Produto::findOrFail($dados['produto_id']);

        $preco = $produto->preco;
        $subtotal = $preco * $dados['quantidade'];

        // Se já existir item do produto no pedido, atualiza a quantidade (opcional)
        $item = ItemPedido::where('pedido_id', $pedido->id)
            ->where('produto_id', $produto->id)
            ->first();

        if ($item) {
            $item->quantidade += $dados['quantidade'];
            $item->preco_unitario = $preco;
            $item->subtotal = $item->quantidade * $preco;
            $item->save();
        } else {
            ItemPedido::create([
                'pedido_id' => $pedido->id,
                'produto_id' => $produto->id,
                'quantidade' => $dados['quantidade'],
                'preco_unitario' => $preco,
                'subtotal' => $subtotal,
            ]);
        }

        // Recalcular total
        $pedido->total = ItemPedido::where('pedido_id', $pedido->id)->sum('subtotal');
        $pedido->save();

        return redirect()->route('pedidos.edit', $pedido)
            ->with('sucesso', 'Item adicionado ao pedido!');
    }

    public function destroy(Pedido $pedido, ItemPedido $itemPedido)
    {
        // Garante que o item pertence ao pedido
        abort_unless($itemPedido->pedido_id === $pedido->id, 404);

        $itemPedido->delete();

        $pedido->total = ItemPedido::where('pedido_id', $pedido->id)->sum('subtotal');
        $pedido->save();

        return redirect()->route('pedidos.edit', $pedido)
            ->with('sucesso', 'Item removido!');
    }
}
```

#### 4.7. Views Blade (index, create, edit)

Crie a pasta `resources/views/pedidos/`.

`resources/views/pedidos/index.blade.php`:

**PHP**

```php
@extends('layouts.app')
@section('title', 'Pedidos')
@section('content')
    @include('partials.alerts')

    <div class="d-flex justify-content-between align-items-center mb-3">
        <h2>Pedidos</h2>
        <a class="btn btn-primary" href="{{ route('pedidos.create') }}">Novo Pedido</a>
    </div>

    <div class="card">
        <div class="card-body p-0">
            <table class="table table-striped mb-0">
                <thead class="table-light">
                    <tr>
                        <th>#</th>
                        <th>Atendente</th>
                        <th>Status</th>
                        <th class="text-end">Total</th>
                        <th class="text-end">Ações</th>
                    </tr>
                </thead>
                <tbody>
                    @forelse($pedidos as $p)
                        <tr>
                            <td>{{ $p->id }}</td>
                            <td>{{ $p->user->name ?? '—' }}</td>
                            <td>{{ $p->status }}</td>
                            <td class="text-end">R$ {{ number_format($p->total, 2, ',', '.') }}</td>
                            <td class="text-end">
                                <a class="btn btn-sm btn-outline-secondary" href="{{ route('pedidos.edit', $p) }}">Abrir</a>
                            </td>
                        </tr>
                    @empty
                        <tr><td colspan="5" class="text-center p-4 text-muted">Nenhum pedido.</td></tr>
                    @endforelse
                </tbody>
            </table>
        </div>
    </div>

    <div class="mt-3">{{ $pedidos->links() }}</div>
@endsection
```

`resources/views/pedidos/create.blade.php`:

**PHP**

```php
@extends('layouts.app')
@section('title', 'Novo Pedido')
@section('content')
    @include('partials.alerts')

    <h2 class="mb-3">Iniciar Pedido</h2>

    <form method="POST" action="{{ route('pedidos.store') }}">
        @csrf
        <div class="mb-3">
            <label class="form-label">Observações (opcional)</label>
            <textarea name="observacoes" class="form-control" rows="3">{{ old('observacoes') }}</textarea>
        </div>
        <button class="btn btn-primary">Criar e adicionar itens</button>
        <a class="btn btn-outline-secondary" href="{{ route('pedidos.index') }}">Cancelar</a>
    </form>
@endsection
```

`resources/views/pedidos/edit.blade.php` (adicionar itens + listar itens):

**PHP**

```php
@extends('layouts.app')
@section('title', 'Editar Pedido')
@section('content')
    @include('partials.alerts')

    <div class="d-flex justify-content-between align-items-center mb-3">
        <h2>Pedido #{{ $pedido->id }}</h2>
        <a class="btn btn-outline-secondary" href="{{ route('pedidos.index') }}">Voltar</a>
    </div>

    <div class="row g-3">
        <div class="col-lg-5">
            <div class="card">
                <div class="card-body">
                    <h5 class="fw-bold">Adicionar item</h5>
                    <form method="POST" action="{{ route('pedidos.itens.store', $pedido) }}">
                        @csrf
                        <div class="mb-3">
                            <label class="form-label">Produto</label>
                            <select name="produto_id" class="form-select" required>
                                <option value="">Selecione...</option>
                                @foreach($produtos as $prod)
                                    <option value="{{ $prod->id }}">{{ $prod->nome }} (R$ {{ number_format($prod->preco,2,',','.') }})</option>
                                @endforeach
                            </select>
                        </div>
                        <div class="mb-3">
                            <label class="form-label">Quantidade</label>
                            <input type="number" name="quantidade" class="form-control" value="1" min="1" max="99" required>
                        </div>
                        <button class="btn btn-primary">Adicionar</button>
                    </form>
                </div>
            </div>
        </div>

        <div class="col-lg-7">
            <div class="card">
                <div class="card-body">
                    <h5 class="fw-bold">Itens do pedido</h5>

                    <table class="table table-sm align-middle">
                        <thead>
                            <tr>
                                <th>Produto</th>
                                <th class="text-end">Qtd</th>
                                <th class="text-end">Unit.</th>
                                <th class="text-end">Subtotal</th>
                                <th class="text-end">Ações</th>
                            </tr>
                        </thead>
                        <tbody>
                            @forelse($pedido->itens as $item)
                                <tr>
                                    <td>{{ $item->produto->nome ?? '—' }}</td>
                                    <td class="text-end">{{ $item->quantidade }}</td>
                                    <td class="text-end">R$ {{ number_format($item->preco_unitario,2,',','.') }}</td>
                                    <td class="text-end">R$ {{ number_format($item->subtotal,2,',','.') }}</td>
                                    <td class="text-end">
                                        <form method="POST" action="{{ route('pedidos.itens.destroy', [$pedido, $item]) }}" class="d-inline"
                                              onsubmit="return confirm('Remover este item?')">
                                            @csrf
                                            @method('DELETE')
                                            <button class="btn btn-sm btn-outline-danger">Remover</button>
                                        </form>
                                    </td>
                                </tr>
                            @empty
                                <tr><td colspan="5" class="text-center text-muted p-3">Nenhum item ainda.</td></tr>
                            @endforelse
                        </tbody>
                    </table>

                    <div class="d-flex justify-content-end">
                        <div class="fw-bold">Total: R$ {{ number_format($pedido->total,2,',','.') }}</div>
                    </div>

                </div>
            </div>
        </div>
    </div>
@endsection
```

#### 4.8. Link no menu para Pedidos

Em sua navbar, inclua um link para pedidos (visível para usuários autenticados):

**PHP**

```php
@auth
    <li class="nav-item">
        <a class="nav-link" href="{{ route('pedidos.index') }}">Pedidos</a>
    </li>
@endauth
```

#### 4.9. Commit no Git

**Shell**

```bash
git add .
git commit -m "Capítulo 6: relacionamentos (Pedido/ItemPedido) + fluxo de pedido"
git push
```

### 5) Atividades correlatas (para a Semana B)

Objetivo: consolidar relacionamentos, regras de negócio e telas de pedido. Entrega via repositório (commit + push).

1. **Calcular total do pedido de forma consistente**
    - Recalcular total também ao atualizar quantidade (crie rota e formulário para editar item).
    - Exibir resumo do pedido com total, status e observações.
2. **Status do pedido (aberto, em preparo, pronto, entregue, fechado)**
    - Adicionar botão/ação para mudar status (ex.: “Enviar para preparo”).
    - Regra: pedidos “fechados” não podem ser editados (bloquear add/remover itens).
3. **Integridade e performance**
    - Usar `with('itens.produto')` na listagem/visualização para evitar N+1.
    - Criar um relatório simples: pedidos do dia (apenas tabela na view).

> **Plus (opcional)**
>
> Criar um model `Cliente` e relacionar pedido a cliente (belongsTo), com campo opcional.

### 6) Pesquisas complementares (para aprofundar)

- Relacionamentos: diferença entre `hasMany`, `belongsTo` e `belongsToMany`.
- Eager loading: como `with()` evita N+1 e como medir consultas (debugbar/log).
- Regras de negócio: por que salvar `preco_unitario` no item (histórico) é importante.
- Integridade referencial: por que usar FK com `constrained()` e o que é `cascadeOnDelete()`.
- UX: como melhorar a tela de pedido antes de usar AJAX (Cap. 7) — ex.: agrupamento e mensagens.
### 9) Entregáveis do capítulo

1. Repositório com migrations/models/controllers e views de Pedido e ItemPedido.
2. Fluxo funcionando: iniciar pedido → adicionar itens → remover itens → total atualizado.
3. Capturas de tela em `docs/`: (a) lista de pedidos, (b) tela de adicionar itens, (c) total atualizado.

---

## Capítulo 07 — Requisições Assíncronas (AJAX) no Laravel/Blade

**Carga horária:** 2 semanas (100 min/semana)

**Formato das aulas:**

- Semana A (100 min): Conceitos + demonstração do professor + início do passo a passo.
- Semana B (100 min): Conclusão do passo a passo + atividades correlatas + revisão.

> Contexto do projeto: pedidos e itens já existem (Cap. 6). Agora vamos deixar a tela de pedido “responsiva” sem recarregar a página.

### 1) Objetivos de aprendizagem

Ao final deste capítulo, o(a) aluno(a) será capaz de:

- Explicar o que é AJAX e por que melhora a experiência do usuário (sem recarregar a página).
- Fazer requisições assíncronas usando `fetch()` e trabalhar com JSON.
- Criar rotas que retornam JSON no Laravel e usar códigos de status (200/201/422/403/404).
- Atualizar a UI do pedido dinamicamente: adicionar/remover item e atualizar total.
- Implementar tratamento de erros e mensagens (toast) para sucesso/erro.
### 2) Pré-requisitos e ferramentas

- Pré-requisitos: Cap. 6 concluído (Pedido e ItemPedido com tela edit funcionando) e autenticação (Cap. 5).
- Ferramentas: VS Code, Git, MySQL, navegador com DevTools (aba Network/Console).
- Opcional: Postman/Insomnia para testar endpoints JSON (Cap. 8 aprofunda documentação/testes).
### 3) Conteúdo teórico

#### 3.1. O que é AJAX (moderno)

AJAX é um conjunto de técnicas para fazer requisições HTTP em segundo plano e atualizar apenas partes da página, sem recarregar tudo. O nome original (Asynchronous JavaScript and XML) aparece muito em livros antigos, mas hoje quase sempre trocamos dados em JSON. O ponto central não é a sigla, e sim a experiência: o usuário interage com a tela e recebe retorno rápido, com menos “piscar” de página e sem perder o contexto (scroll, campos preenchidos, foco do cursor).

Em uma aplicação tradicional (sem AJAX), ao enviar um formulário o navegador faz um POST e recarrega a página inteira após o redirecionamento. Esse fluxo é estável e simples, mas pode deixar a interface lenta em operações repetitivas, como adicionar vários itens em um pedido. Com AJAX, a tela continua “viva”: o front envia somente os dados necessários (produto_id e quantidade), o servidor responde com um JSON contendo o item criado/atualizado e o novo total, e o JavaScript atualiza a tabela e o total na hora.

É importante entender que AJAX não elimina o backend — ele apenas muda a forma de comunicação. Você continua tendo rotas, controllers, validação e regras de negócio no Laravel. A diferença é que, em vez de responder com HTML e redirecionar, você responde com JSON e um status HTTP apropriado. Isso permite que o JavaScript decida como atualizar a interface. Em termos de arquitetura, você está criando uma “mini-API interna” para melhorar a UX.

Benefícios e cuidados comuns ao adotar AJAX:

- `Melhor UX` — Atualiza somente o que mudou e mantém o usuário no contexto.
- `Menos tráfego` — Em geral, troca menos HTML e envia/recebe apenas dados.
- `Depuração` — Você precisa usar DevTools (Network/Console) para acompanhar requests.
- `Atenção a estados` — A UI precisa tratar loading, sucesso e erro para não confundir o usuário.

> **Exemplo aplicado no passo a passo (Cap. 7)**
>
> Na seção 4.4, o formulário “Adicionar (AJAX)” deixa de recarregar a página: você intercepta o submit, envia os dados com fetch() para a rota JSON (seção 4.2) e, quando recebe o JSON, chama upsertRow() para atualizar/inserir a linha na tabela e setTotal() para atualizar o total. O usuário percebe o ganho ao adicionar vários itens seguidos sem refresh.

#### 3.2. JSON, headers e códigos de status

JSON (JavaScript Object Notation) é um formato de dados leve e fácil de ler, baseado em objetos e listas. Ele é muito usado porque funciona bem no navegador, no servidor e em ferramentas de teste. Em uma requisição AJAX, o ideal é que o servidor responda sempre em JSON (inclusive em caso de erro), para que o front consiga tratar a resposta de forma consistente.

Para “negociar” o formato da resposta, usamos headers. O mais importante aqui é Accept: application/json, que diz ao servidor: “eu espero JSON como resposta”. No Laravel, esse header faz diferença principalmente em erros de validação: com Accept: application/json, o framework tende a devolver 422 com um corpo JSON contendo message e errors, em vez de redirecionar de volta ao formulário com sessão.

O Content-Type (quando você envia JSON) indica o formato do corpo da requisição. Porém, neste capítulo, você envia FormData no fetch, então não precisa setar manualmente Content-Type: o navegador define o boundary corretamente. Se você setar Content-Type errado ao enviar FormData, o servidor pode não conseguir ler os dados. Por isso, a regra prática é: (1) FormData → não setar Content-Type; (2) JSON.stringify(...) → setar Content-Type: application/json.

Códigos de status HTTP tornam a comunicação mais “profissional”: o front entende rapidamente se foi sucesso ou erro. Em AJAX, usar status corretos é ainda mais importante porque você não está navegando entre páginas — você precisa saber se deve atualizar a UI, mostrar toast de sucesso, ou exibir erros de validação. Os status mais comuns aqui são: 200/201 (sucesso), 422 (validação), 403 (proibido), 404 (não encontrado), e ocasionalmente 500 (erro inesperado).

Mapa rápido de status e o que o front deve fazer:

- `200 OK` — Atualizar UI e mostrar confirmação.
- `201 Created` — Semelhante ao 200, mas indica criação de recurso.
- `422 Unprocessable Entity` — Exibir mensagens de validação (data.errors) e manter o usuário no formulário.
- `403 Forbidden` — Informar falta de permissão e possivelmente redirecionar/ocultar ações.
- `404 Not Found` — Informar que o recurso não existe (pedido/item removido, id inválido).

> **Exemplo aplicado no passo a passo (Cap. 7)**
>
> Na seção 4.4, o fetch envia o header Accept: application/json. Assim, se a validação falhar no storeJson (seção 4.3), o Laravel responde com 422 e JSON. O script verifica resp.ok; se não for ok, mostra um toast de erro e você consegue inspecionar data.errors no console. Quando dá certo, o JSON retorna o item e o novo total, e a UI é atualizada.

#### 3.3. CSRF em requisições AJAX

Mesmo usando AJAX, você continua fazendo requisições para rotas web (routes/web.php) que são protegidas por CSRF no Laravel. CSRF é a proteção contra um ataque em que um site externo tenta disparar uma ação no seu sistema usando a sessão do usuário. Por isso, toda requisição que altera dados (POST/PUT/PATCH/DELETE) precisa carregar o token CSRF válido.

Em formulários Blade, o token entra com @csrf automaticamente. Em AJAX, você precisa enviar o token manualmente. O padrão mais prático é colocar o token em uma meta tag no layout (`<meta name="csrf-token" ...>`) e, no JavaScript, ler esse valor e enviá-lo no header X-CSRF-TOKEN. Assim, você não precisa “injetar” o token em cada script, e mantém um único ponto de configuração.

Além do token, é boa prática enviar Accept: application/json para que, em caso de erro (incluindo 419/CSRF inválido, 422/validação), você receba uma resposta que o front possa tratar. E lembre-se: CSRF está ligado a sessão; em rotas de API (routes/api.php) normalmente se usa token (Sanctum/Passport) e CSRF não é aplicado da mesma forma. Neste capítulo, como estamos no mundo Blade + sessão, CSRF é obrigatório.

Checklist mental para AJAX seguro em rotas web:

- `Token disponível no HTML` — Adicionar meta csrf-token no layout.
- `Enviar token no header` — X-CSRF-TOKEN: csrfToken().
- `Usar métodos corretos` — POST para adicionar, DELETE para remover, PATCH para atualizar quantidade (atividade).
- `Tratar erros` — Mostrar feedback e logar detalhes no console para depurar.

> **Exemplo aplicado no passo a passo (Cap. 7)**
>
> Na seção 4.1, você adiciona a meta csrf-token no layout. Na seção 4.4, a função csrfToken() lê a meta e o fetch envia X-CSRF-TOKEN em POST e DELETE. Sem isso, você veria erro de CSRF (geralmente 419). Com o token correto, as rotas storeJson/destroyJson funcionam e o front consegue atualizar a tabela e o total em tempo real.

### 4) Passo a passo guiado — Pedido com AJAX (fetch + JSON)

Meta: criar endpoints JSON e atualizar a tela de pedido sem recarregar.

#### 4.1. Inserir CSRF token no layout (meta)

Edite `resources/views/layouts/app.blade.php` e adicione no `<head>`:

**PHP**

```php
<meta name="csrf-token" content="{{ csrf_token() }}">
```

#### 4.2. Criar rotas JSON para itens do pedido

Em `routes/web.php` (dentro do grupo `auth`):

**PHP**

```php
use App\Http\Controllers\ItemPedidoController;

Route::post('pedidos/{pedido}/itens-json', [ItemPedidoController::class, 'storeJson'])
    ->name('pedidos.itens.storeJson');

Route::delete('pedidos/{pedido}/itens-json/{itemPedido}', [ItemPedidoController::class, 'destroyJson'])
    ->name('pedidos.itens.destroyJson');
```

#### 4.3. Implementar métodos JSON no ItemPedidoController

Adicione dois métodos: `storeJson` e `destroyJson`.

**PHP**

```php
public function storeJson(Request $request, Pedido $pedido)
{
    $dados = $request->validate([
        'produto_id' => 'required|exists:produtos,id',
        'quantidade' => 'required|integer|min:1|max:99',
    ]);

    $produto = Produto::findOrFail($dados['produto_id']);

    $preco = $produto->preco;

    $item = ItemPedido::where('pedido_id', $pedido->id)
        ->where('produto_id', $produto->id)
        ->first();

    if ($item) {
        $item->quantidade += $dados['quantidade'];
        $item->preco_unitario = $preco;
        $item->subtotal = $item->quantidade * $preco;
        $item->save();
    } else {
        $item = ItemPedido::create([
            'pedido_id' => $pedido->id,
            'produto_id' => $produto->id,
            'quantidade' => $dados['quantidade'],
            'preco_unitario' => $preco,
            'subtotal' => $dados['quantidade'] * $preco,
        ]);
    }

    $pedido->total = ItemPedido::where('pedido_id', $pedido->id)->sum('subtotal');
    $pedido->save();

    $item->load('produto');

    return response()->json([
        'message' => 'Item adicionado!',
        'pedido' => [
            'id' => $pedido->id,
            'total' => (float) $pedido->total,
        ],
        'item' => [
            'id' => $item->id,
            'produto' => [
                'id' => $item->produto->id,
                'nome' => $item->produto->nome,
            ],
            'quantidade' => (int) $item->quantidade,
            'preco_unitario' => (float) $item->preco_unitario,
            'subtotal' => (float) $item->subtotal,
        ]
    ], 200);
}

public function destroyJson(Pedido $pedido, ItemPedido $itemPedido)
{
    abort_unless($itemPedido->pedido_id === $pedido->id, 404);

    $itemPedido->delete();

    $pedido->total = ItemPedido::where('pedido_id', $pedido->id)->sum('subtotal');
    $pedido->save();

    return response()->json([
        'message' => 'Item removido!',
        'pedido' => [
            'id' => $pedido->id,
            'total' => (float) $pedido->total,
        ],
        'removed_item_id' => (int) $itemPedido->id,
    ], 200);
}
```

> **Dica de depuração**
>
> Abra o DevTools (F12) → Network para ver o request e a resposta JSON.

#### 4.4. Atualizar a view do pedido para enviar via fetch

No `resources/views/pedidos/edit.blade.php`, troque o formulário de adicionar item por um formulário com id e evite submit padrão. Exemplo (apenas o bloco do form):

**PHP**

```php
<form id="formAddItem">
    @csrf
    <div class="mb-3">
        <label class="form-label">Produto</label>
        <select name="produto_id" class="form-select" required>
            <option value="">Selecione...</option>
            @foreach($produtos as $prod)
                <option value="{{ $prod->id }}">{{ $prod->nome }} (R$ {{ number_format($prod->preco,2,',','.') }})</option>
            @endforeach
        </select>
    </div>
    <div class="mb-3">
        <label class="form-label">Quantidade</label>
        <input type="number" name="quantidade" class="form-control" value="1" min="1" max="99" required>
    </div>
    <button class="btn btn-primary" type="submit">Adicionar (AJAX)</button>
</form>

<script>
  window.PW3 = {
    pedidoId: {{ $pedido->id }},
    urlAdd: "{{ route('pedidos.itens.storeJson', $pedido) }}",
    urlDelBase: "{{ url('pedidos/'.$pedido->id.'/itens-json') }}"
  };
</script>
```

Agora, adicione um script (no final da view) para interceptar o submit e atualizar a tabela. Você pode manter a tabela com um `<tbody id="itensBody">`.

**JavaScript**

```javascript
function csrfToken() {
  return document.querySelector('meta[name="csrf-token"]').getAttribute('content');
}

function moneyBR(value) {
  return (value ?? 0).toLocaleString('pt-BR', { style: 'currency', currency: 'BRL' });
}

function showToast(title, body) {
  const el = document.getElementById('pw3Toast');
  document.getElementById('pw3ToastTitle').textContent = title;
  document.getElementById('pw3ToastBody').textContent = body;
  const toast = bootstrap.Toast.getOrCreateInstance(el, { delay: 2500 });
  toast.show();
}

function upsertRow(item) {
  const tbody = document.getElementById('itensBody');
  let row = document.getElementById('item-' + item.id);

  const html = `
    <tr id="item-${item.id}">
      <td>${item.produto.nome}</td>
      <td class="text-end">${item.quantidade}</td>
      <td class="text-end">${moneyBR(item.preco_unitario)}</td>
      <td class="text-end">${moneyBR(item.subtotal)}</td>
      <td class="text-end">
        <button class="btn btn-sm btn-outline-danger" data-remove="${item.id}">Remover</button>
      </td>
    </tr>`;

  if (row) {
    row.outerHTML = html;
  } else {
    tbody.insertAdjacentHTML('beforeend', html);
  }
}

function removeRow(itemId) {
  const row = document.getElementById('item-' + itemId);
  if (row) row.remove();
}

function setTotal(total) {
  document.getElementById('pedidoTotal').textContent = moneyBR(total);
}

document.getElementById('formAddItem').addEventListener('submit', async (e) => {
  e.preventDefault();

  const form = e.currentTarget;
  const fd = new FormData(form);

  try {
    const resp = await fetch(window.PW3.urlAdd, {
      method: 'POST',
      headers: {
        'X-CSRF-TOKEN': csrfToken(),
        'Accept': 'application/json'
      },
      body: fd
    });

    const data = await resp.json();

    if (!resp.ok) {
      // 422 validação vem com errors
      const msg = data.message || 'Erro ao adicionar item.';
      showToast('Erro', msg);
      console.error(data);
      return;
    }

    upsertRow(data.item);
    setTotal(data.pedido.total);
    showToast('Sucesso', data.message);

    // reset rápido
    form.quantidade.value = 1;
    form.produto_id.value = '';

  } catch (err) {
    console.error(err);
    showToast('Erro', 'Falha de conexão. Verifique servidor e console.');
  }
});

// Delegação de evento para botões remover
document.getElementById('itensBody').addEventListener('click', async (e) => {
  const btn = e.target.closest('[data-remove]');
  if (!btn) return;

  const itemId = btn.getAttribute('data-remove');
  if (!confirm('Remover este item?')) return;

  try {
    const resp = await fetch(`${window.PW3.urlDelBase}/${itemId}`, {
      method: 'DELETE',
      headers: {
        'X-CSRF-TOKEN': csrfToken(),
        'Accept': 'application/json'
      }
    });

    const data = await resp.json();

    if (!resp.ok) {
      showToast('Erro', data.message || 'Erro ao remover.');
      console.error(data);
      return;
    }

    removeRow(data.removed_item_id);
    setTotal(data.pedido.total);
    showToast('Sucesso', data.message);

  } catch (err) {
    console.error(err);
    showToast('Erro', 'Falha de conexão.');
  }
});
```

> **Resultado esperado**
>
> Adicionar/remover itens sem recarregar a página, com atualização do total e toast de feedback.

#### 4.5. Ajuste mínimo na tabela para suportar atualização dinâmica

Na tabela de itens do pedido, garanta:

- `<tbody id="itensBody">`
- total exibido em `<span id="pedidoTotal">`
**PHP**

```php
<tbody id="itensBody">
  @foreach($pedido->itens as $item)
    <tr id="item-{{ $item->id }}">
      <td>{{ $item->produto->nome }}</td>
      <td class="text-end">{{ $item->quantidade }}</td>
      <td class="text-end">R$ {{ number_format($item->preco_unitario,2,',','.') }}</td>
      <td class="text-end">R$ {{ number_format($item->subtotal,2,',','.') }}</td>
      <td class="text-end">
        <button class="btn btn-sm btn-outline-danger" data-remove="{{ $item->id }}">Remover</button>
      </td>
    </tr>
  @endforeach
</tbody>

<div class="fw-bold">Total: <span id="pedidoTotal">R$ {{ number_format($pedido->total,2,',','.') }}</span></div>
```

#### 4.6. Commit no Git

**Shell**

```bash
git add .
git commit -m "Capítulo 7: AJAX (fetch) no pedido + endpoints JSON + UI dinâmica"
git push
```

### 5) Atividades correlatas (para a Semana B)

Objetivo: consolidar AJAX, tratamento de erros e melhorias de UX. Entrega via repositório (commit + push).

1. **Remover item via AJAX (já base) + confirmação e estado de loading**
    - Desabilitar botão enquanto o request está em andamento.
    - Mostrar spinner no botão “Adicionar (AJAX)”.
2. **Atualizar quantidade via AJAX com debounce**
    - Criar endpoint `PATCH` para alterar quantidade de item.
    - No front, colocar input number na tabela e enviar após 400ms sem digitar (debounce).
3. **Mostrar toast de confirmação/erro (melhorar mensagens)**
    - Em validação 422, listar quais campos estão inválidos.
    - Exibir mensagens amigáveis em português.

> **Plus (opcional)**
>
> Criar um “mini-carrinho” no topo da página mostrando quantidade de itens e total atualizando em tempo real.

### 6) Pesquisas complementares (para aprofundar)

- Fetch API: diferenças entre enviar FormData e JSON (Content-Type e parsing).
- Códigos de status: quando usar 201, 204, 409 e 422 em APIs.
- Tratamento de erros: boas práticas para padronizar respostas JSON no Laravel.
- UX: debounce, optimistic UI e acessibilidade em interações assíncronas.
- Segurança: por que CSRF importa em rotas web e quando usar rotas de API (api.php) com tokens.
### 9) Entregáveis do capítulo

1. Repositório com endpoints JSON (storeJson/destroyJson) e rotas configuradas.
2. Tela de pedido (edit) atualizando itens e total sem recarregar (AJAX).
3. Capturas de tela em `docs/`: (a) Network mostrando resposta JSON, (b) item adicionado sem refresh, (c) toast de confirmação.

---

## Capítulo 08 — Consumindo APIs Públicas + Postman

**Carga horária:** 2 semanas (100 min/semana)

**Formato das aulas:**

- Semana A (100 min): Teoria + demonstração + início do passo a passo.
- Semana B (100 min): Conclusão do passo a passo + atividades correlatas + revisão.

> Contexto do projeto: pedidos com AJAX (Cap. 7). Agora vamos integrar uma API pública para preencher endereço de entrega e documentar/testar com Postman.

### 1) Objetivos de aprendizagem

Ao final deste capítulo, o(a) aluno(a) será capaz de:

- Consumir uma API pública no Laravel com `Http` (cliente HTTP do framework).
- Tratar erros de rede, timeouts e respostas inválidas.
- Usar cache simples para reduzir chamadas repetidas (ex.: CEP consultado várias vezes).
- Integrar o consumo da API no front (autopreencher endereço via AJAX).
- Criar uma coleção no Postman (com variáveis/ambiente) e salvar exemplos de requisições.
### 2) Pré-requisitos e ferramentas

- Pré-requisitos: Cap. 5 a 7 (autenticação, pedidos e AJAX) funcionando.
- Ferramentas: VS Code, Git, MySQL, navegador, Postman (obrigatório neste capítulo).
- Recomendado: ter uma tela de “pedido/entrega” ou uma seção de endereço no pedido para o preenchimento via CEP.
### 3) Conteúdo teórico

#### 3.1. Consumindo APIs públicas com responsabilidade

Consumir uma API pública significa que sua aplicação passa a depender de um serviço que você não controla. Isso traz vantagens (dados prontos, integração rápida, redução de trabalho) mas também cria riscos: o serviço pode ficar fora do ar, pode demorar a responder, pode mudar o formato da resposta, ou impor limites de uso (rate limiting). Se você não tratar esses cenários, o usuário percebe travamentos e erros confusos — e o sistema “parece quebrado” mesmo quando o problema está no serviço externo.

Para consumir APIs de forma responsável, você precisa aplicar alguns princípios básicos: (1) definir timeout para não ficar esperando indefinidamente; (2) tratar falhas e devolver mensagens amigáveis; (3) validar o que veio na resposta antes de usar; (4) reduzir chamadas repetidas com cache; e (5) registrar logs para facilitar diagnóstico quando algo falhar. No Laravel, o HTTP Client (facade Http) ajuda muito porque já trabalha bem com JSON, headers, timeouts e métodos como retry().

Outro cuidado importante é separar “erro do usuário” de “erro do serviço”. Se o CEP tem formato inválido (menos de 8 dígitos), isso é erro de validação do usuário e deve retornar 422 com uma mensagem clara. Se o ViaCEP não encontra o CEP, isso é “não encontrado” e faz sentido retornar 404 com message. Se o ViaCEP estiver lento ou indisponível, você pode retornar um status de erro (muitas vezes 503 Service Unavailable) e orientar o usuário a tentar novamente. Essa distinção melhora a UX e facilita depuração.

Boas práticas resumidas ao integrar uma API externa:

- `Timeout` — Evita travar a aplicação esperando resposta.
- `Validação` — Garante que você não usa dados inválidos/inesperados.
- `Tratamento de erro` — Retorna mensagens claras e status adequados.
- `Cache` — Reduz chamadas repetidas e risco de bloqueio por excesso.
- `Logs` — Ajudam a entender falhas em produção ou laboratório.

> **Exemplo aplicado no passo a passo (Cap. 8)**
>
> Na seção 4.2, o CepController normaliza o CEP (mantém só números), valida se tem 8 dígitos e, se não tiver, retorna 422 com errors. Depois, consulta o ViaCEP com Http::timeout(3)->acceptJson(). Se a API retornar erro ou demorar, você não trava o sistema; você devolve um JSON com message. Isso garante que o front (seção 4.4) consiga tratar sucesso/erro com toast.

#### 3.2. Timeouts e tratamento de erro

Timeout é um limite máximo de tempo que sua aplicação está disposta a esperar por uma resposta. Sem timeout, uma requisição a um serviço externo pode ficar pendurada, segurando recursos do servidor e atrasando o usuário. Em ambientes de aula, isso aparece como “não acontece nada” e o aluno fica perdido. Portanto, timeout não é “otimização”: é estabilidade e previsibilidade.

Além do timeout, você precisa tratar a resposta e decidir o que fazer com cada caso. Existem pelo menos quatro classes de problema: (1) erro do usuário (entrada inválida); (2) erro do serviço externo (fora do ar, DNS, timeout); (3) erro de “não encontrado” (o serviço respondeu, mas não existe aquele recurso, como CEP inexistente); e (4) erro interno (bug seu). Um bom endpoint interno (no seu Laravel) transforma essas situações em respostas consistentes, com JSON padronizado e status claros. Isso facilita o front: ele só precisa ler data.message e, se existir, data.errors.

Em APIs modernas, 422 Unprocessable Entity é muito usado para validação. 404 Not Found é usado quando o recurso não existe. 503 Service Unavailable indica indisponibilidade temporária. E 200 OK indica sucesso. Mesmo quando você decide mapear alguns erros externos como 404 (por simplicidade didática), o principal é manter consistência e dar feedback compreensível.

Dicas práticas de tratamento de erro em consumo de API:

- `Timeout curto e realista` — 2–5 segundos costuma ser suficiente para ViaCEP em ambiente normal.
- `Tratar !ok()` — Se o status HTTP não for 2xx, não assuma que existe JSON válido.
- `Tratar formato inesperado` — Verifique campos-chave (ex.: erro=true no ViaCEP) antes de usar.
- `Padronizar message/errors` — Facilita toasts e validação no front.

> **Exemplo aplicado no passo a passo (Cap. 8)**
>
> Na seção 4.2, o código usa Http::timeout(3) e verifica !$resp->ok() antes de usar $resp->json(). Isso evita quebrar o controller com resposta inválida. Também checa o campo erro=true do ViaCEP para identificar CEP inexistente e retorna um JSON com message, permitindo que o front mostre “CEP não encontrado” de forma amigável (seção 4.4).

#### 3.3. Cache: reduzindo chamadas repetidas

Cache é uma técnica para guardar temporariamente um resultado e reutilizá-lo em chamadas futuras, evitando repetir o mesmo trabalho. Quando o assunto é API externa, cache é ainda mais importante: ele reduz latência, diminui a dependência da internet e ajuda a evitar rate limits. No caso de CEP, o dado muda raramente, então é perfeito para cache: se várias pessoas consultarem o mesmo CEP, você pode responder instantaneamente na segunda vez.

O Laravel oferece Cache::remember(chave, tempo, função). A ideia é simples: se a chave existir, ele devolve o valor; se não existir, ele executa a função (que chama o ViaCEP), salva o resultado e devolve. Isso é ótimo para didática porque você consegue observar o comportamento: a primeira chamada demora mais (porque consulta a API), e as seguintes são rápidas.

O tempo de vida (TTL) do cache deve ser escolhido com equilíbrio: tempo curto reduz risco de dados desatualizados, mas aumenta chamadas; tempo longo reduz chamadas, mas pode manter dados antigos. Para CEP, um TTL de 10 minutos é seguro e simples para aula. Em produção, você poderia usar horas ou dias, dependendo do seu cenário. Também é importante considerar o driver de cache: em ambientes simples, file funciona; em ambientes maiores, Redis é mais eficiente.

Boas práticas de cache em integrações:

- `Chave bem definida` — Ex.: cep:01001000 (inclui o parâmetro).
- `TTL adequado` — Ex.: 10 min (aula) / 24h (produção, dependendo do caso).
- `Evitar cache de erro por muito tempo` — Se a API falhar, não faz sentido “congelar” erro por muito tempo.

> **Exemplo aplicado no passo a passo (Cap. 8)**
>
> Na seção 4.2, o código define $cacheKey = "cep:$cep" e usa Cache::remember(..., now()->addMinutes(10), function(){ ... }). Assim, quando você consultar o mesmo CEP várias vezes (pelo front ou pelo Postman), as próximas consultas tendem a ser mais rápidas e não dependem de nova chamada ao ViaCEP.

#### 3.4. Postman: testar, documentar e automatizar

Postman é uma ferramenta para testar requisições HTTP sem depender da interface do sistema. Isso é extremamente útil quando você está criando endpoints JSON: antes de integrar no front, você pode validar se a rota está correta, se o status está adequado e se o JSON contém os campos esperados. Além disso, Postman ajuda a documentar: você salva requisições em coleções e consegue compartilhar com colegas ou entregar junto do projeto.

Um conceito essencial no Postman é o Environment (ambiente). Nele você define variáveis como baseUrl e evita repetir a URL completa em cada request. Isso é particularmente importante em aulas, porque às vezes a porta muda, ou o servidor roda em outra máquina. Com {{baseUrl}}, você ajusta uma vez e todas as requisições continuam funcionando.

Outro recurso valioso é a aba Tests. Você consegue escrever pequenos scripts para validar automaticamente o status e a presença de campos. Isso cria um “mini-teste” manual automatizado: toda vez que você clicar em Send, o Postman avalia se a resposta está correta. Com o tempo, isso vira uma forma simples de regressão: você refaz o teste depois de alterações e garante que não quebrou a rota.

O que um aluno deve praticar no Postman neste capítulo:

- `Criar Environment` — baseUrl = http://127.0.0.1:8000
- `Criar Collection` — Lanchonete PW3
- `Salvar requests e exemplos` — 200 OK, 422 inválido, 404 não encontrado.
- `Adicionar Tests` — Verificar status e campos essenciais do JSON.

> **Exemplo aplicado no passo a passo (Cap. 8)**
>
> Na seção 4.5, você cria um environment com {{baseUrl}} e testa GET {{baseUrl}}/cep/01001000 (200) e GET {{baseUrl}}/cep/123 (422). Também adiciona testes no Postman para validar status e campos como logradouro, bairro, localidade e uf. Isso garante que, antes de integrar no front (seção 4.4), seu endpoint interno já está correto.

### 4) Passo a passo guiado — ViaCEP + Cache + Postman

Meta: criar endpoint interno no Laravel que consulta ViaCEP e retorna JSON para o front.

#### 4.1. Criar rota e controller para consulta de CEP

Crie um controller simples:

**Shell**

```bash
php artisan make:controller CepController
```

Em `routes/web.php`, crie uma rota protegida (ou pública, se preferir). Aqui usaremos `auth`:

**PHP**

```php
use App\Http\Controllers\CepController;

Route::middleware(['auth'])->group(function () {
    Route::get('/cep/{cep}', [CepController::class, 'show'])->name('cep.show');
});
```

#### 4.2. Implementar consumo da API ViaCEP com Http + timeout + cache

Edite `app/Http/Controllers/CepController.php`:

**PHP**

```php
<?php

namespace App\Http\Controllers;

use Illuminate\Http\Request;
use Illuminate\Support\Facades\Cache;
use Illuminate\Support\Facades\Http;

class CepController extends Controller
{
    public function show(string $cep)
    {
        // Normaliza CEP: mantém apenas números
        $cep = preg_replace('/\D/', '', $cep);

        // Validação simples (CEP brasileiro tem 8 dígitos)
        if (strlen($cep) !== 8) {
            return response()->json([
                'message' => 'CEP inválido. Informe 8 dígitos.',
                'errors' => ['cep' => ['CEP deve conter 8 números.']]
            ], 422);
        }

        $cacheKey = "cep:$cep";

        $data = Cache::remember($cacheKey, now()->addMinutes(10), function () use ($cep) {
            // ViaCEP: https://viacep.com.br/ws/{cep}/json/
            $resp = Http::timeout(3)->acceptJson()
                ->get("https://viacep.com.br/ws/{$cep}/json/");

            if (!$resp->ok()) {
                return ['_error' => 'Falha ao consultar serviço de CEP.'];
            }

            $json = $resp->json();

            // ViaCEP retorna {"erro": true} quando não encontra
            if (isset($json['erro']) && $json['erro'] === true) {
                return ['_error' => 'CEP não encontrado.'];
            }

            return $json;
        });

        if (isset($data['_error'])) {
            return response()->json([
                'message' => $data['_error']
            ], 404);
        }

        // Padroniza resposta para o front
        return response()->json([
            'message' => 'CEP encontrado!',
            'cep' => $data['cep'] ?? $cep,
            'logradouro' => $data['logradouro'] ?? '',
            'bairro' => $data['bairro'] ?? '',
            'localidade' => $data['localidade'] ?? '',
            'uf' => $data['uf'] ?? '',
            'ibge' => $data['ibge'] ?? null,
        ], 200);
    }
}
```

> **Cache em 10 minutos**
>
> Isso reduz chamadas repetidas quando vários usuários consultam o mesmo CEP. Ajuste o tempo conforme necessidade.

#### 4.3. Criar campos de entrega no pedido (exemplo simples)

Se você ainda não tem campos de entrega, crie colunas no pedido (opcional) ou mantenha apenas no front. Para didática, vamos assumir que a tela de pedido tem um bloco “Entrega” com: CEP, logradouro, bairro, cidade, UF.

Exemplo de bloco em `resources/views/pedidos/edit.blade.php`:

HTML/Blade

```php
<div class="card mt-3">
  <div class="card-body">
    <h5 class="fw-bold">Entrega</h5>

    <div class="row g-2">
      <div class="col-md-4">
        <label class="form-label">CEP</label>
        <input id="cep" class="form-control" placeholder="00000-000">
        <div class="form-text">Digite o CEP e clique em Buscar.</div>
      </div>
      <div class="col-md-2 d-flex align-items-end">
        <button id="btnBuscarCep" class="btn btn-outline-secondary w-100" type="button">Buscar</button>
      </div>

      <div class="col-md-6">
        <label class="form-label">Logradouro</label>
        <input id="logradouro" class="form-control">
      </div>

      <div class="col-md-4">
        <label class="form-label">Bairro</label>
        <input id="bairro" class="form-control">
      </div>
      <div class="col-md-6">
        <label class="form-label">Cidade</label>
        <input id="cidade" class="form-control">
      </div>
      <div class="col-md-2">
        <label class="form-label">UF</label>
        <input id="uf" class="form-control" maxlength="2">
      </div>
    </div>
  </div>
</div>

<script>
  window.PW3CEP = {
    urlBase: "{{ url('/cep') }}" // GET /cep/{cep}
  };
</script>
```

#### 4.4. Front-end: buscar CEP via fetch e autopreencher

JavaScript (pode ficar no final da view):

**JavaScript**

```javascript
function showToast(title, body) {
  const el = document.getElementById('pw3Toast');
  document.getElementById('pw3ToastTitle').textContent = title;
  document.getElementById('pw3ToastBody').textContent = body;
  const toast = bootstrap.Toast.getOrCreateInstance(el, { delay: 2500 });
  toast.show();
}

function onlyDigits(v){
  return (v || '').replace(/\D/g, '');
}

document.getElementById('btnBuscarCep')?.addEventListener('click', async () => {
  const cepEl = document.getElementById('cep');
  const cep = onlyDigits(cepEl.value);

  try {
    const resp = await fetch(`${window.PW3CEP.urlBase}/${cep}`, {
      headers: { 'Accept': 'application/json' }
    });

    const data = await resp.json();

    if (!resp.ok) {
      showToast('Erro', data.message || 'Falha ao consultar CEP.');
      return;
    }

    document.getElementById('logradouro').value = data.logradouro || '';
    document.getElementById('bairro').value = data.bairro || '';
    document.getElementById('cidade').value = data.localidade || '';
    document.getElementById('uf').value = data.uf || '';

    showToast('Sucesso', data.message);
  } catch (e) {
    console.error(e);
    showToast('Erro', 'Falha de conexão. Verifique servidor e internet.');
  }
});
```

> **Boa prática**
>
> Valide CEP no back (422) e trate no front com mensagens amigáveis. Se a API externa falhar, retorne 404/503 com JSON padronizado.

#### 4.5. Testar com Postman (coleção e ambiente)

Passos sugeridos:

1. Crie um **Environment** com variável `baseUrl` = `http://127.0.0.1:8000`.
2. Crie uma **Collection** chamada **Lanchonete PW3**.
3. Adicione a requisição **GET {{baseUrl}}/cep/01001000** (exemplo).
4. Envie e verifique status 200 e campos (logradouro, bairro, localidade, uf).
5. Teste erro: **GET {{baseUrl}}/cep/123** → deve retornar 422.
6. Salve exemplos (“Save Response”) na coleção.

Script de teste simples no Postman (aba Tests):

**JavaScript**

```javascript
pm.test("Status 200", function () {
  pm.response.to.have.status(200);
});

pm.test("Tem campos de endereço", function () {
  const json = pm.response.json();
  pm.expect(json).to.have.property('logradouro');
  pm.expect(json).to.have.property('bairro');
  pm.expect(json).to.have.property('localidade');
  pm.expect(json).to.have.property('uf');
});
```

#### 4.6. Commit no Git

**Shell**

```bash
git add .
git commit -m "Capítulo 8: consumo ViaCEP + cache + endpoint interno + testes Postman"
git push
```

### 5) Atividades correlatas (para a Semana B)

Objetivo: consolidar consumo de API, cache, UX e Postman. Entrega via repositório (commit + push).

1. **Cachear resposta do CEP por alguns minutos (melhorar)**
    - Ajustar TTL do cache e criar um botão “Limpar cache do CEP” (rota admin/gerente).
    - Mostrar no JSON um campo `cached` (true/false) para fins didáticos.
2. **Tratar CEP inválido com mensagens amigáveis**
    - Validar CEP com regex e retornar 422 com errors.
    - No front, destacar campo CEP e exibir mensagem abaixo do input.
3. **Máscara de CEP no front**
    - Implementar máscara simples: 00000-000 (JS).
    - Garantir que o back recebe apenas números (normalização).

> **Plus (opcional)**
>
> Criar uma coleção Postman completa com rotas de Categoria/Produto/Pedido e exemplos de payloads.

### 6) Pesquisas complementares (para aprofundar)

- O que é rate limiting e como uma API pública pode limitar chamadas?
- Estratégias de cache: quando usar cache em arquivo, database ou Redis.
- Boas práticas de consumo de API: timeouts, retries e circuit breaker (conceito).
- Postman: variáveis de ambiente, pre-request scripts e como exportar coleção.
- Segurança: por que não expor chaves/segredos no front e como usar .env para credenciais.
### 9) Entregáveis do capítulo

1. Repositório com CepController, rota /cep/{cep}, cache e integração no front (autopreenchimento).
2. Pasta `docs/` com prints: (a) Postman retornando 200, (b) Postman retornando 422, (c) tela preenchendo endereço.
3. Export da coleção Postman (arquivo .json) salvo no repositório em `docs/postman/`.

---

## Capítulo 09 — API REST (api.php), Resources e Autenticação por Token (Sanctum)

**Carga horária:** 2 semanas (100 min/semana)

**Formato das aulas:**

- Semana A (100 min): Conceitos de REST + demonstração + criação da primeira API.
- Semana B (100 min): Autenticação por token + testes no Postman + atividades correlatas.

> Contexto do projeto: Sistema da Lanchonete. Vamos expor endpoints REST para Produtos/Pedidos e proteger com tokens.

### 1) Objetivos de aprendizagem

Ao final deste capítulo, o(a) aluno(a) será capaz de:

- Explicar o conceito de REST e mapear recursos para endpoints.
- Criar endpoints no arquivo `routes/api.php` e retornar JSON consistente.
- Usar `ApiResource` para controlar o formato da resposta.
- Validar entrada de dados em endpoints (Form Request ou validate()).
- Proteger a API com autenticação por token usando Laravel Sanctum.
### 2) Pré-requisitos e ferramentas

- Projeto Laravel com catálogo (Produto/Categoria) e pedidos (Cap. 6–8).
- Postman instalado (usaremos para testar tokens e endpoints).
- Ambiente local rodando: `php artisan serve`.
### 3) Conteúdo teórico

#### 3.1. REST: recursos e verbos HTTP

REST (Representational State Transfer) é um estilo arquitetural para construir APIs HTTP. A ideia central é tratar o sistema como um conjunto de “recursos” — coisas que existem no domínio do problema — e manipulá-los por meio de URLs e métodos HTTP. No projeto da Lanchonete, recursos típicos são produtos, categorias e pedidos. Em vez de criar URLs como /api/criarProduto ou /api/deletarProduto, o padrão REST prefere usar a mesma URL do recurso e mudar o verbo HTTP para expressar a ação.

Pensar em recursos ajuda a projetar uma API consistente. Um recurso normalmente tem uma coleção (lista) e itens individuais (detalhe). Por exemplo: /api/produtos representa a coleção de produtos; /api/produtos/{id} representa um produto específico. Com isso, as ações mais comuns do CRUD ficam padronizadas: GET para ler, POST para criar, PUT/PATCH para atualizar e DELETE para remover. Essa padronização facilita o consumo por aplicações front-end, apps mobile e integrações externas, porque o padrão se repete para qualquer recurso.

Outra característica importante do REST é que ele é stateless: o servidor não depende de estado armazenado no navegador para entender a requisição. Em uma API, isso significa que cada requisição precisa carregar as informações necessárias (por exemplo, o token de autenticação). É por isso que, neste capítulo, saímos do modelo de sessão do Blade (capítulos anteriores) e passamos a usar autenticação por token (Sanctum) via header Authorization.

Mapeamento típico de um recurso “produtos” em REST:

- `GET /api/produtos` — Listar produtos (coleção).
- `GET /api/produtos/{id}` — Detalhar um produto (item).
- `POST /api/produtos` — Criar um novo produto.
- `PUT/PATCH /api/produtos/{id}` — Atualizar um produto existente.
- `DELETE /api/produtos/{id}` — Remover um produto.

> **Exemplo aplicado no passo a passo (Cap. 9)**
>
> No passo a passo, você cria um ProdutoApiController com métodos index/show/store/update/destroy (seção 4.4) e registra as rotas com Route::apiResource("produtos", ...) (seção 4.5). Isso materializa o conceito REST: a URL é /api/produtos e o verbo HTTP define a ação (GET lista, POST cria, DELETE remove).

#### 3.2. Status HTTP e “contratos” de API

Uma API bem projetada não se comunica apenas pelo corpo JSON: ela também comunica “o que aconteceu” pelo status HTTP. Essa combinação (status + JSON) forma o contrato da API: o consumidor sabe como interpretar cada cenário sem precisar “adivinhar”. Por exemplo, se a API retorna 201, o consumidor entende que um recurso foi criado; se retorna 422, entende que os dados enviados não passaram na validação; se retorna 401, entende que falta autenticação.

Um ponto didático importante é diferenciar 401 e 403. 401 Unauthorized significa “você não está autenticado” (sem token, token inválido/expirado). Já 403 Forbidden significa “você está autenticado, mas não tem permissão para esta ação”. No projeto da Lanchonete, isso aparece quando um atendente tenta criar/editar produtos via API: ele pode ter token válido (autenticado), mas a regra do sistema pode bloquear por perfil (role), retornando 403.

Outro status útil é 204 No Content, usado quando a ação foi concluída com sucesso mas não há corpo para retornar. Em operações de delete, é comum responder 204. Porém, em projetos didáticos você pode optar por retornar 200 com uma mensagem. O principal é consistência: escolha um padrão e aplique em todos os endpoints.

Status mais comuns e como o consumidor deve reagir:

- `200 OK` — Sucesso com corpo JSON (ex.: show, update).
- `201 Created` — Recurso criado; normalmente retorna o recurso criado.
- `204 No Content` — Sucesso sem corpo (comum em delete).
- `401 Unauthorized` — Token ausente/inválido; pedir login/token novamente.
- `403 Forbidden` — Sem permissão; ocultar ação e mostrar aviso.
- `404 Not Found` — Recurso não existe; informar e evitar nova tentativa com mesmo id.
- `422 Unprocessable Entity` — Validação falhou; exibir erros por campo.

> **Exemplo aplicado no passo a passo (Cap. 9)**
>
> No ProdutoApiController (seção 4.4), o store retorna 201 ao criar e o destroy retorna 204 ao excluir. Já a validação em store/update usa $request->validate(...); se falhar, o Laravel retorna 422 em JSON (desde que o request seja para /api e/ou Accept: application/json). No AuthController (seção 4.2), credenciais inválidas retornam 401.

#### 3.3. Versionamento e padronização de respostas

Quando você expõe uma API, outras aplicações podem passar a depender dela. Se você mudar o formato do JSON “do nada”, pode quebrar integrações. Por isso, mesmo em projetos pequenos, vale pensar em versionamento e padronização. Versionar significa manter uma “linha do tempo” de mudanças sem quebrar quem já usa a versão antiga. O padrão mais simples é colocar a versão na URL (ex.: /api/v1/produtos).

Padronização significa que suas respostas seguem um formato previsível. Um padrão comum é usar chaves como message, data e errors. Assim, em sucesso você devolve data; em erro de validação você devolve errors; em erro de autenticação você devolve message. Você não é obrigado a usar esse formato em todos os lugares, mas quanto mais consistente, mais fácil fica para o consumidor tratar respostas no front-end ou no Postman.

No Laravel, API Resources ajudam a padronizar a “forma” do JSON de saída. Em vez de retornar diretamente o Model (o que pode vazar campos indesejados ou gerar formatos diferentes), você cria um Resource que define exatamente quais campos aparecem e como eles aparecem (por exemplo, converter preço para float e datas para ISO). Isso também facilita evoluções: se amanhã você decidir expor a categoria dentro do produto, você faz isso no Resource com whenLoaded, mantendo controle.

Boas práticas simples para padronização/versionamento:

- `Use API Resources` — Controla campos e evita expor dados sensíveis por acidente.
- `Pense em /v1` — Mesmo que você não aplique agora, saiba como faria.
- `Erros consistentes` — Padronize {message, errors} em validação e autorização.
- `Não retorne dados sensíveis` — Nunca retorne senha, hash, tokens completos em logs/respostas.

> **Exemplo aplicado no passo a passo (Cap. 9)**
>
> Na seção 4.3, você cria ProdutoResource para controlar a saída (id, nome, preço, categoria e timestamps). Na seção 4.4, o controller retorna ProdutoResource::collection(...) e new ProdutoResource(...), garantindo padronização. Já a sugestão de versionamento aparece nas atividades (seção 5) ao mencionar mover para /api/v1.

> **Segurança (regra de ouro para APIs)**
>
> APIs devem validar entrada, autenticar (token), autorizar por regra de negócio (ex.: role) e expor apenas os campos necessários. Mesmo com Sanctum, trate 401/403 corretamente e nunca confie em dados vindos do cliente.

### 4) Passo a passo — API de Produtos + Token (Sanctum)

Meta: criar endpoints REST para Produtos e proteger com token.

#### 4.1. Instalar e configurar Sanctum

**Shell**

```bash
composer require laravel/sanctum
php artisan vendor:publish --provider="Laravel\\Sanctum\\SanctumServiceProvider"
php artisan migrate
```

> **Obs.**
>
> O Sanctum cria uma tabela para armazenar tokens pessoais. Vamos gerar tokens via endpoint de login.

#### 4.2. Criar um endpoint de login para gerar token

Crie um controller para autenticação de API:

**Shell**

```bash
php artisan make:controller Api/AuthController
```

Em `app/Http/Controllers/Api/AuthController.php`:

**PHP**

```php
<?php

namespace App\Http\Controllers\Api;

use App\Http\Controllers\Controller;
use Illuminate\Http\Request;
use Illuminate\Support\Facades\Hash;
use App\Models\User;

class AuthController extends Controller
{
    public function login(Request $request)
    {
        $data = $request->validate([
            'email' => 'required|email',
            'password' => 'required|string',
            'device_name' => 'nullable|string|max:50',
        ]);

        $user = User::where('email', $data['email'])->first();

        if (!$user || !Hash::check($data['password'], $user->password)) {
            return response()->json([
                'message' => 'Credenciais inválidas.'
            ], 401);
        }

        $device = $data['device_name'] ?? 'postman';
        $token = $user->createToken($device)->plainTextToken;

        return response()->json([
            'message' => 'Login OK',
            'token' => $token,
            'token_type' => 'Bearer',
            'user' => [
                'id' => $user->id,
                'name' => $user->name,
                'email' => $user->email,
                'role' => $user->role ?? null,
            ]
        ], 200);
    }

    public function logout(Request $request)
    {
        $request->user()->currentAccessToken()->delete();

        return response()->json([
            'message' => 'Logout OK'
        ], 200);
    }
}
```

#### 4.3. Criar ApiResource para Produto

**Shell**

```bash
php artisan make:resource ProdutoResource
```

Em `app/Http/Resources/ProdutoResource.php`:

**PHP**

```php
public function toArray($request)
{
    return [
        'id' => $this->id,
        'nome' => $this->nome,
        'preco' => (float) $this->preco,
        'categoria' => $this->whenLoaded('categoria', function () {
            return [
                'id' => $this->categoria->id,
                'nome' => $this->categoria->nome,
            ];
        }),
        'created_at' => $this->created_at?->toISOString(),
        'updated_at' => $this->updated_at?->toISOString(),
    ];
}
```

#### 4.4. Criar controlador de API para Produtos

**Shell**

```bash
php artisan make:controller Api/ProdutoApiController --api
```

Em `app/Http/Controllers/Api/ProdutoApiController.php` (exemplo mínimo):

**PHP**

```php
<?php

namespace App\Http\Controllers\Api;

use App\Http\Controllers\Controller;
use App\Http\Resources\ProdutoResource;
use App\Models\Produto;
use Illuminate\Http\Request;

class ProdutoApiController extends Controller
{
    public function index()
    {
        $produtos = Produto::with('categoria')->orderBy('nome')->paginate(10);
        return ProdutoResource::collection($produtos);
    }

    public function show(Produto $produto)
    {
        $produto->load('categoria');
        return new ProdutoResource($produto);
    }

    public function store(Request $request)
    {
        $data = $request->validate([
            'nome' => 'required|string|max:120',
            'preco' => 'required|numeric|min:0',
            'categoria_id' => 'required|exists:categorias,id',
        ]);

        $produto = Produto::create($data);
        $produto->load('categoria');

        return (new ProdutoResource($produto))
            ->response()
            ->setStatusCode(201);
    }

    public function update(Request $request, Produto $produto)
    {
        $data = $request->validate([
            'nome' => 'sometimes|required|string|max:120',
            'preco' => 'sometimes|required|numeric|min:0',
            'categoria_id' => 'sometimes|required|exists:categorias,id',
        ]);

        $produto->update($data);
        $produto->load('categoria');

        return new ProdutoResource($produto);
    }

    public function destroy(Produto $produto)
    {
        $produto->delete();
        return response()->json(null, 204);
    }
}
```

#### 4.5. Rotas em routes/api.php (protegidas por Sanctum)

Edite `routes/api.php`:

**PHP**

```php
use App\Http\Controllers\Api\AuthController;
use App\Http\Controllers\Api\ProdutoApiController;

Route::post('/login', [AuthController::class, 'login']);

Route::middleware('auth:sanctum')->group(function () {
    Route::post('/logout', [AuthController::class, 'logout']);

    Route::apiResource('produtos', ProdutoApiController::class);
});
```

#### 4.6. Testes no Postman (passo a passo)

1. Faça login:

POST `{{baseUrl}}/api/login` com body JSON:

**JSON**

```json
{
  "email": "seuemail@exemplo.com",
  "password": "suasenha",
  "device_name": "postman"
}
```

Copie o token e configure Authorization → Bearer Token nas próximas requisições.

2. Listar produtos:

GET `{{baseUrl}}/api/produtos`

3. Criar produto:

POST `{{baseUrl}}/api/produtos` com JSON:

**JSON**

```json
{
  "nome": "Coxinha",
  "preco": 7.5,
  "categoria_id": 1
}
```

> **Padrão de retorno**
>
> Usando Resource, a resposta já vem padronizada e pronta para consumo (inclusive paginada).

#### 4.7. Commit no Git

**Shell**

```bash
git add .
git commit -m "Capítulo 9: API REST (produtos) + Resource + Sanctum token + Postman"
git push
```

### 5) Atividades correlatas

Objetivo: ampliar a API e melhorar segurança e padrões.

1. **API de Pedidos (listar e detalhar)**
    - Criar `PedidoResource` com itens e produtos.
    - Usar eager loading (`with('itens.produto')`) e paginação.
2. **Regras de autorização**
    - Permitir criar/editar produtos apenas para role='gerente'.
    - Retornar 403 quando o token pertence a atendente.
3. **Padronização de erros**
    - Criar um formato de erro padrão: `{message, errors}`.
    - Garantir que 422 sempre retorne errors com nome do campo.

> **Plus (opcional)**
>
> Implementar versionamento: mover rotas para `/api/v1` e manter compatibilidade futura.

### 6) Pesquisas complementares

- Diferença entre Sanctum e Passport (cenários de uso).
- Autorização com Policies/Gates e middleware customizado.
- Boas práticas de paginação e filtros em APIs (q, sort, dir).
- Rate limiting no Laravel: `throttle` e limites por usuário.
### 9) Entregáveis

1. Repositório com Sanctum, controllers de API, resources e rotas em `routes/api.php`.
2. Coleção Postman exportada em `docs/postman/` contendo login + produtos (CRUD).
3. Prints em `docs/`: login com token, GET produtos com Bearer, POST produto retornando 201.

---

## Capítulo 10 — Padronização de API: filtros, ordenação, paginação, rate limit e documentação

**Carga horária:** 2 semanas (100 min/semana)

**Formato das aulas:**

- Semana A: melhorar a API (filtros/ordenação/paginação) + boas práticas de resposta.
- Semana B: documentação OpenAPI (Swagger) + rate limiting + testes no Postman.

> Contexto: a API de Produtos com Sanctum (Cap. 9) já existe. Agora vamos deixá-la “profissional”.

### 1) Objetivos de aprendizagem

Ao final deste capítulo, o(a) aluno(a) será capaz de:

- Implementar filtros e busca em endpoints (ex.: `?q=cox&categoria_id=1`).
- Implementar ordenação segura com whitelist (ex.: `?sort=preco&dir=asc`).
- Padronizar paginação e manter contratos estáveis.
- Aplicar rate limiting (`throttle`) em rotas de API.
- Criar documentação básica em OpenAPI (arquivo YAML/JSON) e exportar coleção Postman.
### 2) Pré-requisitos e ferramentas

- Capítulo 9 concluído: API de Produtos + login/token com Sanctum.
- Postman (para testar filtros/ordenação/paginação) e DevTools.
- Recomendado: banco com dados suficientes (produtos e categorias) para testar paginação.
### 3) Conteúdo teórico

#### 3.1. Contrato de API e compatibilidade

Quando você publica uma API, você está oferecendo um contrato para quem consome. Esse contrato inclui: quais endpoints existem, quais parâmetros são aceitos, quais campos aparecem no JSON, quais status HTTP podem ser retornados e como os erros são estruturados. Mesmo que hoje só o Postman consuma, amanhã pode ser um aplicativo mobile, um front-end separado, ou outro sistema da escola/empresa. Se você mudar o contrato sem cuidado, o consumidor quebra — às vezes silenciosamente, gerando bugs difíceis de rastrear.

Por isso, “padronização” não é perfumaria: é estabilidade. Em APIs, pequenas escolhas fazem grande diferença: (1) sempre usar o mesmo nome de campo (ex.: categoria_id vs categoriaId), (2) sempre devolver datas no mesmo formato (ISO), (3) sempre devolver erros em um formato previsível e (4) manter paginação consistente (links/meta). Quando você aplica essas regras desde cedo, você reduz retrabalho e melhora a manutenção.

Compatibilidade também se relaciona com evolução. Se você precisar mudar algo grande (por exemplo, trocar um campo ou adicionar novos filtros), o ideal é versionar (ex.: /api/v1). Assim, você pode manter v1 funcionando enquanto cria v2 para a mudança. Em projetos didáticos, basta conhecer o conceito e aplicar uma versão simples quando necessário — o mais importante é não quebrar o consumidor sem aviso.

Práticas simples para manter um contrato estável:

- `Padrão de resposta` — Definir convenção como {data, meta, links} (paginado) e {message, errors} (falha).
- `Campos consistentes` — Nunca alternar nomes/tipos entre endpoints (preco sempre float, por exemplo).
- `Mudanças aditivas primeiro` — Adicionar campos é mais seguro do que renomear/remover.
- `Versionamento` — Quando precisar quebrar compatibilidade, crie /v2 e mantenha /v1 por um tempo.

> **Exemplo aplicado no passo a passo (Cap. 10)**
>
> No capítulo, você evolui o endpoint GET /api/produtos para aceitar filtros e ordenação (seção 4.1), mas sem mudar o formato central do retorno: a lista continua paginada via Resource collection. Além disso, você cria docs/openapi.yaml (seção 4.4), que documenta o contrato para evitar ambiguidades e “surpresas” para quem consome.

#### 3.2. Filtros, ordenação e segurança

Filtros em APIs normalmente são enviados por query string (por exemplo, ?q=cox&categoria_id=1). Isso é simples e funciona bem com cache e com links de paginação. Porém, todo parâmetro de filtro precisa ser validado e normalizado: limite de tamanho para strings (evita abuso), conversão para inteiro quando for id, e checagem de valores permitidos (por exemplo, status ∈ {ativo,inativo}).

Ordenação é o ponto mais sensível. Um erro comum é fazer orderBy($request->sort) diretamente. Se sort vier com um valor inesperado, você pode causar erro SQL, expor comportamento do banco e, em alguns casos, criar brechas de injeção em trechos não parametrizáveis (orderBy aceita nome de coluna, não parâmetro). A defesa correta é whitelist: uma lista de colunas permitidas e uma lista de direções válidas (asc/desc). Se o cliente enviar algo fora da lista, você cai para um padrão seguro (ex.: sort=nome, dir=asc).

Além da segurança, whitelist também melhora previsibilidade: o consumidor sabe quais campos pode usar para ordenar e não perde tempo tentando sort inválido. Em documentação (OpenAPI), você pode inclusive colocar enum com os valores permitidos. Por fim, sempre considere performance: filtros com LIKE (%texto%) podem ser mais lentos; para bases maiores, você pode indexar colunas ou usar busca full-text. Neste capítulo, o foco é o padrão correto e seguro.

Checklist de segurança para filtros/ordenação:

- `Limitar tamanho de q` — Ex.: substr(q, 0, 80) para evitar payload exagerado.
- `Converter tipos` — categoria_id deve virar int; preço deve ser numeric.
- `Whitelist em sort/dir` — Permitir apenas colunas e direções esperadas.
- `Não concatenar SQL manual` — Use Query Builder/Eloquent para where e bindings.

> **Exemplo aplicado no passo a passo (Cap. 10)**
>
> Na seção 4.1, o controller limita q, filtra por categoria_id e faz ordenação segura com $allowedSort e $allowedDir antes de chamar orderBy($sort, $dir). Isso evita o erro clássico de orderBy com input livre e garante um comportamento estável.

#### 3.3. Paginação e performance

Paginação é essencial em APIs porque evita respostas gigantes e melhora a performance do servidor e do cliente. Em vez de retornar milhares de registros, você retorna um “pedaço” (por exemplo, 10 por página) e fornece links/metadados para navegar. No Laravel, paginate() cria automaticamente meta e links (page, per_page, total, next/prev) quando usado com Resource collection.

Quando você combina paginação com filtros e ordenação, o consumidor espera consistência: a página 1 de um filtro deve continuar sendo a página 1 daquele filtro ao navegar. Em APIs, isso normalmente é garantido porque os parâmetros continuam na URL. É por isso que você deve documentar claramente quais parâmetros existem e como se combinam. Também é boa prática permitir o parâmetro per_page com limites máximos (ex.: max 50) para evitar abuso.

Performance não é só paginação: também envolve eager loading. Se você retorna produtos com categoria, carregar categoria com with("categoria") evita N+1 e reduz consultas. Além disso, defina índices no banco para colunas muito filtradas (categoria_id) e colunas ordenadas com frequência (nome, created_at). Neste capítulo, o essencial é entender que paginação + filtros + eager loading formam o tripé de uma listagem eficiente em API.

Boas práticas para paginação em API:

- `per_page com limite` — Aceitar per_page, mas com máximo (ex.: 50) para evitar abuso.
- `Meta/links consistentes` — Manter o formato de paginação igual em todos os endpoints de lista.
- `Eager loading` — with("categoria") para evitar N+1 quando incluir categoria.
- `Padrões de ordenação` — Definir sort padrão (nome) para estabilidade.

> **Exemplo aplicado no passo a passo (Cap. 10)**
>
> Na seção 4.1, a lista usa paginate(10) e retorna via ProdutoResource::collection($produtos). Isso faz com que o JSON inclua metadados e links de paginação automaticamente, mantendo o contrato do capítulo anterior e facilitando consumo no Postman.

#### 3.4. Rate limiting e proteção contra abuso

Rate limiting (limite de requisições) é uma proteção para evitar abuso, reduzir carga e manter a API disponível para todos. Mesmo em projetos pequenos, ele é útil para evitar que um script ou erro no front dispare centenas de requisições por minuto. Em APIs públicas, rate limit é obrigatório; em APIs internas, ainda é uma boa prática, principalmente em endpoints de login.

No Laravel, você pode aplicar rate limit pelo middleware throttle:60,1 (60 requisições por minuto). Quando o limite é atingido, o Laravel retorna 429 Too Many Requests. O consumidor pode então reduzir ritmo, implementar backoff e tentar novamente mais tarde. Além do throttle simples por IP, você pode configurar regras por usuário autenticado usando RateLimiter, criando limites diferentes para login e para endpoints protegidos. Isso é importante porque login costuma ser alvo de força bruta.

Rate limiting deve ser combinado com mensagens e documentação. Se o consumidor não sabe que existe limite, ele vai interpretar 429 como “erro estranho”. Por isso, documentar o limite e orientar como agir (esperar, repetir com backoff) faz parte de uma API “profissional”.

Boas práticas de rate limiting:

- `Limites diferentes por rota` — Login pode ter limite menor (ex.: 10/min), endpoints comuns podem ter 60/min.
- `Por usuário quando autenticado` — Mais justo do que só por IP em redes compartilhadas.
- `Tratamento no cliente` — Reconhecer 429 e aplicar espera/backoff.
- `Monitorar` — Registrar logs quando houver muitas ocorrências de 429.

> **Exemplo aplicado no passo a passo (Cap. 10)**
>
> Na seção 4.3, você aplica throttle:60,1 no grupo auth:sanctum. Isso faz com que, ao disparar muitas requisições no Postman rapidamente, você possa observar o retorno 429 e entender como a proteção funciona na prática.

#### 3.5. Documentação (OpenAPI/Swagger) e coleções Postman

Documentar a API reduz dúvidas e acelera integração. OpenAPI é um padrão de especificação que descreve endpoints, parâmetros, bodies e respostas. A partir de um arquivo OpenAPI, ferramentas como Swagger UI conseguem gerar documentação interativa. Mesmo que você não rode um Swagger UI no projeto, ter um openapi.yaml versionado no Git já cria uma referência única e confiável.

Coleções do Postman complementam a documentação: elas são “executáveis”. Você consegue rodar a sequência login → listar → criar → atualizar → deletar e validar respostas. Em projetos didáticos, é uma forma excelente de demonstrar funcionamento, repetir testes e entregar uma evidência objetiva do que foi construído.

O que documentar no mínimo:

- `Autenticação` — Como obter token e como enviar Authorization: Bearer ...
- `Parâmetros` — q, categoria_id, sort, dir, paginação (page, per_page) se existir.
- `Respostas e erros` — Exemplos de 200/201/204/401/403/422/429.

> **Exemplo aplicado no passo a passo (Cap. 10)**
>
> Na seção 4.4, você cria docs/openapi.yaml com endpoints /api/login e /api/produtos e enum de sort/dir. Na seção 4.5, você testa no Postman e salva exemplos, garantindo que a documentação e os testes estejam alinhados.

### 4) Passo a passo guiado

#### 4.1. Adicionar filtros e busca no endpoint GET /api/produtos

Atualize o método `index()` do `ProdutoApiController`:

**PHP**

```php
public function index(Request $request)
{
    $q = $request->query('q');
    $categoriaId = $request->query('categoria_id');

    $query = Produto::query()->with('categoria');

    if ($q) {
        $q = substr($q, 0, 80); // limita tamanho
        $query->where('nome', 'like', "%{$q}%");
    }

    if ($categoriaId) {
        $query->where('categoria_id', (int) $categoriaId);
    }

    // Ordenação segura (whitelist)
    $sort = $request->query('sort', 'nome');
    $dir = strtolower($request->query('dir', 'asc'));

    $allowedSort = ['nome', 'preco', 'created_at'];
    $allowedDir = ['asc', 'desc'];

    if (!in_array($sort, $allowedSort, true)) $sort = 'nome';
    if (!in_array($dir, $allowedDir, true)) $dir = 'asc';

    $produtos = $query->orderBy($sort, $dir)->paginate(10);

    return ProdutoResource::collection($produtos);
}
```

#### 4.2. Documentar parâmetros aceitos (exemplo rápido)

> **Query string**
>
> Use: `/api/produtos?q=cox&categoria_id=1&sort=preco&dir=desc`

#### 4.3. Adicionar rate limit (throttle) nas rotas de API

Em `routes/api.php`, aplique throttle no grupo protegido:

**PHP**

```php
Route::middleware(['auth:sanctum', 'throttle:60,1'])->group(function () {
    Route::post('/logout', [AuthController::class, 'logout']);
    Route::apiResource('produtos', ProdutoApiController::class);
});
```

#### 4.4. Criar uma especificação OpenAPI mínima (arquivo YAML)

Crie `docs/openapi.yaml` no seu repositório (exemplo mínimo):

**YAML**

```yaml
openapi: 3.0.3
info:
  title: Lanchonete PW3 API
  version: 1.0.0
servers:
  - url: http://127.0.0.1:8000
paths:
  /api/login:
    post:
      summary: Gera token de acesso
      requestBody:
        required: true
        content:
          application/json:
            schema:
              type: object
              required: [email, password]
              properties:
                email: { type: string, format: email }
                password: { type: string }
                device_name: { type: string }
      responses:
        '200':
          description: Token gerado
  /api/produtos:
    get:
      summary: Lista produtos (paginado)
      parameters:
        - in: query
          name: q
          schema: { type: string }
        - in: query
          name: categoria_id
          schema: { type: integer }
        - in: query
          name: sort
          schema: { type: string, enum: [nome, preco, created_at] }
        - in: query
          name: dir
          schema: { type: string, enum: [asc, desc] }
      responses:
        '200':
          description: Lista paginada
    post:
      summary: Cria produto
      security:
        - bearerAuth: []
      responses:
        '201':
          description: Criado
components:
  securitySchemes:
    bearerAuth:
      type: http
      scheme: bearer
      bearerFormat: JWT
```

> **Nota**
>
> O Sanctum usa Bearer token, mas não é JWT. No OpenAPI, ainda usamos o esquema bearer para documentar o header.

#### 4.5. Testar no Postman

Crie requests e salve exemplos:

- Login: `POST {{baseUrl}}/api/login` → copia token
- GET produtos com filtros: `GET {{baseUrl}}/api/produtos?q=cox&sort=preco&dir=desc`
- Teste rate limit: dispare várias chamadas rapidamente e observe headers/erros 429 (se atingir limite).
#### 4.6. Commit no Git

**Shell**

```bash
git add .
git commit -m "Capítulo 10: filtros/ordenação/paginação + throttle + OpenAPI básica"
git push
```

### 5) Atividades correlatas

1. **Filtros avançados**
    - Adicionar filtro `preco_min` e `preco_max` com validação numérica.
    - Adicionar filtro por status/ativo (se existir no seu model).
2. **Padronização de resposta**
    - Envolver respostas em `{ message, data }` em endpoints de create/update/delete.
    - Criar um handler para exceptions de validação com JSON padronizado.
3. **Documentação melhor**
    - Completar OpenAPI com schemas de Produto e paginação.
    - Salvar export do Postman em `docs/postman/` e atualizar README.
### 6) Pesquisas complementares

- Qual a diferença entre OpenAPI, Swagger UI e Postman Collections?
- Como usar RateLimiter no Laravel para limites por usuário vs por IP?
- Como projetar filtros escaláveis (Specification pattern / Query objects)?
- Caching em APIs: quando faz sentido cachear respostas públicas?
### 9) Entregáveis

1. API de produtos com filtros/ordenação/paginação funcionando.
2. Rate limit aplicado nas rotas de API (throttle).
3. Arquivo `docs/openapi.yaml` no repositório.
4. Export da coleção Postman em `docs/postman/` com exemplos.

---

## Capítulo 11 — Testes Automatizados (PHPUnit/Pest), Factories/Seeders e Qualidade

**Carga horária:** 2 semanas (100 min/semana)

**Formato das aulas:**

- Semana A (100 min): Conceitos + criar testes Feature para Web e API.
- Semana B (100 min): Factories/Seeders, testes com Sanctum e ajustes de qualidade.

> Contexto do projeto: Sistema da Lanchonete com API (Cap. 9–10). Agora vamos garantir qualidade com testes.

### 1) Objetivos de aprendizagem

Ao final deste capítulo, o(a) aluno(a) será capaz de:

- Diferenciar testes **Unit** e **Feature** no Laravel.
- Criar testes Feature para páginas web e para endpoints de API.
- Usar `factories` e `seeders` para gerar dados consistentes para testes.
- Testar autenticação por token com Sanctum (`Sanctum::actingAs`).
- Verificar contratos JSON (estrutura/campos) e status HTTP.
### 2) Pré-requisitos e ferramentas

- Projeto Laravel com autenticação e API (Cap. 9–10).
- Composer atualizado e ambiente rodando.
- Opcional: Pest (se o professor quiser testar com sintaxe alternativa).
### 3) Conteúdo teórico

#### 3.1. Testes Unit x Feature (e onde cada um faz sentido)

No Laravel, é comum separar testes em duas grandes categorias: Unit e Feature. Testes Unit focam em uma “unidade” pequena de código (um método, uma classe, uma função) com o mínimo de dependências possível. A ideia é testar lógica pura: por exemplo, um cálculo de subtotal, uma regra de transformação de dados, ou uma classe de serviço que não precisa necessariamente de HTTP e views. Em geral, Unit tests são rápidos e ajudam a localizar problemas com precisão.

Já testes Feature verificam o comportamento do sistema como um todo: rotas, controllers, middleware, validação, banco de dados e respostas (HTML ou JSON). Eles são mais próximos do que um usuário/cliente realmente faz: um request chega, passa por autenticação, executa uma action, interage com models e retorna uma resposta. Por isso, Feature tests dão confiança de que as partes estão integradas corretamente. Em APIs, esse tipo de teste é especialmente útil porque valida status HTTP, estrutura JSON e regras de autenticação/autorização.

Uma forma simples de decidir: se o seu teste precisa “bater em uma rota” (get/postJson) e verificar status e JSON, ele é Feature. Se o seu teste só precisa chamar um método e comparar resultado, ele tende a ser Unit. Na prática, projetos Laravel iniciantes costumam usar mais Feature, porque grande parte do valor está em garantir que rotas e validações funcionam. Conforme o projeto cresce, você começa a extrair regras de negócio para classes/serviços e aí Unit tests ganham espaço.

Comparação rápida:

- `Unit` — Mais rápido; testa lógica isolada; fácil de diagnosticar falhas.
- `Feature` — Testa o fluxo real (HTTP → controller → DB → response); valida integração.
- `Estratégia didática` — Comece com Feature para rotas principais e crie Unit para regras de negócio que você extrair.

> **Exemplo aplicado no passo a passo (Cap. 11)**
>
> Na seção 4.3, você cria um teste Feature (tests/Feature/Api/ProdutoApiTest.php) que faz getJson/postJson em /api/produtos e verifica status 401/200/201/422. Isso é Feature porque passa pela rota, middleware do Sanctum, validação e Resource. Um exemplo de Unit (não obrigatório aqui) seria testar um método que calcula subtotal = quantidade \* preco_unitario sem depender de HTTP.

#### 3.2. Por que testar? (valor prático e “documentação viva”)

Testes automatizados têm três benefícios diretos em projetos reais e didáticos. Primeiro: reduzem bugs — você pega erro cedo, antes de entregar. Segundo: dão confiança para refatorar — quando você melhora um controller, troca validação ou muda um Resource, os testes avisam se você quebrou algo. Terceiro: viram documentação viva — diferente de um README que pode ficar desatualizado, o teste descreve o comportamento esperado e precisa passar para o projeto estar “ok”.

No contexto da nossa API (Cap. 9–10), testes também ajudam a garantir contrato: a estrutura paginada (data/links/meta), os status corretos (201 no create, 422 na validação), e a exigência de token (401). Isso evita regressões comuns: por exemplo, alguém remover middleware auth:sanctum sem perceber, ou alterar o Resource e parar de retornar campo preco como float.

Outro ponto pedagógico: testes ajudam a aprender o “jeito Laravel” de programar. Você usa helpers como getJson/postJson, assertions como assertJsonStructure, assertJsonPath e assertJsonValidationErrors, e passa a entender melhor contratos HTTP. Além disso, quando você acopla testes a factories, você aprende a criar dados previsíveis sem depender do banco real do seu computador.

O que vale priorizar em uma suíte mínima de testes:

- `Autenticação` — Rotas protegidas retornam 401 sem token e 200 com token.
- `Validação` — Payload inválido retorna 422 e indica os campos com erro.
- `Contrato JSON` — Estrutura esperada (data/links/meta) e campos essenciais do recurso.
- `Caminho feliz` — Criar/atualizar um recurso retorna status correto e dados consistentes.

> **Exemplo aplicado no passo a passo (Cap. 11)**
>
> A “meta prática” do capítulo (seção 3) é ter testes para 401 sem token, 200 com token e 201 no create. Esses três cenários cobrem autenticação + contrato + validação básica, gerando confiança de que a API está funcional e estável.

#### 3.3. Dados de teste: Factories, Seeders e RefreshDatabase

Testes confiáveis dependem de dados controlados. Se você depender do seu banco real (com dados que mudam a cada aula), os testes ficam instáveis: um dia passa, no outro quebra. Factories resolvem isso criando registros falsos de forma consistente e repetível. Você consegue criar 15 produtos com Produto::factory()->count(15)->create() e saber que sempre haverá registros suficientes para testar paginação.

O trait RefreshDatabase é essencial porque garante isolamento: cada teste começa com um banco “limpo”. O Laravel faz migrate/rollback (ou reusa migrações) para garantir que alterações de um teste não contaminem o próximo. Isso é o que transforma testes em algo reproduzível. Sem RefreshDatabase, um teste pode depender do que outro test criou e isso vira uma bagunça.

Seeders entram em dois cenários diferentes: (1) seeders para demonstrar o sistema (demo) — como o DemoSeeder do passo a passo; e (2) seeders como parte do setup de testes — quando você precisa de um conjunto base de dados. No geral, para testes, factories são mais flexíveis e preferíveis. Seeders são úteis quando você quer uma massa padrão para todos (por exemplo, permissões, perfis, configurações).

Boas práticas para dados em testes:

- `Prefira factories` — Mais flexíveis e fáceis de ajustar por teste.
- `Use RefreshDatabase` — Evita dependência entre testes e garante isolamento.
- `Evite banco real` — Testes não devem depender do estado do seu MySQL local com dados antigos.
- `Crie relações com factories` — categoria_id => Categoria::factory() garante integridade e simplicidade.

> **Exemplo aplicado no passo a passo (Cap. 11)**
>
> Na seção 4.2, você cria CategoriaFactory e ProdutoFactory (incluindo categoria_id apontando para Categoria::factory()). Na seção 4.3, o teste usa RefreshDatabase e cria dados com factories antes de chamar getJson/postJson. Isso deixa os testes determinísticos e repetíveis em qualquer máquina.

#### 3.4. Testando APIs protegidas com Sanctum (Sanctum::actingAs)

Quando uma API é protegida por token (Sanctum), o comportamento esperado é: sem token → 401; com token válido → acesso permitido. Em testes, você não precisa realmente chamar /api/login e guardar token para cada request. O Laravel oferece Sanctum::actingAs(), que simula um usuário autenticado no contexto do teste. Assim, você consegue testar endpoints protegidos com simplicidade, sem depender do fluxo de login.

Essa simulação é importante por dois motivos: (1) deixa os testes mais rápidos e focados (você testa o endpoint em si, e não o login toda hora); (2) evita flutuações e complexidade desnecessária. Mesmo assim, é interessante ter pelo menos um teste específico para o endpoint de login (AuthController), verificando 200 com credenciais corretas e 401 com credenciais inválidas — isso garante que o fluxo real funciona.

Além de autenticação, você pode evoluir para autorização: por exemplo, permitir criar produtos apenas para role=gerente. Nesse caso, seus testes devem cobrir 403 quando o usuário autenticado tem role=atendente. Isso conecta o Cap. 5 (roles) com o Cap. 9–10 (API) e reforça que segurança é sempre “autenticar + autorizar”.

O que testar em endpoints com Sanctum:

- `401 sem token` — getJson/postJson deve falhar sem autenticação.
- `200/201 com token` — actingAs permite simular usuário e verificar sucesso.
- `403 por role (se existir)` — Usuário autenticado mas sem permissão deve ser bloqueado.

> **Exemplo aplicado no passo a passo (Cap. 11)**
>
> No teste ProdutoApiTest (seção 4.3), Sanctum::actingAs(User::factory()->create()) habilita o acesso ao /api/produtos. O primeiro teste confirma 401 sem token e o segundo confirma 200 com token e JSON paginado. Isso valida rapidamente a proteção auth:sanctum aplicada nas rotas.

> **Meta prática (qualidade mínima que vale ouro)**
>
> Se você tiver 4 testes bem escolhidos — (1) 401 sem token, (2) 200 com token, (3) 201 criando produto, (4) 422 para payload inválido — você já reduz muito a chance de regressão na API e ganha segurança para evoluir filtros/ordenação e documentação.

### 4) Passo a passo guiado

#### 4.1. Rodar testes no Laravel

**Shell**

```bash
php artisan test
# ou
./vendor/bin/phpunit
```

#### 4.2. Criar factories (Categoria e Produto)

**Shell**

```bash
php artisan make:factory CategoriaFactory --model=Categoria
php artisan make:factory ProdutoFactory --model=Produto
```

Exemplo de `database/factories/CategoriaFactory.php`:

**PHP**

```php
public function definition(): array
{
    return [
        'nome' => $this->faker->unique()->words(2, true),
    ];
}
```

Exemplo de `database/factories/ProdutoFactory.php`:

**PHP**

```php
public function definition(): array
{
    return [
        'nome' => $this->faker->unique()->word(),
        'preco' => $this->faker->randomFloat(2, 1, 50),
        'categoria_id' => \App\Models\Categoria::factory(),
    ];
}
```

#### 4.3. Criar teste Feature para a API de Produtos

**Shell**

```bash
php artisan make:test Api/ProdutoApiTest
```

Em `tests/Feature/Api/ProdutoApiTest.php` (exemplo):

**PHP**

```php
<?php

namespace Tests\Feature\Api;

use Tests\TestCase;
use Illuminate\Foundation\Testing\RefreshDatabase;
use Laravel\Sanctum\Sanctum;
use App\Models\User;
use App\Models\Produto;
use App\Models\Categoria;

class ProdutoApiTest extends TestCase
{
    use RefreshDatabase;

    public function test_lista_produtos_exige_autenticacao()
    {
        $this->getJson('/api/produtos')
            ->assertStatus(401);
    }

    public function test_lista_produtos_com_token_retorna_estrutura_paginada()
    {
        Sanctum::actingAs(User::factory()->create());
        Produto::factory()->count(15)->create();

        $this->getJson('/api/produtos')
            ->assertOk()
            ->assertJsonStructure([
                'data',
                'links',
                'meta'
            ]);
    }

    public function test_cria_produto_com_validacao()
    {
        Sanctum::actingAs(User::factory()->create());
        $cat = Categoria::factory()->create();

        $payload = [
            'nome' => 'Coxinha',
            'preco' => 7.50,
            'categoria_id' => $cat->id,
        ];

        $this->postJson('/api/produtos', $payload)
            ->assertStatus(201)
            ->assertJsonPath('data.nome', 'Coxinha');
    }

    public function test_validacao_rejeita_payload_invalido()
    {
        Sanctum::actingAs(User::factory()->create());

        $this->postJson('/api/produtos', ['nome' => ''])
            ->assertStatus(422)
            ->assertJsonValidationErrors(['nome', 'preco', 'categoria_id']);
    }
}
```

> **Dica**
>
> Use `getJson/postJson` para garantir headers JSON automaticamente.

#### 4.4. (Opcional) Instalar Pest

**Shell**

```bash
composer require pestphp/pest --dev
php artisan pest:install
```

#### 4.5. Seed de dados para demo (não confundir com testes)

**Shell**

```bash
php artisan make:seeder DemoSeeder
```

Em `database/seeders/DemoSeeder.php`:

**PHP**

```php
public function run(): void
{
    \App\Models\Categoria::factory()->count(5)->create();
    \App\Models\Produto::factory()->count(30)->create();
}
```

#### 4.6. Rodar testes e commitar

**Shell**

```bash
php artisan test

git add .
git commit -m "Capítulo 11: testes Feature API + factories/seed + qualidade"
git push
```

### 5) Atividades correlatas (Semana B)

Objetivo: ampliar cobertura e garantir contratos.

1. **Testar filtros/ordenação (Cap. 10) na API**
    - Criar um teste para `?q=` e outro para `?sort=preco&dir=desc`.
2. **Testar autorização por role (gerente/atendente)**
    - Se sua API restringe criação/edição a gerente, testar 403 para atendente.
3. **Testar rotas web principais**
    - Feature test para login e acesso protegido (ex.: /pedidos exige auth).

> **Plus (opcional)**
>
> Configurar um workflow de CI (GitHub Actions) para rodar `php artisan test` em cada push.

### 6) Pesquisas complementares

- Diferença entre mocks, fakes e stubs em testes.
- Como testar jobs/queues e notifications no Laravel.
- Cobertura de código: o que é e como medir (conceito).
- Testes de API: contract testing e snapshots (conceito).
### 9) Entregáveis do capítulo

1. Suíte de testes com pelo menos 3 cenários (401 sem token, 200 com token, 201 create).
2. Factories criadas e usadas nos testes.
3. Prints em `docs/`: saída do `php artisan test` e estrutura JSON validada.

---

## Capítulo 12 — Consumindo sua própria API: Cliente JS, CORS e tokens (Sanctum)

**Carga horária:** 2 semanas (100 min/semana)

**Formato das aulas:**

- Semana A: CORS + cliente JS (fetch) consumindo /api/* com token.
- Semana B: UX, armazenamento seguro do token, logout e pequenos ajustes de segurança.

> Contexto: você já tem API protegida (Cap. 9–10) e testes (Cap. 11). Agora vamos criar um cliente externo (mini dashboard) consumindo a API.

### 1) Objetivos

Ao final deste capítulo, você será capaz de:

- Explicar CORS e por que navegadores bloqueiam requisições cross-origin.
- Configurar CORS para permitir um cliente separado consumir sua API.
- Construir um mini cliente em HTML/JS usando `fetch()` com Bearer token.
- Implementar login (obter token), listagem de produtos (paginada) e logout (revogar token).
- Aplicar boas práticas: headers, tratamento de erro e feedback ao usuário.
### 2) Pré-requisitos

- API funcionando com Sanctum (Cap. 9) + filtros/ordenação (Cap. 10).
- Testes rodando (Cap. 11) para garantir que a API está estável.
- Postman para conferir rapidamente login e endpoints.
- Um usuário válido no banco para realizar login e gerar token.
### 3) Teoria (CORS e Tokens)

#### 3.1. O que é CORS? (origem, navegador e preflight)

CORS (Cross-Origin Resource Sharing) é uma regra de segurança aplicada pelo navegador para controlar quais páginas podem chamar recursos (APIs) de outras origens. “Origem” é a combinação de protocolo + domínio + porta. Isso significa que http://localhost:5173 e http://127.0.0.1:8000 são origens diferentes, mesmo sendo o mesmo computador. Quando um front tenta chamar uma API em outra origem, o navegador bloqueia por padrão, a menos que o servidor autorize explicitamente por meio de headers CORS.

O ponto mais importante: CORS não é “segurança do servidor”; é uma proteção do navegador para o usuário. Ferramentas como Postman não sofrem bloqueio de CORS porque não são navegadores. Por isso, pode acontecer do endpoint funcionar no Postman e falhar no browser com erro de CORS. O jeito correto de resolver é ajustar a política CORS no servidor para permitir apenas as origens necessárias, sem abrir tudo para qualquer site.

Além do simples GET, muitas requisições disparam um preflight (requisição OPTIONS) antes da requisição real. Isso acontece quando o browser detecta “requisição não simples”, como: uso de Authorization header, Content-Type application/json, métodos como PUT/DELETE, ou headers customizados. O preflight pergunta ao servidor: “você aceita que essa origem envie este método e estes headers?” Se o servidor não responder com os headers corretos, o navegador bloqueia a chamada real. Em projetos com token Bearer, o Authorization quase sempre aciona preflight — então CORS precisa estar bem configurado.

Pontos-chave para entender CORS neste capítulo:

- `CORS é do navegador` — Postman não bloqueia; o browser bloqueia.
- `Origem inclui porta` — 5173 e 8000 são origens diferentes.
- `Authorization geralmente gera preflight` — OPTIONS precisa ser permitido para api/\*.
- `Permita só o necessário` — allowed_origins deve ser lista de origens do seu cliente.

> **Exemplo aplicado no passo a passo (Cap. 12)**
>
> Na seção 4.1, você ajusta config/cors.php para permitir as origens do cliente (ex.: http://localhost:5173). Isso faz o preflight e as requisições com Authorization funcionarem no browser. Se der erro, a própria seção 4.4 orienta a conferir a origem e limpar cache de config com php artisan config:clear.

#### 3.2. Tokens Bearer (Sanctum) e diferença para sessão

Nos capítulos anteriores (Blade), a autenticação era baseada em sessão: o servidor cria uma sessão e o navegador guarda um cookie. A cada requisição, o cookie identifica o usuário. Para APIs consumidas por clientes externos (como um mini dashboard em outra porta), o fluxo mais comum é token: você faz login, recebe um token e envia esse token em cada requisição no header Authorization: Bearer ...

No Sanctum com tokens pessoais, cada token é armazenado no banco e pode ser revogado (apagado) a qualquer momento. Isso é útil para simular dispositivos: um usuário pode ter um token “postman” e outro token “cliente-js”. Se um token vazar, você revoga apenas aquele token sem derrubar todos os acessos. No nosso exemplo, o endpoint /api/logout remove o token atual (currentAccessToken), o que representa “sair daquele cliente”.

Outro detalhe importante: quando você usa token Bearer, o servidor não depende do cookie de sessão, então a chamada é naturalmente stateless. Isso combina com REST e com clientes externos. Por outro lado, o token precisa ser protegido no cliente, porque quem possui o token possui acesso. Essa é a ponte para o próximo tópico: armazenamento seguro.

Boas práticas de token Bearer em clientes:

- `Sempre enviar Accept: application/json` — Facilita tratar erros (401/422) em JSON.
- `Não logar token em público` — Evitar console/prints/commits com token visível.
- `Separar tokens por device_name` — Facilita revogar tokens por cliente/dispositivo.
- `Logout revoga token` — POST /api/logout para invalidar acesso daquele cliente.

> **Exemplo aplicado no passo a passo (Cap. 12)**
>
> Na seção 4.3, a função api() injeta Authorization: Bearer `<token>` automaticamente quando existe token salvo. No login, você chama /api/login e salva data.token. No logout, você chama POST /api/logout e remove o token do storage. Isso implementa o ciclo completo login → consumir API → logout com revogação.

#### 3.3. Armazenamento do token (localStorage, riscos e alternativas)

Guardar token em localStorage é simples e funciona bem para didática: você fecha e abre o navegador e o token ainda está lá. Porém, existe um risco importante: se houver uma falha de XSS (injeção de script) na página, um script malicioso pode ler localStorage e roubar o token. Esse é o principal motivo pelo qual, em aplicações reais, localStorage é considerado arriscado para tokens de alto privilégio.

Alternativas mais seguras dependem do tipo de aplicação. Em SPAs com Sanctum, um padrão comum é usar autenticação via cookies HttpOnly (que JavaScript não consegue ler) combinada com CSRF, evitando expor token ao JS. Outra alternativa é guardar o token apenas em memória (variável) e pedir login de novo ao recarregar a página — melhora segurança, piora conveniência. Em projetos didáticos, é suficiente explicar o trade-off: conveniência x exposição.

Mesmo usando localStorage, dá para mitigar: (1) reduzir risco de XSS usando escaping correto e evitando {!! !!} em dados do usuário; (2) aplicar Content Security Policy (CSP) — tema avançado; (3) limitar escopo do token (criar tokens com menos permissões, quando aplicável); (4) expirar o token logicamente no front, apagando após X minutos (atividade sugerida no capítulo).

Resumo didático (o que dizer para o aluno):

- `localStorage é fácil` — Bom para aprender e prototipar.
- `Risco principal é XSS` — Se tiver script malicioso, ele lê o token.
- `Cookies HttpOnly são alternativa` — Mais seguro, mas exige fluxo SPA e CSRF.
- `Mitigação básica` — Evitar XSS, expirar token no front e revogar no logout.

> **Exemplo aplicado no passo a passo (Cap. 12)**
>
> Na seção 4.3, você usa localStorage (tokenKey = pw3_token) para persistir o token e reaproveitar nas chamadas. A seção 3.3 do capítulo já alerta que isso é didático e que, em projetos reais, você deve considerar cookies HttpOnly ou estratégias mais seguras. Nas atividades correlatas (seção 5), há a sugestão de expiração lógica no front (timestamp) para reduzir risco.

#### 3.4. Boas práticas de cliente JS (fetch): headers, erros e UX

Quando você constrói um cliente JS para consumir uma API, consistência é essencial. O cliente deve sempre enviar Accept: application/json, tratar resp.ok, lidar com erros de rede e mostrar feedback ao usuário. Além disso, ao usar JSON, você deve controlar Content-Type: application/json apenas quando o corpo realmente é JSON. Isso evita bugs de parsing no servidor.

Outra boa prática é centralizar o acesso à API em uma função (como api() no passo a passo). Assim, você coloca em um único lugar a lógica de headers, Authorization, parsing e tratamento de erros. Isso evita duplicação e facilita evoluir o cliente: paginação, filtros, criação de produto etc. A partir dessa base, você consegue criar componentes simples de UI: botões Próximo/Anterior lendo links/meta, campo de busca e selects para filtros.

Por fim, sempre depure com DevTools. Em CORS, o erro aparece no Console/Network; em 401, você vê o status; em 422, você vê a estrutura de errors. Ensinar o aluno a olhar Network/Console é tão importante quanto o código.

Checklist do cliente JS “bem comportado”:

- `Centralizar função api()` — Um ponto único de headers, token e parsing.
- `Tratar 401/422` — Mostrar mensagem e orientar (login obrigatório / corrigir campos).
- `Erros de rede` — try/catch e mensagem “verifique servidor e internet”.
- `UX mínima` — Loading, mensagens claras e limpar token no logout mesmo se falhar.

> **Exemplo aplicado no passo a passo (Cap. 12)**
>
> Na seção 4.3, a função api() sempre define Accept, injeta Authorization quando há token e faz parsing defensivo (text → JSON). Se resp.ok for falso, lança Error com message. Os handlers de click capturam e exibem alert, garantindo feedback básico. Na seção 4.4, você valida o fluxo no navegador e usa o callout de depuração para resolver CORS rapidamente.

### 4) Passo a passo — Mini cliente consumindo a API

#### 4.1. Configurar CORS no Laravel

Em Laravel, o arquivo é `config/cors.php`. Ajuste `allowed_origins` para o endereço do seu cliente.

**PHP**

```php
// config/cors.php
return [
  'paths' => ['api/*'],
  'allowed_methods' => ['*'],
  'allowed_origins' => ['http://localhost:5173', 'http://127.0.0.1:5173'],
  'allowed_headers' => ['*'],
  'supports_credentials' => false,
];
```

> Dica: se você servir o cliente com Live Server em outra porta, inclua a origem correta.

#### 4.2. Criar um mini cliente (arquivo HTML)

Crie um arquivo simples fora do Laravel (ex.: `client/index.html`). Ele fará login e listará produtos.

**HTML**

```html
<!doctype html>
<html lang="pt-BR">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Cliente PW3 (API)</title>
</head>
<body>
  <h1>Cliente da API (Produtos)</h1>

  <section>
    <h2>Login</h2>
    <input id="email" placeholder="email" />
    <input id="password" type="password" placeholder="senha" />
    <button id="btnLogin">Entrar</button>
    <button id="btnLogout">Sair</button>
  </section>

  <section>
    <h2>Produtos</h2>
    <button id="btnLoad">Carregar produtos</button>
    <pre id="out"></pre>
  </section>

  <script src="app.js"></script>
</body>
</html>
```

#### 4.3. Implementar app.js (fetch + Bearer)

**JavaScript**

```javascript
const baseUrl = 'http://127.0.0.1:8000';
const tokenKey = 'pw3_token';

function getToken(){
  return localStorage.getItem(tokenKey);
}

function setToken(t){
  if(t) localStorage.setItem(tokenKey, t);
}

function clearToken(){
  localStorage.removeItem(tokenKey);
}

async function api(path, options = {}){
  const headers = options.headers || {};
  headers['Accept'] = 'application/json';

  const token = getToken();
  if(token){
    headers['Authorization'] = 'Bearer ' + token;
  }

  const resp = await fetch(baseUrl + path, { ...options, headers });
  const text = await resp.text();
  let data;
  try { data = text ? JSON.parse(text) : null; } catch { data = { raw: text }; }

  if(!resp.ok){
    const msg = (data && data.message) ? data.message : ('HTTP ' + resp.status);
    throw new Error(msg);
  }

  return data;
}

document.getElementById('btnLogin').addEventListener('click', async () => {
  const email = document.getElementById('email').value;
  const password = document.getElementById('password').value;

  try {
    const data = await api('/api/login', {
      method: 'POST',
      headers: { 'Content-Type': 'application/json' },
      body: JSON.stringify({ email, password, device_name: 'cliente-js' })
    });

    setToken(data.token);
    alert('Login OK!');
  } catch (e){
    alert('Erro: ' + e.message);
  }
});

document.getElementById('btnLoad').addEventListener('click', async () => {
  try {
    const data = await api('/api/produtos?sort=nome&dir=asc');
    document.getElementById('out').textContent = JSON.stringify(data, null, 2);
  } catch (e){
    alert('Erro: ' + e.message);
  }
});

document.getElementById('btnLogout').addEventListener('click', async () => {
  try {
    await api('/api/logout', { method: 'POST' });
  } catch(e){
    // se token estiver inválido, ainda assim limpe
  }
  clearToken();
  alert('Logout OK');
});
```

#### 4.4. Testar no navegador

1. Rode o Laravel: `php artisan serve`
2. Rode o cliente com Live Server (VS Code) ou outro servidor simples.
3. Faça login e clique em “Carregar produtos”.

> **Se der erro de CORS…**
>
> Confirme a origem (porta) do cliente e ajuste `allowed_origins`. Depois rode `php artisan config:clear`.

#### 4.5. Commit no Git

**Shell**

```bash
git add .
git commit -m "Capítulo 12: cliente JS consumindo API + CORS + fluxo token/login/logout"
git push
```

### 5) Atividades correlatas

1. **Paginação no cliente**
    - Ler `links` e `meta` do JSON e criar botões “Próximo/Anterior”.
2. **Busca e filtros**
    - Adicionar campo de busca (q) e filtro por categoria_id no cliente.
3. **Melhorar segurança do token**
    - Implementar expiração lógica (salvar timestamp e expirar no front).
    - Estudar alternativa SPA do Sanctum com cookies (conceito).

> **Plus (opcional)**
>
> Criar uma página de “Cadastro de Produto” no cliente (POST /api/produtos) com validação e mensagens.

### 6) Pesquisas complementares

- Qual a diferença entre CORS e CSRF?
- Quais riscos de guardar token em localStorage (XSS) e como mitigar?
- Sanctum SPA auth (cookies) vs tokens pessoais: quando usar cada um?
- Headers úteis: `Accept`, `Content-Type`, `Authorization`, `Retry-After`.
### 9) Entregáveis

1. Configuração CORS adequada e versionada.
2. Mini cliente em `client/` consumindo login/logout e GET produtos.
3. Prints em `docs/`: (a) login OK, (b) JSON de produtos no cliente, (c) Network mostrando Authorization Bearer.

---

## Capítulo 13 — Deploy de Aplicação Laravel (Produção)

**Carga horária:** 2 semanas (100 min/semana)

**Formato das aulas:**

- Semana A (100 min): Conceitos + checklist de produção + deploy em ambiente controlado.
- Semana B (100 min): Ajustes finais (storage, filas, cache, logs) + validação com testes e monitoramento.

> Contexto: Projeto da Lanchonete está pronto. Agora vamos colocá-lo em produção com segurança e boas práticas.

### 1) Objetivos

Ao final deste capítulo, você será capaz de:

- Preparar um projeto Laravel para produção (env, cache, build, permissões).
- Fazer deploy em VPS (Nginx) ou hospedagem compatível com PHP.
- Configurar fila/cron, logs e monitoramento básico.
- Aplicar práticas mínimas de segurança (debug off, headers, backups).
### 2) Pré-requisitos

- Projeto final funcionando localmente (web + API + testes).
- Acesso a um servidor (VPS) ou serviço de hospedagem (com PHP 8+ e Composer).
- Git configurado (repositório remoto) e noções de terminal/SSH.
### 3) Teoria (produção)

#### 3.1. O que muda em produção? (mentalidade e configurações essenciais)

“Subir para produção” não é apenas copiar arquivos para um servidor. Em produção, seu sistema vira um serviço real: precisa ser estável, performático e seguro. Isso muda a mentalidade e muda configurações. No desenvolvimento, você aceita mensagens detalhadas de erro, recarrega assets no Vite e usa configurações locais. Em produção, você evita expor detalhes internos, otimiza carregamento e garante que segredos não vazem.

No Laravel, as mudanças mais básicas incluem: desligar debug (APP_DEBUG=false), usar APP_ENV=production, ativar caches (config/route/view) para reduzir custo de boot a cada request e configurar corretamente o APP_URL para geração de links e callbacks. Também entra a diferença de build do front-end: em vez de servir assets no modo dev, você gera uma build (npm run build) e publica os arquivos estáticos.

Outro ponto central é o filesystem: uploads e arquivos gerados pela aplicação vivem em storage. Em produção, a pasta public não deve receber uploads “diretos” sem controle; o padrão Laravel é salvar em storage/app/public e expor via storage:link. Se isso estiver errado, o sistema pode funcionar localmente e quebrar no servidor (uploads somem, 404 em imagens, erros de permissão).

Checklist de mentalidade de produção (o mínimo):

- `Debug OFF` — APP_DEBUG=false para não expor stack traces e detalhes internos.
- `Segredos fora do Git` — .env só no servidor; nunca versionar chaves e senhas.
- `Caches ligados` — config:cache, route:cache e view:cache para performance.
- `Storage correto` — uploads em storage + storage:link para acesso público controlado.
- `Build do front` — assets em modo produção (build), não dev server.

> **Exemplo aplicado no passo a passo (Cap. 13)**
>
> Na seção 4.3, você ajusta APP_ENV/APP_DEBUG/APP_URL no .env e gera a APP_KEY. Na seção 4.4, você executa storage:link e ativa caches (config/route/view). Esses passos materializam exatamente as mudanças de “mentalidade de produção”.

#### 3.2. Erros comuns de deploy (e por que eles acontecem)

A maioria dos erros de deploy no Laravel não é “bug do código”; é ambiente e configuração. O clássico erro 500 após subir o projeto costuma estar relacionado a uma destas causas: .env errado (DB inválido), APP_KEY ausente, permissões incorretas em storage/bootstrap/cache, ou cache desatualizado. Por isso, deploy precisa de um checklist repetível: se você seguir sempre a mesma sequência, você reduz muito o tempo de diagnóstico.

Permissões são campeãs de problema. O PHP-FPM roda como um usuário (por exemplo www-data). Se esse usuário não consegue escrever em storage/ ou bootstrap/cache, o Laravel não consegue criar logs, compilar views e salvar cache. O resultado aparece como erro 500 ou como falhas em features específicas (upload não salva, sessão não grava, log não escreve).

Outro erro frequente é esquecer migrations. Em produção, o banco geralmente começa vazio ou diferente do seu local. Se você não rodar migrate --force, tabelas e colunas podem faltar, quebrando o sistema. Ainda: quando você muda rotas ou config e não limpa/regera cache, o servidor “continua vendo” o estado antigo. Isso gera bugs confusos: rota existe no código, mas 404 no servidor; variável do .env mudou, mas continua com valor antigo.

Principais erros e como reconhecer rapidamente:

- `Erro 500 após deploy` — Verificar logs em storage/logs/laravel.log; geralmente .env, key ou permissão.
- `Imagens/uploads 404` — storage:link ausente ou permissões no storage/app/public.
- `Rota 404 que existe no código` — route:cache desatualizado; rodar route:clear e route:cache.
- `Banco “não tem coluna”` — migrations não rodaram ou rodaram incompletas.
- `Assets quebrados` — build do Vite não foi feita ou public/build não foi publicado.

> **Exemplo aplicado no passo a passo (Cap. 13)**
>
> A seção 4.5 trata exatamente do erro mais comum: permissões. Ela ajusta ownership e chmod para garantir escrita em storage/ e bootstrap/cache. Já a seção 4.4 cobre migrations, storage:link e caches — o trio que resolve a maioria dos “bugs de deploy”.

#### 3.3. Operação em produção: logs, filas, cache e tarefas agendadas

Deploy não termina quando o site abre. Em produção, você precisa cuidar do “funcionamento contínuo”: logs para diagnosticar problemas, filas (queue) para tarefas demoradas, cache para performance e scheduler (cron) para rotinas periódicas. Mesmo que seu projeto ainda não use filas, entender o conceito é importante porque muitas features reais dependem disso (envio de e-mail, geração de relatórios, integrações com APIs, processamento de imagens etc.).

Logs: o Laravel registra em storage/logs e isso é sua primeira fonte de verdade quando algo quebra. Em produção, você precisa também pensar em rotação (não deixar o arquivo crescer infinito) e em coletar logs (por exemplo, via ferramentas do servidor). Cache: em produção, usar config/route/view cache melhora performance. Para caches de dados (ex.: consultas), drivers como Redis dão mais escala, mas file cache já serve para ambiente pequeno.

Filas e scheduler: o scheduler do Laravel é disparado pelo cron (um comando por minuto), e ele decide o que rodar. Já as filas precisam de workers sempre ativos. Rodar queue:work no terminal funciona para estudo, mas em produção real você usa Supervisor ou Systemd para manter o worker vivo após reboot e reiniciar se cair. Sem isso, jobs ficam presos e features “param” silenciosamente.

O que manter sob controle em produção (nível mínimo):

- `Logs acessíveis` — Conseguir abrir storage/logs/laravel.log e identificar erros.
- `Caches corretos` — Regerar caches após mudanças: config:cache/route:cache/view:cache.
- `Cron do scheduler` — Uma linha no crontab chamando schedule:run.
- `Worker de fila` — queue:work mantido por Supervisor/Systemd.
- `Backups` — Dump do banco + rotina de restauração testada.

> **Exemplo aplicado no passo a passo (Cap. 13)**
>
> Na seção 4.7, você adiciona o cron para schedule:run e mostra queue:work para estudo. O callout “Produção de verdade” reforça o uso de Supervisor/Systemd e HTTPS. Na seção 4.8, o “script mental” inclui queue:restart, que é crucial após deploy para reiniciar workers e aplicar mudanças.

#### 3.4. Segurança básica em produção (o que não pode faltar)

Produção exige um mínimo de segurança operacional. O primeiro passo é não expor detalhes: APP_DEBUG=false. Isso evita que um erro mostre caminhos do servidor, queries e detalhes do framework. O segundo passo é proteger segredos: nunca versionar .env, nunca colocar senha de banco em commit, e garantir permissões adequadas no servidor para que arquivos sensíveis não fiquem públicos.

Também é fundamental usar HTTPS. Sem HTTPS, tokens, sessões e senhas podem ser interceptados em redes inseguras. Com HTTPS, além de criptografar tráfego, você pode aplicar HSTS e forçar redirecionamento 80→443. Em Nginx, Certbot (Let’s Encrypt) é o caminho comum. Em hospedagens, muitas já oferecem SSL simplificado. Mesmo que o capítulo não mostre todos os comandos, o conceito deve ser fixado: produção ≠ HTTP simples.

Outros cuidados úteis: limitar permissões de escrita apenas onde é necessário (storage e cache), bloquear acesso a arquivos ocultos (ex.: .env), configurar headers básicos (X-Content-Type-Options, X-Frame-Options), e manter o servidor atualizado. Para o projeto da Lanchonete, isso já é suficiente como “segurança mínima viável”.

Checklist rápido de segurança mínima:

- `APP_DEBUG=false` — Nunca deixar debug ligado em produção.
- `HTTPS obrigatório` — Tráfego criptografado; proteger login e tokens.
- `.env fora do Git` — Segredos só no servidor.
- `Permissões restritas` — Escrita apenas em storage/ e bootstrap/cache.
- `Backups` — Se der ruim, você consegue restaurar.

> **Exemplo aplicado no passo a passo (Cap. 13)**
>
> Na seção 4.3, você define APP_ENV=production e APP_DEBUG=false. Na configuração do Nginx (seção 4.6), a root aponta para public/ e há uma regra deny para arquivos .ht\*, reduzindo risco de exposição. O callout da seção 4.7 reforça HTTPS e Supervisor como parte do “produção de verdade”.

### 4) Passo a passo — Deploy (VPS com Nginx)

#### 4.1. Preparar servidor (pacotes essenciais)

**Shell**

```bash
# Ubuntu/Debian (exemplo)
sudo apt update
sudo apt install -y nginx git unzip
sudo apt install -y php8.2-fpm php8.2-mysql php8.2-xml php8.2-mbstring php8.2-curl php8.2-zip php8.2-bcmath

# Composer (se não tiver)
php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
php composer-setup.php
sudo mv composer.phar /usr/local/bin/composer
```

#### 4.2. Clonar o projeto e instalar dependências

**Shell**

```bash
cd /var/www
sudo git clone https://seu-repo.git lanchonete
cd lanchonete

composer install --no-dev --optimize-autoloader
```

#### 4.3. Configurar .env de produção

Copie o exemplo e edite variáveis:

**Shell**

```bash
cp .env.example .env
php artisan key:generate
```

Checklist mínimo no .env:

- `APP_ENV=production`
- `APP_DEBUG=false`
- `APP_URL=https://seu-dominio.com`
- DB_\* apontando para o banco do servidor
#### 4.4. Migrations, storage e caches

**Shell**

```bash
php artisan migrate --force
php artisan storage:link

php artisan config:cache
php artisan route:cache
php artisan view:cache
```

#### 4.5. Permissões (storage e cache)

**Shell**

```bash
sudo chown -R www-data:www-data /var/www/lanchonete
sudo find /var/www/lanchonete -type f -exec chmod 644 {} \;
sudo find /var/www/lanchonete -type d -exec chmod 755 {} \;

sudo chmod -R 775 /var/www/lanchonete/storage /var/www/lanchonete/bootstrap/cache
```

#### 4.6. Configurar Nginx (server block)

Crie `/etc/nginx/sites-available/lanchonete`:

**Nginx**

```nginx
server {
    listen 80;
    server_name seu-dominio.com;

    root /var/www/lanchonete/public;
    index index.php index.html;

    location / {
        try_files $uri $uri/ /index.php?$query_string;
    }

    location ~ \.php$ {
        include snippets/fastcgi-php.conf;
        fastcgi_pass unix:/run/php/php8.2-fpm.sock;
    }

    location ~ /\.ht {
        deny all;
    }
}
```

Ative e reinicie:

**Shell**

```bash
sudo ln -s /etc/nginx/sites-available/lanchonete /etc/nginx/sites-enabled/
sudo nginx -t
sudo systemctl reload nginx
```

#### 4.7. Filas/cron (opcional, mas recomendado)

Se usar filas (jobs) e agendamentos (scheduler):

**Shell**

```bash
# crontab
* * * * * cd /var/www/lanchonete && php artisan schedule:run >> /dev/null 2>&1

# worker simples (p/ estudos):
php artisan queue:work --tries=3
```

> **Produção de verdade**
>
> Use Supervisor/Systemd para manter o worker sempre ativo e configure HTTPS (Certbot) no Nginx.

#### 4.8. Checklist de “deploy” rápido (script mental)

**Shell**

```bash
git pull
composer install --no-dev --optimize-autoloader
php artisan migrate --force
php artisan config:cache
php artisan route:cache
php artisan view:cache
php artisan queue:restart
```

#### 4.9. Commit no Git

**Shell**

```bash
git add .
git commit -m "Capítulo 13: guia de deploy + configs de produção + checklist"
git push
```

### 5) Atividades correlatas

1. **Deploy em hospedagem compartilhada**
    - Ajustar `public/` como diretório público e proteger arquivos sensíveis.
    - Criar `.htaccess` (Apache) e testar uploads.
2. **HTTPS + Headers**
    - Configurar HTTPS (Certbot) e redirecionamento 80→443.
    - Adicionar headers básicos de segurança (HSTS, X-Content-Type-Options).
3. **Backup e restore**
    - Criar rotina de backup do banco (dump) e testar restauração.

> **Plus (opcional)**
>
> Automatizar deploy com GitHub Actions + SSH (deploy on push) — com cuidado e chaves protegidas.

### 6) Pesquisas complementares

- Qual diferença entre Nginx e Apache para apps PHP?
- O que é Supervisor e por que usar para queue workers?
- Estratégias de logs: Laravel logs + rotacionamento.
- Cache em produção: Redis vs file cache (conceito).
### 9) Entregáveis

1. Aplicação publicada (URL acessível) com login e páginas principais funcionando.
2. Documento em `docs/` com passos do deploy e prints (Nginx/URL/health-check).
3. Checklist de produção preenchido e evidências (logs/commands).

---

## Capítulo 14 — Observabilidade e Segurança em Produção

**Carga horária:** 2 semanas (100 min/semana)

**Formato das aulas:**

- Semana A (100 min): Logs, monitoramento, health-check e alertas básicos.
- Semana B (100 min): HTTPS, hardening, backup/restore e revisão final.

> Contexto: Após o deploy (Cap. 13), precisamos manter o sistema confiável e seguro em produção.

### 1) Objetivos de aprendizagem

Ao final deste capítulo, você será capaz de:

- Criar um endpoint de health-check e validar status do app.
- Configurar logs e identificar erros de produção com rapidez.
- Implementar monitoramento básico (uptime) e alertas simples.
- Ativar HTTPS e aplicar hardening mínimo no Nginx.
- Implementar backup do banco + storage e testar restore.
### 2) Pré-requisitos

- Deploy concluído (Cap. 13) e URL do sistema funcionando.
- Acesso SSH ao servidor e permissão para editar Nginx/cron.
- Banco de dados em produção configurado.
### 3) Conteúdo teórico — Observabilidade

#### 3.1. O que é observabilidade? (logs, métricas e traces na prática)

Observabilidade é a capacidade de entender o que está acontecendo dentro do sistema apenas olhando seus “sinais”. Ela vai além de “ter logs”: envolve conseguir responder rapidamente perguntas como: o sistema está no ar? está lento? onde está o gargalo? qual requisição falhou? qual usuário foi afetado?

Os três sinais clássicos são: logs, métricas e traces. Logs contam “eventos” (ex.: pedido criado, erro 500, usuário logou). Métricas resumem comportamento ao longo do tempo (ex.: taxa de erro, tempo médio de resposta, uso de CPU/RAM). Traces (rastreamentos) mostram o caminho de uma requisição por várias camadas (controller → banco → API externa), permitindo descobrir onde o tempo está sendo gasto. Em projetos didáticos, você pode começar por logs e health-check; conforme evolui, adiciona métricas e correlação por request_id.

A regra prática é: sem observabilidade, você depende de “achismo”. Com observabilidade, você transforma incidentes em diagnóstico: você vê o erro, identifica a causa provável, valida com dados e aplica uma correção. Esse capítulo coloca a fundação: um health-check para medir disponibilidade e logs com contexto para explicar “por quê”.

Sinais e o que cada um responde com mais facilidade:

- `Logs` — O que aconteceu? Qual erro? Qual usuário/rota?
- `Métricas` — Está degradando? Quantos erros por minuto? Qual latência?
- `Traces` — Onde está lento? Em qual camada (DB, API externa, código)?

> **Exemplo aplicado no passo a passo (Cap. 14)**
>
> Na seção 4.1, você cria /health para ter um sinal simples de disponibilidade (uptime). Na seção 4.2, você aprende onde olhar logs (laravel.log e logs do Nginx) e como registrar contexto com Log::info(). Isso cobre o “mínimo viável” de observabilidade: saber se caiu e entender por que caiu.

#### 3.2. Logs úteis: o que registrar (e o que NÃO registrar)

Logs são úteis quando ajudam a reconstruir um incidente. Um log bom responde: qual ação ocorreu, quando ocorreu, em qual rota, para qual recurso, por qual usuário, e com qual resultado. Por isso, em produção é comum registrar eventos importantes (login, criação/fechamento de pedido, falhas em integrações), sempre adicionando contexto mínimo: ids, rota, status e um identificador de correlação (request_id).

Mas logs também podem ser perigosos: eles podem vazar dados sensíveis. Nunca registre senhas, tokens, dados de cartão, ou conteúdo completo de requisições que tenham informações pessoais. Mesmo registrar e-mail e IP deve ser feito com propósito e cuidado. O objetivo é diagnosticar sem violar privacidade e sem criar um “vazamento interno” por meio de arquivos de log.

Logs estruturados (por exemplo, JSON) facilitam análise por ferramentas e tornam buscas mais eficientes. Mesmo sem uma plataforma (ELK/Splunk), você pode começar padronizando campos em Log::info() e garantindo consistência. Outra boa prática é registrar tempo de resposta (latência) em milissegundos, especialmente em endpoints críticos. Isso ajuda a detectar degradação antes de virar queda.

Checklist de logs “bons” para este projeto:

- `Erros e exceptions` — Sempre registrar com stacktrace no servidor, mas sem expor ao usuário.
- `Eventos críticos` — login/logout, pedido criado/fechado, falha em API externa.
- `Contexto mínimo` — user_id, pedido_id, rota, status, request_id.
- `Evitar dados sensíveis` — Nunca logar password, tokens, secrets, dumps completos.

> **Exemplo aplicado no passo a passo (Cap. 14)**
>
> Na seção 4.2, você configura LOG_CHANNEL/LOG_LEVEL e registra um evento com contexto: Log::info("Pedido criado", \[pedido_id, user_id\]). A atividade correlata 5.1 sugere request_id para correlação, que é justamente o próximo passo para deixar logs “profissionais”.

#### 3.3. Health-check e monitoramento: detectar queda antes do usuário reclamar

Um health-check é um endpoint simples que responde rápido e indica se o sistema está operacional. Ele não precisa expor detalhes; ele precisa ser confiável. O objetivo é permitir que uma ferramenta externa (ou mesmo um script) verifique periodicamente se o sistema está “vivo”. Quando o health-check falha, você dispara um alerta e atua antes que o usuário perceba.

O health-check pode ser básico (retornar status ok) ou mais completo (checar conexão com banco, cache, filas). Em projetos didáticos, o básico já é muito útil. Em produção real, é comum ter pelo menos dois níveis: liveness (o processo responde) e readiness (o sistema está pronto para receber tráfego, incluindo dependências).

Monitoramento de uptime funciona como “alarme” de disponibilidade. Ferramentas como UptimeRobot e similares fazem GET a cada X minutos e avisam por e-mail/Telegram quando o endpoint falha. Mesmo sem ferramenta paga, isso já muda o jogo: você deixa de descobrir falhas “por acaso”.

Boas práticas para health-check/monitoramento:

- `Responder rápido` — Sem consultas pesadas; ideal < 200ms.
- `Não expor segredos` — Sem dados internos; apenas status e timestamp.
- `Usar HTTPS` — Evita interceptação e falsos positivos por bloqueios.
- `Alertas claros` — Saber quando caiu e quando voltou (downtime window).

> **Exemplo aplicado no passo a passo (Cap. 14)**
>
> Na seção 4.1, você cria /health retornando JSON simples (status/app/time). Na seção 4.3, você conecta isso a um monitor de uptime chamando /health periodicamente. Isso responde a primeira pergunta da regra prática: “Caiu?”.

#### 3.4. Segurança em produção (mínimo essencial) e hardening

Segurança em produção é sobre reduzir superfície de ataque e minimizar impacto de falhas. Dois pilares são obrigatórios: HTTPS e backups. HTTPS protege tráfego (senhas, cookies, tokens) e evita interceptação. Backups garantem que você consegue recuperar dados após incidentes (erro humano, falha de disco, ataque).

Hardening é o conjunto de ajustes que deixam o servidor “menos permissivo” e mais seguro: headers de segurança (nosniff, frame options, referrer policy), HSTS (após validar HTTPS), e configurações de servidor que bloqueiam arquivos sensíveis. Esses ajustes não substituem correção de vulnerabilidades, mas ajudam a mitigar ataques comuns e reduzem riscos simples.

O ponto mais didático deste capítulo é entender que segurança não é só “colocar senha”. É processo: atualizar sistema, restringir permissões, não expor debug, monitorar logs e testar restore de backup. Se você tem HTTPS mas não tem restore testado, seu risco continua alto, porque perda de dados é um incidente grave.

Mínimo essencial de segurança/operacional para o projeto:

- `HTTPS obrigatório` — Forçar redirecionamento 80→443 e usar certificados válidos.
- `Headers de hardening` — nosniff, SAMEORIGIN, Referrer-Policy, HSTS (com cuidado).
- `Backups automatizados` — Banco + storage; rotina agendada.
- `Restore testado` — Backup só vale se você consegue restaurar.

> **Exemplo aplicado no passo a passo (Cap. 14)**
>
> Na seção 4.4, você instala Certbot e habilita HTTPS com redirecionamento. Na seção 4.5, adiciona headers de hardening no Nginx. Na seção 4.6, cria rotina de backup (mysqldump + tar do storage) e na 4.7 testa restore. Isso responde às perguntas “Como voltar rápido?” e “Como não perder dados?”.

### 4) Passo a passo — Logs, Health-check, HTTPS e Backups

#### 4.1. Criar rota de health-check

Crie uma rota simples em `routes/web.php` (pode ser pública):

**PHP**

```php
Route::get('/health', function () {
    return response()->json([
        'status' => 'ok',
        'app' => config('app.name'),
        'time' => now()->toIso8601String(),
    ]);
});
```

> Teste: `curl https://seu-dominio.com/health`

#### 4.2. Logs: onde olhar e como configurar

Em produção, confira:

- `storage/logs/laravel.log`
- logs do servidor web: Nginx/Apache

Se necessário, ajuste o canal em `.env`:

ENV

```bash
LOG_CHANNEL=stack
LOG_LEVEL=info
```

Exemplo de log com contexto no código:

**PHP**

```php
use Illuminate\Support\Facades\Log;

Log::info('Pedido criado', [
  'pedido_id' => $pedido->id,
  'user_id' => auth()->id(),
]);
```

#### 4.3. Monitoramento básico (uptime) com health-check

Estratégia didática:

- Um monitor (UptimeRobot, StatusCake etc.) chamando `/health` a cada 5 min
- Alertas por e-mail/Telegram quando cair

> **Importante**
>
> Mesmo sem ferramentas pagas, um health-check simples + alertas já evita “descobrir” a queda tarde demais.

#### 4.4. HTTPS com Certbot (Nginx)

**Shell**

```bash
sudo apt install -y certbot python3-certbot-nginx
sudo certbot --nginx -d seu-dominio.com
# escolha redirecionar HTTP -> HTTPS
```

#### 4.5. Hardening: headers básicos no Nginx

Adicione no bloco server (exemplo):

**Nginx**

```nginx
add_header X-Content-Type-Options "nosniff" always;
add_header X-Frame-Options "SAMEORIGIN" always;
add_header Referrer-Policy "strict-origin-when-cross-origin" always;
# HSTS (use após confirmar HTTPS ok)
add_header Strict-Transport-Security "max-age=31536000; includeSubDomains" always;
```

#### 4.6. Backup do banco + storage (rotina simples)

Crie uma pasta segura e faça dump do MySQL:

**Shell**

```bash
sudo mkdir -p /var/backups/lanchonete
sudo chown -R root:root /var/backups/lanchonete

# dump do banco
mysqldump -u SEU_USUARIO -p SUA_BASE > /var/backups/lanchonete/db_$(date +%F).sql

# compactar storage (uploads)
tar -czf /var/backups/lanchonete/storage_$(date +%F).tar.gz -C /var/www/lanchonete storage/app/public
```

Automatize com cron (diário, por exemplo):

**Shell**

```bash
# crontab -e
0 2 * * * /usr/bin/mysqldump -u SEU_USUARIO -pSENHA SUA_BASE > /var/backups/lanchonete/db_$(date +\%F).sql
0 2 * * * /bin/tar -czf /var/backups/lanchonete/storage_$(date +\%F).tar.gz -C /var/www/lanchonete storage/app/public
```

> Dica: evite senha em crontab usando arquivo `~/.my.cnf` (melhor prática).

#### 4.7. Testar restore (muito importante)

Restore do banco (em ambiente de teste):

**Shell**

```bash
mysql -u SEU_USUARIO -p SUA_BASE < /var/backups/lanchonete/db_2026-04-04.sql
```

Restore do storage:

**Shell**

```bash
tar -xzf /var/backups/lanchonete/storage_2026-04-04.tar.gz -C /var/www/lanchonete
```

#### 4.8. Commit no Git

**Shell**

```bash
git add .
git commit -m "Capítulo 14: observabilidade (health/logs) + HTTPS + hardening + backup/restore"
git push
```

### 5) Atividades correlatas

1. **Logs estruturados**
    - Criar um `request_id` por requisição e registrar no log.
2. **Monitorar erros de API**
    - Padronizar erro JSON e registrar falhas 500 com contexto.
3. **Rotação de backups e logs**
    - Apagar backups antigos (ex.: manter últimos 7 dias) e configurar logrotate.

> **Plus (opcional)**
>
> Adicionar um painel admin com status do sistema: último backup, último deploy, versão do app.

### 6) Pesquisas complementares

- Diferença entre logs, métricas e traces (observabilidade).
- Como usar Redis para cache/filas em produção.
- O que é WAF e quando faz sentido (conceito).
- Estratégias de backup: full vs incremental (conceito).
### 9) Entregáveis

1. Endpoint de health-check funcionando e monitorado.
2. HTTPS habilitado e hardening mínimo configurado.
3. Rotina de backup automatizada e restore testado.
4. Prints e logs em `docs/` comprovando: health ok, HTTPS, backups e teste de restore.

---

## Capítulo 15 — CI/CD e Automação (GitHub Actions): testes, qualidade e deploy (opcional)

**Carga horária:** 2 semanas (100 min/semana)

**Formato das aulas:**

- Semana A (100 min): CI — rodar testes automaticamente, lint/format e checagens de segurança.
- Semana B (100 min): CD — deploy automatizado (opcional) e pipeline de release.

> Contexto: app já está no ar (Cap. 13–14). Agora vamos automatizar qualidade e reduzir erros humanos com pipelines.

### 1) Objetivos

Ao final deste capítulo, você será capaz de:

- Configurar um pipeline de CI para rodar `php artisan test` automaticamente.
- Executar checagens adicionais: `composer validate`, `composer audit` e lint básico.
- Entender e usar Secrets/Variables no GitHub com segurança.
- (Opcional) Automatizar deploy via SSH (CD) com passos controlados.
- Criar uma rotina de release: tags, changelog e versão.
### 2) Pré-requisitos

- Repositório no GitHub com o projeto Laravel.
- Testes do Cap. 11 funcionando localmente.
- Para CD (opcional): servidor com SSH e um usuário com permissões restritas.
### 3) Teoria (CI x CD, branches e secrets)

#### 3.1. CI vs CD (e por que isso reduz erro humano)

CI (Integração Contínua) e CD (Entrega/Deploy Contínuo) são duas partes de uma mesma ideia: automatizar o caminho do código até o ambiente final com segurança. CI roda verificações automaticamente a cada push ou Pull Request: testes, validações, checagens de dependências e, quando possível, análise de segurança. O objetivo é simples: descobrir problemas cedo, quando é barato corrigir.

CD é o passo seguinte: depois que o CI passa, você pode automatizar a entrega. Dependendo do time, “CD” pode significar apenas gerar um artefato pronto para deploy (entrega contínua) ou realmente fazer deploy automaticamente em staging/produção (deploy contínuo). No contexto do nosso projeto, o CD é opcional e deve ser tratado com cuidado: automatizar deploy sem controle pode causar quedas. Por isso, a abordagem didática é: primeiro CI confiável; depois CD com gatilhos claros, branch protegida e rollback planejado.

O principal ganho de CI/CD é reduzir erro humano e padronizar processos. Sem pipeline, alguém esquece de rodar testes, esquece de migrar banco, ou faz deploy com dependências incompletas. Com pipeline, esses passos viram “regras automáticas”: se falhar, não passa. Isso cria uma cultura de qualidade: o time passa a confiar mais no código e a refatorar com menos medo.

Resumo de propósito:

- `CI` — Validar automaticamente (testes + checks) antes do merge/deploy.
- `CD` — Entregar ou fazer deploy automatizado quando CI estiver verde.
- `Resultado` — Menos bugs em produção, menos retrabalho e mais previsibilidade.

> **Exemplo aplicado no passo a passo (Cap. 15)**
>
> Na seção 4.1, você cria um workflow de CI que instala dependências, prepara .env, roda migrations e executa php artisan test. Na seção 4.3 (opcional), você cria deploy automático via SSH apenas quando o CI conclui com sucesso e a branch é main. Isso representa exatamente a sequência CI → CD.

#### 3.2. Branches, Pull Requests e “branch protection”

Um pipeline só ajuda de verdade se o fluxo de trabalho obrigar que ele seja executado antes de mudanças chegarem à branch estável. É aqui que entram branches e Pull Requests (PR). A ideia é separar “trabalho em andamento” de “código estável”. Uma estratégia simples, comum em projetos educacionais, é manter main como a branch estável (produção) e develop como a branch de integração. As features são desenvolvidas em branches feature/\* e entram via PR.

Branch protection é a configuração no GitHub que impede ações perigosas, como push direto na main, e exige que critérios sejam atendidos antes do merge. O critério mais importante é: CI precisa passar. Isso evita que código quebrado chegue na branch principal. Você também pode exigir revisão (code review) e bloquear merges sem aprovação. Em sala, o foco é entender que “merge” deve ser um momento controlado e rastreável.

Além de proteger a main, é comum usar regras de gatilho para deploy: apenas tags (v1.0.0) ou apenas merge na main disparam CD. Isso reduz risco. Em projetos reais, ainda existe staging: deploy automático em develop para testar em ambiente similar ao de produção antes de publicar de vez.

Boas práticas simples de fluxo com PR:

- `Sem push direto na main` — Exigir PR para qualquer mudança.
- `CI obrigatório` — Merge só quando o workflow estiver verde.
- `Mensagens e histórico` — PR descreve mudança e facilita auditoria.
- `Staging (se possível)` — Testar em develop/staging antes de produção.

> **Exemplo aplicado no passo a passo (Cap. 15)**
>
> Na seção 4.2, você configura branch protection para exigir que o CI passe antes do merge na main e impedir push direto. Isso faz o pipeline virar “porta de entrada” obrigatória para a branch estável.

#### 3.3. Secrets e princípio do menor privilégio (segurança no pipeline)

Automação não pode virar um atalho para vazar credenciais. Em CI/CD, o maior risco é expor segredos: senha de banco, tokens, chave SSH, chaves de API. Por isso, segredos nunca devem estar no repositório, nem em arquivos versionados. O lugar correto para isso, no GitHub, é Settings → Secrets and variables → Actions. O workflow lê esses valores em runtime, sem imprimir o conteúdo.

O princípio do menor privilégio significa: dar apenas o acesso mínimo necessário. Para deploy por SSH, isso significa criar um usuário específico de deploy sem acesso root, com permissões apenas para atualizar o projeto e executar comandos necessários. A chave SSH deve ser exclusiva para aquele repositório/servidor e, se possível, com restrições (por exemplo, permitir apenas certos comandos). Assim, se um secret vazar, o estrago é limitado.

Também é importante entender que logs do Actions podem vazar informações se você imprimir demais. Evite echo de variáveis sensíveis e evite logs verbosos em produção. Em geral, o pipeline deve registrar apenas o necessário para diagnosticar falhas (por exemplo, status de comandos e saídas não sensíveis).

Checklist de segurança para secrets em CI/CD:

- `Nunca versionar secrets` — Nada de senha/token/SSH key no Git.
- `Usar Secrets do GitHub` — Guardar SSH_HOST, SSH_USER, SSH_KEY em Actions secrets.
- `Menor privilégio` — Usuário de deploy sem root; permissões restritas.
- `Rotacionar chaves` — Se suspeitar vazamento, revogar e gerar nova chave.

> **Exemplo aplicado no passo a passo (Cap. 15)**
>
> Na seção 4.4, você cadastra SSH_HOST, SSH_USER e SSH_KEY nos Secrets do repositório. Na seção 4.3 (deploy), o workflow usa esses secrets no action appleboy/ssh-action, evitando colocar credenciais no código.

#### 3.4. O que vale automatizar no pipeline (qualidade e saúde do projeto)

Em um projeto Laravel, o pipeline pode ir além de “rodar testes”. Ele pode validar dependências (composer validate), checar vulnerabilidades conhecidas (composer audit), aplicar lint/format (Laravel Pint/PHP-CS-Fixer), e até executar análises estáticas (PHPStan/Psalm) em níveis mais avançados. O objetivo é criar uma esteira de qualidade: cada commit é verificado automaticamente, e o time recebe feedback rápido.

No nosso capítulo, o foco é manter o pipeline simples e confiável: instalar dependências, preparar .env, migrar banco (ou usar SQLite), e rodar php artisan test. Isso já cobre a maior parte das regressões. Depois, você adiciona camadas. Se você adicionar tudo de uma vez, o pipeline vira frágil e difícil de manter. Portanto, a estratégia recomendada é incremental: garantir que testes passam de forma consistente e só depois adicionar novas checagens.

Trilha incremental recomendada (do básico ao avançado):

- `Nível 1` — composer install + php artisan test
- `Nível 2` — composer validate + composer audit
- `Nível 3` — Lint/format automático (Pint) no PR
- `Nível 4` — Análise estática (PHPStan) + relatórios/cobertura
- `Nível 5` — CD com staging + deploy controlado + rollback

> **Exemplo aplicado no passo a passo (Cap. 15)**
>
> O workflow ci.yml (seção 4.1) já inclui composer validate, composer audit e php artisan test. As atividades correlatas (seção 5) sugerem cobertura, Pint/PHP-CS-Fixer e staging, que correspondem aos níveis mais avançados da trilha incremental.

### 4) Passo a passo — Workflow de CI + Deploy (opcional)

#### 4.1. Criar workflow de CI (GitHub Actions)

Crie o arquivo `.github/workflows/ci.yml`:

**YAML**

```yaml
name: CI

on:
  push:
    branches: [ "main", "develop" ]
  pull_request:

jobs:
  tests:
    runs-on: ubuntu-latest

    services:
      mysql:
        image: mysql:8
        env:
          MYSQL_DATABASE: laravel
          MYSQL_ROOT_PASSWORD: root
        ports:
          - 3306:3306
        options: >-
          --health-cmd="mysqladmin ping --silent"
          --health-interval=10s
          --health-timeout=5s
          --health-retries=5

    steps:
      - name: Checkout
        uses: actions/checkout@v4

      - name: Setup PHP
        uses: shivammathur/setup-php@v2
        with:
          php-version: '8.2'
          extensions: mbstring, pdo_mysql, bcmath
          coverage: none

      - name: Cache Composer
        uses: actions/cache@v4
        with:
          path: ~/.composer/cache/files
          key: ${{ runner.os }}-composer-${{ hashFiles('**/composer.lock') }}

      - name: Install dependencies
        run: composer install --no-interaction --prefer-dist

      - name: Prepare env
        run: |
          cp .env.example .env
          php artisan key:generate
          php artisan config:clear

      - name: Configure DB for tests
        run: |
          php -r "file_put_contents('.env', str_replace('DB_CONNECTION=mysql', 'DB_CONNECTION=mysql', file_get_contents('.env')));"
          php -r "file_put_contents('.env', preg_replace('/DB_HOST=.*/', 'DB_HOST=127.0.0.1', file_get_contents('.env')));"
          php -r "file_put_contents('.env', preg_replace('/DB_PORT=.*/', 'DB_PORT=3306', file_get_contents('.env')));"
          php -r "file_put_contents('.env', preg_replace('/DB_DATABASE=.*/', 'DB_DATABASE=laravel', file_get_contents('.env')));"
          php -r "file_put_contents('.env', preg_replace('/DB_USERNAME=.*/', 'DB_USERNAME=root', file_get_contents('.env')));"
          php -r "file_put_contents('.env', preg_replace('/DB_PASSWORD=.*/', 'DB_PASSWORD=root', file_get_contents('.env')));"

      - name: Migrate
        run: php artisan migrate --force

      - name: Composer validate
        run: composer validate --no-check-publish

      - name: Security audit (Composer)
        run: composer audit --no-interaction

      - name: Run tests
        run: php artisan test
```

> **Observação**
>
> Se seus testes usam SQLite em memória, você pode simplificar e remover o serviço MySQL.

#### 4.2. Proteger a branch main (recomendado)

No GitHub → Settings → Branches:

- Exigir que o CI passe antes de merge
- Exigir PR (sem push direto na main)
#### 4.3. (Opcional) Workflow de deploy via SSH

Crie `.github/workflows/deploy.yml` (exemplo didático):

**YAML**

```yaml
name: Deploy

on:
  workflow_run:
    workflows: ["CI"]
    types:
      - completed

jobs:
  deploy:
    if: ${{ github.event.workflow_run.conclusion == 'success' && github.ref_name == 'main' }}
    runs-on: ubuntu-latest

    steps:
      - name: Deploy via SSH
        uses: appleboy/ssh-action@v1.0.3
        with:
          host: ${{ secrets.SSH_HOST }}
          username: ${{ secrets.SSH_USER }}
          key: ${{ secrets.SSH_KEY }}
          script: |
            cd /var/www/lanchonete
            git pull
            composer install --no-dev --optimize-autoloader
            php artisan migrate --force
            php artisan config:cache
            php artisan route:cache
            php artisan view:cache
            php artisan queue:restart
```

> **Segurança**
>
> Crie um usuário de deploy sem root e limite o comando. Teste em ambiente de staging antes de produção.

#### 4.4. Salvar Secrets no GitHub

Repository → Settings → Secrets and variables → Actions:

- `SSH_HOST` (IP ou domínio)
- `SSH_USER` (usuário de deploy)
- `SSH_KEY` (chave privada)
#### 4.5. Commit no Git

**Shell**

```bash
git add .
git commit -m "Capítulo 15: CI/CD com GitHub Actions (testes, audit, deploy opcional)"
git push
```

### 5) Atividades correlatas

1. **Cobertura e relatórios**
    - Adicionar relatório de cobertura (conceito) e badge no README.
2. **Lint/format automático**
    - Adicionar PHP-CS-Fixer ou Laravel Pint no pipeline (rodar em PR).
3. **Staging**
    - Criar ambiente staging com deploy automático em branch develop.

> **Plus (opcional)**
>
> Adicionar pipeline de build do front (Vite) e publicar assets no deploy.

### 6) Pesquisas complementares

- O que é “branch protection” e por que ajuda em qualidade?
- Diferença entre CD (deploy contínuo) e entrega contínua.
- Como armazenar secrets com segurança (Vault/KMS) — conceito.
- Blue/Green deployment e rollback — conceito.
### 9) Entregáveis

1. Workflow CI funcional no GitHub Actions com testes passando.
2. Branch protection configurada (main protegida).
3. (Opcional) Workflow de deploy com Secrets corretamente configurados.
4. Evidências em `docs/`: prints do Actions (job success) e do pipeline rodando em PR.

---

## Capítulo 16 — Projeto Final e Apresentação

**Carga horária:** 2 semanas (100 min/semana)

**Formato das aulas:**

- Semana A (100 min): consolidação do sistema + revisão de requisitos + ajustes finais.
- Semana B (100 min): apresentação do projeto + avaliação + retrospectiva e encerramento.

> Contexto: você concluiu CRUD, pedidos, AJAX, consumo de API, API própria com Sanctum, testes, deploy e observabilidade. Agora é a hora de fechar o ciclo com um projeto pronto e bem apresentado.

### 1) Objetivos do projeto final

Ao final do projeto final, você deverá:

- Integrar backend Laravel, banco, views e/ou cliente JS de forma consistente.
- Demonstrar domínio do fluxo de negócio (ex.: lanchonete: produtos → pedidos → itens → total → status).
- Mostrar pelo menos um consumo de API (pública ou interna) e uma API própria documentada/testada.
- Aplicar boas práticas: validação, autorização, logs básicos, e organização do repositório.

> **Meta**
>
> O projeto deve estar “apresentável”: sem erros 500, com telas coerentes, com dados de exemplo e com instruções claras de execução.

### 2) Escopo mínimo obrigatório

Você deve entregar, no mínimo:

- **CRUD principal** (ex.: Produtos, Pedidos ou Usuários) com validação e mensagens.
- **Autenticação** (login/logout) e **controle de acesso** (roles/perfis, quando aplicável).
- **Fluxo de negócio completo** (ex.: criar pedido, adicionar item, total atualizado, status).
- **API** com pelo menos 1 endpoint protegido (Sanctum) e testado/documentado.
- **Deploy** (URL) OU ambiente de demonstração (passo a passo para rodar local).

> **Sugestão de “demo”**
>
> Prepare um usuário gerente e um atendente, com dados seedados, para demonstrar permissões e o fluxo de pedidos em 3–5 minutos.

### 3) Critérios de avaliação (rubrica sugerida)

A avaliação pode considerar (exemplo de pesos):

- **Funcionalidade e fluxo** (40%): CRUD, pedidos, validações, consistência do total/status.
- **Qualidade técnica** (25%): organização, boas práticas Laravel, relações, resources, segurança básica.
- **API e testes** (20%): endpoints, autenticação por token, testes passando, Postman/OpenAPI.
- **Apresentação** (15%): clareza, domínio do projeto, roteiro, evidências e capacidade de responder perguntas.

> **Requisitos que derrubam nota**
>
> Debug ligado em produção, token/senha vazando no repositório, ou projeto que não roda com as instruções entregues.

### 4) Roteiro de apresentação (5–8 minutos)

1. Contexto e problema: o que o sistema resolve?
2. Demonstração rápida: login → tela principal → CRUD → fluxo de pedido.
3. Destaques técnicos: relacionamentos, AJAX, API (Sanctum), testes (php artisan test), deploy/health-check.
4. Segurança e qualidade: validação, roles, logs, backups (se aplicável).
5. Fechamento: melhorias futuras e lições aprendidas.

> **Dica de ouro**
>
> Não leia slides: mostre o sistema funcionando. Deixe a API aberta no Postman com um request pronto e o Actions/CI com um print do workflow passando.

### 5) Validação final (plano rápido de testes)

Antes de apresentar, execute um “smoke test” (5 minutos):

- Rodar testes automatizados: `php artisan test`.
- Verificar rotas protegidas: pedido/itens exigem auth; API exige token.
- Fluxo de pedido: criar pedido → adicionar itens → remover → total consistente.
- API: login gera token; GET /api/produtos retorna paginado; POST cria (se permitido).
- Deploy: `/health` responde ok (se implantado) e HTTPS ativo (se houver).

Sugestão de comandos (local):

```bash
php artisan test
php artisan serve
# (opcional) limpar caches se algo estranho acontecer
php artisan config:clear
php artisan route:clear
php artisan view:clear
```

> **Se algo falhar**
>
> Corrija o erro mais crítico primeiro: (1) 500/DB, (2) autenticação/roles, (3) fluxo de pedido, (4) API. Evite “mexer em tudo” sem um plano.

### 6) Entregáveis e evidências

Entregar no repositório:

- Código completo (com README atualizado).
- Pasta `docs/` com prints: testes passando, Postman, health-check, deploy (se houver).
- Export da coleção Postman em `docs/postman/` e (se existir) `docs/openapi.yaml`.
- Dados de demonstração: seeders/factories ou instruções para criar registros mínimos.

> **Checklist de README**
>
> Inclua: requisitos (PHP/MySQL), comandos de instalação, configuração .env, migrate/seed, como logar (usuários), e como testar a API (token).

### 9) Encerramento e próximos passos

Parabéns por chegar até aqui! 🎉

Agora que você concluiu o ciclo, próximos caminhos possíveis são:

- Refatorar regras de negócio para Services + testes Unit (melhor arquitetura).
- Melhorar UX (debounce, loading states, acessibilidade).
- Evoluir API (versionamento, filtros avançados, rate limit por usuário).
- Fortalecer produção (monitoramento, backups rotacionados, CI/CD com staging).

> **Dica final**
>
> Mostre o que você aprendeu, não só o que você fez. Se você consegue explicar decisões (por que usar Sanctum, por que eager loading, por que cache, por que testes), você domina o conteúdo.
