# kafka-test-L0

Задание
Необходимо разработать демонстрационный сервис с простейшим интерфейсом, отображающий данные о заказе. Модель данных можно найти в конца задания.

Что нужно сделать:

Развернуть локально PostgreSQL

Создать свою БД

Настроить своего пользователя

Создать таблицы для хранения полученных данных

Разработать сервис

Реализовать подключение к брокерам и подписку на топик orders в Kafka

Полученные данные записывать в БД

Реализовать кэширование полученных данных в сервисе (сохранять in memory)

В случае прекращения работы сервиса необходимо восстанавливать кэш из БД

Запустить http-сервер и выдавать данные по id из кэша

Разработать простейший интерфейс отображения полученных данных по id заказа

Советы
Данные статичны, исходя из этого подумайте насчет модели хранения в кэше и в PostgreSQL. Модель в файле model.json

Подумайте как избежать проблем, связанных с тем, что в канал могут закинуть что-угодно

Чтобы проверить работает ли подписка онлайн, сделайте себе отдельный скрипт, для публикации данных в топик

Подумайте как не терять данные в случае ошибок или проблем с сервисом

Apache Kafka разверните локально

Удобно разворачивать сервисы для тестирования можно через docker-compose

Для просмотра сообщений в Apache Kafka можно пользоваться Redpanda Console

Бонус-задание
Покройте сервис автотестами — будет плюсик вам в карму

Устройте вашему сервису стресс-тест: выясните на что он способен

Логи в JSON-формате делают их более удобными для машинной обработки

Воспользуйтесь утилитами WRK и Vegeta, попробуйте оптимизировать код.
