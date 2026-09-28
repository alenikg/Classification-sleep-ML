# Классификация нарушений сна.

Учебный проект по машинному обучению. Цель — обучить модели, способные предсказать наличие нарушения сна у человека по данным о его образе жизни и состоянии здоровья.

## Описание задачи:

По набору признаков нужно определить одну из трёх категорий:
- `Healthy` — нет нарушения;
- `Insomnia` — бессонница;
- `Sleep Apnea` — апноэ сна.
Проект выполнен в виде Jupyter Notebook.

## Данные:

Используется файл `sleep.csv`. Целевая переменная — `Sleep Disorder`.  
Пропуски в ней заполняются значением `Healthy`.

В ходе предобработки:
- названия колонок приводятся к нижнему регистру;
- выявляются коррелирующие признаки и удаляются: `Person ID`, `Blood Pressure`, `Sleep Duration`, `Daily Steps`, `Stress Level`, `Diastolic_BP`;
- категориальные признаки кодируются one-hot encoding;
- числовые признаки масштабируются `MinMaxScaler`.

Обучаются модели KNeighborsClassifier, LogisticRegression, DecisionTreeClassifier.

## Установка:

pip install pandas numpy scikit-learn matplotlib seaborn jupyter