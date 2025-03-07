<center><img src = https://avatars.mds.yandex.net/i?id=ca68e85a861ec6c8cef2a2292fdfd17147b6d6bb-5334658-images-thumbs&n=13 alt="drawing" style="width:400px;"></center>

# <center>Проект: Модель предсказания оценки отзыва посетителя отеля</center>

## Оглавление  
[1. Описание проекта](README.md#Описание-проекта)  
[2. Какой кейс решаем?](README.md#Какой-кейс-решаем)  
[3. Краткая информация о данных](README.md#Краткая-информация-о-данных)  
[4. Результаты](README.md#Результаты)

### Описание проекта
Одна из проблем компании [Booking.com](https://www.booking.com) — это нечестные отели, которые накручивают себе рейтинг. Одним из способов обнаружения таких отелей является построение модели, которая предсказывает рейтинг отеля. Если предсказания модели сильно отличаются от фактического результата, то, возможно, отель ведёт себя нечестно, и его стоит проверить.

:arrow_up:[к оглавлению](README.md#Оглавление)


### Какой кейс решаем?   
В рамках данного проекта необходимо создать модель предсказания оценки отзыва посетителя отеля с использованием алгоритма [RandomForestRegressor](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.RandomForestRegressor.html). Для оценки точности прогнозов, сделанных моделью, использовать метрику MAPE (mean absolute percentage error - средняя абсолютная процентная ошибка).

Проект включает в себя несколько этапов:
- удаление строковых значений;
- очистка от пропущенных значений;
- создание новых признаков;
- преобразование признаков;
- отбор признаков.

**Критерии оценивания**     
- Качество кода. Оформление проекта.
- Очистка данных.
- Исследование данных.
- Генерация признаков.
- Отбор признаков.
- Преобразование признаков.
- Качество решения: метрика MAPE меньше 13.5%.

**Что практикуем**
- Проведение базового анализа структуры данных.
- Проведение разведывательного анализа.
- Статистический анализ данных, формирование и проверка гипотез.
- Построение и оценка предсказательной модели.
- Улучшение качества модели.

:arrow_up:[к оглавлению](README.md#Оглавление)

### Краткая информация о данных
Данные представлены в соревновании Kaggle [[SF-DST] Booking reviews](https://www.kaggle.com/competitions/sf-booking):

Файлы данных:  
- *hotels_train.csv* - набор данных для обучения
- *hotels_test.csv* - набор данных для оценки качества
- *submission.csv* - файл сабмишна в нужном формате

Признаки:
- **hotel_address** - адрес отеля;
- **review_date** - дата, когда рецензент разместил соответствующий отзыв;
- **average_score** - средний балл отеля, рассчитанный на основе последнего комментария за последний год;
- **hotel_name** - название отеля;
- **reviewer_nationality** - национальность рецензента;
- **negative_review** - отрицательный отзыв, который рецензент дал отелю;
- **review_total_negative_word_counts** - общее количество слов в отрицательном отзыв;
- **positive_review** - положительный отзыв, который рецензент дал отелю;
- **review_total_positive_word_counts** - общее количество слов в положительном отзыве;
- **reviewer_score** - оценка, которую рецензент поставил отелю на основе своего опыта;
- **total_number_of_reviews_reviewer_has_given** - количество отзывов, которые рецензенты дали в прошлом;
- **total_number_of_reviews** - общее количество действительных отзывов об отеле;
- **tags** - теги, которые рецензент дал отелю;
- **days_since_review** - продолжительность между датой проверки и датой очистки;
- **additional_number_of_scoring** - есть также некоторые гости, которые просто поставили оценку сервису, а не оставили отзыв. Это число указывает, сколько там действительных оценок без проверки;
- **lat** - широта отеля;
- **lng** - долгота отеля.
  
:arrow_up:[к оглавлению](README.md#Оглавление)

### Результаты  
В ходе выполнения задания построена предсказательная модель оценки отзыва посетителя отеля. Ноутбук booking_reviews.ipynb содержит решение, полученная модель обеспечивает рассчетную среднюю абсолютную процентную ошибку (MAPE) в размере 12.36%, контрольные тестовые данные соревнования на платформе Kaggle - 12.47%, что удовлетворяет условию задачи в полном объеме.

:arrow_up:[к оглавлению](README.md#Оглавление)