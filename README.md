# Sistema de Emissão de Notas Fiscais

![Status](https://img.shields.io/badge/status-desafio%20t%C3%A9cnico-2ea44f?style=for-the-badge)
![Node.js](https://img.shields.io/badge/Node.js-backend-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![Express](https://img.shields.io/badge/Express.js-000000?style=for-the-badge&logo=express&logoColor=white)
![MariaDB](https://img.shields.io/badge/MariaDB-003545?style=for-the-badge&logo=mariadb&logoColor=white)
![Licença](https://img.shields.io/badge/licença-MIT-042570?style=for-the-badge)

> Desafio de backend para candidatos: construir uma API de emissão de notas fiscais eletrônicas, com
> validações fiscais, cálculo de impostos e geração de XML. Este repositório traz o enunciado; o
> projeto de cada candidato roda no próprio deploy, na Vercel ou na Netlify.

## Sumário

- [Sobre o sistema](#-sobre-o-sistema)
- [O que ele faz](#-o-que-ele-faz)
- [Ajustes e melhorias](#-ajustes-e-melhorias)
- [Pré-requisitos](#-pré-requisitos)
- [Instalando o Sistema de Emissão de Notas Fiscais](#-instalando-o-sistema-de-emissão-de-notas-fiscais)
- [Usando o Sistema de Emissão de Notas Fiscais](#-usando-o-sistema-de-emissão-de-notas-fiscais)
- [Configuração](#-configuração)
- [Arquitetura](#-arquitetura)
- [Testes](#-testes)
- [CI e deploy](#-ci-e-deploy)
- [Contribuindo para o Sistema de Emissão de Notas Fiscais](#-contribuindo-para-o-sistema-de-emissão-de-notas-fiscais)
- [Colaboradores](#-colaboradores)
- [Documentação](#-documentação)
- [Licença](#-licença)

## 📌 Sobre o sistema

Bem-vindo ao desafio de backend!

Este projeto tem o objetivo de aplicar boas práticas, regras de negócio reais e validações fiscais!

## 🧭 O que ele faz

### Funcionalidades

- Cadastro de **clientes** e **produtos**
- Emissão de **notas fiscais eletrônicas**
- Validações fiscais:
  - CNPJ
  - CFOP
  - NCM
- Cálculo automático de impostos:
  - **ICMS** (18%)
  - **IPI** (4%)
- Geração de **XML da Nota Fiscal**
- Listagem e consulta de notas emitidas
- Histórico de emissão
- Autenticação de usuários via JWT

### Regras de Negócio

- **CNPJ** validado conforme Receita Federal
- **CFOP** e **NCM** validados conforme padrões fiscais
- **ICMS** aplicado em todos os produtos (18%)
- **IPI** aplicado se o produto for industrializado (4%)

## 🚧 Ajustes e melhorias

O enunciado não traz lista de melhorias: o escopo do desafio é o descrito nesta página.

## 💻 Pré-requisitos

As tecnologias que o desafio pede estão em [Arquitetura](#-arquitetura). Você também precisa de uma
conta no GitHub para fazer o fork.

## 🚀 Instalando o Sistema de Emissão de Notas Fiscais

Este repositório traz só o enunciado: não há código para instalar. As instruções de instalação do
seu projeto fazem parte da [entrega](#-contribuindo-para-o-sistema-de-emissão-de-notas-fiscais).

## ☕ Usando o Sistema de Emissão de Notas Fiscais

### Endpoints Principais

**Clientes**

- `POST /clients` - Criar cliente
- `GET /clients` - Listar clientes

**Produtos**

- `POST /products` - Cadastrar produto
- `GET /products` - Listar produtos

**Notas Fiscais**

- `POST /invoices` - Emitir nota fiscal
- `GET /invoices` - Listar notas
- `GET /invoices/:id` - Detalhar nota

### Exemplo de Payload para Emissão de Nota

```json
{
  "clientId": "cliente-uuid",
  "products": [
    {
      "productId": "produto-uuid",
      "quantity": 3
    },
    {
      "productId": "produto-uuid-2",
      "quantity": 1
    }
  ]
}
```

A resposta incluirá:

- Detalhes da nota
- Cálculo de impostos
- Valor total
- XML da nota em base64

## 🔧 Configuração

O enunciado não define variáveis de ambiente: documente as do seu projeto no README da entrega.

## 🧱 Arquitetura

### Tecnologias Utilizadas

- **Node.js** + **TypeScript**
- **Express.js**
- **MariaDB**
- **Joi** para validações
- **JWT** para autenticação
- **Swagger** para documentação da API

## 🧪 Testes

O enunciado não exige testes automatizados.

## 🔁 CI e deploy

O enunciado não exige pipeline de CI. A entrega inclui a URL do deploy na Vercel ou na Netlify.

## 📫 Contribuindo para o Sistema de Emissão de Notas Fiscais

Este repositório não recebe contribuições de código: cada candidato trabalha no próprio fork,
seguindo as regras abaixo.

### Regras de Entrega

#### **1. Repositório no GitHub**

- Faça um **fork** deste repositório para sua conta pessoal
- Mantenha o repositório **público** durante o desenvolvimento
- Nome do repositório: `nf-emition-system-[seu-nome]`

#### **2. Padrão de Commits**

- Use **commits atômicos** (1 feature por commit)
- Formato: `tipo: descrição` (ex: `feat: autenticação jwt`)
- Tipos válidos: `feat`, `fix`, `style`, `refactor`, `docs`, `test`

#### **3. Organização do Código**

- Mantenha uma **estrutura de pastas clara**
- **Documente** componentes complexos
- Siga boas práticas de **clean code**

#### **4. Prazo de Entrega**

- **7 dias corridos** a partir do recebimento
- **Entregas tardias serão desconsideradas**

#### **5. Itens Obrigatórios para Entrega**

- ✅ Link do **repositório GitHub** (com histórico de commits)
- ✅ URL do **deploy na vercel ou Netlify**
- ✅ README completo com:
  - 📌 **Instruções de instalação**
  - 📌 **Dependências utilizadas**
  - 📌 **Dificuldades encontradas**

#### **6. Critérios de Avaliação**

- ✅ **Funcionalidades implementadas**
- ✅ **Qualidade do código**
- ✅ **Organização dos commits**
- ✅ **Documentação**

## 🤝 Colaboradores

Este desafio é mantido pela GpDevLab.

## 📚 Documentação

Não há documentação além deste enunciado.

## 📝 Licença

Este projeto está sob a licença MIT. Veja o arquivo [LICENSE](LICENSE).
