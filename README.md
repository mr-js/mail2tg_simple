# mail2tg_simple
 Get all your mail in Telegram

 Пересылка почты в телеграм

 ## Демонстрация

 ### Вход

 ![mail2tg_simple](/images/1.png)

 ### Выход
 
 ![mail2tg_simple](/images/2.png)

 ## Установка

 Создать файл ```mail2tg_simple.cfg```, в котором прописать реквизиты и настройки:

 ```ini
 [TG]
 AUTH_TOKEN = YOUR_TELEGRAM_AUTH_TOKEN
 CHAT_ID = YOUR_TELEGRAM_CHAT_ID
 
 [IMAP]
 SERVER = YOUR_IMAP_SERVER
 USER = YOUR_IMAP_USER
 PASSWORD = YOUR_IMAP_PASSWORD
 
 [SETTINGS]
 CHECK_INTERVAL = 60
 MSG_MAX = 4096
 ```

 > ```CHECK_INTERVAL``` -- интервал проверки почтового ящика в секундах, MSG_MAX -- максимальный размер сообщения в ТГ (не рекомендуется менять)

 > ```AUTH_TOKEN``` и ```CHAT_ID``` -- токен бота и идентификатор чата бота (перед использованием надо обязаетльно написать боту в указанный чат ```CHAT_ID``` любое сообщение)

  ## Запуск

  Просто запустить ```mail2tg_simple.py```

  > При каждой успешной проверке в консоли будет отображаться ```checked```, а при обнаружении и отправки нового письма -- ```sended```.

  > Если объем письма превысит лимит сообщения ТГ ```MSG_MAX```, то оно будет разделено и отправлено в нескольких сообщениях ТГ