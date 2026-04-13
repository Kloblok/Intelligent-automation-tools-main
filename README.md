# 🧠 Intelligent Automation Tools

> Курс лабораторных работ по работе с большими языковыми моделями (LLM) и мультимодальными системами

[![Python](https://img.shields.io/badge/Python-3.8+-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![PyTorch](https://img.shields.io/badge/PyTorch-2.0+-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)](https://pytorch.org/)
[![Transformers](https://img.shields.io/badge/Transformers-4.48.0+-FFD500?style=for-the-badge&logo=huggingface&logoColor=black)](https://huggingface.co/docs/transformers)
[![License](https://img.shields.io/badge/License-Educational-blue?style=for-the-badge)](LICENSE)

---

## 📋 Оглавление

- [Описание](#-описание)
- [Цели курса](#-цели-курса)
- [Структура лабораторных](#-структура-лабораторных)
- [Требования](#-требования)
- [Установка](#-установка)
- [Быстрый старт](#-быстрый-старт)
- [Подробное описание лабораторных](#-подробное-описание-лабораторных)
- [Troubleshooting](#-troubleshooting)
- [Полезные ресурсы](#-полезные-ресурсы)
- [Лицензия](#-лицензия)

---

## 📖 Описание

Проект представляет собой комплексный курс из **6 лабораторных работ**, охватывающих ключевые технологии современного **NLP** и **компьютерного зрения**. Каждая работа построена как самостоятельное Jupyter-ноутбук с подробными объяснениями, примерами кода и практическими заданиями.

---

## 🎯 Цели курса

| Цель | Описание |
|------|----------|
| 🤖 | Освоить работу с предобученными языковыми моделями |
| 🔧 | Научиться дообучать модели под специфичные задачи |
| 📚 | Построить систему ответов на вопросы по документам (RAG) |
| 🖼️ | Реализовать мультимодальные приложения (текст + изображения) |
| 🧬 | Изучить современные архитектуры VLM и LMM |

---

## 📚 Структура лабораторных

| № | Лабораторная | Тема | Ключевые технологии |
|---|--------------|------|---------------------|
| 1 | **lab-01** | Введение в LLM | `Hugging Face Transformers`, `pipeline()`, `Qwen-2.5` |
| 2 | **lab-02** | Тонкая настройка LLM (Fine-tuning) | `PEFT`, `LoRA`, `QLoRA`, `bitsandbytes`, `Dolly-15k` |
| 3 | **lab-03** | RAG: Retrieval-Augmented Generation | `LangChain`, `FAISS`, `эмбеддинги`, `векторный поиск` |
| 4 | **lab-04** | Векторные базы данных | `ChromaDB`, `семантический поиск`, `метаданные` |
| 5 | **lab-05** | Мультимодальные LLM (LMM) | `Qwen2.5-VL`, `Visual Question Answering` |
| 6 | **lab-06** | Vision-Language Models (VLM) | `CLIP`, `zero-shot классификация`, `ViT`, `ResNet` |

---

## 💻 Требования

### Минимальные конфигурации

| Компонент | Требование |
|-----------|------------|
| **Python** | 3.8+ |
| **RAM** | 8 GB |
| **Диск** | 10 GB свободного места |

### Рекомендуемые конфигурации

| Компонент | Требование |
|-----------|------------|
| **GPU** | NVIDIA T4 / RTX 3060+ (6+ GB памяти) |
| **RAM** | 16 GB |
| **Доступ** | Hugging Face Hub |

### Основные зависимости

```txt
transformers >= 4.48.0
torch >= 2.0
peft
bitsandbytes
langchain
chromadb
faiss-cpu
sentence-transformers
Pillow
```

---

## 🚀 Установка

### 1. Клонирование репозитория

```bash
git clone <repository-url>
cd Intelligent-automation-tools
```

### 2. Создание виртуального окружения

```bash
# Windows
python -m venv venv
venv\Scripts\activate

# Linux/macOS
python3 -m venv venv
source venv/bin/activate
```

### 3. Установка зависимостей

```bash
# Базовые зависимости
pip install --upgrade pip
pip install transformers torch accelerate

# Все зависимости для курса
pip install -r requirements.txt
```

> 💡 **Совет:** Для установки всех зависимостей создайте файл `requirements.txt` на основе списка выше.

---

## ⚡ Быстрый старт

### Запуск лабораторных работ

```bash
# Запуск Jupyter Notebook
jupyter notebook lab-01.ipynb

# Или через Jupyter Lab
jupyter lab
```

### Проверка установки

```python
import torch
import transformers

print(f"PyTorch version: {torch.__version__}")
print(f"Transformers version: {transformers.__version__}")
print(f"GPU available: {torch.cuda.is_available()}")
```

---

## 📖 Подробное описание лабораторных

### 🔹 Лабораторная 1: Введение в LLM

**Цель:** Знакомство с предобученными языковыми моделями и экосистемой Hugging Face.

**Что вы изучите:**
- Работа с `Hugging Face pipeline()` для упрощения взаимодействия с моделями
- Генерация текста с различными параметрами (temperature, top-k, top-p)
- Классификация тональности текста (sentiment analysis)
- Построение Question-Answering систем

**Результат:** Готовые скрипты для анализа текста и генерации ответов.

---

### 🔹 Лабораторная 2: Fine-tuning

**Цель:** Освоение техник эффективной дообучения больших языковых моделей.

**Что вы изучите:**
- Transfer Learning в NLP и его преимущества
- PEFT (Parameter-Efficient Fine-Tuning) и LoRA адаптеры
- 4-bit квантование для экономии памяти
- Дообучение модели на датасете инструкций (Dolly-15k)

**Результат:** Дообученная модель для генерации инструкций.

---

### 🔹 Лабораторная 3: RAG (Retrieval-Augmented Generation)

**Цель:** Построение системы ответов на вопросы с использованием внешней базы знаний.

**Что вы изучите:**
- Борьба с галлюцинациями LLM через внешний контекст
- Создание и использование эмбеддингов
- Векторный поиск с помощью FAISS
- Генерация ответов с учётом найденного контекста

**Результат:** RAG-система для ответов на вопросы по документам.

---

### 🔹 Лабораторная 4: Векторные базы данных

**Цель:** Изучение современных векторных баз данных для хранения и поиска эмбеддингов.

**Что вы изучите:**
- ChromaDB для хранения и управления эмбеддингами
- Семантический поиск по текстовым данным
- Фильтрация результатов по метаданным
- Гибридный поиск (векторный + ключевые слова)

**Результат:** Система семантического поиска с метаданными.

---

### 🔹 Лабораторная 5: Мультимодальные LLM

**Цель:** Работа с моделями, способными обрабатывать текст и изображения одновременно.

**Что вы изучите:**
- Архитектура Qwen2.5-VL и её особенности
- Visual Question Answering (VQA)
- Генерация описаний изображений (image captioning)
- Анализ графиков, диаграмм и визуальных данных

**Результат:** Мультимодальная система для анализа изображений.

---

### 🔹 Лабораторная 6: Vision-Language Models

**Цель:** Изучение контрастивного обучения и zero-shot классификации.

**Что вы изучите:**
- CLIP и контрастивное обучение
- Zero-shot классификация изображений без дообучения
- Поиск изображений по текстовому описанию
- Сравнение архитектур (ViT-B/32, ViT-L/14, RN50)

**Результат:** Система zero-shot классификации и поиска изображений.

---

## 🛠️ Troubleshooting

### Частые проблемы и решения

| Проблема | Решение |
|----------|---------|
| **Нехватка памяти GPU** | Используйте `bitsandbytes` для 4/8-bit квантования |
| **Ошибки при загрузке модели** | Проверьте доступ к Hugging Face Hub, используйте `HF_TOKEN` |
| **Медленная работа без GPU** | Установите CUDA-версию PyTorch или используйте Google Colab |
| **Конфликты зависимостей** | Создайте чистое виртуальное окружение |

### Полезные команды

```bash
# Проверка версии PyTorch и CUDA
python -c "import torch; print(torch.__version__); print(torch.cuda.is_available())"

# Очистка кэша Hugging Face
huggingface-cli logout
rm -rf ~/.cache/huggingface
```

---

## 🔗 Полезные ресурсы

### Документация

- [🤗 Hugging Face Documentation](https://huggingface.co/docs)
- [📐 LangChain Documentation](https://python.langchain.com/)
- [🔥 PyTorch Documentation](https://pytorch.org/docs/)

### Модели и датасеты

- [Qwen Models](https://huggingface.co/Qwen)
- [Hugging Face Model Hub](https://huggingface.co/models)
- [Hugging Face Datasets](https://huggingface.co/datasets)

### Научные статьи

- [📄 CLIP Paper](https://arxiv.org/abs/2103.00020)
- [📄 LoRA Paper](https://arxiv.org/abs/2106.09685)
- [📄 RAG Paper](https://arxiv.org/abs/2005.11401)

### Платформы для запуска

- [Google Colab](https://colab.research.google.com/) — бесплатный GPU/TPU
- [Kaggle Notebooks](https://www.kaggle.com/code) — GPU на 30 часов/неделю
- [Hugging Face Spaces](https://huggingface.co/spaces) — деплой моделей

---

## 📁 Структура проекта

```
Intelligent-automation-tools/
├── 📄 README.md              # Документация проекта
├── 📓 lab-01.ipynb           # Введение в LLM
├── 📓 lab-02.ipynb           # Fine-tuning
├── 📓 lab-03.ipynb           # RAG
├── 📓 lab-04.ipynb           # Векторные базы данных
├── 📓 lab-05.ipynb           # Мультимодальные LLM
└── 📓 lab-06.ipynb           # Vision-Language Models
```

---

## 📄 Лицензия

Образовательный проект для изучения технологий NLP и компьютерного зрения.

---

<div align="center">

**Сделано с ❤️ для изучения интеллектуальных систем автоматизации**

[🔝 Наверх](#-intelligent-automation-tools)

</div>
