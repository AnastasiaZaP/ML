Итоговый проект курса "Машинное обучение в бизнесе"
Стек:

ML: sklearn, pandas, numpy API: flask Данные: с kaggle - https://www.kaggle.com/datasets/chitwanmanchanda/fraudulent-transactions-data
Задача: предсказать, является ли транзакция фродовой (мошеннической). Бинарная классификация

Используемые признаки:
- type (text)
- step (number)
- amount (number)
- oldbalanceOrg (number)
- newbalanceOrig (number)
- oldbalanceDest (number)
- newbalanceDest (number)
- isFlaggedFraud (number)

Преобразования признаков: BaseEstimator, TransformerMixin

Модель: RandomForestClassifier


git clone https://github.com/AnastasiaZaP/definition_of_fraudulent_transactions.git
cd definition_of_fraudulent_transactions
docker build -t a_zap/definition_of_fraudulent_transactions
docker run -d -p 8180:8180 -p 8181:8181 -v C:/Настя/Geek University/Projects/definition_of_fraudulent_transactions/app/app/models a_zap/definition_of_fraudulent_transactions

