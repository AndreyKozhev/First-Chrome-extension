# Первое расширение для браузера Chrome
Сегодня мы создадим расширение для браузера Chrome, которое будет выводить окно с приветствием
## Создание файлов
Нам нужно 3 файла:
+ **manifest.json**
+ **popup.html**
+ **popup.js**
## Манифест
Манифест - главный файл в нашем проекте, он содержит описание расширения.
Вот содержимое файла **manifest.json**:
```json
{
    "manifest_version": 2,

    "name": "First Chrome Extension",
    "version": "1.0",
    "browser_action": {
        "default_title": "Открыть",
        "default_popup": "popup.html"
    }
}
```
Рассмотрим его:
+ `manifest_version` - версия нашего манифеста, на данный момент актуальна версия 2.
+ `name` - имя нашего расширения
+ `version` - версия расширения
+ `browser_action` - заголовок и содержимое окна, которое откроется при нажатии на расширение
## Содержимое всплывающего окна
Данное окно - основной способ взаимодействия с пользователем.
Вот код файла **popup.html**:
```html
<!DOCTYPE html>
<html>
    <head>
        <!-- Подключение скрипта -->
        <script src="popup.js"></script>
    </head>
    <body>
        <!-- Заголовок -->
        <h1>My first extension</h1>
    </body>
</html>
```
Здесь мы подключаем файл JS, выводим надпись **"My first extension"** в главное окно расширения
## Код на JavaScript
В файле **popup.js**, который отвечает за логику взаимодействия, только одна строка, которая выводит сообщение **"Hello World!"**:
```js
//Вывод окна с сообщением
alert("Hello World!");
```
## Запуск нашего расширения
+ Заходим на страницу ```chrome://extensions``` в браузере **Chrome**
+ Включаем режим разработчика
+ Нажимаем "Загрузить распакованное расширение", выбираем папку с нашим кодом
+ На панели инструментов нажимаем кнопку "Расширения" с изображением пазла, находим там наше расширение, кликаем на него левой кнопкой мыши.
В итоге у вас откроется окно. Нажмите в нём кнопку ОК. У вас откроется главное окно расширения.
