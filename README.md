# CIFAR-10 CNN Model Comparison (PyTorch)
Исследование сверточных сетей (CNN): **архитектуры, transfer learning и fine-tuning**, плюс **сравнение обучения с/без data augmentation** на датасете **CIFAR-10**.

---

## Цели проекта
- Построить и обучить **базовую CNN (SimpleCNN)** с нуля на CIFAR-10
- Сравнить подходы:
  - обучение “с нуля”
  - **transfer learning** (ResNet18 с замороженными слоями)
  - **fine-tuning ResNet18** (разморозка верхних слоёв)
- Проверить влияние **data augmentation**
- Провести оценку качества:
  - **train/val curves** (loss/accuracy)
  - **classification report**
  - **confusion matrix**
  - финальные выводы и сравнение моделей

---

## Модели в ноутбуке
- **SimpleCNN (no aug)** — базовая CNN без аугментации  
- **SimpleCNN (+aug)** — базовая CNN с data augmentation  
- **ResNet18 (frozen)** — transfer learning: “голова” обучается, backbone заморожен  
- **ResNet18 (finetuned)** — fine-tuning: разморозка верхних слоёв и дообучение  

---

## Датасет
Используется **CIFAR-10** через `torchvision.datasets`.

В ноутбуке сейчас стоит `download=False`.  
Поэтому для первого запуска у тебя есть два варианта:

**Вариант A (рекомендуется):** поменять на `download=True` в ячейках с CIFAR-10 и запустить.  
**Вариант B:** заранее положить датасет в папку `./data`.

---

## Структура репозитория
- `Project-2.ipynb` — основной ноутбук со всеми экспериментами, графиками и выводами
- `requirements.txt` — зависимости проекта
- `.gitignore` — исключения (venv, data, caches и т.д.)

---

## Как запустить локально
### 1) Клонирование
```bash
git clone https://github.com/Tural-Kazimov/cifar10-cnn-model-comparison.git
cd <YOUR_REPO_FOLDER> 
