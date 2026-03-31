This is a modification of a simple IRC client for the ZX Spectrum. It's been adapted for the ZX WiFi card.

Это модификация простого IRC клиента для ZX Spectrum. Адаптирован для карты ZX WiFi.
Оригинал тут:
https://github.com/nihirash/zxuno-irc

Управляющий символ '/' (shift+V), а не '!', как было
 * `/j #channel` - присоединиться (join) к каналу. Можно создать свой канал.
 * `/l` - покинуть (leave) канал
 * `/s #channel` or `!s user` - установить текущий поток или пользователя
 * `/m user - послать сообщение пользователю user

Краткий список команд ля IRC протокола:
JOIN, PART, QUIT, NICK, PRIVMSG, NOTICE, TOPIC, MODE, KICK, WHO, WHOIS, LIST, NAMES

/list список каналов
/quit отключиться
/nick задать своё имя
/list список каналов
/names список пользователей

Параметры подключения, для примера:
Сервер: irc.forestnet.org
Порт: 7000

Файлы:
irc_EE.tap - для порта #EE
IRC_EE.TRD
irc_EF.tap - то же для порта #EF
IRC_EF.TRD


Для сборки использованы:
z88dk-win32-1.99C
make-3.81

Ниже оригинальное описание:








# Simple IRC Client for ZX-Uno

This is client works only on zx-uno and compatible computers with UART-core and WiFi shield.

## Requirements

 * ZX-Uno with UART core active
 * WiFi shield attached to ZX-Uno
 * WiFi settings stored via [iwconfig](https://github.com/nihirash/iwconfig)

## Usage

Just run tap-file and application starts and in dialog mode ask all necessary data.

If you have issue with dialing to IRC-server try use [esprst](http://www.zxuno.com/forum/viewtopic.php?f=39&t=2898#p26066) tool.

After using this software you may require use esprst or power down and power up your zx-uno.

For sending IRC commands used symbol '!' but not '/'. Cause it simpler to type from rubber keyboard.

There some shortcuts:

 * `!j #channel` - will joins specified channel
 * `!l` - will leave current channel(you must switch on channel what you want leave)
 * `!s #channel` or `!s user` - will sets current talk stream to channel or user.
 * `!m user and there goes your message` sends to `user` private message

 If you need send some other command just write it after bang, example: 
 
 ```
 !KICK user
 ```

 ## Legals

Some parts of code based of SIC(simple irc client/suckless irc client).

My code is public domain. 