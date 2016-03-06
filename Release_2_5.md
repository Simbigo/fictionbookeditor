Рекомендуется для установки вместо релиза 2.4

# Введение #

В этом релизе FBE исправлена "хитрая" ошибка, возникшая из-за добавления настройки тулбаров команд и скриптов, а также сделаны дополнительные значимые улучшения функциональности.


Список изменений:

● Устранена ошибка "не запуска" FBE (вероятность около 99%, но 100% гарантировать невозможно, ошибка плохо отлавливаемая).

● Значительно ускорен редактор исходного текста fb2 (режим SOURCE) Scintilla.

● Для режимов BODY и SOURCE заменен "движок" регулярных выражений на мощный PCRE (Perl Compatible Regular Expressions). В скриптах пока остался старый VBScript-овый "движок" регэкспов. Среди плюсов PCRE, к примеру, - поддержка конструкций (?<= ... ) и (?<! ... ) и "жадных" регэкспов. Регэксп \b (граница слова), однако, по-прежнему не работает для русских букв. В режиме Source, как и в режиме Body, поиск по регэкспам происходит в пределах каждой отдельной строки, а не по всему документу сразу.

● Добавлен код проверки обновления приложения (через диалог "About").

● Диалог "About" ("О программе") получил красивый динамический 3D логотип (OpenGL based). Кликните мышью два раза на вращающейся "колючке" (так ее называет создатель, профессиональный дизайнер Владимир Прохоренков, "The eBook", владелец и администратор популярнейшего сайта об электронном чтении).

● Незапланированная, но, несомненно, давно ожидаемая многими "фича". Теперь FBE умеет открывать "неправильно построенные" (т.е. имеющие нарушение или нарушения правил xml-синтаксиса) fb2 (а точнее, неправильно построенные XML) документы. FBE открывает их, естественно, в режиме SOURCE, но, после исправления, можно перейти в режим BODY и продолжить редактирование в режиме WYSIWYG.

● Теперь неразрывные пробелы отображаются выбранным символом не только в body, но и в history и annotation.

● Исправлен алгоритм группы скриптов "Разметка подзаголовков, чистка пустых строк". Теперь, по идее, более правильно должно определяться, когда не следует удалять пустую строку для сохранения валидности.

● Теперь скрипт "Расстановка только елочек" не выдает ошибку, если кавычка получается ни левой, ни правой, просто оставляет ее прямой: ". Так что расстановка елочек теперь выполняется всегда до конца документа, чем можно воспользоваться, если некогда или неохота расставлять кавычки нескольких уровней.

● Скрипты, расставляющие елочки и лапки, теперь не проверяют, чтобы все кавычки, открытые в одной stanza, в ней же были и закрыты.

● Скрипты, расставляющие елочки и лапки, теперь не выделяют текст, который им нужно обработать, благодаря чему должно быть некоторое ускорение их работы.

● Надпись "Острый комбинированный акцент" в "Настройки -> Клавиши -> Символы" заменена на "Стандартное комбинирующееся ударение".

● Combining-символы в "Настройки -> Клавиши -> Символы" теперь видны.

● Исправлена ошибка в проверке орфографии.