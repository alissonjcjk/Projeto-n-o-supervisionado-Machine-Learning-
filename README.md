# 🧭 Titanic Clustering Analysis - Unsupervised Learning

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Status](https://img.shields.io/badge/Status-Completed-success)
![License](https://img.shields.io/badge/License-MIT-green)

## 📋 Sobre o Projeto

Este projeto aplica técnicas de **Aprendizado de Máquina Não Supervisionado** para identificar padrões e agrupar passageiros do Titanic em clusters, sem o uso prévio de rótulos de sobrevivência.

O objetivo principal é explorar como algoritmos de clusterização conseguem segmentar os dados e se esses grupos formados espontaneamente possuem correlação com as características socioeconômicas e de sobrevivência dos passageiros.

## 🎯 Objetivos

O trabalho foi estruturado para cumprir as seguintes etapas técnicas:

1.  **EDA (Análise Exploratória de Dados):** Compreensão da distribuição dos dados.
2.  **Pré-processamento:** Tratamento de dados para adequação aos algoritmos de distância.
3.  **Seleção do K Ideal:** Utilização de múltiplos métodos robustos (Elbow, Silhouette, etc.) para definir o número ótimo de clusters.
4.  **Modelagem Híbrida:**
    * **K-Means:** Para dados numéricos.
    * **K-Prototypes:** Para lidar corretamente com dados mistos (numéricos e categóricos).
5.  **Análise de Clusters:** Interpretação das características (centroides) de cada grupo formado.

## 🛠️ Tecnologias Utilizadas

* **Linguagem:** Python
* **Manipulação de Dados:** Pandas, NumPy
* **Visualização:** Matplotlib, Seaborn
* **Machine Learning:**
    * Scikit-learn (K-Means, Métricas)
    * `kmodes` (Biblioteca específica para o algoritmo K-Prototypes)

## 📊 Metodologia

### 1. Definição do Número de Clusters (K)
Para evitar a escolha arbitrária de *K*, foram comparados cinco métodos estatísticos diferentes para validar a melhor decisão:
* **Método do Cotovelo (Elbow Method)**
* **Índice Calinski-Harabasz**
* **Índice Davies-Bouldin**
* **Silhouette Score**
* **BIC (Bayesian Information Criterion)**

### 2. Algoritmos Aplicados
* **K-Means:** Aplicado inicialmente nas variáveis numéricas padronizadas.
* **K-Prototypes:** Escolhido como a abordagem principal por permitir a clusterização simultânea de variáveis numéricas (Idade, Tarifa) e categóricas (Sexo, Classe, Embarque), mantendo a riqueza da informação original sem a distorção excessiva causada por *One-Hot Encoding* em algoritmos baseados em distância euclidiana.

### 3. Análise dos Resultados
Após a formação dos clusters, foi realizada uma análise cruzada (crosstab) para entender o perfil de cada grupo (ex: "Grupo de mulheres da 1ª classe", "Grupo de tripulação/homens da 3ª classe") e verificar a taxa de sobrevivência intrínseca de cada cluster.

## 🚀 Como Executar

1.  Clone o repositório:
    ```bash
    git clone [https://github.com/SEU_USUARIO/NOME_DO_REPO.git](https://github.com/SEU_USUARIO/NOME_DO_REPO.git)
    ```
2.  Instale as dependências (incluindo a lib `kmodes`):
    ```bash
    pip install pandas numpy matplotlib seaborn scikit-learn kmodes
    ```
3.  Execute o Notebook:
    ```bash
    jupyter notebook Projeto_Não_Supervisionado.ipynb
    ```

## ✒️ Autor
**Alisson Silva**
