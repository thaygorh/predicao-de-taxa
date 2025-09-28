# MVP: Machine Learning & Analytics - Predição de Fluxo de Massa a partir da Corrente de um Motor  

**Autor:** Thaygor Henrique Gonçalves  
**Data:** 28/09/2025  

---

## Objetivo
Este trabalho foi desenvolvido como **MVP da disciplina Machine Learning & Analytics**, com o objetivo de avaliar a viabilidade de prever o fluxo de massa (t/h) a partir da corrente elétrica de um motor (A), utilizando os dados de uma balança como referência.  

---

## Metodologia
- Problema tratado como **regressão supervisionada**.  
- Divisão dos dados em **90% treino/validação** e **10% holdout**.  
- Modelos avaliados: DummyRegressor (baseline), Ridge, RandomForest, GradientBoosting, LightGBM e CatBoost.  
- Otimização via **GridSearchCV** com validação cruzada temporal (TimeSeriesSplit).  
- Métricas utilizadas: **MAE, RMSE e R²**.  
- Melhor resultado obtido com **CatBoost**.  
- A partir das predições do melhor modelo, foi criada uma **função saturante híbrida**, representando de forma matemática e interpretável a relação entre corrente e fluxo de massa.  

---

##  Arquivos do Repositório
- **`predicao_fluxo_motor_vfinal.ipynb`** → Notebook com todo o código e explicações do MVP.  
- **`MVP_MLA_dados_tratados2.csv`** → Dataset com a corrente do motor (A) e a taxa da balança (t/h).  
- **`best_model.pkl`** → Artefato salvo do treinamento com validação cruzada, usado para evitar retreinamento a cada execução.  
- **`Funcao_Saturante_Hibrida_MVP.xlsx`** → Validação prática da função híbrida no Excel, aplicada sobre os dados reais de corrente e comparada (A) com a taxa da balança (ton/h).

