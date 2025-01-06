# Датасет
Мною был взят вот этот датасет([https://www.kaggle.com/datasets/ceebloop/rap-lyrics-for-nlp]). В нем содержатся текста рэп-песен разных исполнителей. Задача - отгадывать исполнителя по тексту трека.

# Классификация
В файле classification.ipynb содержатся все алгоритмы из заданий на примере классификаций. По ноутбуку видно, что самым неточным алгоритмом оказался KNN, а самым точным - градиентный бустинг.

| Метрики            | KNN   | Линейная регрессия | Решающее дерево | Случайный лес | Градиентный бустинг |
|--------------------|-------|--------------------|------------------|---------------|----------------------|
| Бейзлайн           | 0.3302  | 0.6415               | 0.8868             | 0.9151          | 0.9340                 |
| Улучшенный бейзлайн| 0.4057  | 0.7170               | 0.8774             | 0.9528          | 0.9528                 |

# Было принятно решение поменять датасет, так как в первом слишком мало данных
Новый датасет ([https://www.kaggle.com/datasets/hetbabariya/imdb-movies-data-collection-5000-records])
## Для задачи Классификации - относится ли фильм к категории "рейтинг >= 8.3" или нет.
## Для задачи Регресии - предсказываем числовое значение Average Rating.

