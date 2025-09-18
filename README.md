# Kittygram - Социальная сеть для любителей котиков 🐱

![CI/CD Status](https://github.com/arturioo22/kittygram_final/actions/workflows/main.yml/badge.svg)
![Docker](https://img.shields.io/badge/Docker-✓-blue.svg)
![Django](https://img.shields.io/badge/Django-3.2-green.svg)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-✓-blue.svg)

## 📖 Описание проекта

Kittygram — это полнофункциональная социальная сеть для обмена фотографиями и информацией о котиках. Пользователи могут создавать профили своих питомцев, добавлять достижения и просматривать котиков других пользователей.

### Основные функции:
- Публикация карточек котиков
- Достижения питомцев
- Система лайков и комментариев
- Загрузка фотографий котиков
- Docker-контейнеризация
- CI/CD автоматизация

## 🛠️ Стек технологий

### Backend
- **Django** - веб-фреймворк
- **Django REST Framework** - построение REST API
- **PostgreSQL** - реляционная база данных
- **SQLite** — для разработки и тестирования
- **Djoser** - аутентификация и управление пользователями
- **Pillow** - работа с изображениями
- **CORS headers** - кросс-доменные запросы

### Инфраструктура
- **Docker** — контейнеризация
- **Docker Compose** — оркестрация
- **Nginx** — веб-сервер и прокси
- **GitHub Actions** — CI/CD
- **Docker Hub** — реестр образов

## 🚀 Развертывание проекта

### Предварительные требования

- Docker и Docker Compose
- Python 3.8+ (для разработки)
- Git

### 1. Клонирование репозитория
git clone <ссылка-на-репозиторий>
cd kittygram

### 2. Настройка переменных окружения
Создайте файл .env в корневой директории:

## env
# Django
SECRET_KEY=your-super-secret-key-here
DEBUG=True
ALLOWED_HOSTS=kitygrammm.ddns.net,localhost,127.0.0.1
CSRF_TRUSTED_ORIGINS=http://kitygrammm.ddns.net,http://www.kitygrammm.ddns.net,http://89.169.184.73
CORS_ALLOWED_ORIGINS=http://kitygrammm.ddns.net,http://www.kitygrammm.ddns.net

# Database
POSTGRES_DB= DB_name
POSTGRES_USER= DB_user_name
POSTGRES_PASSWORD=DB_pas
DB_HOST=db
DB_PORT=5432
### 3. Запуск с помощью Docker
docker-compose up -d --build
### 4. Применение миграций
docker-compose exec backend python manage.py migrate
### 5. Сбор статических файлов
docker-compose exec backend python manage.py collectstatic --no-input

### 👤 Автор
Фисунов Артур

Email: fisunov.arthur@yandex.ru

GitHub: arturioo22

## 🔗 Ссылки для проверки:

- **Репозиторий:** https://github.com/arturioo22/kittygram_final
- **Workflow:** https://github.com/arturioo22/kittygram_final/actions
- **Production:** https://kitygrammm.ddns.net
- **Docker Hub:** https://hub.docker.com/u/arturioo22