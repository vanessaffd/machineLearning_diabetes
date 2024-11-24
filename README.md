# Predição da Ocorrência de Diabetes com Machine Learning

## Objetivo
O presente projeto teve como objetivo treinar cinco modelos preditivos de *machine learning*, de forma supervisionada, para prever a ocorrência de diabetes entre o público analisado. Avaliou-se a capacidade dos modelos em predizer a incidência da doença com base em fatores de risco conhecidos.

## Base de Dados
- **Fonte**: Dataset hospedado na plataforma Kaggle.  
- **Tamanho Original**: 100.000 registros com 9 atributos, incluindo o status de incidência de diabetes.  
- **Ferramentas Utilizadas**:  
  - **Linguagem**: Python.  
  - **Ambiente**: Jupyter Notebook.  
  - **Bibliotecas**: Pandas, scikit-learn, entre outras.

## Etapas do Projeto

### 1. **Pré-processamento dos Dados**
1. **Remoção de Dados Incompletos**: Foram removidos 35.816 registros que não apresentavam informações sobre o histórico de tabagismo.  
2. **Transformação de Variáveis Categóricas**:  
   - Utilizou-se o método `get_dummies` da biblioteca Pandas para transformar as variáveis categóricas em variáveis numéricas binárias.  
   - Colunas transformadas: `gender` e `smoking_history`.  
3. **Normalização dos Dados**:  
   - Aplicou-se o método `MinMaxScaler` (scikit-learn) para normalizar as colunas:  
     - `bmi`  
     - `HbA1c_level`  
     - `blood_glucose_level`.

### 2. **Divisão dos Dados**
- O dataset foi dividido em:  
  - Variáveis independentes (*features*): `X`.  
  - Variável dependente (*target*): `y`.  
- Criaram-se amostras de treino e teste:  
  - `X_treino`, `X_teste`, `y_treino`, `y_teste`.  

### 3. **Modelagem**
Foram avaliados cinco modelos preditivos:  
- **Regressão Logística**  
- **Árvore de Decisão**  
- **SVC (Support Vector Classifier)**  
- **Random Forest**  
- **K-Nearest Neighbors (KNN)**  

### 4. **Métrica de Avaliação**
- Utilizou-se o **F1-Score** para medir o desempenho dos modelos.  
  - Essa métrica é especialmente útil em cenários com desbalanceamento de classes, como a baixa incidência de doenças.

## Resultados
Os valores de F1-Score obtidos foram:  
1. **Random Forest**: 0,800  
2. **Árvore de Decisão**: 0,738  
3. Demais modelos apresentaram desempenhos inferiores.

### Observação
O **Random Forest** destacou-se como o modelo mais eficaz para predizer a ocorrência de diabetes com base nos fatores de risco.

## Conclusões
- O modelo **Random Forest** demonstrou boa capacidade preditiva ao utilizar fatores como obesidade, histórico de tabagismo e hipertensão.  
- Possíveis aplicações práticas:  
  - Apoio à tomada de decisão em saúde pública.  
  - Triagem médica.  
  - Medicina preventiva.  
  - Pesquisas epidemiológicas.  
