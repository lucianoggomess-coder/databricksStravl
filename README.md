# Recomendador de destinos de viagem

Trabalho final da disciplina **Hands-On – Engenharia de Dados em Big Data e Analytics** – MBA em Engenharia de Dados, Universidade Presbiteriana Mackenzie.

## Integrantes
- José Carlos Marques Filho
- Luciano Gomes da Silva
- Renato de Oliveira de Souza

## O problema
Agências de viagem oferecem os mesmos pacotes para todos os clientes. O projeto recomenda os destinos com maior chance de aceitação a partir de um formulário curto: tipo de grupo, experiência desejada, paisagem, estação do ano e orçamento.

## Base de dados
[Stravl-Data](https://github.com/Stravl/Stravl-Data): 80.301 viajantes e 851.133 avaliações (swipes Sim / Não / Talvez) de 1.486 destinos. A base é anonimizada na origem. Os arquivos de dados não ficam neste repositório; eles são carregados no Databricks.

## Arquitetura
Lakehouse no Databricks com camadas Bronze, Silver e Gold em Delta Lake, governança pelo Unity Catalog, modelo de recomendação em Python e dashboard no Power BI.

## Notebooks
| Notebook | Camada | O que faz |
|---|---|---|
| `01_Bronze_Importacao_Stravl.ipynb` | Bronze | Importa os arquivos originais do Stravl |
| `02_Silver_Tratamento.ipynb` | Silver | Limpa e trata os dados |
| `3_Gold_Filezinho.ipynb` | Gold | Gera as tabelas finais para análise e modelo |
| `4 - Análises.ipynb` | Análise | Análise exploratória dos dados |

## Como executar
1. No Databricks, carregue os arquivos do Stravl em um Volume do catálogo `workspace`.
2. Conecte este repositório pelas Git Folders do Databricks.
3. Rode os notebooks na ordem: 01 → 02 → 3 → 4.
