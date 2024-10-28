Описние задачи: 

Интернет-магазин собирает историю покупателей, проводит рассылки предложений и планирует будущие продажи. Для оптимизации процессов надо выделить пользователей, которые готовы совершить покупку в ближайшее время.

Цель - предсказать вероятность покупки в течение 90 дней

Задачи:

1. Изучить данные
2. Создать дополнительные признаки
3. Создать модель классификации пользователей
4. Выполнить тестирование
   
Загружены данные об истории покупателей, истории рекламных рассылок и целевого признака. Выполнена предобработка данных: установлены соответствующие типы данных, удалены дубликаты, значение категорий разбито на 5 отдельных столбцов. В результате анализа датасетов были добавлены следующие признаки:

- месяц и год заказа;
- прологарифмировали столбец с ценой
- сумма за покупку в категории
  
Были построены две модели классификации: CatBoost и XGBoost. Обе модели были настроены на максимизацию метрики ROC AUC, что позволяет оценить качество предсказаний в контексте бинарной классификации.

Для финального прогноза на тестовых данных была выбрана модель CatBoostClassifier, так как она продемонстрировала наилучший баланс между качеством предсказаний и временем обучения. 

Метрика ROC-AUC при тестировании - 0.68.
