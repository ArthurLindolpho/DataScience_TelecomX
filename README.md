Previsão de Churn em Empresa de Telecomunicações
📌 Sobre o Projeto
Este projeto tem como objetivo analisar e prever a taxa de evasão de clientes (Churn) numa empresa de telecomunicações. Através da análise de dados demográficos, serviços subscritos e detalhes de faturação, procuramos identificar os principais fatores que levam um cliente a cancelar a sua assinatura e construir modelos preditivos de Machine Learning para mitigar este problema.

🛠️ Técnicas e Tecnologias Utilizadas
O projeto foi desenvolvido em Python (Jupyter Notebook) e tira partido das seguintes bibliotecas e técnicas de Análise de Dados e Machine Learning:

Manipulação e Tratamento de Dados: pandas, numpy.

Visualização de Dados: matplotlib, seaborn.

Pré-processamento de Dados:

Transformação Binária: Substituição de variáveis categóricas de resposta direta (como "Yes"/"No" ou "Male"/"Female") por valores numéricos (1 e 0).

One-Hot Encoding: Utilizado através do make_column_transformer para transformar variáveis com múltiplas categorias (Ex: InternetService, Contract, PaymentMethod) em colunas numéricas distintas.

Normalização: Utilização do MinMaxScaler para colocar as variáveis contínuas (como os custos mensais e totais) na mesma escala de grandeza.

Modelagem Preditiva: Foram importados algoritmos de classificação robustos da biblioteca scikit-learn para prever o Churn:

Random Forest Classifier

Support Vector Machines (SVC)

K-Nearest Neighbors (KNN)

Decision Tree Classifier

Logistic Regression

Métricas de Avaliação: O projeto está estruturado para utilizar Acurácia, Recall, F1-Score, Precisão e Matriz de Confusão.

⚙️ Processamento e Preparação dos Dados
Para garantir a qualidade e a eficácia dos modelos, os dados passaram por um rigoroso processo de engenharia de variáveis:

Limpeza inicial: Exclusão de colunas de identificação irrelevantes para a modelagem preditiva, como o customerID.

Ajuste de Tipos: A base de dados original contava com 22 colunas e mais de 7000 registos. O pré-processamento transformou esses dados em 42 colunas ajustadas para treino.

📊 Resultados e Insights Obtidos
A análise exploratória e a avaliação inicial dos dados revelaram padrões de comportamento fundamentais para o negócio de telecomunicações:

Distribuição do Churn: Identificou-se que a base de dados possui uma proporção basal de evasão de aproximadamente 26.6%, contra 73.4% de clientes retidos.

Impacto do Gasto Total: Observou-se que uma grande parte dos cancelamentos foi efetuada por clientes que apresentaram um gasto total acumulado até perto dos R$ 2000.

Fator Tempo de Contrato (Tenure): O tempo de contrato demonstrou ser uma variável de altíssima importância.

A análise confirmou que quanto maior o tempo de permanência (contrato), menor a probabilidade de o cliente cancelar a assinatura.

Constatou-se através de gráficos de boxplot que cerca de 50% dos clientes que cancelaram a assinatura tinham um tempo de contrato de apenas até 10 meses.

Recomendações Estratégicas: Verificou-se uma clara correlação entre o tempo de contrato e o gasto total. O projeto sugere que a empresa crie incentivos para planos de maior duração (anuais ou bianuais), pois reter o cliente para além dos primeiros 10 meses críticos pode diminuir consideravelmente as taxas de evasão.
