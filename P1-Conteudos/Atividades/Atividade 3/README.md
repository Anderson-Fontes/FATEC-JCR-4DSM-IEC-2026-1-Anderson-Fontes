# Entrega da Atividade - Aula 03: Automação com GitHub Actions

**Aluno:** Anderson
**Disciplina:** Integração e Entrega Contínua (IEC)
**Professora:** Lucineide

## Objetivo
Habilitar e configurar o GitHub Actions para integração contínua no repositório.

## Exercícios Concluídos

### 1. Ativação e Criação do Workflow Inicial
Foi criado o arquivo `ci.yml` através da aba Actions do repositório. O código YAML configurado estabelece um job de build rodando em ambiente Linux (`ubuntu-latest`):

```yaml
name: CI Simples
on:
  push:
    branches: [ dev ]
  pull_request:
    branches: [ dev ]
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout do repositório
        uses: actions/checkout@v4
      - name: Teste de funcionamento
        run: echo "Cl funcionando no projeto INPE!"
