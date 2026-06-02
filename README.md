# 📂 papers

Репозиторий с кодом к статьям. Каждый ноутбук — самостоятельный пример, разобранный в соответствующей публикации.

---

## Содержание

### 🧬 Генетический алгоритм для отбора признаков
**Файл:** `fs_genetic_example.ipynb`

Реализация генетического алгоритма для feature selection в задачах классификации.
В примере используется CatBoostClassifier и метрика Gini как fitness-функция.

Что внутри:
- Абстрактный интерфейс модели (`ModelGeneric`) и класс особи (`Individual`)
- Инициализация популяции, оценка fitness, ранжирование и отбор
- Мутация, скрещивание и переход к следующему поколению
- Класс `GeneticSelector` с методом `.select()` и свойством `.selected_features`

```bash
# Зависимости
pip install catboost scikit-learn pandas
```

---

### 📊 Оптимальное бинирование с optbinning
**Файл:** `optbinning_example_real_task.ipynb`

Практический пример работы с библиотекой [optbinning](https://github.com/guillermo-navas-palencia/optbinning) на реальных данных кредитного скоринга.

Что внутри:
- Загрузка и препроцессинг данных (числовые, категориальные, флаговые признаки)
- Построение биннинга через `BinningProcess`
- Визуализация WOE-таблиц и IV-статистик
- Применение в пайплайне классификации

Данные: [`sampled_app_train.csv`](https://github.com/sberbank-ai-lab/LightAutoML/blob/master/examples/data/sampled_app_train.csv) из репозитория LightAutoML

```bash
# Зависимости
pip install optbinning scikit-learn pandas numpy matplotlib seaborn psutil
```

---

## Запуск

```bash
git clone https://github.com/kgrushin/papers.git
cd papers
jupyter notebook
```

Каждый ноутбук запускается независимо. Данные для `optbinning_example_real_task.ipynb` нужно положить в папку `data/`.