# 📊 Previsão de Evasão de Clientes - Telecom X

## 📌 Objetivo
Este projeto tem como objetivo prever quais clientes têm maior probabilidade de cancelar os serviços da **Telecom X**, possibilitando ações proativas de retenção.  
Foi desenvolvido como parte de um desafio do curso de Ciência de Dados da Alura, com foco em **Machine Learning aplicado a churn prediction**.

---

## 📂 Etapas do Projeto

### 1️⃣ Preparação e Limpeza dos Dados
- Leitura e estruturação dos dados a partir de arquivo JSON.
- Tratamento de valores ausentes.
- Conversão de variáveis categóricas para numéricas usando **OneHotEncoder**.
- Separação de variáveis preditoras (features) e variável alvo (**Churn**).

### 2️⃣ Análise Exploratória
- **Matriz de correlação** para identificar variáveis mais associadas ao churn.
- Visualizações direcionadas:
  - Tempo de contrato × Evasão
  - Total gasto × Evasão
- Gráficos de dispersão, boxplots e contagens para padrões relevantes.
- Utilização do **Plotly** para visualizações interativas, facilitando a exploração de padrões e insights.

### 3️⃣ Modelagem Preditiva
Foram criados e avaliados diferentes modelos de classificação:

| Modelo | Normalização | Motivo da Escolha |
|--------|--------------|-------------------|
| **KNN** | Sim | Modelo baseado em distância, sensível à escala. |
| **Regressão Logística** | Sim | Bom para interpretar coeficientes e probabilidades. |
| **Decision Tree** | Não | Fácil interpretação, não sensível à escala. |
| **Random Forest** | Não | Modelo robusto e de alta performance para dados tabulares. |

### 4️⃣ Avaliação dos Modelos
Métricas utilizadas:
- **Acurácia**
- **Precisão**
- **Recall**
- **F1-score**
- **Matriz de confusão**

O **Random Forest** apresentou o melhor equilíbrio entre desempenho e robustez, enquanto a **Regressão Logística** foi útil para interpretação dos fatores.

### 5️⃣ Importância das Variáveis
- **Random Forest** destacou:  
  - Tipo de contrato (clientes mês a mês têm maior risco de churn)  
  - Total gasto  
  - Presença de serviços adicionais (como suporte técnico e segurança online)  
- **Regressão Logística** reforçou que contratos mais longos reduzem a evasão.

---

## 📈 Principais Insights
- **Contratos mensais** e **pagamento via cheque eletrônico** estão fortemente associados à evasão.
- **Baixo tempo de permanência** é um dos maiores indicadores de risco.
- Serviços como **suporte técnico** e **segurança online** estão ligados a maior fidelização.
- Clientes com **gasto total baixo** tendem a cancelar mais.

---

## 🛠 Tecnologias Utilizadas
- **Python**
- **Pandas**, **NumPy**
- **Matplotlib**, **Seaborn**, **Plotly**
- **Scikit-learn**

---

## 🚀 Estratégias de Retenção Sugeridas
1. **Oferecer incentivos** para clientes em contratos mensais migrarem para planos anuais ou bianuais.  
2. **Criar pacotes de valor** com serviços adicionais (segurança online, suporte técnico) para aumentar retenção.  
3. **Ações personalizadas** para clientes com baixo tempo de permanência, incluindo descontos e onboarding reforçado.  
4. **Campanhas de reativação** para clientes inativos ou com uso reduzido.  

---

💡 *Este projeto reforça como análises preditivas podem ser usadas para aumentar a retenção e reduzir perdas financeiras na base de clientes.*
