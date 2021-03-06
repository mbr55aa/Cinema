## Требования

- Используйте предложенную [cхему индекса](https://code.s3.yandex.net/middle-python/learning-materials/es_schema.txt){target="_blank"}💾  `movies`, в которую должна производиться загрузка фильмов.
- Ваш код должен корректно вести себя при потере связи с ES или Postgres. Используйте технику backoff, чтобы ваш сервис не мешал восстановлению БД.
- При перезапуске приложения оно должно продолжить работу с места остановки, а не начинать процесс заново. Здесь вам поможет хранение состояния.
- ES с загруженными данными успешно проходит [Postman-тесты](https://code.s3.yandex.net/middle-python/learning-materials/ETLTests.json){target="_blank"}💾.

**Если придумали свой вариант архитектуры, то необходимо вначале показать её наставнику.**

И ещё несколько советов:

- валидируйте конфигурации с помощью `pydantic`;
- избегайте дублирования кода и SQL-запросов;
- используйте аннотации типов;
- документируйте функции, используя комментарии;
- для логирования используйте модуль `logging` из стандартной библиотеки Python;
- соблюдайте `PEP8`.

**Решение задачи залейте в папку `postgres_to_es` вашего репозитория.**

## Вам пригодится

- освежить в памяти базовые элементы SQL-запросов: `SELECT` и `JOIN`;
- локально поднять сервер Elasticsearch, используя Docker;
- определиться с архитектурой скрипта. Очень помогает нарисовать её на листочке и разбить на основные элементы. Подсказка: такими элементами могут быть загрузка данных из Postgres, преобразование каждой строки фильма в удобный для загрузки формат и подготовка данных для загрузки в Elasticsearch.

Желаем вам удачи в написании ETL! Вы обязательно справитесь 💪

**Решение задачи залейте в папку `postgres_to_es` вашего репозитория.**
