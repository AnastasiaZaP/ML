# python-flask-docker
Итоговый проект курса "Машинное обучение в бизнесе"
Стек:

ML: sklearn, pandas, numpy API: flask Данные: с kaggle - https://www.kaggle.com/datasets/chitwanmanchanda/fraudulent-transactions-data

Задача: предсказать вероятность - является ли транзакция фродовой (мошеннической). Бинарная классификация

Используемые признаки:
- step (number) - единица времени (1 шаг - 1 час)
- type (text) - типы платежа (CASH-IN, CASH-OUT, DEBIT, PAYMENT and TRANSFER)
- amount (number) - сумма транзакции
- nameOrig (text) - клиент, начавший транзакцию
- oldbalanceOrg (number) - начальный баланс перед транзакцией
- newbalanceOrig (number) - новый баланс после транзакции
- nameDest (text) - клиент, который является получателем транзакции
- oldbalanceDest (number) - получатель начального баланса перед транзакцией
- newbalanceDest (number) - новый получатель баланса после транзакции
- isFlaggedFraud (number) - флаг массовых переводов (попыткой в передачи более 200 000 за одну транзакцию)

Преобразования признаков: BaseEstimator, TransformerMixin

Модель: RandomForestClassifier


# Клонирование репозитория и создание образа:

git clone https://github.com/AnastasiaZaP/definition_of_fraudulent_transactions.git

cd definition_of_fraudulent_transactions

docker build -t a_zap/definition_of_fraudulent_transactions .

# Запуск контейнера:

λ docker run -d -p 8180:8180 -p 8181:8181 -v Projects/definition_of_fraudulent_transactions/models a_zap/definition_of_fraudulent_transactions

