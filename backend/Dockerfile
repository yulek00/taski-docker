FROM python:3.10

WORKDIR /app

# Установка системной зависимости — Gunicorn
RUN pip install gunicorn==20.1.0

# Копирование и установка зависимостей приложения
COPY requirements.txt .
RUN pip install -r requirements.txt --no-cache-dir

# Копирование исходного кода
COPY . .

# Запуск приложения через Gunicorn
CMD ["gunicorn", "--bind", "0.0.0.0:8000", "backend.wsgi"]