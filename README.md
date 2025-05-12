# Величко Дмитро ІПЗ 3.02
## Практичне заняття №1
### Проходження інтерактивного курсу «Git How To»

Пройти інтерактивний курс [Git How To](https://githowto.com/uk)

# Зміст
- [0. Підготовка](#0-Підготовка)
- [0.1. Основи Git](#01-Основи-Git)
## Частина 1
# 0. Підготовка
За посиланням завантажити матеріал для подальшої роботи
https://githowto.com/githowto.zip
Далі розпакуємо і у нас буде 2 файла

- ```repositories```: порожня директорія, в якій ви будете створювати свої репозиторії.
- ```files```: завчасно упаковані файли для того, щоб ви могли продовжити роботу з навчальними матеріалами на будь-якому етапі.
Цей файл створений у тому випадку якщо десь виникнуть проблеми.

# 0.1. Основи Git
Тут розповідається про те що таке сам Git для чого він потрібен і про основні терміни, на кшталт ```репозиторій```, ```коміт```, ```гілка```.

# 1. Фінальні приготування
Так зайшовши в термінал нам треба було встановити своє ім'я і пошту.

Далі ми встановили гілку яка у нас буде за замовчуванням.
![1](https://github.com/user-attachments/assets/9ea54e9c-15dd-4172-adbe-7a3317090892)

# 2. Створення проєкту
Так створемо файл у якому ми створемо файл hello.html
Для цього виканаємо такі команди: 

```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories
$ mkdir work
```

```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories
$ cd work
```

```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work
$ touch hello.html
```

```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work
$ nvim hello.html
```

Відкривши ```NeoVim``` ми напишемо:

```hello.html```

```1. Hello, World```

Зберігши файл виходимо.

Далі ми створимо репозиторій. Для цього виконаємо таку комунду:

```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work
$ git init
```

В результаті чого виникає таке повідомлення:

```Initialized empty Git repository in D:/all you need/Общее/учеба/Git tutor/githowto/repositories/work/.git/```

Так, тепер додамо наш файл у це репозиторій. Для цього виконаємо таку команду:

```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ git add hello.html
```

Далі додамо коміт

```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ git commit -m "Initial Comit"
```

У результаті буде:

```
[main (root-commit) 937b340] Initial Comit
 1 file changed, 1 insertion(+)
 create mode 100644 hello.html
```

![2](https://github.com/user-attachments/assets/4624e228-562e-491a-99e5-9bdd4d499982)


# 3. Перевірка стану
Перевіремо стан репозиторію виконавши команду:

```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ git status
```

У результаті з'явиться таке повідомлення:

```
On branch main
nothing to commit, working tree clean
```

![3](https://github.com/user-attachments/assets/db0a9c9f-6a48-44d3-a9af-d7470a48164b)

# 4. Внесення змін

Змінемо файл hello.html. Для цього виконаємо таку команду:

```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ nvim hello.html
```

Додамо теги:

![_3](https://github.com/user-attachments/assets/ed1452b8-eb52-4a69-a269-1746af3a9654)

Зберігши зміни перевіримо стан, для цього напишемо команду: 

```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ git status
```

У результаті буде: 

```
On branch main
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   hello.html

no changes added to commit (use "git add" and/or "git commit -a")
```

![4](https://github.com/user-attachments/assets/ad8373e6-360e-4892-9652-30d218db7ceb)


# 5. Індексація змін

Так додамо наш змінений файл, для цього виконаємо команду:

```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ git add hello.html
```

Потім перевіримо його статус, виконавши команду: 
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ git status
```

У результаті 
```
On branch main
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   hello.html
```

![5](https://github.com/user-attachments/assets/f40da849-2708-496f-8e29-f00d94847d11)

# 6. Індексація та коміт
Тут розповідається про індексацію і як можна аби файли йшли одним комітом, а інші другим комітом. Використовуючи такі команди:
```
git add a.html
git add b.html
git commit -m "Changes for a and b"
```

А потім виконати таку команду:

```
git add c.html
git commit -m "Unrelated change to c"
```

# 7. Коміт змін
Виконаємо наступну команду: 
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ git commit
```

![7 1](https://github.com/user-attachments/assets/1ea9cb92-66b4-4b63-9eae-54fbda19bb43)

У результаті буде таке: 
```
|
# Please enter the commit message for your changes. Lines starting
# with '#' will be ignored, and an empty message aborts the commit.
#
# On branch main
# Changes to be committed:
#       modified:   hello.html
#
```
Відкривши редактор ```NeoVim```, ми зробимо такі зміни:
```
Added h1 tag
# Please enter the commit message for your changes. Lines starting
# with '#' will be ignored, and an empty message aborts the commit.
#
# On branch main
# Changes to be committed:
#       modified:   hello.html
#
```
![7 vim](https://github.com/user-attachments/assets/1ac1aee8-be80-4adb-baa2-e35cdfb9c1b9)

Після збереження у нас буде наступне повідомлення:
```
[main a31cf4c] Added h1 tag
 1 file changed, 1 insertion(+), 1 deletion(-)
```

Тепер перевіримо статус:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ git status
```
У результаті:
```
On branch main
nothing to commit, working tree clean
```
![7 3](https://github.com/user-attachments/assets/e4b32225-c488-4723-bdba-00dde862c06c)

# 8. Зміни, а не файли
Так, додамо першу зміну у наш файл, для цього виконаємо команду: 
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ nvim hello.html
```
І зробимо такі заміни:

![3 1(друга зміна файлу html)](https://github.com/user-attachments/assets/65dc0969-82f3-4600-bbb2-a9c8671afdec)

Далі після збереження додамо ці зміни за допомогою команди: 
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ git add hello.html
```

Далі ще зробимо зміну файлу hello.html, виконавши наступну команду:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ nvim hello.html
```

Тепер зробимо такі зміни:

![3 2](https://github.com/user-attachments/assets/e4ccc693-3a37-4b54-86a9-3b3049f6199e)

Збережемо і перевіримо статус: 
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ git status
```

В результаті буде таке:
```
On branch main
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   hello.html

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   hello.html
```

Зробимо коміти наших змін.
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ git commit -m "Added standard HTML page tags"
```

В результаті буде таке:
```
[main 205f3f9] Added standard HTML page tags
 1 file changed, 5 insertions(+), 1 deletion(-)
```

Перевіримо ще раз статус:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ git status
```


В результаті буде таке:
```
On branch main
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   hello.html

no changes added to commit (use "git add" and/or "git commit -a")
```

Додамо другу зміну: 
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ git add .
```

Перевіримо статус:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ git status
```

В результаті буде таке:
```
On branch main
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   hello.html
```

Зробимо коміт другої зміни:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ git commit -m "Added HTML header"
```

В результаті буде:
```
[main 9b6ab77] Added HTML header
 1 file changed, 3 insertions(+)
```

![8](https://github.com/user-attachments/assets/a10007e9-6eec-461f-a74d-29d54f3b11bb)

# 9. Історія проєкту
Виконаємо команду: 

```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ git log
```

Ця команда дає нам список зроблених змін. Ось результат:
```
commit 9b6ab7710eeb16dfe8d683b312d0725dbb658ec7 (HEAD -> main)
Author: Dmytro <dima2005157@gmail.com>
Date:   Mon Mar 10 18:42:55 2025 +0200

    Added HTML header

commit 205f3f95c3bed0727150184cb3ba882fe0d86465
Author: Dmytro <dima2005157@gmail.com>
Date:   Mon Mar 10 18:40:55 2025 +0200

    Added standard HTML page tags

commit a31cf4cb45f3581757a69c79fd6350c99425e3ed
Author: Dmytro <dima2005157@gmail.com>
Date:   Mon Mar 10 18:29:56 2025 +0200

    Added h1 tag

commit 937b340b521e2191b4dac1f1fac9b46c261d24f0
Author: Dmytro <dima2005157@gmail.com>
Date:   Mon Mar 10 18:13:32 2025 +0200

    Initial Comit
```

Напишемо команду для однорядкового формату:

```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ git log --pretty=oneline
```

Результат:
```
9b6ab7710eeb16dfe8d683b312d0725dbb658ec7 (HEAD -> main) Added HTML header
205f3f95c3bed0727150184cb3ba882fe0d86465 Added standard HTML page tags
a31cf4cb45f3581757a69c79fd6350c99425e3ed Added h1 tag
937b340b521e2191b4dac1f1fac9b46c261d24f0 Initial Comit
```

Далі виконаємо команди для різних форматів відображення змін:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ git log --oneline --max-count=2
9b6ab77 (HEAD -> main) Added HTML header
205f3f9 Added standard HTML page tags
```

```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ git log --oneline --since="5 minutes ago"
```
Тут нічого)

```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ git log --oneline --until="5 minutes ago"
9b6ab77 (HEAD -> main) Added HTML header
205f3f9 Added standard HTML page tags
a31cf4c Added h1 tag
937b340 Initial Comit
```

```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ git log --oneline --author="Dmytro"
9b6ab77 (HEAD -> main) Added HTML header
205f3f9 Added standard HTML page tags
a31cf4c Added h1 tag
937b340 Initial Comit
```

```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ git log --oneline --all
9b6ab77 (HEAD -> main) Added HTML header
205f3f9 Added standard HTML page tags
a31cf4c Added h1 tag
937b340 Initial Comit
```

```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ git log --all --pretty=format:"%h %cd %s (%an)" --since="7 days ago"
9b6ab77 Mon Mar 10 18:42:55 2025 +0200 Added HTML header (Dmytro)
205f3f9 Mon Mar 10 18:40:55 2025 +0200 Added standard HTML page tags (Dmytro)
a31cf4c Mon Mar 10 18:29:56 2025 +0200 Added h1 tag (Dmytro)
937b340 Mon Mar 10 18:13:32 2025 +0200 Initial Comit (Dmytro)
```

Так ми тепер напишемо наступну команду, яка нам буде комфортна для подальшої роботи:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ git log --pretty=format:"%h %ad | %s%d [%an]" --date=short
```

Результат:
```
9b6ab77 2025-03-10 | Added HTML header (HEAD -> main) [Dmytro]
205f3f9 2025-03-10 | Added standard HTML page tags [Dmytro]
a31cf4c 2025-03-10 | Added h1 tag [Dmytro]
937b340 2025-03-10 | Initial Comit [Dmytro]
```

Тепер зробимо такий формат за замовчуванням:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ git config --global format.pretty '%h %ad | %s%d [%an]'

dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ git config --global log.date short
```

![9](https://github.com/user-attachments/assets/d43011be-e270-4250-92b0-fe9dd3412c67)

# 10. Отримання старих версій
Отримаємо хеші попередніх комітів, виконавши наступну команду:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ git log
```

Отриимаємо:
```
9b6ab77 2025-03-10 | Added HTML header (HEAD -> main) [Dmytro]
205f3f9 2025-03-10 | Added standard HTML page tags [Dmytro]
a31cf4c 2025-03-10 | Added h1 tag [Dmytro]
937b340 2025-03-10 | Initial Comit [Dmytro]
```

Тепер виконавши наступну команду, перевіримо хеш першого коміту.
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ git checkout 937b340
```
Результат:
```
Note: switching to '937b340'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

HEAD is now at 937b340 Initial Comit
```
Далі перевіримо його зміст виконавши наступну команду:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work ((937b340...))
$ cat hello.html
```

У результаті ми отримаємо:

```
Hello, world
```

Перемкнемось на останню версію гілки ```main```
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work ((937b340...))
$ git switch main
Previous HEAD position was 937b340 Initial Comit
Switched to branch 'main'
```

Тепер ще раз перевіримо зміст файлу:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ cat hello.html
<html>
  <head>
  </head>
  <body>
    <h1>Hello, world</h1>
  </body>
</html>
```
![10](https://github.com/user-attachments/assets/347d5235-400c-45e7-b46e-83eb23463e88)

# 11. Створення тегів версій
Створемо тег для першої версії:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ git tag v1
```

```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ git log
9b6ab77 2025-03-10 | Added HTML header (HEAD -> main, tag: v1) [Dmytro]
205f3f9 2025-03-10 | Added standard HTML page tags [Dmytro]
a31cf4c 2025-03-10 | Added h1 tag [Dmytro]
937b340 2025-03-10 | Initial Comit [Dmytro]
```

Тепер поточна версія називається ```v1```

Перемкнемось на іншу версію аби теж надати тег. Для цього виконаємо команду:

```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ git checkout v1^
```

У результаті буде:
```
Note: switching to 'v1^'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

HEAD is now at 205f3f9 Added standard HTML page tags
```

Тепер прочитаємо вміст цієї гілки, виконавши команду:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work ((205f3f9...))
$ cat hello.html
```
У результаті:
```
<html>
  <body>
    <h1>Hello, world</h1>
  </body>
</html>
```

Надамо йому тег ```v1-beta```.
Виконаємо наступну команду:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work ((205f3f9...))
$ git tag v1-beta
```

Тепер перевіримо, що тут було встановлено тег, виконавши наступну команду:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work ((v1-beta))
$ git log
```

Результат:
```
205f3f9 2025-03-10 | Added standard HTML page tags (HEAD, tag: v1-beta) [Dmytro]
a31cf4c 2025-03-10 | Added h1 tag [Dmytro]
937b340 2025-03-10 | Initial Comit [Dmytro]
```

Тепер перемкнемось, виконавши наступну команду:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work ((v1-beta))
$ git checkout v1
Previous HEAD position was 205f3f9 Added standard HTML page tags
HEAD is now at 9b6ab77 Added HTML header
```

```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work ((v1))
$ git checkout v1-beta
Previous HEAD position was 9b6ab77 Added HTML header
HEAD is now at 205f3f9 Added standard HTML page tags
```

Переглянемо теги, для цього виконаємо команду:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work ((v1-beta))
$ git tag
v1
v1-beta
```

Тепер так само, але у логах, виконаємо наступну команду:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work ((v1-beta))
$ git log main --all
```

Результат:
```
9b6ab77 2025-03-10 | Added HTML header (tag: v1, main) [Dmytro]
205f3f9 2025-03-10 | Added standard HTML page tags (HEAD, tag: v1-beta) [Dmytro]
a31cf4c 2025-03-10 | Added h1 tag [Dmytro]
937b340 2025-03-10 | Initial Comit [Dmytro]
```

![11](https://github.com/user-attachments/assets/d2b4a38f-3310-4333-bb30-40bcd2b30d8f)

# 12. Скасування локальних змін (до індексації)
Перемкнемось на основну гілку ```main```, виконавши наступну команду:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work ((v1-beta))
$ git switch main
Previous HEAD position was 205f3f9 Added standard HTML page tags
Switched to branch 'main'
```

Додамо небажаний коментар у наш файл ```hello.html```, виконавши наступну команду:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ nvim hello.html
```
Тепер додамо коментар:

![3 3](https://github.com/user-attachments/assets/25c74a89-49de-4cf1-89b6-ec9eefd184dd)

Перевіремо статус:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ git status
```

Результат:
```
On branch main
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   hello.html

no changes added to commit (use "git add" and/or "git commit -a")
```

Тепер скасуємо наші зміни, виконавши наступну команду:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ git restore hello.html
```

Тепер, ще раз перевіримо статус:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ git status
```

Результат:
```
On branch main
nothing to commit, working tree clean
```

Тепер прочитаємо зміст файлу:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ cat hello.html
<html>
  <head>
  </head>
  <body>
    <h1>Hello, world</h1>
  </body>
</html>
```

![12](https://github.com/user-attachments/assets/9a6e06bb-8bc0-40a7-bdca-210eeec8b1bf)

# 13. Скасування проіндексованих змін (перед комітом)
Знову внесемо наші зміни у файл.

![3 4](https://github.com/user-attachments/assets/ba7d0a97-b29d-4847-9992-58b7ae4f9237)

Тепер додамо цей файл, виконавши команду:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ git add hello.html
```

Тепер перевіримо стан, виконавши команду:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ git status
```
Результат:
```
On branch main
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   hello.html
```

Наступною командою, ми очищемо область показу:

```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ git restore --staged hello.html
```

Відновимо файл до стану останнього коміту виконавши команду:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ git restore hello.html
```

Перевіримо наш статус:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ git status
On branch main
nothing to commit, working tree clean
```

![13](https://github.com/user-attachments/assets/405cef77-8814-4253-b045-75a44a0f7da8)

# 14. Скасування комітів
Змінимо наш файл. Відкривши його у редакторі ```NeoVim```

![3 3](https://github.com/user-attachments/assets/16dd06f2-9db9-4da9-9165-2afe843b4c6e)

Виконаємо наступні команду:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ git add hello.html
```

Додамо коміт, виконавши команду:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ git commit -m "Oops, we didn't want this commit"
[main a966b56] Oops, we didn't want this commit
 1 file changed, 1 insertion(+)
```

Скасуємо наш коміт, виконавши команду:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ git revert HEAD
[main 96c756f] Revert "Oops, we didn't want this commit"
 1 file changed, 1 deletion(-)
```

Тепер перевіримо лог, виконавши наступну команду:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ git log
```

Результат: 
```
96c756f 2025-03-10 | Revert "Oops, we didn't want this commit" (HEAD -> main) [Dmytro]
a966b56 2025-03-10 | Oops, we didn't want this commit [Dmytro]
9b6ab77 2025-03-10 | Added HTML header (tag: v1) [Dmytro]
205f3f9 2025-03-10 | Added standard HTML page tags (tag: v1-beta) [Dmytro]
a31cf4c 2025-03-10 | Added h1 tag [Dmytro]
937b340 2025-03-10 | Initial Comit [Dmytro]
```

![14](https://github.com/user-attachments/assets/ed94a9d1-8f0b-4d8d-8635-50591d8c4149)

# 15. Видалення комітів з гілки (revert)
Перевіримо нашу історію комітів. Для цього виконаємо команду:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ git log
```

У результаті:
```
96c756f 2025-03-10 | Revert "Oops, we didn't want this commit" (HEAD -> main) [Dmytro]
a966b56 2025-03-10 | Oops, we didn't want this commit [Dmytro]
9b6ab77 2025-03-10 | Added HTML header (tag: v1) [Dmytro]
205f3f9 2025-03-10 | Added standard HTML page tags (tag: v1-beta) [Dmytro]
a31cf4c 2025-03-10 | Added h1 tag [Dmytro]
937b340 2025-03-10 | Initial Comit [Dmytro]
```

У нас тут два коміти ```Revert Oops```, ```Oops```. Видалимо їх. 
Але перед цим надамо їм теги, аби було простіше видалити.
Виконаємо наступну команду:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ git tag oops
```

У результаті буде:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ git log
96c756f 2025-03-10 | Revert "Oops, we didn't want this commit" (HEAD -> main, tag: oops) [Dmytro]
a966b56 2025-03-10 | Oops, we didn't want this commit [Dmytro]
9b6ab77 2025-03-10 | Added HTML header (tag: v1) [Dmytro]
205f3f9 2025-03-10 | Added standard HTML page tags (tag: v1-beta) [Dmytro]
a31cf4c 2025-03-10 | Added h1 tag [Dmytro]
937b340 2025-03-10 | Initial Comit [Dmytro]
```

Зробимо відкіт до тега ```v1```, виконавши наступну команду:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ git reset --hard v1
HEAD is now at 9b6ab77 Added HTML header
```

Тепер перевіремо:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ git log
9b6ab77 2025-03-10 | Added HTML header (HEAD -> main, tag: v1) [Dmytro]
205f3f9 2025-03-10 | Added standard HTML page tags (tag: v1-beta) [Dmytro]
a31cf4c 2025-03-10 | Added h1 tag [Dmytro]
937b340 2025-03-10 | Initial Comit [Dmytro]
```

Що ж трапляється з помилковими комітами? Виявляється, що коміти все ще знаходяться в репозиторії, ми все ще можемо на них посилатися. 

Напишемо наступну команду:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ git log --all
```

У результаті ми побачимо, що:
```
96c756f 2025-03-10 | Revert "Oops, we didn't want this commit" (tag: oops) [Dmytro]
a966b56 2025-03-10 | Oops, we didn't want this commit [Dmytro]
9b6ab77 2025-03-10 | Added HTML header (HEAD -> main, tag: v1) [Dmytro]
205f3f9 2025-03-10 | Added standard HTML page tags (tag: v1-beta) [Dmytro]
a31cf4c 2025-03-10 | Added h1 tag [Dmytro]
937b340 2025-03-10 | Initial Comit [Dmytro]
```
наші помилкові коміти нікуди не зникли, просто вони відсутні на головній гілці  ```main```.

![15](https://github.com/user-attachments/assets/da8c15a2-a7de-48d2-9342-541a286e1c44)

# 16. Видалення тегу ```oops```

Видалемо наш тег ```oops```. Виконаємо наступну команду:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ git tag -d oops
Deleted tag 'oops' (was 96c756f)
```

Тепеp перевіримо:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ git log --all
9b6ab77 2025-03-10 | Added HTML header (HEAD -> main, tag: v1) [Dmytro]
205f3f9 2025-03-10 | Added standard HTML page tags (tag: v1-beta) [Dmytro]
a31cf4c 2025-03-10 | Added h1 tag [Dmytro]
937b340 2025-03-10 | Initial Comit [Dmytro]
```

Усе наш тег більше не відображається у репозиторії.

![16](https://github.com/user-attachments/assets/1c010ac7-acda-4823-a8b5-64f8d9390341)

# 17. Внесення змін до комітів

Додамо у наш файл коментар автора, для цього відкриємо наш файл.
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ nvim hello.html
```
Замінимо:

![3 5](https://github.com/user-attachments/assets/56194256-5807-4b1b-852a-9a32ecf77c2b)

Зберігши зміни, виконаємо наступні команди:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ git add hello.html
```

Закомітимо:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ git commit -m "Added copyright statement"
[main ce0884d] Added copyright statement
 1 file changed, 1 insertion(+)
```

І переглянемо коміти:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ git log
ce0884d 2025-03-10 | Added copyright statement (HEAD -> main) [Dmytro]
9b6ab77 2025-03-10 | Added HTML header (tag: v1) [Dmytro]
205f3f9 2025-03-10 | Added standard HTML page tags (tag: v1-beta) [Dmytro]
a31cf4c 2025-03-10 | Added h1 tag [Dmytro]
937b340 2025-03-10 | Initial Comit [Dmytro]
```

Упс. Нам треба було додати пошту у наш файл, добре відкриємо наш файл.
Виконаємо команду:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ nvim hello.html
```

Зробимо такі зміни:

![3 6](https://github.com/user-attachments/assets/0643a1f8-d4f6-408a-8929-0b3bc9ae9b22)

Тепер додамо зміни, виконавши команду:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ git add hello.html
```

Робимо коміт.
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ git commit --amend -m "Added copyright statement with email"
[main c410e88] Added copyright statement with email
 Date: Mon Mar 10 20:02:54 2025 +0200
 1 file changed, 1 insertion(+)
```

Переглянемо історію:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ git log
c410e88 2025-03-10 | Added copyright statement with email (HEAD -> main) [Dmytro]
9b6ab77 2025-03-10 | Added HTML header (tag: v1) [Dmytro]
205f3f9 2025-03-10 | Added standard HTML page tags (tag: v1-beta) [Dmytro]
a31cf4c 2025-03-10 | Added h1 tag [Dmytro]
937b340 2025-03-10 | Initial Comit [Dmytro]
```

![17](https://github.com/user-attachments/assets/06a071a0-c8e8-4242-9b89-582ef961737a)

# 18. Створення гілки

Створемо нову гілку наступною командою:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ git switch -c style
Switched to a new branch 'style'
```

Тепер перевіримо статус, наступною командою:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (style)
$ git status
On branch style
nothing to commit, working tree clean
```
Побачимо що у нас тут у терміналі у душках написано ```style```, тобто ми автоматично перемикнулись на новостворену гілку.

Створемо файл ```style.css``` за допомогою команди:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (style)
$ touch style.css
```
