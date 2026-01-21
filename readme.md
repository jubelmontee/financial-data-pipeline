# financial-data-pipeline

Projeto **de Engenharia de Dados (para estudo)** que constrói uma **pipeline de coleta e organização de dados financeiros** utilizando a **Arquitetura Medalhão (Bronze / Silver / Gold)**.

O objetivo principal é extrair cotações de ativos (ex.: **ouro, petróleo, prata** via **yFinance**) e **Bitcoin** (via **API**), salvar os dados em camadas e simular uma ingestão recorrente (ex.: **a cada 5 minutos**), conforme apresentado no vídeo de referência.

---

## Objetivo

Praticar conceitos essenciais de Engenharia de Dados:
* **Ingestão:** Extração de dados via APIs.
* **Tratamento/Padronização:** Limpeza e normalização de dados brutos.
* **Persistência por camadas:** Organização de dados seguindo boas práticas de Data Lake.
* **Arquitetura Medalhão:** Aplicar o fluxo do dado "bruto" ao "pronto para consumo".

---

## Arquitetura (Medalhão)

O fluxo de dados segue o padrão: **Fontes → Bronze → Silver → Gold**.

### 1. Fontes (APIs)
* **yFinance:** Extração de ativos como:
    * Ouro (`GC=F`)
    * Petróleo / Crude Oil (`CL=F`)
    * Prata (`SI=F`)
* **API de Bitcoin:** Cotação atual do BTC.
* **Execução:** Simulação de atualização frequente (ex.: a cada 5 minutos).

### 2. Camadas de Dados
* **Bronze (raw):** * Armazena o retorno bruto das APIs sem qualquer tratamento.
    * **Objetivo:** Garantir a rastreabilidade e permitir reprocessamento total se necessário.
* **Silver (curado):** * Dados limpos e normalizados.
    * Tratamento de tipos numéricos e data/hora, renomeação de colunas e validações básicas (nulos/formatos).
* **Gold (consumo):** * Estrutura final otimizada para BI, relatórios ou análise de dados.
    * Contém séries temporais consolidadas e indicadores (variação %, médias, etc.).

---

## Tecnologias Utilizadas

Em construção
---

## Estrutura  do Repositório

Em construção