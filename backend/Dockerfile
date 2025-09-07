# Используем официальный образ Python
FROM python:3.10-slim

# Устанавливаем рабочую директорию
WORKDIR /app

# Копируем файл с зависимостями
COPY ./requirements.txt /app/requirements.txt

# Устанавливаем системные зависимости и зависимости Python
RUN apt-get update \
    && apt-get -y install libpq-dev gcc \
    && pip install --no-cache-dir --upgrade pip \
    && pip install --no-cache-dir -r requirements.txt \
    && apt-get purge -y --auto-remove gcc

# Копируем весь код проекта
COPY . /app

# Собираем статику
RUN python manage.py collectstatic --noinput

# Указываем команду для запуска сервера
CMD ["gunicorn", "--bind", "0.0.0.0:9000", "kittygram_backend.wsgi"]