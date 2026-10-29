# Лабораторная работа №3

- **ФИО:** Топакова Полина Васильевна
- **Номер зачётной книжки:** 230470
- **Вариант:** 0
- **Датасет:** CIFAR-10 (10 классов, 32×32 RGB)
- **Backbone для transfer learning:** `mobilenetv2_100` (`timm`)
- **Seed:** 42

## Окружение
- Python 3.12
- torch==2.14.0 (CPU)
- torchvision==0.29.0
- timm==1.0.29
- numpy==2.5.3
- scipy==1.18.1
- matplotlib==3.11.2
- scikit-learn==1.9.1
- pandas==2.2.3

## Установка и запуск

### 1. Клонирование репозитория
    git clone https://github.com/polina-topakova/Lab3_Deep_Learning.git
    cd Lab3_Deep_Learning

### 2. Создание и активация виртуального окружения
    python3.12 -m venv .venv
    source .venv/bin/activate
    .venv\Scripts\activate

### 3. Установка зависимостей
    pip install -r requirements.txt

Для CPU-колёс PyTorch:

    pip install torch==2.14.0 torchvision==0.29.0 --index-url https://download.pytorch.org/whl/cpu

### 4. Запуск ноутбука
    jupyter lab

Откройте файл `Lab3_0_Topakova.ipynb` и выполните все ячейки последовательно.

## Структура проекта

    lab3_0_topakova/
    ├── README.md
    ├── requirements.txt
    ├── Lab3_0_Topakova.ipynb
    └── .gitignore

## Версия Python
Проект протестирован на Python 3.12.

## Воспроизводимость
- Все случайные процессы засеяны (`SEED = 42`).
- Версии пакетов зафиксированы в `requirements.txt`.
- Запуск на чистом окружении не требует ручных правок.
- Для CPU-инференса и обучения используется `torch.set_num_threads(...)`.

## Краткие результаты

| Модель | Test Accuracy | Test Macro-F1 |
|---|---:|---:|
| Original CNN | 0.7317 | 0.7294 |
| MobileNetV2 (transfer learning) | 0.4845 | 0.4827 |
| Original CNN + MixUp | 0.7350 | 0.7329 |

Лучшая модель по валидационному Macro-F1: `original_cnn`, validation Macro-F1 = **0.7388**.

## Автор
- **ФИО:** Топакова Полина Васильевна
- **Номер зачётной книжки:** 230470
- **Вариант:** 0