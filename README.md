## Manifestos-k8s

Repositório contendo os manifestos Kubernetes utilizados para orquestrar a infraestrutura de uma aplicação em ambiente de desenvolvimento (**Dev**). Os manifestos estão organizados por componentes da aplicação e seguem uma estrutura clara entre **frontend**, **backend** e **monitoramento**.

### 📋 Índice

- [Introdução](#introdução-1)
- [Estrutura do Repositório](#estrutura-do-repositório)
- [Componentes Incluídos](#componentes-incluídos)
- [Ambiente de Destino](#ambiente-de-destino)
- [Aplicação dos Manifestos](#aplicação-dos-manifestos)
- [Dependências](#dependências)
- [Contribuição](#contribuição-1)
- [Licença](#licença-1)

### 📖 Introdução

Este repositório agrupa os arquivos de configuração do Kubernetes para a aplicação da organização. Ele permite a manutenção centralizada dos recursos de infraestrutura, facilitando o deploy e a atualização dos serviços que compõem o sistema.

### 📂 Estrutura do Repositório

Os manifestos estão organizados em duas pastas principais:

```bash
manifestos-k8s/
├── backend/
│   ├── configmap.yaml
│   ├── deployment.yaml
│   ├── service.yaml
│   └── secret.yaml
├── frontend/
│   ├── configmap.yaml
│   ├── deployment.yaml
│   ├── ingress.yaml
│   ├── service.yaml
│   └── secret.yaml
└── monitoring/
    └── (se aplicável)
```

### 🧩 Componentes Incluídos

O repositório inclui os seguintes tipos de recursos Kubernetes:

- `ConfigMap` – Configurações da aplicação
- `Deployment` – Definição das réplicas e containers
- `Service` – Exposição interna dos serviços
- `Ingress` – Exposição externa (frontend)
- `Secret` – Informações sensíveis (senhas, tokens)

### 🌐 Ambiente de Destino

Atualmente, os manifestos são direcionados ao **ambiente de desenvolvimento** (*Dev*). Outros ambientes podem ser adicionados futuramente.

### 🚀 Aplicação dos Manifestos

A aplicação dos manifestos deve ser feita com `kubectl`. Exemplo:

```bash
kubectl apply -f backend/
kubectl apply -f frontend/
```

> 💡 Certifique-se de estar no contexto correto do cluster Kubernetes (`kubectl config current-context`).

### 📦 Dependências

- [Kubernetes CLI (kubectl)](https://kubernetes.io/docs/tasks/tools/)
- Acesso ao cluster de desenvolvimento

### 🤝 Contribuição

Pull requests são bem-vindos. Sinta-se à vontade para sugerir melhorias ou adicionar novos recursos. Por enquanto, não há testes ou validações automáticas — esse é um ponto de evolução futura.
