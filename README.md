# 🧪 Chaos Simulator – DevOps Incident Lab

## About the Project

Chaos Simulator is a lightweight application designed to simulate common failure scenarios in production environments. It's ideal for training developers, SREs, and DevOps engineers to identify issues, validate observability tools, and practice incident response safely.

### 🔥 Available Failure Scenarios

- ❌ Graceful shutdown (`/exit/success`)
- 💥 Crash with error (`/exit/fail`)
- 🧠 High memory usage (`/stress/memory`)
- 🧮 High CPU load (`/stress/cpu`)
- 🚫 Temporary unavailability for 60s (`/health`)
- ⚠️ Manual application breakdown (`/break`)

> The application exposes an HTML interface with buttons to trigger each chaos scenario.

---

## 🚀 Running the Application (Docker)

```bash
docker build -t chaos-simulator ./src
docker run -p 3000:3000 --name chaos-simulator chaos-simulator
````

Then open your browser at [http://localhost:3000](http://localhost:3000)

---

## 🔧 Requirements

* Docker
* Optional: `stress` installed in the container (used via `exec` for CPU/memory overload)

---

## Sobre o Projeto

O **Simulador do Caos** é uma aplicação leve criada para simular cenários reais de falha em produção. O objetivo é treinar desenvolvedores, SREs e engenheiros DevOps em práticas de monitoramento, resposta a incidentes e resiliência.

### 🔥 Cenários Disponíveis

* ❌ Encerramento controlado da aplicação
* 💥 Encerramento com erro
* 🧠 Uso elevado de memória
* 🧮 Estresse de CPU
* 🚫 Indisponibilidade temporária
* ⚠️ Aplicação quebrada manualmente

> Um painel web simples com botões permite disparar cada cenário com um clique.

---

## 🚀 Como Executar (Docker)

```bash
docker build -t simulador-do-caos ./src
docker run -p 3000:3000 --name simulador-do-caos simulador-do-caos
```
```

Acesse via navegador: [http://localhost:3000](http://localhost:3000)

---

## 📁 Estrutura do Projeto

```
├── src
│   ├── server.ts           # Servidor Express
│   ├── views/index.ejs     # Interface HTML
│   ├── Dockerfile          # Multi-stage build com stress tool
│   ├── package.json        # Dependências do projeto
│   └── tsconfig.json       # Configuração TypeScript
```

---

## 🛠 Ferramentas Utilizadas

* TypeScript
* Node.js + Express
* Docker (multi-stage build)
* stress (para carga de CPU e memória)
* EJS (renderização da UI)

---