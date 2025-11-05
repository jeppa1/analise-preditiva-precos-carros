# 🚗 Análise Preditiva de Preços de Veículos (Portfólio)

**Status:** Projeto Concluído ✅

Este repositório contém um projeto completo de Ciência de Dados para analisar e prever o preço de veículos usados. O notebook (`.ipynb`) demonstra todo o fluxo de trabalho, desde a limpeza dos dados até a construção de um modelo de Machine Learning com **98,86% de precisão (R²)**.

### 🔗 Links Rápidos
* **[Ver o Notebook no Kaggle](https://www.kaggle.com/code/jadsonchagas/an-lise-metodol-gica-de-pre-os-de-carros)**
* **[Notebook (GitHub)](./analise_preditiva_preco_carros.ipynb)**

---

### 1. Visão Geral do Projeto

O objetivo deste projeto foi utilizar um conjunto de dados de preços de carros para construir um modelo preditivo. Mais do que apenas aplicar um algoritmo, o foco foi seguir um **escopo metodológico rigoroso** para garantir que a análise fosse estatisticamente sólida e os resultados, confiáveis.

### 2. Metodologia

O fluxo de trabalho seguiu as etapas clássicas de um projeto de Ciência de Dados:

1.  **Definição do Problema:** Entender quais fatores (`Brand`, `Year`, `Mileage`, etc.) impactam o `Price` final de um veículo.
2.  **Tratamento de Dados:**
    * Limpeza de dados duplicados.
    * **Engenharia de Features:** Criação da feature `Age` (Idade do Veículo) a partir do `Year` e aplicação de uma **transformação logarítmica** (`log_Price`) na variável alvo para normalizar sua distribuição, uma etapa crucial para a performance do modelo.
3.  **Análise Exploratória de Dados (AED):**
    * Análise da distribuição do preço e das principais features numéricas usando histogramas e boxplots.
    * Investigação de correlações entre `Price`, `Age`, `Mileage` e `Engine_Size` usando `Heatmaps` (Mapas de Calor).
    * Análise de variáveis categóricas (`Fuel_Type`, `Transmission`) para identificar diferenças de preço.
4.  **Modelagem Preditiva:**
    * Criação de um `Pipeline` robusto do Scikit-learn, incluindo `StandardScaler` (para escalonamento de dados) e `OneHotEncoder` (para tratar variáveis categóricas).
    * Comparação de um modelo *baseline* (Regressão Linear) com um modelo avançado (Random Forest Regressor).

### 3. Resultados e Insights

O modelo **Random Forest Regressor** foi o grande vencedor, apresentando resultados excelentes e demonstrando a capacidade de capturar relações não-lineares nos dados.

| Modelo | R² (Score de Teste) | RMSE (Erro em Log) |
| :--- | :---: | :---: |
| Regressão Linear | 0.9387 | 0.0980 |
| **Random Forest** | **0.9886** | **0.0423** |

O modelo final consegue explicar **98,86%** da variação nos preços dos veículos e apresentou um erro médio (RMSE) 56% menor que o modelo linear.

A análise de *Feature Importance* (Importância das Features) revelou que os fatores mais decisivos para o modelo são:
1.  **Idade (`Age`)**
2.  **Tamanho do Motor (`Engine_Size`)**
3.  **Quilometragem (`Mileage`)**

### 4. Como Executar este Projeto

1.  Clone este repositório.
2.  (Opcional) Crie um ambiente virtual e instale as dependências (veja `requirements.txt`).
3.  Abra o notebook `an-lise-metodol-gica-de-pre-os-de-carros.ipynb` em um ambiente Jupyter (como Jupyter Lab ou VS Code).
4.  O dataset `car_price_dataset.csv` e o PDF da metodologia `Metodologia_Quantitativa.pdf` já estão incluídos.

---
*Este projeto foi desenvolvido como um estudo de caso para portfólio de Ciência de Dados, focado na aplicação de uma análise metodológica e na construção de um modelo preditivo de alta performance.*
