# 📈 Linear Regression from Scratch — Salary Prediction

## 📌 Descrição do Projeto

Este projeto implementa **Linear Regression do zero (from scratch)** utilizando apenas **NumPy, Pandas e Matplotlib**, sem bibliotecas de machine learning como `scikit-learn`.

O objetivo é **entender profundamente** como funciona:
- Função de custo
- Gradiente
- Gradient Descent
- Atualização dos parâmetros `w` e `b`

O modelo é treinado para prever **salários com base em anos de experiência**.

---

## 🧠 Motivação

Embora na prática seja comum usar algo como:
```python
from sklearn.linear_model import LinearRegression
```

este projeto existe para:
- entender o que acontece por baixo do capô
- conectar matemática → código → aprendizado
- evitar usar ML como "caixa-preta"

---

## 📊 Dataset

- **Nome:** `Salary_Data.csv`
- **Features:**
  - `YearsExperience` → anos de experiência
- **Target:**
  - `Salary` → salário anual

Dataset simples, ideal para regressão linear básica.

---

## 🛠️ Tecnologias Utilizadas

- Python 3
- NumPy
- Pandas
- Matplotlib
- Jupyter Notebook

---

## ⚙️ Implementação

### 1️⃣ Visualização dos dados
Os dados são plotados para verificar se existe relação linear entre experiência e salário.

### 2️⃣ Função de custo (Mean Squared Error)
A função de custo utilizada é:

$$J(w,b) = \frac{1}{2m} \sum_{i=1}^{m} (wx^{(i)} + b - y^{(i)})^2$$

Implementada manualmente usando um loop.

### 3️⃣ Gradiente
O gradiente da função de custo em relação aos parâmetros é calculado como:

$$\frac{\partial J}{\partial w} = \frac{1}{m} \sum (f(x) - y)x$$

$$\frac{\partial J}{\partial b} = \frac{1}{m} \sum (f(x) - y)$$

### 4️⃣ Gradient Descent
O algoritmo de Gradient Descent é usado para atualizar os parâmetros:
```
w = w - α * ∂J/∂w
b = b - α * ∂J/∂b
```

- `α` (alpha) é a learning rate
- O processo é repetido por várias iterações
- O custo é monitorado para garantir convergência

---

## 📉 Resultados

Após o treinamento:
- O custo diminui progressivamente
- O modelo encontra uma reta que se ajusta bem aos dados
- A linha de regressão é plotada sobre os pontos reais

---

## 🧪 Experimentos

Durante o projeto, foram testados:
- Diferentes valores de learning rate (`alpha`)
- Diferentes números de iterações
- Observação de divergência quando `alpha` é muito alto
- Efeito do gradient descent ao longo do tempo

---

## 🚀 Próximos Passos

- Separar dados em treino e teste
- Implementar Multiple Linear Regression
- Comparar com `sklearn.LinearRegression`
- Normalizar os dados
- Adicionar métricas como RMSE e R²

---

## 🧠 Aprendizados

- Gradient ≠ Gradient Descent
- Learning rate controla estabilidade do aprendizado
- Regressão linear tem solução convexa
- Entender o básico facilita escalar para redes neurais

---

## 📎 Observação Final

Este projeto tem foco educacional, priorizando clareza e entendimento sobre performance ou otimização.
