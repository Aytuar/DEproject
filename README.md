# DEproject
Регистрируемся на https://developer.schiphol.nl для получения app_id и app_key.
Описание всех эндпоинтов API и параметров - https://developer.schiphol.nl/documentation

Запускаем контейнеры с сервисами.
```
docker-compose up
```
После загрузки docker образов ждём примерно минуту для старта сервиса streamsets и преходим в браузере на http://127.0.0.1:16830
Загружаем архив pipelines.zip через меню.
В streamsets открываем pipeline "flight data to kafka - Arrived today" и меняем app_id и app_key в Get Schiphol API.
Тоже самое меняем и в pipeline "flight data to kafka - Departed today".

Сервис elasticsearch и kibana запускаются примерно минуты 3.
После этого можно запускать pipeline в streamsets.

Данные можно увидеть в kibana http://127.0.0.1:5601