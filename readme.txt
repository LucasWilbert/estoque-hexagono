# estoque-hexagono

## Objetivo

Reorganizar o sistema *estoque-camadas* utilizando **Arquitetura Hexagonal**, separando regras de negócio da infraestrutura.

---

## Estrutura

```id="jzv1b5"
domain/        → regras de negócio  
application/   → casos de uso  
ports/         → interfaces (entrada e saída)  
adapters/      → implementações (controller e repository)  
```

---

## Fluxo

```id="q0q9jk"
Controller → UseCase → Port → Adapter
```

* Controller recebe a requisição
* UseCase executa a lógica
* Port define o contrato
* Adapter implementa o acesso externo

---

## Conceitos aplicados

* Separação de responsabilidades
* Baixo acoplamento
* Inversão de dependência

---

## Observação

O sistema não utiliza banco de dados real.
A persistência é simulada em memória.

---
