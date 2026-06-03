# 🏥 BioSaúde Farma · Landing Page Automática

Este repositório contém o código-fonte e a infraestrutura como código (IaaS) para a implantação automatizada da solução web da **BioSaúde Farma**. O objetivo principal do projeto é aplicar os conceitos de Computação em Nuvem, Containerização e Integração/Entrega Contínua (CI/CD).

## 📊 Arquitetura e Fases do Projeto

A solução foi dividida em 4 fases fundamentais de desenvolvimento e operações:

* **Fase 1 · Infraestrutura Base:** Provisionamento de uma instância virtual Amazon EC2 (`Amazon_Farmaceutics`) executando Ubuntu Server, com configuração de Security Groups para liberação das portas 80 (HTTP) e 22 (SSH).
* **Fase 2 · Gestão de Repositório:** Centralização do código-fonte e versionamento utilizando o GitHub como fonte única da verdade.
* **Fase 3 · GitActions (CI/CD):** Criação de uma esteira de automação que realiza o build e o deploy automático a cada atualização na branch `main`.
* **Fase 4 · IaaS (Docker):** Containerização da aplicação utilizando Docker para garantir portabilidade e isolamento do servidor web.

---

## 🏛️ Alinhamento com os Pilares AWS Well-Architected

A estrutura deste projeto foi desenhada seguindo as boas práticas de arquitetura de nuvem da AWS:

1. **Excelência Operacional:** Toda a implantação foi automatizada via pipeline de CI/CD, eliminando processos manuais e permitindo rastreabilidade de alterações.
2. **Segurança:** Utilização do *GitHub Secrets* para mascarar e proteger as chaves de acesso SSH (`.pem`) do servidor, impedindo a exposição de dados sensíveis no código.
3. **Eficiência de Performance:** A aplicação foi isolada em um container Docker leve, otimizando o consumo de CPU e Memória da instância EC2.

---

## 🚀 Como Visualizar o Projeto

* **URL de Produção (IP Público EC2):** http://54.166.139.61
* **Rótulo da Instância:** `Amazon_Farmaceutics`
