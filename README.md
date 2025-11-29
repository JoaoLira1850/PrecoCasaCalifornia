# 🏠 Previsão de Preços de Imóveis na Califórnia (California Housing)

## 📄 Sobre o Projeto

Este projeto utiliza técnicas de **Machine Learning** para prever o valor mediano das casas em diferentes distritos da Califórnia. A análise foi realizada utilizando a linguagem Python e bibliotecas de Ciência de Dados, culminando na criação de um modelo de **Regressão Linear**.

O dataset utilizado é o **California Housing**, um clássico da biblioteca Scikit-Learn, que contém dados do censo de 1990.

## 📊 Dataset

O conjunto de dados possui 20.640 registros e 8 atributos preditores:

| Coluna | Descrição |
| :--- | :--- |
| **MedInc** | Renda mediana da região (em dezenas de milhares de dólares). |
| **HouseAge** | Idade mediana das casas na região. |
| **AveRooms** | Número médio de cômodos por domicílio. |
| **AveBedrms** | Número médio de quartos por domicílio. |
| **Population** | População total da região. |
| **AveOccup** | Média de ocupação (pessoas) por domicílio. |
| **Latitude** | Latitude da região. |
| **Longitude** | Longitude da região. |
| **Target** | **MedHouseVal**: Valor mediano das casas (variável alvo). |

## ⚙️ Etapas do Projeto

1.  **Coleta de Dados:** Importação do dataset via `sklearn.datasets`.
2.  **Análise Exploratória (EDA):**
    * Estatísticas descritivas.
    * Matriz de correlação (Heatmap).
    * Identificação de outliers e distribuições.
3.  **Pré-processamento:** Seleção de features relevantes para evitar multicolinearidade.
4.  **Modelagem:** Treinamento de um algoritmo de Regressão Linear Simples.
5.  **Validação:** Teste do modelo com dados não vistos (split 90/10).

## 📈 Resultados Obtidos

O modelo foi avaliado com as seguintes métricas de desempenho:

| Métrica | Resultado | Interpretação |
| :--- | :---: | :--- |
| **R² Score** | `0.48` | O modelo explica cerca de 48% da variação dos preços. |
| **MAE** | `0.61` | Erro Médio Absoluto (em $100k). |
| **MSE** | `0.68` | Erro Quadrático Médio. |

> **Insight Principal:** A variável **Renda Mediana (MedInc)** demonstrou a maior correlação positiva com o preço das casas, sendo o fator mais determinante para a predição neste modelo linear.

## 💻 Instalação e Execução

Para rodar este projeto localmente, você precisará das seguintes bibliotecas:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
