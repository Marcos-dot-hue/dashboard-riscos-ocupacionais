# 📊 Dashboard Executivo de Riscos Ocupacionais e Psicossociais

Solução completa de visualização de dados voltada para a Gestão de Segurança e Saúde do Trabalho (SST), integrando automação de fluxos via **n8n** e um painel executivo interativo em **HTML5/JavaScript (ECharts)**.

---

## 🚀 Visão Geral do Projeto
O objetivo deste projeto foi estruturar um pipeline automatizado de dados e entregar um painel executivo limpo, responsivo e acionável. A ferramenta sintetiza indicadores complexos de fatores de risco psicossocial e ocupacional, permitindo que a liderança tome decisões rápidas baseadas em evidências de conformidade e bem-estar corporativo.

---

## ⚙️ Arquitetura e Tecnologias
O projeto foi desenvolvido utilizando uma stack moderna e leve:
* **Automação & Processamento:** [n8n](https://n8n.io/) rodando em ambiente containerizado (Docker) na porta `5678`, com dados persistidos via volumes locais para garantir segurança contra perdas de dados.
* **Frontend / Dashboard:** HTML5, CSS3 (Flexbox), JavaScript e **Apache ECharts** (embutido via base64 para total portabilidade sem dependência de CDNs externos).
* **Indicadores (KPIs):** Monitoramento de criticidade, taxas de incidência e matrizes de risco.

---

## 📸 Demonstração do Projeto

### 1. Painel Executivo (Dashboard)
*(Substitua o link abaixo pela imagem real do seu dashboard rodando)*
![Dashboard Executivo](caminho-para-sua-imagem/dashboard-preview.png)

### 2. Fluxo Automatizado no n8n
*(Substitua o link abaixo pela imagem real do seu workflow no n8n)*
![Fluxo n8n](caminho-para-sua-imagem/n8n-workflow-preview.png)

---

## 🛠️ Como Executar o Projeto Localmente

### Pré-requisitos
* Docker e Docker Compose instalados na sua máquina.

### 1. Subindo o ambiente n8n com persistência de dados
Para garantir que você não perca suas construções e fluxos na porta `5678`, execute o container com mapeamento de volume:

```bash
docker run -d \
  --name n8n \
  -p 5678:5678 \
  -v ~/.n8n:/home/node/.n8n \
  n8nio/n8n
