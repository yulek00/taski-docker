# Базовый образ
FROM node:18

# Рабочая директория в контейнере
WORKDIR /app

# Копируем файлы зависимостей
COPY package.json package-lock.json ./

# Устанавливаем зависимости
RUN npm install

# Копируем исходный код приложения
COPY . .

# Сборка приложения
RUN npm run build

# Команда запуска встроенного сервера разработки
CMD ["npm", "run", "start"]