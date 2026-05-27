# Привет, я Варвара 👋

Backend-разработчик с 3+ годами коммерческого опыта в Python backend и опытом разработки production-компонентов на Go.

Сейчас фокусируюсь на Go backend-разработке: REST API, PostgreSQL, Redis, RabbitMQ, Docker, Linux, асинхронная обработка данных и сервисная архитектура.

## Основной стек

**Языки:** Go, Python, SQL  
**Backend:** REST API, net/http, chi, FastAPI, Flask  
**Базы данных:** PostgreSQL, ClickHouse, Redis  
**Брокеры сообщений:** RabbitMQ, Kafka  
**Инфраструктура:** Docker, Docker Compose, Linux, Git  
**Дополнительно:** SQL-миграции, structured logging, testing, TCP/IP, context, goroutines, channels

## Коммерческий опыт

- Разработка backend-сервисов и интеграций на Python.
- Работа с PostgreSQL, ClickHouse, RabbitMQ, Docker и Linux.
- Разработка Go-компонента для мониторинга IoT-устройств.
- Реализация TCP-взаимодействия, парсинга ответов устройств, retry/cache/error handling.
- Настройка тестовой инфраструктуры с QEMU VM и mock-сервером.

## Go-проекты

### Fleet Events API

Backend-сервис на Go для приёма, хранения и асинхронной обработки telemetry events от транспортных IoT/GPS-устройств.

**Стек:** Go, chi/net/http, PostgreSQL, pgx, Redis, RabbitMQ, Docker Compose, golang-migrate, slog, goroutines, channels, context.

Что реализовано:

- REST API для управления автопарками, транспортом и устройствами;
- приём telemetry events через HTTP API;
- хранение событий в PostgreSQL;
- хранение последнего состояния транспорта в Redis;
- публикация `event.created` сообщений в RabbitMQ;
- отдельный Go worker для асинхронной обработки событий;
- worker pool на goroutines/channels;
- генерация alerts по правилам;
- graceful shutdown для API и worker;
- миграции, логирование, Docker Compose и тесты.

Репозиторий: [fleet-events-api](https://github.com/VarvaraKurakova/fleet-events-api)

---

### Subscription Aggregator API

REST API на Go для управления онлайн-подписками пользователей и расчёта суммарной стоимости подписок за выбранный период.

**Стек:** Go, chi/net/http, PostgreSQL, pgx, Docker Compose, SQL migrations, Swagger/OpenAPI, slog, REST API, UUID.

Что реализовано:

- CRUD API для управления подписками;
- хранение подписок в PostgreSQL;
- SQL-миграции, индексы и constraints;
- расчёт суммарной стоимости подписок за период;
- фильтрация по `user_id` и `service_name`;
- бизнес-логика пересечения периодов подписки и запрошенного интервала;
- слоистая структура `handler/service/repository`;
- разделение DTO и domain-моделей;
- конфигурация через `.env`;
- Swagger/OpenAPI-документация;
- Docker Compose и README с примерами запросов.

Репозиторий: [subscription-aggregator-api](https://github.com/VarvaraKurakova/subscription-aggregator-api)

## Сейчас изучаю и закрепляю

- Go backend development
- Проектирование REST API
- PostgreSQL и SQL-миграции
- Redis caching
- RabbitMQ и асинхронная обработка событий
- Worker pool на goroutines/channels
- Тестирование backend-сервисов
- Dockerized local development

## Контакты

- Telegram: [@kurakova_v](https://t.me/kurakova_v)
- Email: v-kurakova@mail.ru
