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
В файле imdb.ipynb находится код для второй попытки.
## Для задачи Классификации - относится ли фильм к категории "рейтинг >= 8.3" или нет.
## Для задачи Регресии - предсказываем числовое значение Average Rating.

| Алгоритм            | Задача        | Бейзлайн                                    | Улучшенный бейзлайн                        | Самостоятельная реализация алгоритма       |
|---------------------|---------------|---------------------------------------------|--------------------------------------------|--------------------------------------------|
| KNN                 | классификация | Accuracy: 0.4628<br>                        | Accuracy: 0.5240<br>                       | Accuracy: 0.4743<br>                       |
|                     | регрессия     | MAE: 0.3022 <br> MSE: 0.1442<br>R²: 0.0014  | MAE: 0.2925<br> MSE: 0.1318<br>R²: 0.0869  | MAE: 0.2722<br> MSE: 0.1299<br>R²: 0.0325  |
| Линейные модели     | классификация | Accuracy: 0.9369<br>                        | Accuracy: 0.9218<br>                       | Accuracy: 0.9201<br>                       |
|                     | регрессия     | MAE: 0.6005<br> MSE: 0.5808<br>R²: -3.0234  | MAE: 0.7174<br> MSE: 0.8291<br>R²: -4.7438 | MAE: 0.6913<br> MSE: 0.7272<br>R²: -3.4759 |
| Решающее дерево     | классификация | Accuracy: 0.8788<br>                        | Accuracy: 0.9208<br>                       | Accuracy: 0.8758<br>                       |
|                     | регрессия     | MSE: 0.2334<br> MAE: 0.3664<br>R^2: -0.6172 | MSE: 0.1317<br>MAE: 0.2927<br>R^2: 0.0878  | MSE: 0.1545<br>MAE: 0.3024<br>R^2: -0.0317 |
| Случайный лес       | классификация | Accuracy: 0.9279<br>                        | Accuracy: 0.9238<br>                       | Accuracy: 0.9087<br>                       |
|                     | регрессия     | MSE: 0.1246<br>MAE: 0.2791<br>R^2: 0.1371   | MSE: 0.1227<br>MAE: 0.2822<br>R^2: 0.1498  | MSE: 0.1234<br>MAE: 0.2697<br>R^2: 0.1403  |
| Градиентный бустинг | классификация | Accuracy: 0.9238<br>                        | Accuracy:  0.9218<br>                      | Accuracy: 0.9013<br>                       |
|                     | регрессия     | MSE: 0.1269<br>MAE: 0.2897<br>R^2: 0.1209   | MSE: 0.1272<br>MAE: 0.2887<br>R^2: 0.1191  | MSE: 0.1270<br>MAE: 0.2880<br>R^2: 0.1201  |


# Вывод
По табличке видно, что улучшенный бейзлайн почти всегда превосходит базовый благодаря оптимизации гиперпараметров. Классификация показала наилучшие результаты для случайного леса и градиентного бустинга (Accuracy > 0.91), а регрессия демонстрирует низкое качество, что видно по R^2, который в некоторых случаях отрицательный. Самостоятельная реализация моделей чаще всего достигает результатов близких к бейзлайну, но требует доработки для сравнения с улучшенным бейзлайном.
