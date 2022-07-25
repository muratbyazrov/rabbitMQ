# rabbitMQ
Как работает rabbitMQ и др. брокеры сообщений

Подтверждение (ack) отправляется подписчиком для информирования RabbitMQ о том, что полученное сообщение было обработано и RabbitMQ может его удалить.
Можно принудительно включить автоматическое подтверждение сообщений, указав no_ack=True

Сообщения, которые были прочитаны, а затем полностью обработаны сервисом должны быть подтверждены (акнуты, от слова `ack`).
Такие сообщения rabbit удаляет для экономии.

Для обработки сообщений отсутствует тайм-аут. 
RabbitMQ передаст их другому подписчику только если соединение с первым будет закрыто, 
поэтому нет никаких ограничений на время обработки сообщения. 


![image](https://user-images.githubusercontent.com/62685269/180806066-796a8697-4200-485a-9955-41a7759c40b4.png)
