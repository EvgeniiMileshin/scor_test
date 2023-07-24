# scor_test
Организация выдает займы физическим лицам.

Информация о ранее выданных организацией займах в файле [new_training_data_31_08_2022.csv](https://dl.dropboxusercontent.com/s/6tg4aa9kt1y3dar/new_training_data_31_08_2022.csv)

Файл  [all_reject_data.csv](https://dl.dropboxusercontent.com/s/tnvo43de29nu1rb/all_reject_data.csv) содержит данные о клиентах, оставлявших заявки на займ, но в итоге не взявших его по причине отказа финансовой организации или нежеланию самого клиента.

# Необходимо

1. Выполнить анализ и охарактеризовать клиентский портфель организации
2. Построить базовую модель прогнозирования банкротства, одобряющую не менее 35% клиентов при банкротстве среди одобренных не выше 15%.
3. Подготовить рекомендации и предложения по изменению признакового пространства, использованию внешних данных и иному развитию базовой модели.

# Результат
1. Подовляющее большинсво клиентов обращается повторно за займом спустя 7 дней после получения займа. 
Вероятнее всего это разряд клиентов, которые постоянно пользуются займами и берут новый чтобы закрыть предыдуй в льготные период.
Чтобы модель лучше работала можно удалить данные клиентов которые никогда не пользовались микрозаймами


2. При загрузке данных о клиентах, оставлявших заявки на займ в модель, банкротсво предсказыватся 7% потенциальным клиентам.
При этом точность модели на тренировочных данных более 60%.


3. Исходные данные имеют большое количесво признаков и часть из них оказывает минимальнео влияние на модель.
Я бы провел более глубокое исследование признаком и сократил их количесво.
Так же насколько знаю организация может запрашивать данные в БКИ по наличию  данных  о  кредитах у клиента на момент заявки.
(0 – нет данных о  клиенте  вообще  в БКИ, 1 – есть данные, 3 – есть данные о клиенте, но  нет  данных о  кредитах
