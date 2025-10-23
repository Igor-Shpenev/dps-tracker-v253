# 🚗 DPS Tracker v253

## Система мониторинга ДПС и дорожных ситуаций в реальном времени

[![Version](https://img.shields.io/badge/version-253-blue.svg)](https://github.com/Igor-Shpenev/dps-tracker-v253)
[![Status](https://img.shields.io/badge/status-production-green.svg)](https://github.com)
[![Database](https://img.shields.io/badge/database-MySQL-orange.svg)](https://github.com)
[![Node](https://img.shields.io/badge/node-%3E%3D18-brightgreen.svg)](https://github.com)

---

## 📥 Скачивание

**Готовый архив для развертывания доступен в разделе [Releases](https://github.com/Igor-Shpenev/dps-tracker-v253/releases/tag/v253)**

```bash
# Скачайте архив из релиза v253
wget https://github.com/Igor-Shpenev/dps-tracker-v253/releases/download/v253/dps-tracker-v253.tar.gz

# Распакуйте
tar -xzf dps-tracker-v253.tar.gz
cd dps-tracker-v253

# Установите (НЕ от root!)
sudo -u dps_user bash install-v253.sh
```

---

## 📋 О проекте

DPS Tracker - это веб-приложение для отслеживания позиций ДПС, дорожных камер, аварий и других важных объектов на дорогах в реальном времени.

### ✨ Основные возможности

- 🗺️ Интерактивная карта с метками
- 👮 Отслеживание позиций ДПС
- 🚗 Отметки аварий и препятствий
- 📹 Камеры наблюдения
- 🤖 Telegram бот для уведомлений
- 👥 Система пользователей и рейтингов
- 🏆 Достижения и геймификация
- 📊 Статистика по городам
- 🔔 Push-уведомления
- 🌍 Мультиязычность (RU/EN)

---

## ⚙️ Технологический стек

### Frontend
- **Next.js 15** - React фреймворк
- **React 18** - UI библиотека
- **TypeScript** - Типизация
- **Tailwind CSS** - Стилизация
- **MapLibre GL** - Интерактивные карты
- **shadcn/ui** - UI компоненты

### Backend
- **Next.js API Routes** - REST API
- **Prisma** - ORM для работы с БД
- **MySQL** - База данных
- **JWT** - Аутентификация

### Infrastructure
- **PM2** - Process manager
- **Node.js 18+** - Runtime
- **SSE** - Server-Sent Events для real-time обновлений
- **Telegram Bot API** - Интеграция с Telegram

---

## 📊 Системные требования

| Компонент | Требование |
|-----------|------------|
| **Node.js** | ≥ 18.0.0 |
| **MySQL** | ≥ 5.7 или 8.0+ |
| **RAM** | ≥ 1GB |
| **Диск** | ≥ 2GB |
| **PM2** | Latest |
| **OS** | Linux (Ubuntu/Debian) |

---

## 🚀 Быстрая установка

### 1️⃣ Скачайте релиз

Перейдите в раздел [Releases](https://github.com/Igor-Shpenev/dps-tracker-v253/releases/tag/v253) и скачайте `dps-tracker-v253.tar.gz`

### 2️⃣ Распакуйте

```bash
tar -xzf dps-tracker-v253.tar.gz
cd dps-tracker-v253
```

### 3️⃣ Установите

```bash
# ВАЖНО: НЕ от root!
sudo -u dps_user bash install-v253.sh
```

### 4️⃣ Проверьте

```bash
bash diagnose-v253.sh
```

---

## 📖 Документация

Вся документация находится внутри архива:

- **README-v253.md** - Общая информация
- **УСТАНОВКА-v253.md** - Полная инструкция установки
- **БЫСТРЫЙ-СТАРТ-v253.md** - Краткая инструкция (1 страница)
- **СКАЧАТЬ-v253.md** - Инструкция по скачиванию

---

## 🛠️ Что делает install-v253.sh?

Автоматический установщик выполняет:

1. ✅ Останавливает процессы на порту 10000
2. ✅ Очищает базу данных MySQL
3. ✅ Устанавливает зависимости (npm install)
4. ✅ Применяет миграции БД
5. ✅ Инициализирует базовые данные
6. ✅ Настраивает Telegram webhook
7. ✅ Запускает приложение через PM2

---

## 🔍 Диагностика

```bash
# Полная автоматическая диагностика
bash diagnose-v253.sh

# Ручная проверка
pm2 status
pm2 logs dps-tracker
curl http://localhost:10000/api/health
```

---

## 📈 Что нового в v253

### ✅ Исправлено

1. **Импорты** - Все относительные (без @/ алиасов)
2. **Зависимости** - npm install --production в install.sh
3. **Production сборка** - .next папка включена в архив
4. **База данных** - Полная очистка MySQL перед инициализацией
5. **Скрипт диагностики** - Полная проверка системы на русском
6. **Права доступа** - Корректная работа без root
7. **Порт 10000** - Автоматическая очистка при установке
8. **WebSocket** - Убран (используется только SSE)
9. **Webhook** - Правильная настройка Telegram webhook

### 🆕 Добавлено

- Автоматический скрипт установки `install-v253.sh`
- Скрипт полной диагностики `diagnose-v253.sh`
- Подробная документация на русском
- Проверка всех компонентов перед запуском

---

## ⚠️ Важные примечания

1. **НЕ запускайте от root!** Используйте `sudo -u dps_user`
2. **База данных MySQL** - будет полностью очищена при установке
3. **Порт 10000** - будет освобождён автоматически
4. **WebSocket НЕ используется** - только SSE для real-time
5. **Production сборка** - уже включена в архив

---

## 🌐 После установки

- **Сайт:** https://dpstracker.ru
- **API Health:** https://dpstracker.ru/api/health  
- **Telegram Bot:** @YourDPSBot

---

## 📄 Лицензия

Proprietary - DPS Tracker v253

---

**Версия:** v253  
**Дата:** Октябрь 2025  
**Статус:** ✅ Production Ready