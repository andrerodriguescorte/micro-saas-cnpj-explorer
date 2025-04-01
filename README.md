# MicroSaaS - CNPJ Explorer

[![.NET](https://img.shields.io/badge/.NET-8.0-blue)](#)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](#)
[![Status](https://img.shields.io/badge/status-em%20desenvolvimento-yellow)](#)

MicroSaaS para **consulta de CNPJ** via [ReceitaWS](https://developers.receitaws.com.br/#/operations/queryCNPJFree), com armazenamento no banco analítico **ClickHouse** e exibição dos dados em um painel web. Desenvolvido com **ASP.NET Core 8** e arquitetura **DDD**.

> ⚠️ Projeto de estudo com fins didáticos e exploratórios. Não utilizar em produção sem ajustes de segurança e escalabilidade.

---

## 🔧 Tecnologias Utilizadas

- ASP.NET Core 8
- Domain-Driven Design (DDD)
- ClickHouse
- ReceitaWS API (Consulta pública de CNPJ)
- Frontend web (Razor Pages ou SPA)

---

## 📁 Estrutura do Projeto

```
/src
├── MicroSaaS.CNPJ.Explorer.Application.Api                  # Micro API ASP.NET Core
├── MicroSaaS.CNPJ.Explorer.Application.Domain               # Entidades e regras de negócio
├── MicroSaaS.CNPJ.Explorer.Application.Application          # Casos de uso
├── MicroSaaS.CNPJ.Explorer.Application.Infrastructure       # Integrações externas e repositórios (ClickHouse, ReceitaWS)
└── MicroSaaS.CNPJ.Explorer.Application.Presentation         # Painel web com tela de pesquisa e exibição de dados

/tests
├── MicroSaaS.CNPJ.Explorer.Application.Tests 
```

---

## 🔄 Fluxo de Branches

- `dev` → Desenvolvimento contínuo
- `sandbox` → Homologação / testes finais
- `master` → Produção

---

## 🚀 Como rodar o projeto

1. Clone o repositório:

```bash
git clone https://github.com/andrerodriguescorte/micro-saas-cnpj-explorer.git
cd micro-saas-cnpj-explorer
```

2. Configure as variáveis de ambiente ou `appsettings.json` com:
   - Chave de acesso da API ReceitaWS (se necessário)
   - Conexão com o banco ClickHouse

3. Execute o projeto:

```bash
dotnet run --project src/Api
```

4. Acesse a interface web (por padrão):
```
http://localhost:5000
```

---

## 🧪 Executando Testes

```bash
dotnet test
```

---

## 🧠 Funcionalidades previstas

- ✅ Consulta pública de CNPJ na ReceitaWS
- ✅ Armazenamento dos dados em ClickHouse
- ✅ Painel web com tela de pesquisa e visualização
- ⏳ Histórico de consultas e analytics
- ⏳ Exportação de dados

---

## 📄 Licença

Este projeto está licenciado sob os termos da licença [MIT](LICENSE).

---

## 🤝 Contribuição

Contribuições são bem-vindas! Este projeto tem foco educacional e serve como base para construção de soluções reais com ASP.NET Core e arquitetura de micro serviços.
