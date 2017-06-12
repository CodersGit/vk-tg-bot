## Что это, и зачем оно нужно
#### Это бот, который:
1. Отправляет вам все ваши входящие сообщения из vk.com.
1. Даёт вам возможность ответить любому пользователю.
1. Позволяет посмотреть список друзей, а так же посмотреть онлайн ли сейчас конкретный человек.

Нужно это если вы уже давно выбрали Telegram как свой основной мессенджер, но у вас еще остались пара друзей/знакомых которые пишут вам в VK, или же вы просто с Украины (как я), и у вас нет доступа к Вконтакте без всяких неудобных VPN, а вам нужно что-то написать, или просто ответить.

## Установка
Для начала вам нужен сам бот в телеграме, а точнее **\<token\>** бота. Надеюсь вы уже знаете где и как его получить :)
Если у вас есть **\<token\>** бота, тогда идите в ВК, и возьмите **access_token** с правами **"offline,messages,video,photos"**

У вас есть 2 токена? хорошо, скачивайте бота:
```
git clone https://github.com/Seniv/vk-tg-bot.git
```
Загрузите модули:
```
npm install
```
Почти готово!
Далее откройте файл **tkbot.js**, и измените 3 строчки конфигурации:

```js
const VK_TOKEN = 'ВАШ ВК ТОКЕН';
const BOT = 'ВАШ ТОКЕН БОТА';
const USER = *ID пользователя телеграм*;
```

#### Прошу заметить, бот не будет реагировать если ему напишет кто-то, у кого ID не такой как указан в конфигурации!

## Как управлять?
Для начала можете отправить боту команду **"/start"**, чтобы бот создал клавиатуру с основными командами, но это не обязательно.

#### Команды, которые понимает бот:
1. Вышеупомянутый **"/start"**
1. **"/friends"** - Посмотреть список друзей. Ответ вы получите в виде **"Имя Фамилия (*команда для быстрой смены получателя*) *онлайн-статус друга*"**
1. **"/online"** - Посмотреть онлайн-статус текущего получателя

Для того чтобы написать что-то кому-то из ВК, сначала вам нужно выбрать получателя.
Выбрать получателя очень просто - напишите боту слэш(/), а после него - ID получателя (ID пользователя VK). 

Должно получится что то в этом роде: (в примере использован мой айди)
```
/98117105
```
После чего бот сообщит вам что получатель изменён, и напишет имя и фамилию нового получателя, а вы сможете отправлять сообщения этому человеку просто написав боту.

## Возможности
Вы можете отправить боту фото, он загрузит его в ВК и отправит получателю.

Так же бот разбирает основные вложения (фотографии, видео, записи на стене), остальные вложения бот не будет разбирать, и просто отправит вам тип вложения (gift, audio и т.д.).

## От автора
Знаю что бот написан не идеально, но это работает!

Нашли баги?[пишите сюда](https://github.com/Seniv/vk-tg-bot/issues/new)
