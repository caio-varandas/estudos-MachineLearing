# 📊 Previsão de Criminalidade Violenta com Machine Learning

## Visão Geral
Este projeto aplica técnicas avançadas de classificação ao dataset **Communities and Crime** do repositório UCI Machine Learning. O objetivo principal é prever a incidência de crimes violentos (Alto Risco vs. Baixo Risco) combinando dados socioeconômicos e demográficos do censo norte-americano.

O trabalho foca na análise rigorosa de como o pré-processamento e a redução de dimensionalidade impactam o desempenho de modelos preditivos em cenários de segurança pública.

---

## Descrição do Problema
A criminalidade urbana é um fenômeno complexo associado a fatores como desigualdade social e densidade populacional. Este estudo modela essa relação utilizando:

* **Classificação Binária:** Transformação da variável alvo `ViolentCrimesPerPop` com base na mediana para identificar áreas de alto risco.
* **Análise de 8 Algoritmos:** Comparação entre métodos como Regressão Logística, SVM, KNN, Random Forest e Gradient Boosting.

---

## Dataset
* **Fonte:** [UCI Machine Learning Repository - Communities and Crime](https://archive.ics.uci.edu/ml/datasets/communities+and+crime).
* **Instâncias:** 1.994 registros.
* **Atributos:** 128 variáveis socioeconômicas e demográficas.
* **Tarefa:** Classificação Binária (Alto/Baixo Risco).

O conjunto de dados apresenta alta multicolinearidade, o que motivou um estudo profundo sobre agrupamento de variáveis e seleção de atributos.

---

## Metodologia

### 1️⃣ Exploração dos Dados
* **Agrupamento Hierárquico:** Variáveis divididas em 7 blocos temáticos (Renda, Imigração, Mercado de Trabalho, etc.) para diagnosticar a estrutura de correlação.
* **Visualização:** Mapas de calor agrupados pelo método de Ward.

### 2️⃣ Pré-processamento
* **Limpeza:** Remoção de atributos com mais de 80% de dados faltantes (22 variáveis descartadas).
* **Imputação:** Tratamento de valores ausentes remanescentes pela média de cada atributo.
* **Padronização:** Aplicação de **Z-score** para garantir que todas as características contribuam equitativamente para o modelo.
* **Redução de Dimensionalidade:** Testes comparativos utilizando **PCA** (mantendo 95% da variância explicada).

### 3️⃣ Desenvolvimento do Modelo
* **Divisão:** 80% para treinamento e 20% para teste.
* **Validação:** K-Fold Cross-Validation ($K=5$) para garantir a robustez e generalização dos resultados.
* **Ferramentas:** Uso da biblioteca `scikit-learn` para implementação de todos os modelos.

### 4️⃣ Avaliação
Foram utilizadas múltiplas métricas focadas no rigor da segurança pública:
* **Acurácia:** Proporção de acertos totais.
* **Recall (Revocação):** Métrica crítica para minimizar Falsos Negativos (áreas de risco não identificadas).
* **F1-Score:** Equilíbrio entre Precisão e Recall.
* **Matriz de Confusão:** Análise detalhada dos erros de classificação.

---

## Resultados
* **Destaque:** Os modelos treinados **sem PCA** apresentaram desempenho superior, indicando que a redução de dimensionalidade eliminou informações cruciais para as fronteiras de decisão.
* **Líderes de Performance:** **Regressão Logística** e **Gradient Boosting** atingiram **84,7% de acurácia** no conjunto de teste.
* **Aplicabilidade Prática:** O **Gradient Boosting** destacou-se com o maior **Recall (82,9%)**, sendo o modelo mais recomendado para reduzir a omissão de zonas de alto risco em políticas de segurança.

As análises comparativas completas e as justificativas matemáticas de cada modelo estão detalhadas no relatório técnico (PDF) disponível neste repositório.
