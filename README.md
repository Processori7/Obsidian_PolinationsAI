# Polinations AI Chat

[English](README_EN.md) | [Русский](#)

A plugin for integration with Pollinations AI API, allowing you to chat with various AI models and generate images directly from Obsidian with automatic saving to notes.

## Features

- 🤖 Chat with various AI models via Pollinations API
- 🎨 AI image generation (Flux, Turbo, Zimage, and more)
- 💾 Automatic saving of conversations and images to notes
- ⚡ Quick questions with instant answer saving
- 🌍 Multilingual interface (English / Русский)
- 🔒 Free models filter for working without API key
- 🎭 Beautiful interface with dark/light theme
- 📱 Responsive design for mobile devices
- 🔧 Flexible settings

[Full English README →](README_EN.md)

---

# Polinations AI Chat — плагин для Obsidian

Плагин для интеграции с Pollinations AI API, позволяющий общаться с различными ИИ моделями и генерировать изображения прямо из Obsidian с сохранением результатов в заметки.

## Возможности

- 🤖 Чат с различными ИИ моделями через Pollinations API
- 🎨 Генерация изображений с помощью AI (Flux, Turbo, Zimage и др.)
- 💾 Автоматическое сохранение диалогов и изображений в заметки
- ⚡ Быстрые вопросы с мгновенным сохранением ответов
- 🌍 Мультиязычный интерфейс (English / Русский)
- 🔒 Фильтр бесплатных моделей для работы без API ключа
- 🎭 Красивый интерфейс с темной/светлой темой
- 📱 Адаптивный дизайн для мобильных устройств
- 🔧 Гибкие настройки

## Установка

### Вариант 1: Ручная установка
1. Скачайте файлы `main.js`, `manifest.json`, `styles.css` или скачайте архив из релизов
2. Создайте папку `pollinations-ai-chat` в `.obsidian/plugins/`
3. Поместите файлы в созданную папку
4. Перезапустите Obsidian
5. Включите плагин в настройках

### Вариант 2: Разработка
1. Клонируйте репозиторий: `git clone https://github.com/Processori7/Polinations-AI-Chat.git`
2. Переидите в папку `cd Polinations-AI-Chat`
3. Запустите `npm install`
4. Запустите `npm run build`
5. Перенесите файлы `main.js`, `manifest.json`, `styles.css` в папку `.obsidian/plugins/`
6. Перезапустите Obsidian
7. Включите плагин в настройках Obsidian (если не включен)

## Использование

### Команды
- **Ctrl+P** → "Открыть ИИ чат" - открыть полноценный чат
- **Ctrl+P** → "Быстрый вопрос ИИ" - задать вопрос и сохранить ответ
- **Ctrl+P** → "Генерировать ИИ изображение" - создать изображение по описанию
- Клик по иконке в левой панели - открыть чат

### Интерфейс чата
1. Выберите модель ИИ из выпадающего списка
2. Введите ваш вопрос в поле ввода
3. Нажмите Enter или кнопку "Отправить"
4. Используйте кнопки "Сохранить чат" и "Очистить" для управления

### Генерация изображений
1. Откройте команду "Генерировать ИИ изображение"
2. Выберите модель изображений (Flux, Turbo, Zimage и др.)
3. Опишите желаемое изображение
4. Настройте размер (ширина × высота)
5. Нажмите "Генерировать"
6. Изображение автоматически сохранится и вставится в активную заметку

### Настройки
- **Язык интерфейса** - выбор между английским и русским
- **Показывать только бесплатные модели** - фильтр моделей, работающих без API ключа
- **Модель по умолчанию** - выбор предпочитаемой модели для чата
- **Модель изображений по умолчанию** - выбор предпочитаемой модели для генерации изображений
- **Автосохранение чатов** - включение/выключение автоматического сохранения
- **Папка для чатов** - путь для сохранения диалогов
- **Папка для изображений** - путь для сохранения сгенерированных изображений
- **API токен** - ключ для доступа к продвинутым функциям

## Доступные модели

Плагин автоматически загружает список доступных моделей с Pollinations API:

### Текстовые модели
- GPT модели (openai, openai-fast)
- Claude модели
- Gemini модели (gemini-fast)
- Llama модели
- Qwen Coder
- Mistral
- DeepSeek
- Nova Micro
- И многие другие

### Модели генерации изображений
- **Zimage** - стандартная модель (по умолчанию)
- **Flux** - высокое качество
- **Turbo** - быстрая генерация
- **GPT Image** - от OpenAI
- **Kontext** - контекстно-зависимая генерация
- **SeeDream** - художественный стиль
- **Nanobanana** - компактная модель

### Бесплатные модели
При включении опции "Показывать только бесплатные модели" доступны:
- Текст: openai, openai-fast, qwen-coder, mistral, gemini-fast, nova-micro, deepseek
- Изображения: все модели изображений работают без API ключа

## API ключ

Для доступа к расширенным функциям и генерации изображений рекомендуется получить API ключ:

1. Перейдите на [https://enter.pollinations.ai/sign-in](https://enter.pollinations.ai/sign-in)
2. Войдите или зарегистрируйтесь
3. Получите **серверный API ключ** (Server API Key) - он предоставляет больше возможностей
4. Добавьте ключ в настройках плагина

> **Примечание:** Базовые текстовые модели работают без API ключа. Ключ необходим для генерации изображений и доступа к премиум-моделям.

## Структура сохраненных чатов
Чаты сохраняются в формате Markdown со следующей структурой:
```markdown
# Название чата

**Модель:** название-модели
**Дата:** дата и время

---

## 👤 Пользователь

Ваш вопрос

---

## 🤖 ИИ

Ответ ИИ
```

## Разработка

### Требования
- Node.js
- npm
- TypeScript

### Команды
```bash
npm install         # Установка зависимостей
npm run dev         # Разработка с hot-reload
npm run build       # Сборка для продакшена
```

### Структура проекта
```
├── main.ts          # Основной файл плагина
├── manifest.json    # Манифест плагина
├── styles.css       # Стили интерфейса
├── package.json     # Зависимости
├── tsconfig.json    # Настройки TypeScript
├── esbuild.config.mjs # Конфигурация сборки
└── versions.json    # Версии плагина
```

## API
Плагин использует Pollinations AI API:
- **Text Generation:** `https://gen.pollinations.ai/v1/chat/completions`
- **Image Generation:** `https://gen.pollinations.ai/image/{prompt}`
- **Список текстовых моделей:** `https://gen.pollinations.ai/text/models`
- **Список моделей изображений:** `https://gen.pollinations.ai/image/models`
- Бесплатное использование базовых моделей без регистрации
- Расширенные возможности с API ключом
- Поддержка различных моделей: OpenAI, Claude, Llama, Gemini и другие

### Пример использования Text API:
```json
POST https://gen.pollinations.ai/v1/chat/completions
{
  "model": "openai",
  "messages": [
    {"role": "user", "content": "Привет, как дела?"}
  ],
  "private": true
}
```

### Пример использования Image API:
```
GET https://gen.pollinations.ai/image/Beautiful%20sunset?model=flux&width=1024&height=1024&private=true&key=YOUR_API_KEY
```

Возвращает изображение в формате PNG.

## Лицензия

MIT License

## Поддержка

Если у вас есть вопросы или предложения, создайте issue в репозитории проекта.
