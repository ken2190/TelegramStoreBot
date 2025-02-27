## WolframBOT

### ВНИМАНИЕ: Данный бот не рекомендуется к использованию, поскольку это мой первый проект и качество кода там оставляет желать лучшего. 

#### Telegram-бот для автопродаж

---------

Данный бот позволяет создать свой магазин в мессенджере Telegram и продавать цифровые товары.

Данный проект является у меня первым, поэтому есть огромная вероятность столкнуться с говнокодом. Тем не менее, разработка велась почти полтора месяца.

В качестве основной платёжной системы используется ****QIWI****, сам бот разработан на языке программирования ****Python**** с использованием фреймворка ****Aiogram****. База данных - ****SQLite3****. Также есть система логирования (фиксации) действий в консоли и в отдельном файле, что удобно для администрирования, есть система рассылок объявлений в личные сообщения пользователям бота.

Бот очень прост в настройке, добавление товаров, категорий, рассылка и т. п. осуществляется через внедрённую в бота админ-панель.

------

**Установка, первичная настройка и запуск**

Скачайте репозиторий:

В терминале Linux (Ubuntu, Debian): 

```apt install git && git clone https://github.com/TheWolframDev/TelegramStoreBot.git```

На Windows:

```Скачайте репозиторий ZIP-архивом, можно на главной странице или в разделе Releases. Распакуйте при необходимости в удобную директорию.```

Для запуска вам следует установить необходимые модули, с которыми работает бот.

>Предварительно убедитесь в том, что вы корректно установили Python. Для работы требуется, как минимум, Python 3.8. Проверить версию вы можете командой python --version в Windows или python3 --version в Linux

#### Если вы всё установили корректно, то скачайте модули из файла requirements.txt. Для этого вам нужно запустить файл setup.bat или запустите одну из команд в командой строке в той директории, где находится бот, в зависимости от операционной системы.

`python -m pip install -r requirements.txt`  - Windows 

`python3 -m pip install -r requirements.txt` - Linux

Если модули получилось установить, то запуск бота вы можете осуществить через файл main.py. Выполните команду в командой строке:

`python main.py` - Windows 

`python3 main.py` - Linux

Прежде чем запустить бота, вам нужно интегрировать программу с Telegram.

Для этого зайдите в Telegram, добавьте в чат @BotFather, создайте бота и скопируйте токен, откройте файл config.py в папке modules и вставьте в строчке botkey между одинарных кавычек этот токен. Далее получите токен для QIWI. Получите его здесь: `p2p.qiwi.com/api`. Получите пару ключей, но для бота следует использовать именно секретный ключ и вставьте его в строчке qiwi_token.

Если вы хотите выдать себе права администратора, то добавьте свой ID в строчке `owners_id`. Не знаете свой ID? Получите его через всё того же бота в профиле.

Первичная настройка завершена. Запустите бота так, как было описано выше. Не нравятся сообщения? Вы можете изменить их в файлах handler.py, owner.py, кнопки в keyboard.py менять не рекомендуется. Эти файлы лежат в папке modules.

Теперь давайте рассмотрим админ-панель. Команду для доступа к панели вы можете установить самостоятельно, по умолчанию это `Admin`. Сменить команду можно в файле config.py, в строчке "keyword".

Сама панель интуитивно понятна. 

>Попробуйте создать первую категорию, для неё попробуйте создать товар и настроить автовыдачу, измените себе сумму денег на счёте и попробуйте купить этот товар. Поиграйтесь с функционалом бота, думаю, вам понравится.

> Предлагайте идеи и замечания в Discussions или Issues.

