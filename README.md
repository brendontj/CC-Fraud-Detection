# Credit Card Fraud Detection
## -  Exploração dos dados 

- O dataset contém transações feitas por cartões de crédito por titulares de cartões de crédito europeus.
- O conjunto de dados apresenta em suma dados numéricos obtidos após transformação PCA (Principal Component Analysis). Não foi possível obter os dados previamente a esta transformação.
  - Quantidade de registros do dataset: 284807
  - Quantidade de features: 28 features númericas (V1...V28) obtidas após o PCA, além de `amount` representando o valor da transação e `time` que contém os segundos decorridos entre cada transação e a primeira transação do conjunto de dados. 
- Dos registros obtidos 0,172% (492) são registros de fraude, o restante são transações onde não foi detectada fraude.
- Das colunas iniciais do conjunto de dados apenas a váriavel `time` foi removida inicialmente, por considerar que a mesma não deveria dizer muito a respeito de prever se uma transação é fraudulenta ou não. Dos demais atributos foi utilizado uma seleção das `K` "melhores variáveis", onde essas variáveis seriam as mais significativas considerando o conjunto de dados utilizado como sample de treino. É possível ver no notebook deste repositório a análise que identifica as 20 váriaveis mais significativas para utilizar no modelo.'
## - Objetivo
- O objetivo com este conjunto de dados é treinar um modelo de machine learning capaz de predizer se uma transação de cartão de crédito é fraudulenta ou não.

- O dataset apresenta o seguinte label, se `class` é 0 o registro é de uma transação onde não houve fraude. Por outro lado, se `class` é 1 a transação representa uma fraude.

 
## - Extração de características 

- Além da transformação PCA (Principal Component Analysis) durante a fase de criação do Dataset que não foi realizada neste trabalho usamos o `mutual_info_classif` com o `SelectKBest` ambos do scikit-learn para selecionar as features mais representativas para o modelo.
