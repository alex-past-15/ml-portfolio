# Image Classification

Проект по классификации изображений на 6 классов с использованием `PyTorch`.

## Задача

Нужно определить, к какому классу относится изображение:

- `buildings`
- `forest`
- `glacier`
- `mountain`
- `sea`
- `street`

## Что есть в проекте

- анализ датасета;
- визуализация изображений и распределения классов;
- подготовка `Dataset` и `DataLoader`;
- аугментации для обучающей выборки;
- baseline-модель `SimpleCNN`;
- transfer learning с `ResNet18` и `EfficientNet-B0`;
- оценка качества на тестовой выборке;
- инференс на новых изображениях.

## Структура данных

- `data/seg_train/seg_train` — train
- `data/seg_test/seg_test` — test
- `data/seg_pred/seg_pred` — изображения для предсказания

## Модели

В проекте используются три модели:

- `SimpleCNN` — baseline;
- `ResNet18` — pretrained-модель для transfer learning;
- `EfficientNet-B0` — более современная pretrained-архитектура.

## Аугментации

Для обучающей выборки используются:

- `RandomHorizontalFlip`
- `RandomRotation`
- `ColorJitter`

Для валидации, теста и инференса используются только `Resize` и `Normalize`.

## Метрики

Для оценки качества используются:

- `accuracy`
- `macro F1-score`
- `classification report`
- `confusion matrix`

## Структура проекта

```bash
Image Classification/
├── data/
│   ├── seg_train/
│   ├── seg_test/
│   └── seg_pred/
├── checkpoints/
├── image_classification_project.ipynb
└── README.md
```

## Основной файл

Вся основная работа находится в ноутбуке `image_classification_project.ipynb`.

## Стек

- `Python`
- `PyTorch`
- `torchvision`
- `matplotlib`
- `seaborn`
- `scikit-learn`
