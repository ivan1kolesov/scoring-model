# Задача: построить скоринговую модель, нужно предсказать вернет кредит человек или нет.
Данные взял с соревнований.<br>
#### Используемый стек: pandas, numpy, sklearn, lightgbm, catboost, xgboost и библиотеки визуализации.

Что я сделал:
- Для начала разбирался зачем нам нужен ip_flag, в итоге выяснилось что все значение с 1 будет сложно предсказать в пределах одной модели.
- Удалял колонки с большим кол-во пропусков и с высокой кореляцией.
- Поработал с кодами и object признаками и закодировал их.
- Удалил выбросы принципом:
  - Lower Bound: (Q1 - 1.5 * IQR)
  - Upper Bound: (Q3 + 1.5 * IQR)
- Обучение, подбор модели, подбор параметров, удаление малозначимых фич.
