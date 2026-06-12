[![Português](https://img.shields.io/badge/lang-PT--BR-green)](README.br.md)
[![English](https://img.shields.io/badge/lang-EN-white)](README.md)

# Classificação Titanic

Pipeline de Ciência de Dados aplicado à análise exploratória e classificação da sobrevivência de passageiros do Titanic. O projeto foi desenvolvido com o objetivo de aplicar técnicas de pré-processamento de dados, análise exploratória e aprendizado supervisionado utilizando Árvores de Decisão para prever a sobrevivência de passageiros com base em características socioeconômicas e demográficas.

Os dados utilizados são derivados do clássico conjunto de dados do Titanic, amplamente utilizado em problemas de Machine Learning para classificação binária.

### Estrutura do projeto

```text
Analise-Classificacao-Titanic/
├── analise_e_classificacao_titanic.ipynb
├── train.csv
├── validation.csv
└── result.csv
```

# Etapas

**Etapa 1 - Análise Exploratória dos Dados:**

Análise inicial do conjunto de dados para compreensão das características dos passageiros e identificação de padrões relevantes para a classificação.

O que foi realizado:

* Verificação de valores ausentes;
* Distribuição das idades dos passageiros;
* Análise da sobrevivência por classe social;
* Exploração das variáveis disponíveis;
* Identificação de possíveis relações entre atributos e sobrevivência.

**Etapa 2 - Pré-processamento dos Dados:**

Preparação dos dados para treinamento do modelo de Machine Learning.

O que foi realizado:

* Seleção dos atributos mais relevantes;
* Remoção de variáveis com baixo potencial preditivo;
* Conversão de atributos categóricos para valores numéricos utilizando Label Encoding;
* Tratamento de valores ausentes;
* Padronização da estrutura dos dados de treino e validação.

Atributos utilizados:

* Classe do passageiro (`Pclass`);
* Sexo (`Sex`);
* Idade (`Age`);
* Número de irmãos/cônjuges (`SibSp`);
* Número de pais/filhos (`Parch`);
* Tarifa paga (`Fare`);
* Porto de embarque (`Embarked`).

**Etapa 3 - Treinamento do Modelo:**

Construção de um modelo supervisionado para classificação da sobrevivência dos passageiros.

O que foi realizado:

* Separação dos dados em treino e teste;
* Treinamento utilizando Decision Tree Classifier;
* Ajuste dos parâmetros do modelo;
* Avaliação do desempenho em dados não utilizados no treinamento.

**Etapa 4 - Avaliação e Predição:**

Avaliação da capacidade preditiva do modelo e classificação de registros desconhecidos.

O que foi realizado:

* Cálculo da acurácia de treinamento;
* Cálculo da acurácia de teste;
* Geração das previsões para o conjunto de validação;
* Exportação dos resultados para arquivo CSV.

**Etapa 5 - Interpretação do Modelo:**

Visualização da estrutura de decisão construída pelo algoritmo.

O que foi realizado:

* Geração gráfica da árvore de decisão;
* Exportação das regras aprendidas pelo modelo;
* Interpretação dos critérios utilizados para prever sobrevivência.

# Exemplos

* Distribuição de Idades:

```python
sns.histplot(dadosTreino["Age"], bins=20, kde=True)
```

* Sobrevivência por Classe:

```python
sns.countplot(x="Pclass", hue="Survived", data=dadosTreino)
```

* Árvore de Decisão Gerada:

```python
plot_tree(modelo, feature_names=features, filled=True)
```

# Ferramentas Utilizadas

* `pandas`: manipulação e tratamento dos dados;
* `matplotlib`: visualização gráfica;
* `seaborn`: análise exploratória e gráficos estatísticos;
* `scikit-learn`: treinamento e avaliação do modelo de classificação;
* `Jupyter Notebook`: desenvolvimento e documentação do fluxo analítico.

# Conceitos de Ciência de Dados Aplicados

* Análise Exploratória de Dados (EDA);
* Tratamento de Dados Ausentes;
* Engenharia de Atributos;
* Codificação de Variáveis Categóricas;
* Aprendizado Supervisionado;
* Classificação Binária;
* Árvores de Decisão;
* Avaliação de Modelos por Acurácia.
