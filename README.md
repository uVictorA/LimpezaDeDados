# LimpezaDeDados
Limpeza de dados em uma base de compras 
# Regras de Associação em Compras

Este projeto tem como objetivo aplicar técnicas de mineração de dados para identificar **padrões de compra** em uma base de dados de transações de produtos.

Objetivo

Utilizar algoritmos de **Regras de Associação** para descobrir quais produtos são frequentemente comprados juntos, ajudando em estratégias como:
- Sugestão de produtos (recomendação)
- Agrupamento em kits
- Otimização de layout em pontos de venda

Pré-processamento dos Dados

A base de dados original foi tratada para corrigir:
- Nomes de produtos inconsistentes
- Valores inválidos ou faltantes
- Agrupamento de compras pelo identificador `id_da_compra`

Cada transação foi transformada em uma lista de produtos comprados juntos.

Técnicas Utilizadas

- **Algoritmo Apriori** (`mlxtend.frequent_patterns`)
- **FP-Growth** (anteriormente usado para comparação)
- **Geração de Regras de Associação**
    - Métricas: *support*, *confidence* e *lift*

Visualizações

- **Gráficos de Distribuição** das métricas
- **Gráfico de Dispersão 3D** (support x confidence x lift)
- **Gráfico de Coordenadas Paralelas** (comparando regras)
- **Heatmap de Clusters de Regras**
- **Rede de Co-ocorrência de Itens**
- **Grafo das Regras de Associação** (antecedentes → consequentes)

Exemplos de Regras Geradas

```text
{pão} → {manteiga}
    Support: 0.12
    Confidence: 0.85
    Lift: 2.3

{leite, cereal} → {açúcar}
    Support: 0.05
    Confidence: 0.78
    Lift: 3.1
