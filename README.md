# Лабораторная работа №8. Docker Compose и мониторинг (Prometheus + Grafana)

## Структура проекта
- devops8compose/ — веб-приложение на Flask со счетчиком посещений в Redis и эндпоинтом /metrics.
  - app.py — исходный код приложения.
  - dockerfile — инструкция сборки образа.
  - requirements.txt — зависимости Python.
  - compose.yaml — описание сервисов web и redis.
- devops8prom/ — стек мониторинга Prometheus, Grafana и Blackbox Exporter.
  - compose.yaml — описание сервисов мониторинга.
  - prometheus/prometheus.yml — конфигурация сбора метрик.
  - grafana/datasource.yml — автоподключение источника данных Prometheus.

## Запуск
1. Веб-приложение: cd devops8compose && docker compose up -d --build
2. Мониторинг: cd ../devops8prom && docker compose up -d
