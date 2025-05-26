# Homework_Lab2
<details>
<summary>Part I</summary>

1. Создайте пустой репозиторий на сервисе github.com (или gitlab.com, или bitbucket.com).  
[Ссылка на репозиторий](https://github.com/Kiril207/lab02)
2. Выполните инструкцию по созданию первого коммита на странице репозитория, созданного на предыдещем шаге.
3. Создайте файл ```hello_world.cpp``` в локальной копии репозитория (который должен был появиться на шаге 2). Реализуйте программу **Hello world** на языке C++ используя плохой стиль кода. Например, после заголовочных файлов вставьте строку ```using namespace std;```.
```sh
vim hello_world.cpp
```
Откроется редактор файлов, в котором будет написана нужная программа.
4. Добавьте этот файл в локальную копию репозитория.
```git add .```
5. Закоммитьте изменения с осмысленным сообщением.
```git commit -m "add hello_world"```

```
[main 14750bf] add hello world
 1 file changed, 7 insertions(+)
 create mode 100644 hello_world.cpp
```

```
git init

подсказка: Using 'master' as the name for the initial branch. This default branch name
подсказка: is subject to change. To configure the initial branch name to use in all
подсказка: of your new repositories, which will suppress this warning, call:
подсказка: 
подсказка: 	git config --global init.defaultBranch <name>
подсказка: 
подсказка: Names commonly chosen instead of 'master' are 'main', 'trunk' and
подсказка: 'development'. The just-created branch can be renamed via this command:
подсказка: 
подсказка: 	git branch -m <name>
Инициализирован пустой репозиторий Git в /home/Kiril207/workspace/projects/HW02/.git/
git branch -M main
```sh
git remote add origin https://github.com/Kiril207/lab02.git
git push origin main
Перечисление объектов: 3, готово.
Подсчет объектов: 100% (3/3), готово.
При сжатии изменений используется до 5 потоков
Сжатие объектов: 100% (2/2), готово.
Запись объектов: 100% (3/3), 329 байтов | 329.00 КиБ/с, готово.
Всего 3 (изменений 0), повторно использовано 0 (изменений 0), повторно использовано пакетов 0
To https://github.com/Kiril207/lab02.git
 * [new branch]      main -> main

```

6. Изменитьте исходный код так, чтобы программа через стандартный поток ввода запрашивалось имя пользователя. А в стандартный поток вывода печаталось сообщение ```Hello world from @name```, где ```@name``` имя пользователя.\```

7. Закоммитьте новую версию программы. Почему не надо добавлять файл повторно git add?

```git commit -am "change programm"
```


8. Запуште изменения в удалёный репозиторий.\

```
git push origin main
```

9. Проверьте, что история коммитов доступна в удалёный репозитории.\
![Коммиты](https://github.com/Kiril207/lab02/commits)

<summary>Part II</summary>

1. В локальной копии репозитория создайте локальную ветку ```patch1```.\
```git checkout -b patch1
```

2. Внесите изменения в ветке ```patch1``` по исправлению кода и избавления от ```using namespace std;```.\
Изменим файл также через vim.
3. **commit, push** локальную ветку в удалённый репозиторий.
```sh
git commit -am "fix"

git push origin patch1
```
4. Проверьте, что ветка `patch1` доступна в удалёный репозитории.
5. Создайте pull-request `patch1 -> master`.


Для этого на самой странице репозитория надо нажать кнопку `Compare && pull request` .


6. В локальной копии в ветке `patch1` добавьте в исходный код комментарии.

Всё также через vim добавим комментарии.

7. **commit, push**.
8. Проверьте, что новые изменения есть в созданном на **шаге 5** pull-request.\

[Pull-requests](https://github.com/Kiril207/lab02/pulls?q=is%3Apr+is%3Aclosed)

9. В удалённый репозитории выполните слияние PR `patch1 -> master` и удалите ветку `patch1` в удаленном репозитории.\

Это всё делает в интерфейсе GitHub.
```
git checkout main
Переключились на ветку «main»

```

10. Локально выполните **pull**.\

`git pull` - получим все изменения

11. С помощью команды **git log** просмотрите историю в локальной версии ветки ```master```.

```sh
commit 1ce3b917ef4611070ede628b64c7e34e030c934d (HEAD -> main, origin/main)
Merge: 7c05554 8009275
Author: Kiril207 <kirya.sherstyuk.05@mail.ru>
Date:   Mon May 26 19:09:23 2025 +0300

    Merge pull request #1 from Kiril207/patch1
    
    fix

commit 8009275303a2921e384689ea638e00244e69c17f
Author: Guppo207 <kirill.sherstyuk06@mail.ru>
Date:   Mon May 26 16:08:15 2025 +0000

    add comments

commit 0752289db760d989764a0b5074603bb687403fa8
Author: Guppo207 <kirill.sherstyuk06@mail.ru>
Date:   Mon May 26 16:04:02 2025 +0000

    fix

commit 7c05554ed4f825b5a9a4d5430e8da038a7f0f285
Author: Guppo207 <kirill.sherstyuk06@mail.ru>
Date:   Mon May 26 15:59:58 2025 +0000

    change programm

commit 14750bf2cf8dd5d0e6181eaf9becdb6985e566f1
Author: Guppo207 <kirill.sherstyuk06@mail.ru>
Date:   Mon May 26 15:50:43 2025 +0000

    add hello world

commit de63cc2f50d11fb96bc82bbc7a3abe0c82dbab72
Author: Guppo207 <kirill.sherstyuk06@mail.ru>
Date:   Mon May 26 15:46:38 2025 +0000

    Initial commit
```

12. Удалите локальную ветку `patch1`.\
`git branch -d patch1` - удаляем локально ветку `patch1`\
`git fetch --prune` - удаляем информацию об удалённой ветке
</details>
<details>
<summary>Part III</summary>

1. Создайте новую локальную ветку `patch2`.

```sh
git branch patch2 // Содание новой ветки
git checkout patch2 // Переход в новую ветку
```

2. Измените code style с помощью утилиты clang-format. Например, используя опцию ```-style=Mozilla```.\
```clang-format -style=Mozilla -i hello_world.cpp``` - изменили формат
3. **commit, push**, создайте pull-request ```patch2 -> master```.
```sh
git commit -am "change style"
git push --set-upstream origin patch2
```
pull-request так же содаётся через сайт Git-Hub\
4. В ветке master в удаленном репозитории измените комментарии, например, расставьте знаки препинания, переведите комментарии на другой язык.\
Выполняется через сайт, скрины излишни, выполнение пункта можно посмотреть в истории commit'ов репозитория.\
5. Убедитесь, что в pull-request появились конфликтны.
![конфликт версий](./conflict.png)
6. Для этого локально выполните **pull + rebase** (точную последовательность команд, следует узнать самостоятельно). **Исправьте конфликты.**
```sh
git pull --rebase origin main
vim hello_world.cpp // Исправляем конфликт в файле
git add hello_world.cpp // Зафиксируем изменения 
git rebase --continue // Продолжим исправление конфликтов
```
7. Сделайте force push в ветку ```patch2```
```sh
git push origin patch2 --force-with-lease
```
8. Убедитеcь, что в pull-request пропали конфликтны.
9. Вмержите pull-request `patch2 -> master`.
Делается через сайт, шаги показаны в Part II.
