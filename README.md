# Change Data Capture example (Debezium + StreamSets)

## Запуск

1. Выполните в консоли `docker-compose up`. В результате будут развернуты докер-контейнеры со всеми необходимыми сервисами.
2. Для запуска коннектора Debezium выполните в консоли `make register-postgres`.
3. Чтобы увидеть логи изменений в базе, выполните `make create-consumer`. Это запустит kafka consumer, который подключится к топику, содержащему логи.

## Загрузка логов CDC в Hadoop

1. Зайдите в StreamSets по адресу [localhost:18630]. Логин/пароль: admin/admin.
2. Пропустите первый преветственный экран и создайте новый пайплайн, нажав Create New Pipeline.
3. Перед вами откроется окно редактирования пайплайна. Создайте пайплайн для загрузки логов CDC в Hadoop. Для этого вам понадобятся:
    * Kafka Consumer
    * Hadoop FS
    * Остальные операторы выбирайте на свое усмотрение
  
Дополнительная информация:
* [StreamSets tutorial](https://streamsets.com/documentation/datacollector/latest/help/datacollector/UserGuide/Tutorial/BasicTutorial.html)
* [Пример StreamSets + Kafka](https://youtu.be/SiZrkyEzpJc?t=491)
* Адрес Kafka - `kafka:9092`
* Адрес zookeeper - `zookeeper:2181`
* Адрес Hadoop - `hadoop:9000`


