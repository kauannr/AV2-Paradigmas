# AV2-Paradigmas - Análise Supervisionada e Clustering

## 📚 Descrição
Este projeto foi desenvolvido como parte da avaliação da disciplina de Inteligência Artificial, com o objetivo de aplicar técnicas de aprendizado supervisionado e não supervisionado sobre dados radiômicos.

Dividi a resolução em duas partes principais: **Análise Supervisionada (Questão 01)** e **Análise de Clustering (Questão 02)**.

---

## 🚀 Metodologia

### Questão 01 — Análise Supervisionada
- Realizei o pré-processamento dos dados com padronização (`StandardScaler`) e redução de dimensionalidade via PCA, mantendo os 15 principais componentes.
- Treinei dois modelos de classificação:
  - Decision Tree
  - MLP (Perceptron Multicamadas)
- Avaliei os modelos usando validação cruzada (StratifiedKFold com 10 folds), cálculo do F1-Score e curvas ROC.

### Questão 02 — Análise de Clustering
- Utilizei o método do cotovelo para definir **K=3** como número ideal de clusters.
- Apliquei os seguintes algoritmos:
  - K-Means
  - Clustering Hierárquico com ligações Ward e Complete
- Avaliei os agrupamentos com Silhouette Score e Davies-Bouldin Index.

---

## 🏆 Principais Resultados

### Análise Supervisionada
- O modelo **MLP** apresentou o melhor desempenho com F1-Score médio de **0.6181** e AUC de **0.86**, mostrando boa capacidade de generalização.
- A **Decision Tree** atingiu AUC de **1.00**, mas com evidência de overfitting.

### Análise de Clustering
- O **K-Means** gerou clusters mais equilibrados e interpretáveis (Silhouette: **0.3341**, DBI: **1.2152**).
- O linkage **Complete** teve melhores métricas numéricas (Silhouette: **0.8077**, DBI: **0.6630**), mas os clusters ficaram altamente desbalanceados.

---

## 📋 Conclusões

Na análise supervisionada, considerei o **MLP** como o modelo mais robusto e confiável para o problema.

Na análise não supervisionada, embora o linkage Complete tenha mostrado melhores métricas, escolhi o **K-Means** como mais adequado por apresentar uma distribuição de amostras mais realista entre os clusters.

---

## 📦 Entregável

Entreguei um notebook `radiomics_prova2.ipynb` completo e bem estruturado com:
- Todas as etapas do processamento, modelagem e avaliação,
- Códigos comentados e organizados em seções com Markdown,
- Um sumário no topo para facilitar a navegação.

---

## ✍️ Observação

Utilizei `random_state=42` em todos os experimentos para garantir reprodutibilidade dos resultados obtidos.

As respostas das questões e conclusões abrange tudo o que foi perguntado na questão, por isso não especifiquei A, {resposta} B, {resposta} ...
