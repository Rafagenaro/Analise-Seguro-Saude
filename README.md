# Análise Exploratória de Dados - Custos de Seguro de Saúde

Este projeto tem como objetivo realizar uma Análise Exploratória de Dados (EDA) em um dataset de custos de seguro de saúde.  
A análise busca identificar os principais fatores que influenciam os valores cobrados, entendendo como características demográficas e de estilo de vida se correlacionam com os custos médicos.

---

## Dataset

O dataset contém variáveis relacionadas às características dos beneficiários de um seguro de saúde.  

Principais colunas:
- `age` → idade do beneficiário  
- `sex` → gênero do beneficiário  
- `bmi` → Índice de Massa Corporal (IMC)  
- `children` → número de dependentes cobertos pelo seguro  
- `smoker` → se o beneficiário é fumante (`yes` / `no`)  
- `region` → região geográfica do beneficiário nos EUA  
- `charges` → custos médicos individuais cobrados pelo seguro (**variável-alvo**)  

---

## Ferramentas e Bibliotecas

A análise foi conduzida em Python, utilizando:  
- **Pandas** → manipulação e limpeza dos dados  
- **Matplotlib** e **Seaborn** → visualizações  
- **Jupyter Notebook** → desenvolvimento da análise  

---

## Etapas da Análise

1. **Carregamento e inspeção dos dados**  
   - Leitura do arquivo insurance.csv e verificação inicial da estrutura.

2. **Estatísticas descritivas e distribuições**  
   - Análise da distribuição da variável `charges` (custos).

3. **Análise univariada e multivariada**  
   - Exploração de variáveis categóricas (como `smoker`) e numéricas (como `age` e `bmi`).

4. **Correlação entre variáveis**  
   - Uso de um mapa de calor para quantificar a relação entre as variáveis numéricas.

5. **Visualizações para identificar padrões**  
   - Criação de gráficos de dispersão e boxplots para visualizar as relações.

6. **Extração de insights principais**  
   - Sumarização das descobertas mais relevantes.

---

## Principais Insights

- **Ser fumante (`smoker`) é o fator de maior impacto nos custos do seguro.**  
  Fumantes apresentam uma mediana de custos significativamente mais alta e uma maior dispersão nos valores, indicando cobranças muito mais elevadas em comparação aos não fumantes.  

- **Idade (`age`) possui uma correlação positiva (0.30) com os custos.**  
  Pessoas mais velhas tendem a ter seguros mais caros.  

- **A distribuição dos custos (`charges`) é assimétrica à direita.**  
  A maioria dos beneficiários possui custos relativamente baixos, mas um pequeno número de pessoas com custos muito altos eleva a média geral.  
  - **Média:** ~13.270  
  - **Mediana:** ~9.382  

- **Índice de Massa Corporal (`bmi`) apresenta correlação positiva, porém fraca (0.20).**  

- **Número de dependentes (`children`) mostrou correlação muito fraca (0.07), quase insignificante.**

