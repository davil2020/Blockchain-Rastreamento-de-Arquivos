# Projeto — Blockchain Didático para Rastreamento de Arquivos (Go)

Sistema **minimalista** em Go para registrar operações sobre arquivos (upload, leitura, edição) aplicando princípios essenciais de **blockchain**: encadeamento por hash, imutabilidade e consenso distribuído simples (maioria). O foco é **didático**: código pequeno, claro e fácil de expandir.

---

## ✨ Objetivos

- **Rastrear** operações em arquivos com histórico auditável.  
- **Registrar** cada operação como um bloco encadeado por hash.  
- **Validar** blocos entre nós via consenso simplificado (maioria).  
- **Ensinar** fundamentos de blockchain sem complexidade desnecessária.

---

## 🧱 Conceitos-chave

- **Bloco**: metadados da operação (arquivo, ação, autor, timestamp).  
- **Hash / prevHash**: garante a imutabilidade da cadeia.  
- **Consenso (maioria)**: bloco aceito quando a maioria dos peers confirma.  
- **Histórico por arquivo**: consulta rápida de todas as operações registradas.

---

## 🏗️ Arquitetura (visão geral)

- **Node (HTTP)**: endpoints para criar e consultar blocos/arquivos.  
- **Blockchain**: lista encadeada com validações de integridade.  
- **P2P simples**: broadcast de novos blocos para os peers.  
- **Storage**: memória por padrão; opção de persistência local.

**Fluxo**: cliente solicita operação → nó cria bloco → propaga aos peers → maioria aceita → cadeia é atualizada.

---
