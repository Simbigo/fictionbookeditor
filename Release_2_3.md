# Важное дополнение #

В релизе 2.3 сохранились (и немного улучшены) все нововведения 2.2, но исправлены досадные ошибки и повышена производительность работы программы (практически не отличается от скорости работы "январского" релиза, независимо от показа nbsp).

Рекомендуется всем для установки вместо релиза 2.2.

# Введение #

В этом релизе FictionBook Editor-а было добавлено множество новых возможностей, и исправлено немало ошибок предыдущих релизов.

Ключевые моменты:

● исходный код программы открыт под лицензией GNU GPL v.3;

● добавлена поддержка проверки орфографии;

● добавлена поддержка inline images и stylesheets;

● добавлен новый метод добавления  inline images путем копирования и вставки. Теперь создание сложных текстов, содержащих множество таблиц и специальных символов, представленных графикой, значительно упростится;

● добавлена поддержка отображения неразрывных пробелов (nbsp);

● добавлена украинская локализация интерфейса программы;

● добавлена полная поддержка работы под Windows Vista/Windows 7;

● обновлена схема FB2 (используется последняя официальная версия 2.21);

● обновлены и расширены скрипты;

# Примечания к релизу #

_**FBE Team настоятельно рекомендует**_ деинсталлировать предыдущую версию FBE перед установкой текущего релиза. Для обеспечения совместимости работы программы под Windows Vista/Windows 7, настройки программы, изменяемые в процессе работы, сейчас сохраняются:

● для **Windows XP** - "C:\Documents and Settings\<user name>\Local Settings
\Application Data\FBE"

● для **Windows Vista/7** - "C:\Users\<user name>\Local Settings\Applicaiton
Data\FBE"

где, соответственно, вместо "C:\" может быть фактический диск, а <user name> - фактическое
имя пользователя.


Подгрузка словарей для проверки орфографии может увеличить время загрузки программы. _**FBE Team рекомендует**_ не устанавливать словари для редко (или не) используемых языков. Словари также можно удалить или добавить вручную, они расположены в директории "C:\Program Files\FictionBook Editor\Dict".


Отображение неразрывных пробелов также приводит к _небольшому_ замедлению работы программы. Это связано   с одной малоприятной особенностью рендера движка MSHTML использовать для отображения nbsp не специальный символ с кодом 0x00A0 (десятичный код 0160), а обычный пробел (0x020, 032). FBE вынужден заменять (при выбранной опции отображения nbsp иным символом, нежели пробел) неразрывные пробелы во всем HTML или XML на выбранный символ.


_Пользовательский словарь проверки орфографии_ **custom.dic** по умолчанию создается в **текущей рабочей директории** (т.е. там, где находится редактируемый документ). Для того, чтобы этот словарь был постоянным, а не создавался каждый раз на новом месте, следует указать _полный путь к файлу custom.dic_ и разместить его в директории, куда открыт доступ на чтение/запись (не в "Program files" или "Windows", для Vista/7)
Это имеет смысл: допустим, вы редактируете большую книгу с множеством редко встречающихся, но характерных только для данной книги слов. Зачем засорять пользовательский словарь? Вероятно, слова, верные для данной книги, окажутся ошибочными для другой. В этом случае можно иметь уникальный custom.dic, только для данной книги.

(Примечание FBE Team: custom.dic - это простой текстовый файл в кодировке Win-1251, совместимый с custom.dic от MS Word, и может быть просто скопирован в нужное место, либо отредактирован простым текстовым редактором, например, Notepad-ом).