# 📊 Análise de Tendências Hidrológicas no Pantanal

### Modelagem Estatística e Deep Learning para Previsão de Séries Temporais

Projeto de Ciência de Dados aplicado à análise e previsão de séries hidrológicas da região do Pantanal, utilizando modelos estatísticos (SARIMA) e redes neurais recorrentes (LSTM).

---

## 🎯 Objetivo

Analisar o comportamento histórico de séries hidrológicas do Pantanal e avaliar a capacidade preditiva de diferentes abordagens de modelagem temporal, comparando:

* 📌 Baseline (Modelo Ingênuo)
* 📌 SARIMA (Modelagem Estatística)
* 📌 Walk-Forward Validation (Validação Rolling)
* 📌 LSTM (Deep Learning)

O foco é verificar se modelos mais sofisticados agregam valor real em relação a um benchmark simples.

---

## 🌎 Contexto

O Pantanal é uma das maiores planícies alagáveis do mundo e possui dinâmica hidrológica altamente sazonal. Entender padrões de vazão é essencial para:

* Gestão ambiental
* Planejamento hídrico
* Monitoramento climático
* Estudos de tendência de longo prazo

---

## 📂 Fonte de Dados

Os dados foram obtidos via biblioteca:

* `hydrobr`

Contendo séries históricas de vazão de estações fluviométricas localizadas na região do Pantanal.

---

## 🔬 Metodologia

### 1️⃣ Análise Exploratória

* Visualização da série temporal
* Decomposição STL
* Identificação de sazonalidade
* Avaliação de tendência

---

### 2️⃣ Testes Estatísticos

* Teste de estacionariedade (ADF)
* Diagnóstico de resíduos
* Teste Ljung-Box para autocorrelação

---

### 3️⃣ Modelagem SARIMA

* Busca de hiperparâmetros via AIC
* Ajuste do modelo final
* Previsão fora da amostra
* Intervalos de confiança

---

### 4️⃣ Validação Walk-Forward (Rolling Forecast)

Simulação realista de previsão:

1. Treina modelo
2. Prevê 1 passo
3. Incorpora valor real
4. Reestima modelo
5. Repete processo

Essa abordagem reduz viés otimista e testa robustez do modelo.

---

### 5️⃣ Modelo Baseline

Modelo ingênuo baseado em persistência:

> A previsão do próximo período é igual ao último valor observado.

Serve como benchmark mínimo.

---

### 6️⃣ LSTM (Long Short-Term Memory)

Rede neural recorrente aplicada à série temporal:

* Janela deslizante de 12 períodos
* 50 neurônios
* Otimizador Adam
* Função de perda MSE

Objetivo: comparar desempenho com modelo clássico.

---

## 📊 Avaliação de Desempenho

Métrica utilizada:

* **RMSE (Root Mean Squared Error)**

Comparação entre:

* Baseline
* SARIMA Estático
* SARIMA Rolling
* LSTM

Interpretação:

* Se SARIMA < Baseline → modelo agrega valor real
* Se Rolling < Estático → reestimação melhora adaptação
* Se Baseline ≈ SARIMA → série possui alta persistência

---

## 🧠 Principais Insights

* Séries hidrológicas apresentam forte componente sazonal.
* Modelos ingênuos podem ser altamente competitivos.
* A validação rolling é essencial para avaliar robustez fora da amostra.
* Instabilidade de convergência pode ocorrer em reestimações sucessivas.
* Modelos mais complexos nem sempre superam benchmarks simples.

---

## 🛠️ Tecnologias Utilizadas

* Python
* Pandas
* NumPy
* Statsmodels
* Scikit-learn
* TensorFlow / Keras
* Matplotlib
* Seaborn
* HydroBR

---

## 📈 Estrutura do Notebook

1. Coleta e preparação dos dados
2. Análise exploratória
3. Testes estatísticos
4. Modelagem SARIMA
5. Validação rolling
6. Baseline
7. LSTM
8. Comparação final
9. Conclusões

---

## 🎓 Conclusão

O projeto demonstra aplicação prática de modelagem de séries temporais em contexto ambiental real, com comparação crítica entre abordagens clássicas e redes neurais.

A validação fora da amostra foi fundamental para avaliar a capacidade de generalização dos modelos.

---

## 👩‍💻 Autora

Mirian Ajiki Molicawa
Projeto de Ciência de Dados – Análise Hidrológica do Pantanal

