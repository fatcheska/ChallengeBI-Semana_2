# Challenge BI - Semana 2 - Alura

## Dashboard de Marketing

A pessoa que gerencia a área de marketing da AluraShop disponibilizou para a gente os dados da última campanha de marketing, para fazermos nossa análises para tomarem as melhores decisões.

## Base de Dados

A base de dados consiste em duas tabelas no formato JSON:
* Tabela dispositivos
* Tabela gênero e idade

## Ferramentas Utilizadas no Projeto

* Power BI

## Tratamento de Dados

* Limpeza dos dados: eliminação de linhas agregadores com valores "All" na coluna de Plataformas.

## Métricas

### Custo por clique
```
Custo por clique = 
DIVIDE(
    [Valor investido na campanha],
    SUM(Tabela_idade_e_genero[Cliques no link])
)
```

### Date Last Refreshed
```
Date Last Refreshed = VALUES ('Última Atualização'[Date Last Refreshed])
```

### ROAS
```
ROAS = 
DIVIDE(
    SUM(Tabela_idade_e_genero[Valor de conversão de compras]),
    SUM(Tabela_idade_e_genero[Quantia gasta (BRL)])
)
```

### Taxa de Conversão
```
Taxa de Conversão = 
DIVIDE(
    SUM(Tabela_idade_e_genero[Compras]),
    SUM(Tabela_idade_e_genero[Visualizações por página])
)
```

### Ticket Médio
```
Ticket Médio = 
DIVIDE(
    SUM(Tabela_dispositivos[Valor de conversão de compras]),
    SUM(Tabela_dispositivos[Compras])
    )
```

### Total de Compras
```
Total de Compras = SUM(Tabela_idade_e_genero[Compras])
```

### Total de conversão de compras
```
Total de conversão de compras = SUM(Tabela_idade_e_genero[Valor de conversão de compras])
```

### Valor investido na campanha
```
Valor investido na campanha = SUM(Tabela_idade_e_genero[Quantia gasta (BRL)])
```

## Relacionamentos
* Nenhum relacionamento, as tabelas trabalham de forma independente.
## Link do Dashboard
https://app.powerbi.com/view?r=eyJrIjoiMjVmNjBkYTUtMDViYy00NjA4LTkwOWUtNjMzZTg2MjExM2MyIiwidCI6IjJiZWZhNWY5LTEyMjUtNGViYi04MjFiLTM4Yzk1MWZkYjgyZSJ9
