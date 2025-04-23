# azure-data-factory-redundancia-arquivos

# azure-data-factory-redundancia-arquivos

# 🔄 Projeto: Redundância de Arquivos com Azure Data Factory

Este repositório documenta o processo completo de criação de redundância de arquivos a partir de uma fonte SQL Server on-premises para o Azure Blob Storage, utilizando **Azure Data Factory**.

---

## 📌 Objetivo

Demonstrar uma solução de movimentação de dados segura, estruturada e automatizada com uso das ferramentas do Azure, convertendo tabelas SQL em arquivos `.TXT` organizados por camadas (neste caso, bronze).

---

## 🧱 Arquitetura do Fluxo

```mermaid
graph TD
    A[SQL Server (on-premises)] --> B[Integration Runtime Self-hosted]
    B --> C[Linked Service - SQL Server]
    C --> D[Pipeline de Cópia]
    D --> E[Linked Service - Blob Storage]
    E --> F[Azure Data Lake - Bronze Layer]
```

---

## ⚙️ Componentes Utilizados

- **SQL Server Local (on-premises)**  
- **Integration Runtime Self-hosted**
- **Azure Data Factory (ADF)**
- **Azure Blob Storage (camada bronze)**
- **Linked Services** (SQL e Blob)
- **Datasets** de origem e destino
- **Pipeline com atividade Copy Data**

---

## 🖼️ Prints do Projeto

### 🧭 Visão geral dos recursos

![Recursos Azure](imagens/01_Recursos_Azure.png)  
![Dashboard Azure](imagens/02_Dashboard_Azure_Recursos.png)

### ⚙️ Azure Data Factory

![Visão Geral ADF](imagens/03_Visao_Geral_ADF.png)  
![Recursos Recentes ADF](imagens/04_Recursos_Recentes_DataFactory.png)  
![Painel de Monitoramento](imagens/05_Resumo_DataFactory_Painel.png)  
![Criação do Pipeline](imagens/06_ADF_Pipeline_Criacao.png)

### 📥 Fonte de Dados

![Dataset SQL](imagens/07_Dataset_SQL.png)  
![Dataset TXT](imagens/08_Dataset_TXT.png)  
![Editor SQL Server](imagens/09_SQL_Server_Editor.png)  
![Consulta SQL Management](imagens/10_SQL_Management_Consulta.png)

### 💾 Blob Storage

![Arquivo Salvo](imagens/11_Arquivo_Salvo_Em_Blob.png)  
![Propriedades do Arquivo](imagens/12_Arquivo_Propriedades.png)  
![Execução Bem-Sucedida](imagens/13_Execucao_Sucesso.png)  
![Arquivo na Camada Bronze](imagens/14_Listagem_Arquivo_Blob.png)

---

## 📊 Diagramas do Processo

![Diagrama ADF 1](imagens/15_Diagrama_Processo_1.png)  
![Diagrama ADF 2](imagens/16_Diagrama_Processo_2.png)  
![Fluxo Simplificado](imagens/17_Fluxo_Simplificado.png)


---

## 📘 Etapas Executadas

1. Configuração de **SQL Server on-premises** e criação da tabela.
2. Instalação do **Integration Runtime Self-hosted**.
3. Criação dos **Linked Services** (SQL + Blob).
4. Criação dos datasets de origem e destino.
5. Criação do pipeline com atividade de cópia (`Copy Data`).
6. Publicação e execução da pipeline.
7. Geração do arquivo `.TXT` na camada **bronze** do Blob.
8. Verificação de execução e armazenamento redundante.

---

## 📚 Aprendizados

- Montar pipelines no Azure Data Factory
- Trabalhar com integração entre ambientes locais e nuvem
- Aplicar arquitetura em camadas para redundância de dados
- Trabalhar com Linked Services, datasets e Blob Storage
- Analisar execuções e gerar arquivos em formatos padronizados

---

## 👩‍💻 Sobre mim

Me chamo **Lauren Freitas**, sou comissária de bordo em transição para a área de tecnologia.  
Atualmente estudo **Análise e Desenvolvimento de Sistemas** e me dedico a aprender sobre **automção, dados e nuvem**, desenvolvendo projetos práticos como este.

[![LinkedIn](https://img.shields.io/badge/-Lauren%20Freitas-0077B5?logo=linkedin&style=for-the-badge)](https://www.linkedin.com/in/laurend-freitas)  
[![GitHub](https://img.shields.io/badge/-@Lauren--Freitas-181717?logo=github&style=for-the-badge)](https://github.com/Lauren-Freitas)

---

✨ Projeto desenvolvido como parte do **bootcamp DIO – Azure Data Fundamentals**

![17_Fluxo_Simplificado](https://github.com/user-attachments/assets/584b31a4-e26e-4b84-a17f-ac4138983570)
![16_Diagrama_Processo_2](https://github.com/user-attachments/assets/c01803a0-3d84-40bf-b411-8b04f0ce127d)
![15_Diagrama_Processo_1](https://github.com/user-attachments/assets/167145cc-977f-4f54-b44d-faa8e8957cd5)
![14_Listagem_Arquivo_Blob](https://github.com/user-attachments/assets/66a604bb-e263-4405-815a-beb9f8785cff)
![13_Execucao_Sucesso](https://github.com/user-attachments/assets/09a19116-b243-41dd-831e-34f4351644fd)
![12_Arquivo_Propriedades](https://github.com/user-attachments/assets/d556285c-3349-4123-8ec6-bd0a39e20ef4)
![11_Arquivo_Salvo_Em_Blob](https://github.com/user-attachments/assets/b172082f-8fac-48bf-bb2b-b28b54f8fb09)
![10_SQL_Management_Consulta](https://github.com/user-attachments/assets/7393b5e9-3ce9-4371-921b-491013413d08)
![09_SQL_Server_Editor](https://github.com/user-attachments/assets/b9e33361-da16-4e32-b998-cb1652ceb1e2)
![08_Dataset_TXT](https://github.com/user-attachments/assets/cab09bb9-d9ed-44f9-bfae-e647d076232f)
![07_Dataset_SQL](https://github.com/user-attachments/assets/be65943c-a6a8-419e-ad2b-5b11ccb820b8)
![06_ADF_Pipeline_Criacao](https://github.com/user-attachments/assets/541b4715-60b4-446a-b5dc-7c058d2683af)
![05_Resumo_DataFactory_Painel](https://github.com/user-attachments/assets/f11a0395-3546-481f-a160-90576960672f)
![04_Recursos_Recentes_DataFactory](https://github.com/user-attachments/assets/c5a21b66-6f81-4723-bdcb-38b40ddce97d)
![03_Visao_Geral_ADF](https://github.com/user-attachments/assets/a909e5f5-df24-450e-abf0-37d03abc18b3)
![02_Dashboard_Azure_Recursos](https://github.com/user-attachments/assets/166136e1-0647-4c9b-af10-6a462e98447a)
![01_Recursos_Azure](https://github.com/user-attachments/assets/4c0d0c32-f957-4e93-a3bd-5ee00f3907c2)
