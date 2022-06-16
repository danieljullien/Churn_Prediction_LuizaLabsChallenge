# Churn_Prediction_LuizaLabsChallenge

O desafio de prever se um cliente irá sair da Base de Clientes Ativos (também conhecido como churn) não é um problema exclusivo do varejo, sendo uma área de estudos constante da maioria das indústrias e empresas de serviços que dependem da retenção.

Este projeto é um exemplo do tipo de problema que um cientista de Dados do Luizalabs (MagazineLuiza) entra de cabeça e cujas soluções servem para alavancar várias frentes de trabalho. A solução em si já traz muito valor, se tiver alto índice de acertos pode ser usada para elencar automaticamente clientes com alto risco de churn para uma promoção agressiva com o objetivo retê-lo na base.

Também há muito valor nos insights e na validação de hipóteses que acontece durante o processo de análise do problema e das soluções. 

### Objetivo
Nesse desafio, construído em uma parceria da Tera e o Luizalabs, o objetivo principal será construir algumas soluções baseadas em machine learning para prever se um dado cliente do e-commerce do Magalu continuará comprando na plataforma em 2020 usando algumas características próprias do cliente e seu histórico de compras no ano anterior. No final, algumas dessas soluções devem ser combinadas em um ensemble para criar uma solução única com o objetivo de alavancar ainda mais os resultados.

Para que o objetivo principal seja cumprido, será necessário construir uma forma de visualização das soluções criadas e a comparação com o modelo baseline e com o modelo de ensemble criados no processo.

Também é uma boa prática avaliar os modelos treinados, seja através da exploração de seus parâmetros (por exemplo, os pesos de um modelo linear) ou usando técnicas avançadas como o SHAP.

O desafio também possui um dataset de pontuação, contendo dados de clientes que não estão nem nas bases de treino nem nas de teste. Para esses clientes não foram disponibilizadas as respostas (targets), sendo portanto impossível verificar durante o desenvolvimento da solução se o modelo está acertando ou não.

### Modelos 
Para a modelagem, buscaremos um modelo que tenha o melhor F1 Score. Iremos treinar os seguintes modelos:
- Decision Tree (Baseline)
- Logistic Regression
- Random Forest
- SVM
- KNN
- GaussianNB
- Bagging
- AdaBoost
- GradientBoosting
- LGBM
- XGBoost

Para cada modelo será realizado uma busca (RandomizedSearch ou GridSearch) com cross-validate de 5, buscando otimizar os hiperparâmetros para o F1 Score.

Os modelos serão então comparados e, com os que apresentarem melhor performance e potencial de Ensemble, um Voting e Stacking também serão desenvolvidos.
