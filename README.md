# CI/CD Docker Lab 🚀

Projeto prático de **CI/CD** utilizando **GitHub Actions** para automatizar o **build e teste de uma aplicação Docker**.

Este laboratório foi criado com foco em **aprendizado prático**, **boas práticas DevOps** e **portfólio profissional para vagas DevOps Júnior**.

[CI Status](https://github.com/danielviana2127/ci-cd-docker-lab/actions/workflows/ci.yml/badge.svg)


---

## 🎯 Objetivo do Projeto

* Demonstrar um pipeline de **Integração Contínua (CI)** funcional
* Automatizar o **build de imagens Docker**
* Executar **testes automáticos** em containers
* Aplicar boas práticas como **falha controlada** e **cleanup de recursos**
* Servir como projeto prático de **portfólio DevOps**

---

## 🛠️ Tecnologias Utilizadas

* **GitHub Actions** → Automação de CI/CD
* **Docker** → Containerização da aplicação
* **Nginx** → Servidor web para aplicação estática
* **Git / GitHub** → Versionamento e pipeline

---

## 🔄 Pipeline CI/CD

O pipeline é executado automaticamente nos seguintes eventos:

* `push` na branch `main`
* `pull_request`

### Etapas do Pipeline

1. Checkout do código
2. Build da imagem Docker
3. Execução do container
4. Teste automático via `curl`
5. Cleanup do container após o teste

📌 Caso o teste HTTP falhe, o pipeline é interrompido automaticamente.

---

## 📂 Estrutura do Projeto

```text
ci-cd-docker-lab/
├── app/
│   └── index.html
├── Dockerfile
├── .dockerignore
├── .github/
│   └── workflows/
│       └── ci.yml
└── README.md
```

---

## ▶️ Execução Local

### Build da imagem Docker

```bash
docker build -t ci-cd-docker-lab .
```

### Executar o container localmente

```bash
docker run -p 8080:80 ci-cd-docker-lab
```

---

## 🌐 Acessar a Aplicação no Navegador

Após subir o container, acesse no navegador:

```
http://localhost:8080
```

Você deverá visualizar a página com a mensagem indicando que o **CI/CD está funcionando corretamente**.

---

## 📈 Diferenciais do Projeto

* Pipeline CI simples, claro e funcional
* Teste automatizado de containers via HTTP
* Limpeza automática de recursos após execução
* Código reproduzível e fácil de entender
* Foco em práticas reais de CI/CD utilizadas no mercado

---

## 👨‍💻 Autor

**Daniel Viana**
Projeto desenvolvido para estudos em **DevOps, CI/CD e Docker**.

