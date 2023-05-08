В клонированном репозитории:
1.	Найдите полный хеш и комментарий коммита, хеш которого начинается на aefea.

Хэш: aefead2207ef7e2aa5dc81a34aedf0cad4c32545

Комментарий: Update CHANGELOG.md

2.	Ответьте на вопросы.
* Какому тегу соответствует коммит 85024d3?

Тэг: v0.12.23

* Сколько родителей у коммита b8d720? Напишите их хеши.

Два родителя: 56cd7859e05c36c06b56d013b55a252d0bb7e158 и 9ea88f22fc6269854151c571162c5bcf958bee2b

*	Перечислите хеши и комментарии всех коммитов, которые были сделаны между тегами v0.12.23 и v0.12.24.

b14b74c493 [Website] vmc provider links

3f235065b9 Update CHANGELOG.md

6ae64e247b registry: Fix panic when server is unreachable

5c619ca1ba website: Remove links to the getting started guide's old location

06275647e2 Update CHANGELOG.md

d5f9411f51 command: Fix bug when using terraform login on Windows

4b6d06cc5d Update CHANGELOG.md

dd01a35078 Update CHANGELOG.md

225466bc3e Cleanup after v0.12.23 release

Сделано командой git log  v0.12.24 --oneline -20 (параметр количество строк в выводе постепенно увеличивался до тех пор пока в выводе не появился тэг v0.12.23)

*	Найдите коммит, в котором была создана функция func providerSource, её определение в коде выглядит так: func providerSource(...) (вместо троеточия перечислены аргументы).

Сначала при помощи команды grep находим файлы, где используется указанная функция. Это provider_source.go
Затем при помощи команды git log -L :"func providerSource":provider_source.go находим коммит, в котором эта функция была создана:

8c928e83589d90a031f811fae52a81be7153e82f

*	Найдите все коммиты, в которых была изменена функция globalPluginDirs.

Сначала при помощи команды grep находим файлы, где используется указанная функция. Это commands.go и plugins.go. Затем при помощи команды git log -L :globalPluginDirs:commands.go (git log -L :globalPluginDirs:plugins.go) видим, что соответствий в файле commands.go не найдено, а изменения функции были только в файле plugins.go Изменения функции были в коммитах:

66ebff90cdfaa6938f26f908c7ebad8d547fea17

 41ab0aef7a0fe030e84018973a64135b11abcd70
 
 52dbf94834cb970b510f2fba853a5b49ad9b1a46
 
 78b12205587fe839f10d946ea3fdc06719decb05
 
*	Кто автор функции synchronizedWriters?

Команда git log -S"func synchronizedWriters" выдает несколько коммитов. Находим самый первый по дате. Автор: Martin Atkins <mart@degeneration.co.uk>
