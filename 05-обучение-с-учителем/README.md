# Обучение с учителем
## Описание проекта: Прогнозирование оттока клиента Банка

Из «Бета-Банка» стали уходить клиенты. Каждый месяц. Немного, но заметно. Банковские маркетологи посчитали: сохранять текущих клиентов дешевле, чем привлекать новых. Нужно спрогнозировать, уйдёт клиент из банка в ближайшее время или нет. Вам предоставлены исторические данные о поведении клиентов и расторжении договоров с банком. Постройте модель с предельно большим значением F1-меры. Чтобы сдать проект успешно, нужно довести метрику до 0.59. Проверьте F1-меру на тестовой выборке самостоятельно. Дополнительно измеряйте AUC-ROC, сравнивайте её значение с F1-мерой.
## Вывод:
Задача достичь f1 меры 0.59 достигунта, актуальный показатель на лучшей модели 0.6127023661270236. Модель Случайного леса с парметрами n_estimators = 13, max_depth=21. Для преодоления порога было сделано:
- Подготовка данных (удалены пропущенные значения, генеральная выборка разделена на валидационную, обучающую и тестовую, после чего данные были обработаны тезникой OHE и масштабированы).
- Обучены и исследованы показатели трех моделей на не сбалансированных выборках.
- Устранен дизбаланс классов, лучшим образом покащал себя метод class_weight.
- Методом иттерации подобраны оптимальные параметры для модели случайного леса.

Модель сбалансированна по охвату клиентов и качеству предсказаний, показала высокое качество и адекватность, достаточно высокая совокупная мера производительности модели(AUC-ROC), проверка на тестовой выборке показала что модель не переобучилась.

## Решение
[Открыть Notebook](./Bank-Customers-git.ipynb)
