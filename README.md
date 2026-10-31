# 📊 Data Analysis: Modelagem de Preço de Veículos

Projeto desenvolvido no curso **Data Analysis with Python (IBM / Coursera)**. A partir de uma base
com ~200 veículos e 29 atributos (motor, dimensões, consumo, potência), o objetivo é **prever o
preço** e comparar modelos de regressão, avaliando overfitting e escolhendo hiperparâmetros.

> 🇺🇸 Car price prediction project from the IBM *Data Analysis with Python* course: data cleaning,
> linear, multiple, polynomial and Ridge regression, evaluated with R² and tuned with Grid Search.

## Etapas

| Notebook | Conteúdo |
|---|---|
| [`01_analise_exploratoria_carros.ipynb`](01_analise_exploratoria_carros.ipynb) | Carga da base original, divisão treino/teste e comparação de modelos |
| [`02_tratamento_dados_carros.ipynb`](02_tratamento_dados_carros.ipynb) | Mesmo fluxo sobre a base tratada (`carros_cleaned.csv`), com métricas formatadas |

**Modelos avaliados**
1. Regressão linear simples (`horsepower` → `price`)
2. Regressão linear múltipla (`horsepower`, `curb-weight`, `engine-size`, `highway-mpg`)
3. Regressão polinomial de grau 5, para evidenciar overfitting (R² treino × teste)
4. Ridge Regression com features polinomiais de grau 2
5. **Grid Search** com validação cruzada (4 folds) para escolher o `alpha` do Ridge

## Dados

`carros_cleaned.csv`: base *Automobile* (UCI) já tratada, com valores faltantes imputados,
variáveis categóricas convertidas em dummies (`fuel-type`, `aspiration`) e potência discretizada
em faixas (`horsepower-binned`).

## Como rodar

```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
jupyter notebook
```

## Stack

Python · Pandas · NumPy · scikit-learn · Matplotlib · Seaborn · Jupyter

---
Desenvolvido por [Társio Chiconi](https://github.com/chiconitarsio) para fins de estudo (Coursera / IBM).
