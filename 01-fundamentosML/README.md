# 📊 Projeto de Regressão/Classificação com Machine Learning

## Visão Geral

Este projeto aplica técnicas de regressão a um conjunto de dados real obtido no repositório UCI Machine Learning Repository.  
O objetivo é explorar etapas de pré-processamento, análise de atributos, treinamento de modelos e avaliação de desempenho utilizando métodos clássicos de Machine Learning.

O projeto foi desenvolvido em Python como parte de um estudo aplicado em Aprendizado de Máquina, com foco tanto nos fundamentos matemáticos quanto na implementação prática.

---

## Descrição do Problema

O objetivo é modelar a relação entre múltiplos atributos de entrada e uma variável alvo, utilizando:

- **Regressão Linear Múltipla** (para tarefas de regressão), ou  
- **Regressão Logística** (para tarefas de classificação).

O estudo investiga como escolhas de pré-processamento, seleção de atributos e configurações de treinamento impactam o desempenho final do modelo.

---

## Dataset

- Fonte: UCI Machine Learning Repository  
- Mínimo de 200 instâncias  
- Pelo menos 5 atributos  
- Tarefa: Regressão ou Classificação Multiclasse  

O conjunto de dados foi explorado por meio de análises estatísticas e visualizações, buscando compreender melhor a distribuição das variáveis e suas relações.

---

## Metodologia

O projeto segue as seguintes etapas:

### 1️⃣ Exploração dos Dados
- Resumo estatístico dos atributos
- Visualização das distribuições
- Análise das relações entre variáveis

### 2️⃣ Pré-processamento
- Tratamento de valores ausentes (quando aplicável)
- Escalonamento / normalização de atributos (quando necessário)
- Seleção de atributos relevantes

### 3️⃣ Desenvolvimento do Modelo
- Divisão em conjuntos de treino e teste
- Treinamento do modelo utilizando:
  - `scikit-learn`
- Configuração e experimentação de parâmetros

### 4️⃣ Avaliação

Dependendo da tarefa:

**Para Regressão:**
- Erro Quadrático Médio (MSE)
- Coeficiente de Determinação (R²)

**Para Classificação:**
- Acurácia
- Matriz de Confusão
- Precisão / Revocação (quando aplicável)

Foram realizados múltiplos experimentos para analisar como diferentes estratégias de pré-processamento e divisões dos dados influenciam o desempenho do modelo.

---

## Resultados

Os experimentos demonstram como normalização, seleção de atributos e configurações do modelo influenciam o desempenho preditivo.

Os resultados numéricos detalhados e análises comparativas estão apresentados no relatório técnico anexado ao repositório.