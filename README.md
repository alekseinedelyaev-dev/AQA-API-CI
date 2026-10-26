
# Домашнее задание «1.2. Тестирование API, CI»

![Java CI with Gradle](https://github.com/alekseinedelyaev-dev/AQA-API-CI/actions/workflows/gradle.yml/badge.svg)

## Описание проекта

Домашнее задание Нетологии по автоматизированному тестированию API и настройке непрерывной интеграции (CI).

## Используемые технологии

- Java
- Gradle
- JUnit 5
- REST Assured
- JSON Schema Validator
- GitHub Actions

## Задача № 1. Настройка CI

Настроен автоматический запуск тестов через GitHub Actions.

Система запускает учебное банковское приложение `app-mbank.jar` и выполняет API-тесты.

## Задача № 2. JSON Schema

Реализована проверка ответа API на соответствие JSON-схеме.

Для поля `currency` разрешены только значения `RUB` и `USD`.

Проверена работа CI с корректной и намеренно неправильной JSON-схемой (`RUR` вместо `RUB`).

## Запуск приложения

```bash
java -jar ./artifacts/app-mbank.jar
```

## Запуск тестов

Windows:

```powershell
.\gradlew.bat clean test
```

Linux:

```bash
./gradlew clean test
```

## Результаты

При корректной JSON-схеме тесты проходят успешно.

При замене `RUB` на `RUR` проверка JSON Schema завершается ошибкой. Это подтверждено в истории GitHub Actions.
