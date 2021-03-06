# **Инструкция по работе с системой контроля версий Git**

Git — абсолютный лидер по популярности среди современных систем управления версиями. Применяется для управления версиями в рамках колоссального количества проектов по разработке ПО, как коммерческих, так и с открытым исходным кодом. В Git каждая рабочая копия кода сама по себе является репозиторием. Это позволяет всем разработчикам хранить историю изменений в полном объеме.

## Инициализация репозитория
### Что такое репозиторий
Это каталог в файловой системе, где хранится информация о проекте:
1. файлы и папки проекта;
2. история проекта;
3. настройки проекта;
4. служебная информация.

Для инициализации репозитория нужно выполнить команды: 
```
$ git init
$ git add
$ git commit -m "Initial commit"
```
И можно приступать к работе над проектом.

## Проверка состояния репозитория
Команда `git status` отображает состояние рабочего каталога и раздела проиндексированных файлов. С ее помощью можно проверить индексацию изменений и увидеть файлы, которые не отслеживаются *Git*.
## Отслеживание новых файлов
Для того чтобы начать отслеживать (добавить под версионный контроль) новый файл, используется команда `git add` "имя файла". 

Если вы снова выполните команду `status`, то увидите, что файл теперь отслеживаемый и добавлен в индекс.
## Сохранение изменений
Теперь, когда файл находится в нужном состоянии, можно зафиксировать изменения. 
Простейший способ зафиксировать изменения — это набрать `git commit`. При этом можно набрать свой комментарий к коммиту в командной строке вместе с командой `commit` указав его после параметра -m.

*Нужно запомнить, что любые файлы, созданные или изменённые, и для которых не был выполнен git add после редактирования — не войдут в этот коммит.*

## История изменений 
После создания нескольких коммитов понадобится возможность посмотреть их историю. Одним из основных и наиболее мощных инструментов для этого является команда `git log`.

## Переключение между сохранениями
Для переключения на нужный коммит используется действие `checkout`. После переключения, все файлы в проекте станут такими, какими они были в данном коммите.

## Сравнение версий 
Для вывода изменений в файлах по сравнению с последним коммитом, используется `git diff` без параметров. Команда выводит изменения в файлах, которые еще не были добавлены в индекс. Сравнение происходит с последним коммитом.