# 💰 Analisador de Viabilidade de Projeto Financeiro (Machine Learning)

## 💡 Visão Geral do Projeto

Este projeto implementa um modelo de **Machine Learning (ML) de Classificação Supervisionada** para automatizar a decisão sobre a **Viabilidade (1)** ou **Não Viabilidade (0)** de projetos de investimento.

O principal objetivo é demonstrar a construção de uma pipeline completa de ML e, crucialmente, utilizar um modelo que ofereça **alta interpretabilidade** para justificar as decisões no contexto financeiro.

---

## 🚀 Tecnologias e Metodologia

| Fase | Descrição | Ferramentas Chave |
| :--- | :--- | :--- |
| **Data Prep** | Importação, limpeza e estruturação dos dados simulados. | `Pandas` |
| **Pré-processamento** | Separação em conjuntos de treino e teste (`train_test_split`). | `scikit-learn` |
| **Algoritmo** | **Regressão Logística** (Modelo focado em Interpretabilidade). | `sklearn.linear_model.LogisticRegression` |
| **Avaliação** | Geração de métricas de desempenho (`Acurácia`, `Matriz de Confusão`). | `sklearn.metrics` |

---

## 🎯 Modelo Principal: Regressão Logística

### Por que a Regressão Logística?

Para um projeto financeiro, a escolha do modelo não se resume apenas à acurácia, mas à **confiança e transparência**. A Regressão Logística é ideal porque:

1.  **Interpretabilidade Transparente:** Ela fornece **coeficientes diretos** (pesos) para cada variável, permitindo que auditores ou gestores entendam exatamente o **porquê** de uma recomendação. 
2.  **Saída em Probabilidade:** O modelo retorna a probabilidade de viabilidade, o que é essencial para a gestão de risco (ex: "85% de chance de ser viável").

---

## 📊 Estrutura e Variáveis do Dataset

O projeto utiliza um conjunto de dados simulado com 15 projetos.

| Coluna | Tipo | Descrição |
| :--- | :--- | :--- |
| `Taxa_Juros_Anual` | `Float` | Custo do capital envolvido no projeto. |
| `Prazo_Retorno_Anos` | `Int` | Duração do investimento. |
| `Risco` | `Int` | Nível de risco de 1 (baixo) a 5 (alto). |
| `Tamanho_Equipe` | `Int` | Número de colaboradores no projeto. |
| **`Viabilidade`** | **`Int` (Target)** | **1 (Viável) / 0 (Não Viável)** |

---

## ✅ Resultados e Análise Financeira

### 1. Performance do Modelo

O modelo treinado alcançou um desempenho perfeito nos dados de teste:

```python
# Acurácia e Matriz de Confusão no Conjunto de Teste
Acurácia do Modelo: 1.00

Matriz de Confusão:
[[2 0]
 [0 3]]
