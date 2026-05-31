# 🤖 MultiToolBot

Многофункциональный Telegram бот с более чем 15 полезными функциями, включая генерацию изображений через ИИ, игры, утилиты и многое другое.

## ✨ Возможности

### 🎨 ИИ Функции
- **Генерация изображений** - создавайте уникальные изображения по текстовому описанию

### ⏱️ Утилиты
- **Таймер** - установка таймера на определенное количество секунд
- **Переводчик** - перевод текста на русский, английский, немецкий и французский языки
- **Подсчет символов** - подсчет количества символов в тексте (без пробелов)
- **Подсчет слов** - подсчет количества слов в тексте
- **Генератор паролей** - создание надежных паролей заданной длины

### 🎮 Игры
- **Кубики** - различные типы игральных костей (d4, d6, d8, d10, d12, d20, d100)
- **Монетка** - подбрасывание монетки (орел/решка)

## 📋 Команды

### Основные команды
| Команда | Описание |
|---------|----------|
| `/start` или `/menu` | Главное меню |
| `/help` или `/commands` | Показать справку |
| `/info` или `/about` | Информация о боте |

### Утилиты
| Команда | Описание | Пример |
|---------|----------|--------|
| `/timer [секунды]` | Установить таймер | `/timer 60` |
| `/translate [текст]` | Перевести текст | `/translate Hello` |
| `/wordcount [текст]` | Подсчитать слова | `/wordcount Привет мир` |
| `/symbolcount [текст]` | Подсчитать символы | `/symbolcount Привет` |
| `/password [длина]` | Сгенерировать пароль | `/password 16` |

### ИИ Функции
| Команда | Описание | Пример |
|---------|----------|--------|
| `/generate [описание]` | Сгенерировать изображение | `/generate красивый закат` |
| `/image [описание]` | То же самое | `/image cyberpunk city` |
| `/ai [описание]` | То же самое | `/ai кот в космосе` |

### Игры
| Команда | Описание |
|---------|----------|
| `/games` | Открыть меню игр |
| `/roll` или `/dice` | Бросить кубик d6 |
| `/roll d20` | Бросить указанный кубик |
| `/coin` | Подбросить монетку |

## 🚀 Установка и запуск

### Требования
- Python 3.8 или выше
- Telegram Bot Token (получить у [@BotFather](https://t.me/BotFather))

### Установка

1. **Клонируйте репозиторий**
```bash
git clone https://github.com/YOUR_USERNAME/MultiToolBot.git
cd MultiToolBot
Установите зависимости

bash
pip install -r requirements.txt
Настройте конфигурацию

Создайте файл config.py в корневой директории:

python
# config.py
token = "YOUR_BOT_TOKEN_HERE"
Настройте ИИ генератор (опционально)

В файле ai_logic.py настройте функцию generate_image() в соответствии с вашим API для генерации изображений. Пример реализации:

python
# ai_logic.py
def generate_image(prompt, output_path):
    # Ваша реализация генерации изображений
    # Например, через DALL-E, Stable Diffusion или другой сервис
    pass
Запустите бота

bash
python bot.py
📁 Структура проекта
text
MultiToolBot/
├── bot.py              # Основной файл бота
├── ai_logic.py         # Логика генерации изображений
├── config.py           # Конфигурация (токен бота)
├── requirements.txt    # Зависимости Python
├── images/            # Папка для временных изображений (создается автоматически)
└── README.md          # Документация
📦 Зависимости
txt
pyTelegramBotAPI>=4.15.0
translate>=3.6.1
Дополнительные зависимости для генерации изображений (выберите подходящий вариант):

txt
# Для использования OpenAI DALL-E
openai>=1.0.0

# Для использования Stability AI
stability-sdk>=0.5.0

# Для локальной генерации (PyTorch + Diffusers)
torch>=2.0.0
diffusers>=0.24.0
transformers>=4.35.0
🎯 Примеры использования
Генерация изображения
bash
/generate красивый закат на море с пальмами
Таймер с интерактивной остановкой
bash
/timer 30
# Таймер запустится с возможностью остановки через кнопку
Перевод текста
bash
/translate Hello, how are you?
# Бот предложит выбрать язык перевода
🔧 Особенности
Интерактивные кнопки - все функции доступны через удобное меню

Поддержка состояний - бот запоминает, на каком этапе находится пользователь

Безопасная генерация паролей - пароли содержат буквы верхнего и нижнего регистра, цифры

Обработка ошибок - корректная обработка всех возможных ошибок API

Асинхронная генерация - изображения генерируются без блокировки других команд

⚠️ Примечания
Генерация изображений - функция требует настройки ai_logic.py под ваш API сервиса генерации изображений

Переводчик - использует библиотеку translate, может требовать подключения к интернету

Лимиты сообщений - рекомендуется установить ограничения на частоту запросов для production версии

🛠️ Возможные проблемы и решения
Бот не отвечает
Проверьте токен в config.py

Убедитесь, что бот запущен и нет ошибок в консоли

Не работает генерация изображений
Проверьте правильность настройки ai_logic.py

Убедитесь, что все зависимости для генерации установлены

Ошибка "message is not modified"
Это нормальное поведение при повторном нажатии на кнопку, бот корректно обрабатывает это

🤝 Вклад в проект
Приветствуются pull requests и issues! Если вы хотите добавить новую функцию или исправить баг:

Форкните репозиторий

Создайте ветку для ваших изменений

Внесите изменения и сделайте commit

Отправьте pull request

📝 Лицензия
MIT License - свободное использование в любых целях

👨‍💻 Автор
Ваше Имя - @ваш_telegram

🌟 Поддержка проекта
Если вам нравится проект, поставьте звезду на GitHub! ⭐

📞 Контакты
Telegram: @ваш_telegram

GitHub: ваш_username

MultiToolBot - ваш универсальный помощник в Telegram! 🚀

text

А также создайте файл `requirements.txt`:

```txt
pyTelegramBotAPI==4.15.0
translate==3.6.1
Дополнительные файлы для GitHub:
.gitignore
gitignore
# Python
__pycache__/
*.py[cod]
*$py.class
*.so
.Python
env/
venv/
ENV/
env.bak/
venv.bak/

# Config files (если не хотите выкладывать токен)
config.py

# Images
images/
*.png
*.jpg
*.jpeg
*.gif

# IDE
.vscode/
.idea/
*.swp
*.swo

# Logs
*.log
LICENSE (MIT License)
txt
MIT License

Copyright (c) 2024 [Ваше Имя]

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
Инструкция по настройке ai_logic.py:
Создайте пример реализации ai_logic.py:

python
# ai_logic.py
import requests
import os

def generate_image(prompt, output_path):
    """
    Генерирует изображение на основе текстового описания.
    
    Args:
        prompt (str): Текстовое описание изображения
        output_path (str): Путь для сохранения изображения
    
    Returns:
        str: Путь к сохраненному изображению
    
    Raises:
        Exception: Если генерация не удалась
    """
    
    # Пример для OpenAI DALL-E 3
    # from openai import OpenAI
    # client = OpenAI(api_key="YOUR_API_KEY")
    # 
    # response = client.images.generate(
    #     model="dall-e-3",
    #     prompt=prompt,
    #     size="1024x1024",
    #     quality="standard",
    #     n=1,
    # )
    # 
    # image_url = response.data[0].url
    # 
    # # Скачиваем изображение
    # img_response = requests.get(image_url)
    # with open(output_path, 'wb') as f:
    #     f.write(img_response.content)
    # 
    # return output_path
    
    # Пример для Stability AI
    # import stability_sdk.interfaces.gooseai.generation.generation_pb2 as generation
    # from stability_sdk import client
    # 
    # stability_api = client.StabilityInference(
    #     key="YOUR_API_KEY",
    #     verbose=True,
    # )
    # 
    # answers = stability_api.generate(
    #     prompt=prompt,
    #     steps=30,
    #     cfg_scale=7.0,
    #     width=1024,
    #     height=1024,
    #     samples=1,
    # )
    # 
    # for resp in answers:
    #     for artifact in resp.artifacts:
    #         if artifact.finish_reason == generation.FILTER:
    #             raise Exception("Изображение отфильтровано")
    #         if artifact.type == generation.ARTIFACT_IMAGE:
    #             with open(output_path, 'wb') as f:
    #                 f.write(artifact.binary)
    # 
    # return output_path
    
    # Заглушка (замените на реальную реализацию)
    raise NotImplementedError("Настройте функцию generate_image в ai_logic.py")
