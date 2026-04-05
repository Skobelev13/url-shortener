# 🔗 URL Shortener (Go)

Минималистичный backend-сервис для сокращения ссылок, написанный на Go.
Проект демонстрирует архитектуру backend-приложения, работу с базой данных и обработку HTTP-запросов.

---

## 🚀 Возможности

* 🔹 Создание коротких ссылок
* 🔹 Хранение ссылок в базе данных (SQLite)
* 🔹 Уникальные alias для ссылок
* 🔹 Обработка ошибок и логирование
* 🔹 Подготовленная архитектура под масштабирование

---

## 🛠️ Технологии

* Go (Golang)
* SQLite (`database/sql`)
* slog (структурированное логирование)

---

## 📦 Архитектура проекта

```bash
cmd/url-shortener/     # точка входа
internal/
  config/              # загрузка конфигурации
  storage/sqlite/      # работа с БД
  lib/logger/          # логирование
config/                # yaml конфиги
```

Проект разделён на слои (config, storage, logger), что упрощает поддержку и расширение.

---

## ▶️ Запуск

```bash
git clone https://github.com/Skobelev13/url-shortener.git
cd url-shortener

go mod tidy
CONFIG_PATH=./config/local.yaml go run ./cmd/url-shortener
```

---

## 📌 Пример работы

```go
id, err := storage.SaveURL("https://google.com", "google")
```

---

## 🧠 Что реализовано

* работа с `database/sql`
* обработка SQL-ошибок (включая уникальные ограничения)
* использование `LastInsertId()`
* структурированное логирование

---

## 🔥 В планах

* [ ] HTTP API (chi router)
* [ ] POST /shorten
* [ ] GET /{alias} (редирект)
* [ ] статистика переходов
* [ ] Docker
* [ ] Redis (кеширование)

---

## 🎯 Цель проекта

Учебный проект для изучения backend-разработки на Go, включая:

* работу с БД
* архитектуру приложений
* обработку ошибок
* подготовку к разработке production-сервисов

---

## 👨‍💻 Автор

GitHub: https://github.com/Skobelev13
