# Величко Дмитро ІПЗ 3.02
## Практичне заняття №1
### Проходження інтерактивного курсу «Git How To»

Пройти інтерактивний курс [Git How To](https://githowto.com/uk)

# Зміст
# Частина 1
- [0. Підготовка](#0-Підготовка)
- [0.1. Основи Git](#01-Основи-Git)
- [1. Фінальні приготування](#1-Фінальні-приготування)
- [2. Створення проєкту](#2-Створення-проєкту)
- [3. Перевірка стану](#3-Перевірка-стану)
- [4. Внесення змін](#4-Внесення-змін)
- [5. Індексація змін](#5-Індексація-змін)
- [6. Індексація та коміт](#6-Індексація-та-коміт)
- [7. Коміт змін](#7-Коміт-змін)
- [8. Зміни, а не файли](#8-Зміни-а-не-файли)
- [9. Історія проєкту](#9-Історія-проєкту)
- [10. Отримання старих версій](#10-Отримання-старих-версій)
- [11. Створення тегів версій](#11-Створення-тегів-версій)
- [12. Скасування локальних змін (до індексації)](#12-Скасування-локальних-змін-(до-індексації))
- [13. Скасування проіндексованих змін (перед комітом)](#13-Скасування-проіндексованих-змін-(перед-комітом))
- [14. Скасування комітів](#14-Скасування-комітів)
- [15. Видалення комітів з гілки (revert)](#15-Видалення-комітів-з-гілки-(revert))
- [16. Видалення тегу oops](#16-Видалення-тегу-oops)
- [17. Внесення змін до комітів](#17-Внесення-змін-до-комітів)
- [18. Створення гілки](#18-Створення-гілки)
- [19. Перемикання гілок](#19-Перемикання-гілок)
- [20. Переміщення файлів](#20-Переміщення-файлів)
- [21. Зміни в гілці main](#21-Зміни-в-гілці-main)
- [22. Перегляд розбіжних гілок](#22-Перегляд-розбіжних-гілок)
- [23. Злиття](#23-Злиття)
- [24. Створення конфлікту](#24-Створення-конфлікту)
- [25. Вирішення конфліктів](#25-Вирішення-конфліктів)
- [26. rebase проти merge](#26-rebase-проти-merge)
- [27. Відкочування гілки style](#27-Відкочування-гілки-style)
- [28. Перебазування](#28-Перебазування)
- [29. Злиття в гілку main](#29-Злиття-в-гілку-main)
# Частина 2
- [30. Клонування репозиторіїв](#30-Клонування-репозиторіїв)
- [31. Перегляд клонованого репозиторія](#31-Перегляд-клонованого-репозиторія)
- [32. Що таке origin?](#32-Що-таке-origin?)
- [33. Віддалені гілки](#33-Віддалені-гілки)
- [34. Зміна оригінального репозиторія](#34-Зміна-оригінального-репозиторія)
- [35. Підтягування змін](#35-Підтягування-змін)
- [36. Злиття підтягнутих змін](#36-Злиття-підтягнутих-змін)
- [37. Додавання гілки відстеження](#37-Додавання-гілки-відстеження)
- [38. Чисті репозиторії](#38-Чисті-репозиторії)
- [39. Додавання віддаленого репозиторія](#39-Додавання-віддаленого-репозиторія)
- [40. Відправка змін](#40-Відправка-змін)
- [41. Підтягування спільних змін](#41-Підтягування-спільних-змін)
- [42. Розміщення ваших Git репозиторіїв](#42-Розміщення-ваших-Git-репозиторіїв)


# Частина 1
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
У редакторі кода напишемо наступне:

![4 1](https://github.com/user-attachments/assets/fdba5f5f-ca89-4d02-9b86-646c1756639f)

Збережемо наш файл. Виконаємо наступну команду, аби додати наш файл у коміт:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (style)
$ git add style.css
```

Тепер виконаємо коміт:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (style)
$ git commit -m "Added css stylesheet"
[style 58031fb] Added css stylesheet
 1 file changed, 4 insertions(+)
 create mode 100644 style.css
```

Тепер у файлі ```hello.html``` підключемо стилі:

![3 7](https://github.com/user-attachments/assets/48a5a0e1-9fb4-4529-b837-49e0579ad947)

Збережемо і додамо його:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (style)
$ git add hello.html
```

Робимо коміт:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (style)
$ git commit -m "Included stylesheet into hello.html"
[style 14af3d6] Included stylesheet into hello.html
 1 file changed, 1 insertion(+)
```

![18](https://github.com/user-attachments/assets/c4c017ef-afa2-4527-ac27-ab80c2e20d3b)

# 19. Перемикання гілок
Виконаємо наступну команду:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (style)
$ git log --all
```

У результаті побачимо, що:
```
14af3d6 2025-03-10 | Included stylesheet into hello.html (HEAD -> style) [Dmytro]
58031fb 2025-03-10 | Added css stylesheet [Dmytro]
c410e88 2025-03-10 | Added copyright statement with email (main) [Dmytro]
9b6ab77 2025-03-10 | Added HTML header (tag: v1) [Dmytro]
205f3f9 2025-03-10 | Added standard HTML page tags (tag: v1-beta) [Dmytro]
a31cf4c 2025-03-10 | Added h1 tag [Dmytro]
937b340 2025-03-10 | Initial Comit [Dmytro]
```

у нас тут є ще одна гілка ```style```.

Перемкнемось назад у гілку ```main```
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (style)
$ git switch main
Switched to branch 'main'
```

і прочитаємо зміст файлу ```hello.html```
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ cat hello.html
<!-- Author: Alexander Shvets (alex@githowto.com) -->
<html>
  <head>
  </head>
  <body>
    <h1>Hello, world</h1>
  </body>
</html>
```

Тепер знову повернемось до гілки ```style```
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ git switch style
Switched to branch 'style'
```

Тепер тут ми прочитаємо наш файл:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (style)
$ cat hello.html
<!-- Author: Alexander Shvets (alex@githowto.com) -->
<html>
  <head>
    <link type="text/css" rel="stylesheet" media="all" href="style.css" />
  </head>
  <body>
    <h1>Hello, world</h1>
  </body>
</html>
```

Як бачимо різниця чутлива. Якщо на основні гілці ```main``` НЕ БУЛО підключення до стилів, то коли ми змінили гілку (```style```)
то побачили, що зміст одного і того самого файлу різний.

![19](https://github.com/user-attachments/assets/aa7f01e6-7628-4f40-993d-634ea7533361)

# 20. Переміщення файлів
Переглянемо історію змін файлів, для цього виконаємо наступні команди:
# HTML

```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (style)
$ git log hello.html
```

У результаті буде:

```
14af3d6 2025-03-10 | Included stylesheet into hello.html (HEAD -> style) [Dmytro]
c410e88 2025-03-10 | Added copyright statement with email (main) [Dmytro]
9b6ab77 2025-03-10 | Added HTML header (tag: v1) [Dmytro]
205f3f9 2025-03-10 | Added standard HTML page tags (tag: v1-beta) [Dmytro]
a31cf4c 2025-03-10 | Added h1 tag [Dmytro]
937b340 2025-03-10 | Initial Comit [Dmytro]
```
# CSS

```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (style)
$ git log style.css
```

Результат:
```
58031fb 2025-03-10 | Added css stylesheet [Dmytro]
```

Переглянемо різніцю між версіями певного файлу. Для цього виконаємо наступну команду:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (style)
$ git show v1
```

У результаті буде:
```
9b6ab77 2025-03-10 | Added HTML header (tag: v1) [Dmytro]

diff --git a/hello.html b/hello.html
index bd11108..f9ca1fe 100644
--- a/hello.html
+++ b/hello.html
@@ -1,5 +1,8 @@
 <html>
+  <head>
+  </head>
   <body>
     <h1>Hello, world</h1>
   </body>
 </html>
+
```

Так тепер перейменуємо наш файл ```hello.html``` на стандартну назву ```index.html```, за допомогою команди ```mv```
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (style)
$ mv hello.html index.html
```

Тепер перевіримо його статус, виконавши наступну команду: 
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (style)
$ git status
```

Результат буде такий: 
```
On branch style
Changes not staged for commit:
  (use "git add/rm <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        deleted:    hello.html

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        index.html

no changes added to commit (use "git add" and/or "git commit -a")
```

Виконаємо наступну команду:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (style)
$ git add .
```

Тепер перевіремо його статус:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (style)
$ git status
On branch style
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        renamed:    hello.html -> index.html
```

По факту ми зробили так аби наш Git розумів, що ми перейменували файл.
Тепер ми створимо нову директорію і перемістимо наш файл стилю ```style.css``` у цю директорію. Виконаємо наступну команду:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (style)
$ mkdir css
```
Ми створили директорію, тепер перемістимо наш файл, виконавши команду:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (style)
$ git mv style.css css/style.css
```
Перевіримо, для цього напишемо наступну команду:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (style)
$ git status
```

Результатом буде:
```
On branch style
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        renamed:    style.css -> css/style.css
        renamed:    hello.html -> index.html
```
Зробимо коміти і подивимось історію змін у файлі ```css/style.css```. Для цього виконаємо наступну команду:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (style)
$ git commit -m "Renamed hello.html; moved style.css"
```

Результатом буде наступне:
```
[style 37345ad] Renamed hello.html; moved style.css
 2 files changed, 0 insertions(+), 0 deletions(-)
 rename style.css => css/style.css (100%)
 rename hello.html => index.html (100%)
```

Тепер за допомогою логів перевіримо історію змін:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (style)
$ git log css/style.css
```

Результат:
```
37345ad 2025-03-10 | Renamed hello.html; moved style.css (HEAD -> style) [Dmytro]
```

Тепер дещо видозмінемо команду для перевірки історії змін. Додамо наступну опцію ```--follow```
яка нам дозволить подивитись історію змін файлу ДО того як він був переміщений у каталог.
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (style)
$ git log --follow css/style.css
```

Результат: 
```
37345ad 2025-03-10 | Renamed hello.html; moved style.css (HEAD -> style) [Dmytro]
58031fb 2025-03-10 | Added css stylesheet [Dmytro]
```

![20](https://github.com/user-attachments/assets/45deb475-92af-4fd1-9116-9895e8f78040)

# 21. Зміни в гілці ```main```

Cтворемо файл ```README``` і додамо наступну інформацію:
```
This is the Hello World example from the GitHowTo tutorial.
```
Для цього виконаємо таку команди:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (style)
$ nvim README
```
Збережемо наш файл, теперми закомітимо його на основній гілці ```main```. Для цього спочатку перемкнемося на основну гілку.
Виконаємо наступну команду:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (style)
$ git switch main
Switched to branch 'main'
```

Тепер виконаємо наступну команду, аби додати наш файл.
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ git add README
```

Тепер закомітимо його.
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ git commit -m "Added README"
[main 9b72d64] Added README
 1 file changed, 1 insertion(+)
 create mode 100644 README
```

![21](https://github.com/user-attachments/assets/86196e86-7447-4b21-a1ff-1c1aa1ef92d0)

# 22. Перегляд розбіжних гілок
Так як ми створили ще одну гілку ```style``` давайте переглянемо структуру нашого дерева, для цього виконаємо наступну команду:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ git log --all --graph
```

Ось результат:
```
* 9b72d64 2025-03-10 | Added README (HEAD -> main) [Dmytro]
| * 37345ad 2025-03-10 | Renamed hello.html; moved style.css (style) [Dmytro]
| * 14af3d6 2025-03-10 | Included stylesheet into hello.html [Dmytro]
| * 58031fb 2025-03-10 | Added css stylesheet [Dmytro]
|/
* c410e88 2025-03-10 | Added copyright statement with email [Dmytro]
* 9b6ab77 2025-03-10 | Added HTML header (tag: v1) [Dmytro]
* 205f3f9 2025-03-10 | Added standard HTML page tags (tag: v1-beta) [Dmytro]
* a31cf4c 2025-03-10 | Added h1 tag [Dmytro]
* 937b340 2025-03-10 | Initial Comit [Dmytro]
```

![22](https://github.com/user-attachments/assets/95f58910-6555-424b-8b14-40231bb5b975)

# 23. Злиття
Наша задача злити 2 гілки, для цього перемкнемось на іншу гілку, а саме на ```style```.
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ git switch style
Switched to branch 'style'
```

Тепер зіллємо в одну гілку все виконавши наступну команду:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (style)
$ git merge main
Merge made by the 'ort' strategy.
 README | 1 +
 1 file changed, 1 insertion(+)
 create mode 100644 README
```

Тепер переглянемо нашу структуру дерева, виконавши наступну команду:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (style)
$ git log --all --graph
```

Результат: 
```
*   fd5481e 2025-03-10 | Merge branch 'main' into style (HEAD -> style) [Dmytro]
|\
| * 9b72d64 2025-03-10 | Added README (main) [Dmytro]
* | 37345ad 2025-03-10 | Renamed hello.html; moved style.css [Dmytro]
* | 14af3d6 2025-03-10 | Included stylesheet into hello.html [Dmytro]
* | 58031fb 2025-03-10 | Added css stylesheet [Dmytro]
|/
* c410e88 2025-03-10 | Added copyright statement with email [Dmytro]
* 9b6ab77 2025-03-10 | Added HTML header (tag: v1) [Dmytro]
* 205f3f9 2025-03-10 | Added standard HTML page tags (tag: v1-beta) [Dmytro]
* a31cf4c 2025-03-10 | Added h1 tag [Dmytro]
* 937b340 2025-03-10 | Initial Comit [Dmytro]
```

![23](https://github.com/user-attachments/assets/d900eaaa-0423-410f-91a4-6dedc094d7e8)

# 24. Створення конфлікту
Змоделюємо конфлікт. Перемкнемося на основну гілку ```main```.
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (style)
$ git switch main
Switched to branch 'main'
```

Тепер відкриємо наш файл.
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ nvim hello.html
```

Зробимо зміни

![3 8](https://github.com/user-attachments/assets/54dfa06a-cad2-43f2-94c1-016801019bd8)

Після збереження додамо його.
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ git add hello.html
```

Тепер зробимо коміт:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ git commit -m "Added meta title"
[main 07015f1] Added meta title
 1 file changed, 2 insertions(+)
```

Тепер відобразимо наше дерево:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ git log --all --graph
```

```
* 07015f1 2025-03-10 | Added meta title (HEAD -> main) [Dmytro]
| *   fd5481e 2025-03-10 | Merge branch 'main' into style (style) [Dmytro]
| |\
| |/
|/|
* | 9b72d64 2025-03-10 | Added README [Dmytro]
| * 37345ad 2025-03-10 | Renamed hello.html; moved style.css [Dmytro]
| * 14af3d6 2025-03-10 | Included stylesheet into hello.html [Dmytro]
| * 58031fb 2025-03-10 | Added css stylesheet [Dmytro]
|/
* c410e88 2025-03-10 | Added copyright statement with email [Dmytro]
* 9b6ab77 2025-03-10 | Added HTML header (tag: v1) [Dmytro]
* 205f3f9 2025-03-10 | Added standard HTML page tags (tag: v1-beta) [Dmytro]
* a31cf4c 2025-03-10 | Added h1 tag [Dmytro]
* 937b340 2025-03-10 | Initial Comit [Dmytro]
```
Остання зміна в ```main``` конфліктує з деякими змінами в ```style```.

![24](https://github.com/user-attachments/assets/c7575314-85a3-408b-a1a5-d17a954e750c)

# 25. Вирішення конфліктів
Тепер зіллємо наші гілкі. Спочатку перемкнемось на гілку ```style```.
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ git switch style
Switched to branch 'style'
```

Тепер зіллємо з основною гілкою ```main```
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (style)
$ git merge main
```

Тепер подивимось на результат:
```
Auto-merging index.html
CONFLICT (content): Merge conflict in index.html
Automatic merge failed; fix conflicts and then commit the result.
```

Так, у нас виник конфлікт, подивимось, що нам скаже про це ```Git```
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (style|MERGING)
$ git status
```
Ось що нам каже ```Git```
```
On branch style
You have unmerged paths.
  (fix conflicts and run "git commit")
  (use "git merge --abort" to abort the merge)

Unmerged paths:
  (use "git add <file>..." to mark resolution)
        both modified:   index.html

no changes added to commit (use "git add" and/or "git commit -a")
```

Якщо ми відкриємо наш файл, то побачимо наступне:

![3 9](https://github.com/user-attachments/assets/4c97a042-3532-48e8-a3f0-b5390c831afc)


Та частина яка знаходиться між ```<<<<<<<``` ```>>>>>>>``` і є конфліктом.

Перед тим як вирішити наш конфлікт уручну нам треба зробити відкат назад, до злиття. 

Виконаємо наступну команду:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (style|MERGING)
$ git merge --abort
```
Тепер перевіремо статус.
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (style)
$ git status
On branch style
nothing to commit, working tree clean
```
воно нам каже, що ми так відкотились назад і що робоче дерево чисте.

Будемо вирішувати конфлікт.
Зробимо злиття ще раз.
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (style)
$ git merge main
Auto-merging index.html
CONFLICT (content): Merge conflict in index.html
Automatic merge failed; fix conflicts and then commit the result.
```

Так, ну для вирішення конфлікту нам треба відредагувати файл до стану, що нас влаштовує і який не буде конфліктувати.

Відкриємо наш файл. І відредагуємо його таким чинном:

![3 10](https://github.com/user-attachments/assets/7abcba8f-7158-46d5-8a8b-ead53aed3f88)

Після збереження файлу закомітимо його. 

Спочатку додамо його.
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (style|MERGING)
$ git add index.html
```

Комміт
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (style|MERGING)
$ git commit -m "Resolved merge conflict"
[style 1fad50e] Resolved merge conflict
```

Тепер подивимось на поточний стан нашого репозиторію
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (style)
$ git status
On branch style
nothing to commit, working tree clean
```

Тепер подивимось на структуру нашого дерева
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (style)
$ git log --all --graph
```

```
*   1fad50e 2025-03-10 | Resolved merge conflict (HEAD -> style) [Dmytro]
|\
| * 07015f1 2025-03-10 | Added meta title (main) [Dmytro]
* | fd5481e 2025-03-10 | Merge branch 'main' into style [Dmytro]
|\|
| * 9b72d64 2025-03-10 | Added README [Dmytro]
* | 37345ad 2025-03-10 | Renamed hello.html; moved style.css [Dmytro]
* | 14af3d6 2025-03-10 | Included stylesheet into hello.html [Dmytro]
* | 58031fb 2025-03-10 | Added css stylesheet [Dmytro]
|/
* c410e88 2025-03-10 | Added copyright statement with email [Dmytro]
* 9b6ab77 2025-03-10 | Added HTML header (tag: v1) [Dmytro]
* 205f3f9 2025-03-10 | Added standard HTML page tags (tag: v1-beta) [Dmytro]
* a31cf4c 2025-03-10 | Added h1 tag [Dmytro]
* 937b340 2025-03-10 | Initial Comit [Dmytro]
```

![25](https://github.com/user-attachments/assets/eb58cd7e-e2f2-4519-a40a-1f2234903ef1)

# 26. ```rebase``` проти ```merge```

Тут ми розглянемо різницю між цими командами, для цього ми повернемося до репозиторію.

# 27. Відкочування гілки ```style```

Наша задача повернутися у той час коли наші гілки НЕ були злитті. Для цього перемкнемося на іншу гілку:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (style)
$ git switch style
Already on 'style'
```

Тепер подивимось на нашу структуру дерева:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (style)
$ git log --graph
```

```
*   1fad50e 2025-03-10 | Resolved merge conflict (HEAD -> style) [Dmytro]
|\
| * 07015f1 2025-03-10 | Added meta title (main) [Dmytro]
* | fd5481e 2025-03-10 | Merge branch 'main' into style [Dmytro]
|\|
| * 9b72d64 2025-03-10 | Added README [Dmytro]
* | 37345ad 2025-03-10 | Renamed hello.html; moved style.css [Dmytro]
* | 14af3d6 2025-03-10 | Included stylesheet into hello.html [Dmytro]
* | 58031fb 2025-03-10 | Added css stylesheet [Dmytro]
|/
* c410e88 2025-03-10 | Added copyright statement with email [Dmytro]
* 9b6ab77 2025-03-10 | Added HTML header (tag: v1) [Dmytro]
* 205f3f9 2025-03-10 | Added standard HTML page tags (tag: v1-beta) [Dmytro]
* a31cf4c 2025-03-10 | Added h1 tag [Dmytro]
* 937b340 2025-03-10 | Initial Comit [Dmytro]
```

Як бачимо останнім комітом у гілці ```style``` був ```Renamed hello.html; moved style.css```. 

Наша задача повернутися у цей момент часу. Для цього ми можемо використати 2 способи:
- або хеш
- або те що коміт знаходиться за 2 коміти до ```HEAD```

Виконаємо команду яка поверне нас у цей коміт.
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (style)
$ git reset --hard HEAD~2
HEAD is now at 37345ad Renamed hello.html; moved style.css
```

```37345ad``` є нашим хешем.

Тепер перевіримо нашу гілку. Виконаємо наступну команду:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (style)
$ git log --graph
```
Результат 
```
* 37345ad 2025-03-10 | Renamed hello.html; moved style.css (HEAD -> style) [Dmytro]
* 14af3d6 2025-03-10 | Included stylesheet into hello.html [Dmytro]
* 58031fb 2025-03-10 | Added css stylesheet [Dmytro]
* c410e88 2025-03-10 | Added copyright statement with email [Dmytro]
* 9b6ab77 2025-03-10 | Added HTML header (tag: v1) [Dmytro]
* 205f3f9 2025-03-10 | Added standard HTML page tags (tag: v1-beta) [Dmytro]
* a31cf4c 2025-03-10 | Added h1 tag [Dmytro]
* 937b340 2025-03-10 | Initial Comit [Dmytro]
```

![27](https://github.com/user-attachments/assets/5f30c211-d25f-47f3-866e-fb0315203e30)

# 28. Перебазування

Так ми повернулися у той момент ДО того як ми злили гілку ```style``` з ```main```.

В гілці ```main``` є дві коміти, яких зараз немає у гілці ```style```:

- новий файл ```README```
- конфліктна зміна у файлі ```index.html```

Цього разу ми перенесемо ці зміни до гілки ```style``` за допомогою команди ```rebase```, а не ```merge```.

Виконаємо наступні команди:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (style)
$ git switch style
Already on 'style'
```

Тепер команда для переносу:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (style)
$ git rebase main
```

Результат:
```
Auto-merging hello.html
CONFLICT (content): Merge conflict in hello.html
error: could not apply 14af3d6... Included stylesheet into hello.html
hint: Resolve all conflicts manually, mark them as resolved with
hint: "git add/rm <conflicted_files>", then run "git rebase --continue".
hint: You can instead skip this commit: run "git rebase --skip".
hint: To abort and get back to the state before "git rebase", run "git rebase --abort".
Could not apply 14af3d6... Included stylesheet into hello.html
```
Так-с у нас тут конфлікт, перевіримо зараз статус:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (style|REBASE 2/3)
$ git status
```

Результат:
```
interactive rebase in progress; onto 07015f1
Last commands done (2 commands done):
   pick 58031fb Added css stylesheet
   pick 14af3d6 Included stylesheet into hello.html
Next command to do (1 remaining command):
   pick 37345ad Renamed hello.html; moved style.css
  (use "git rebase --edit-todo" to view and edit)
You are currently rebasing branch 'style' on '07015f1'.
  (fix conflicts and then run "git rebase --continue")
  (use "git rebase --skip" to skip this patch)
  (use "git rebase --abort" to check out the original branch)

Unmerged paths:
  (use "git restore --staged <file>..." to unstage)
  (use "git add <file>..." to mark resolution)
        both modified:   hello.html

no changes added to commit (use "git add" and/or "git commit -a")
```
Kонфлікт стався в ```hello.html```, а не в ```index.html```, як минулого разу.
Це тому, що ```rebase``` був у процесі застосування змін ```style``` поверх гілки ```main```.
У той момент в гілці ```main``` ще не було перейменовано файл ```hello.html```, тому він все ще має стару назву.

Відкриємо файл наш ```hello.html```

![3 9](https://github.com/user-attachments/assets/167fb7ba-623b-47df-b90e-27ee6fa65879)

Так тепер вирішемо наш конфлікт. Для цього ми вручну відредагуємо наш файл, аби він відповідав нашим очікуванням

![3 10](https://github.com/user-attachments/assets/5b05056c-162b-4de0-a7e4-25dff721bd9a)

Зберігаємо наш файл.
Але нам не треба робити коміти. Ми можемо просто додати файл до індексу і продовжити процес перебазування.

Виконаємо наступну команду:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (style|REBASE 2/3)
$ git add .
```

Тепер виконаємо наступну:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (style|REBASE 2/3)
$ git rebase --continue
[detached HEAD b57c804] Included stylesheet into hello.html
 1 file changed, 1 insertion(+)
Successfully rebased and updated refs/heads/style.
```

Тепер перевіремо статус.
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (style)
$ git status
On branch style
nothing to commit, working tree clean
```

Статус нам каже, що все гаразд. Тому йдемо далі.

Тепер перевіримо нашу структуру
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (style)
$ git log --all --graph
* ea7021a 2025-03-10 | Renamed hello.html; moved style.css (HEAD -> style) [Dmytro]
* b57c804 2025-03-10 | Included stylesheet into hello.html [Dmytro]
* 8da2d61 2025-03-10 | Added css stylesheet [Dmytro]
* 07015f1 2025-03-10 | Added meta title (main) [Dmytro]
* 9b72d64 2025-03-10 | Added README [Dmytro]
* c410e88 2025-03-10 | Added copyright statement with email [Dmytro]
* 9b6ab77 2025-03-10 | Added HTML header (tag: v1) [Dmytro]
* 205f3f9 2025-03-10 | Added standard HTML page tags (tag: v1-beta) [Dmytro]
* a31cf4c 2025-03-10 | Added h1 tag [Dmytro]
* 937b340 2025-03-10 | Initial Comit [Dmytro]
```

Кінцевий результат перебазування дуже схожий на результат злиття. Гілка ```style``` зараз містить всі свої зміни, 
а також всі зміни гілки ```main```. Однак, дерево комітів значно відрізняється. Дерево комітів гілки ```style``` було переписано 
таким чином, що гілка main є частиною історії комітів. Це робить ланцюг комітів лінійним і набагато більш читабельним.

Тепер зробимо висновок, коли використовувати команду ```rebase```, а коли команду ```merge```?

Використовуємо ✔️: 
- Коли ви підтягуєте зміни з віддаленого репозиторія і хочете злити їх до вашої локальної гілки.
- Якщо ви хочете, щоб історія комітів була лінійною і легкою для читання.

НЕ використовуємо ❌:
- Якщо поточна гілка є загальнодоступною. Перезапис таких гілок заважатиме роботі інших членів команди.
- Коли важлива точна історія гілки комітів (оскільки команда ```rebase``` переписує історію комітів).

Тобто висновок такий. Для локальних ```rebase```, для загальнодоступних ```merge```.

![28](https://github.com/user-attachments/assets/bec843d4-4a70-4a67-b85e-a982fdc6533c)

# 29. Злиття в гілку ```main```

Тепер будемо зливати наші гілки, але спочатку перемкнемось на основну гілку ```main```
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (style)
$ git switch main
Switched to branch 'main'
```

Тепер будемо зливати наші гілки
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ git merge style
Updating 07015f1..ea7021a
Fast-forward
 css/style.css            | 4 ++++
 hello.html => index.html | 1 +
 2 files changed, 5 insertions(+)
 create mode 100644 css/style.css
 rename hello.html => index.html (72%)
```

Переглянемо наші логи
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ git log --all --graph
* ea7021a 2025-03-10 | Renamed hello.html; moved style.css (HEAD -> main, style) [Dmytro]
* b57c804 2025-03-10 | Included stylesheet into hello.html [Dmytro]
* 8da2d61 2025-03-10 | Added css stylesheet [Dmytro]
* 07015f1 2025-03-10 | Added meta title [Dmytro]
* 9b72d64 2025-03-10 | Added README [Dmytro]
* c410e88 2025-03-10 | Added copyright statement with email [Dmytro]
* 9b6ab77 2025-03-10 | Added HTML header (tag: v1) [Dmytro]
* 205f3f9 2025-03-10 | Added standard HTML page tags (tag: v1-beta) [Dmytro]
* a31cf4c 2025-03-10 | Added h1 tag [Dmytro]
* 937b340 2025-03-10 | Initial Comit [Dmytro]
```

Як бачимо усе добре.

![29](https://github.com/user-attachments/assets/745332a8-7919-43c6-99de-38b9e50db39b)


## Частина 2
# 30. Клонування репозиторіїв

Перейдемо у директорію ```repositories```. 

Виконаємо наступну команду:

Спочатку вийдемо з директорії у якій ми зараз
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ cd ..
```

Тепер подивимось на поточну директорію:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories
$ pwd
/d/all you need/Общее/учеба/Git tutor/githowto/repositories
```

Тепер подивимось на список файлів і каталогів
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories
$ ls
work/
```

Створемо клон нашого репозиторію
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories
$ git clone work home
Cloning into 'home'...
done.
```

Перевіримо які є файли і каталоги:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories
$ ls
home/  work/
```

![30](https://github.com/user-attachments/assets/b5e8703f-4241-425a-bdad-2f95f7e5f5fa)

# 31. Перегляд клонованого репозиторія
Переглянемо на клонований репозиторій.
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories
$ cd home
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/home (main)
$ ls
css/  index.html  README
```

Тут знаходяться каталог ```css/```, ```index.html```, ```README```.

Переглянемо історію змін репозиторію. Виконаємо команду:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/home (main)
$ git log --all
```

Результат
```
ea7021a 2025-03-10 | Renamed hello.html; moved style.css (HEAD -> main, origin/style, origin/main, origin/HEAD) [Dmytro]
b57c804 2025-03-10 | Included stylesheet into hello.html [Dmytro]
8da2d61 2025-03-10 | Added css stylesheet [Dmytro]
07015f1 2025-03-10 | Added meta title [Dmytro]
9b72d64 2025-03-10 | Added README [Dmytro]
c410e88 2025-03-10 | Added copyright statement with email [Dmytro]
9b6ab77 2025-03-10 | Added HTML header (tag: v1) [Dmytro]
205f3f9 2025-03-10 | Added standard HTML page tags (tag: v1-beta) [Dmytro]
a31cf4c 2025-03-10 | Added h1 tag [Dmytro]
937b340 2025-03-10 | Initial Comit [Dmytro]
```

Історія повина співпадати з старим репозиторієм.

![31](https://github.com/user-attachments/assets/53aa7d9f-8343-41c8-9bc5-ac4bfccbefcd)

# 32. Що таке origin?

Виконаємо наступну команду:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/home (main)
$ git remote
```

Результатом буде:
```
origin
```
Ми бачимо, що клонований репозиторій знає про ім'я за замовчуванням віддаленого репозиторія.

Подивімось, чи можемо ми отримати більш детальну інформацію про ім'я за замовчуванням:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/home (main)
$ git remote show origin
```
Результат:
```
* remote origin
  Fetch URL: D:/all you need/Общее/учеба/Git tutor/githowto/repositories/work
  Push  URL: D:/all you need/Общее/учеба/Git tutor/githowto/repositories/work
  HEAD branch: main
  Remote branches:
    main  tracked
    style tracked
  Local branch configured for 'git pull':
    main merges with remote main
  Local ref configured for 'git push':
    main pushes to main (up to date)
```

Ми бачимо, що «ім'я за замовчуванням» віддаленого репозиторія — початкове ```work```.

![32](https://github.com/user-attachments/assets/1d41c4d4-9646-4dfb-897f-254aa45e5a6e)

# 33. Віддалені гілки

Подивімось на гілки, доступні в нашому клонованому репозиторії.
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/home (main)
$ git branch
```

Результат:
```
* main
```

Як ми бачимо, у списку лише гілка ```main```. Де гілка ```style```? 
Команда ```git branch```, за замовчуванням, виводить лише список локальних гілок.

Для того аби побачити усі гілки, виконаємо наступну команду:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/home (main)
$ git branch -a
```

Результат:
```
* main
  remotes/origin/HEAD -> origin/main
  remotes/origin/main
  remotes/origin/style
```

![33](https://github.com/user-attachments/assets/bc325cbc-86c4-4215-8c55-a61a47852242)

# 34. Зміна оригінального репозиторія
Внесемо зміни у оригінальний репозиторій ```work```
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/home (main)
$ cd ../work
```

Тепер відкриємо файл ```README``` і зробимо такі зміни:

![3 11](https://github.com/user-attachments/assets/a6746e7c-1d7c-48a1-882a-b68d91458498)

Після зберігання додамо цю зміну і зробимо коміт.

Додавання зміни:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ git add README
```

Виконання коміту:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ git commit -m "Changed README in original repo"
[main 0223813] Changed README in original repo
 1 file changed, 2 insertions(+), 1 deletion(-)
```

![34](https://github.com/user-attachments/assets/55a2ba92-63f8-469d-9f2d-7cc32584442c)

# 35. Підтягування змін
Виконаємо наступну команди: 
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ cd ../home
```

```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/home (main)
$ git fetch
remote: Enumerating objects: 5, done.
remote: Counting objects: 100% (5/5), done.
remote: Compressing objects: 100% (3/3), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (3/3), 372 bytes | 2.00 KiB/s, done.
From D:/all you need/Общее/учеба/Git tutor/githowto/repositories/work
   ea7021a..0223813  main       -> origin/main
```

```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/home (main)
$ git log --all
0223813 2025-03-11 | Changed README in original repo (origin/main, origin/HEAD) [Dmytro]
ea7021a 2025-03-10 | Renamed hello.html; moved style.css (HEAD -> main, origin/style) [Dmytro]
b57c804 2025-03-10 | Included stylesheet into hello.html [Dmytro]
8da2d61 2025-03-10 | Added css stylesheet [Dmytro]
07015f1 2025-03-10 | Added meta title [Dmytro]
9b72d64 2025-03-10 | Added README [Dmytro]
c410e88 2025-03-10 | Added copyright statement with email [Dmytro]
9b6ab77 2025-03-10 | Added HTML header (tag: v1) [Dmytro]
205f3f9 2025-03-10 | Added standard HTML page tags (tag: v1-beta) [Dmytro]
a31cf4c 2025-03-10 | Added h1 tag [Dmytro]
937b340 2025-03-10 | Initial Comit [Dmytro]
```

Зараз в репозиторії є всі коміти з оригінального репозиторія, але вони не злиті в локальні гілки клонованого репозиторія.

В історії вище знайдемо коміт ```Changed README in original repo```. Зверніть увагу, що коміт містить у собі коміти ```origin/main``` і ```origin/HEAD```.
Тепер подивімось на коміт ```Renamed hello.html; moved style.css```. Ви побачите, що локальна гілка ```main``` вказує на цей коміт, а не на новий коміт, котрий ми щойно підтягнули.
Висновком є те, що команда ```git fetch``` буде підтягувати нові коміти з віддаленого репозиторія, але не буде зливати їх з вашими напрацюваннями в локальних гілках.

Перевіримо файл ```README```
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/home (main)
$ cat README
This is the Hello World example from the GitHowTo tutorial.
```

Жодних змін НЕМА.

![35](https://github.com/user-attachments/assets/f16d0135-7f3a-4c4e-bf87-aaf45f0293a4)

# 36. Злиття підтягнутих змін
Виконаємо злиття зміни у локальну гілку ```main```
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/home (main)
$ git merge origin/main
Updating ea7021a..0223813
Fast-forward
 README | 3 ++-
 1 file changed, 2 insertions(+), 1 deletion(-)
```

Ще раз перевіримо файл ```README```
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/home (main)
$ cat README
This is the Hello World example from the Git tutorial.
(changed in origin)
```

Команда ```fetch``` дає вам повний контроль над тим, що саме підтягується та зливається в локальні гілки, 
але для зручності існує також команда ```pull```, яка підтягує та зливає зміни з віддаленої гілки у вашу поточну гілку одним викликом.

```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/home (main)
$ git pull
Already up to date.
```

![36](https://github.com/user-attachments/assets/c8a760ec-5a46-46f6-a214-0031ae40b5d8)

# 37. Додавання гілки відстеження

Додамо локальну гілку, яка відстежує віддалену гілку:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/home (main)
$ git branch --track style origin/style
branch 'style' set up to track 'origin/style'.
```

```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/home (main)
$ git branch -a
* main
  style
  remotes/origin/HEAD -> origin/main
  remotes/origin/main
  remotes/origin/style
```

```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/home (main)
$ git log --max-count=2
0223813 2025-03-11 | Changed README in original repo (HEAD -> main, origin/main, origin/HEAD) [Dmytro]
ea7021a 2025-03-10 | Renamed hello.html; moved style.css (origin/style, style) [Dmytro]
```

Тепер ми можемо бачити гілку ```style``` у списку гілок і у лозі.

![37](https://github.com/user-attachments/assets/19c92bb6-4a79-45f4-9388-7aeb61f87fe5)

# 38. Чисті репозиторії
Cтворемо чистий репозиторій. 

Виконаємо наступні команди:

Вийдемо з поточного каталогу
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/home (main)
$ cd ..
```

Склонуємо 
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories
$ git clone --bare work work.git
Cloning into bare repository 'work.git'...
done.
```

Перевіримо зміст репозиторію
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories
$ ls work.git
config  description  HEAD  hooks/  info/  objects/  packed-refs  refs/
```

![38](https://github.com/user-attachments/assets/f67bfd07-3141-4ccf-ac09-6f6dd92b2653)

# 39. Додавання віддаленого репозиторія

Додаймо репозиторій ```work.git``` до нашого оригінального репозиторія.

Виконаємо наступні команди: 
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories
$ cd work
```

```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ git remote add shared ../work.git
```

![39](https://github.com/user-attachments/assets/d00ad88a-e661-4833-9e58-0ff39b7d51bc)

# 40. Відправка змін
Почнемо зі створення зміни, яку потрібно передати в репозиторій. Відредагуємо ```README``` і зробимо коміт змін.

Виконаємо команду: 
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ nvim README
```

Робимо зміни:

![3 12](https://github.com/user-attachments/assets/957f87e4-3499-4d79-8448-b64372d47bf6)

Зберігаємо наші зміни.

Перемкнемось на іншу гілку ```main```
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ git switch main
Already on 'main'
M       README
```

Додамо зміну 
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ git add README
```

Робимо коміт
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ git commit -m "Added shared comment to readme"
[main 243639b] Added shared comment to readme
 1 file changed, 1 insertion(+), 1 deletion(-)
```

Тепер надішлемо зміни до спільний репозиторій
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ git push shared main
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 398 bytes | 36.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To ../work.git
   0223813..243639b  main -> main
```

![40](https://github.com/user-attachments/assets/0db085ab-ac6c-4a66-b46b-1d9deb571c58)

# 41. Підтягування спільних змін
Перейдемо у каталог ```home```, виконавши команду:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/work (main)
$ cd ../home
```

Додаємо віддалений репозиторій ```shared```:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/home (main)
$ git remote add shared ../work.git
```

Cтворюємо локальну гілку ```shared```, яка відслідковує ```main``` у ```shared```:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/home (main)
$ git branch --track shared main
branch 'shared' set up to track 'main'.
```

Підтягуємо зміни з ```shared```:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/home (main)
$ git pull shared main
remote: Enumerating objects: 5, done.
remote: Counting objects: 100% (5/5), done.
remote: Compressing objects: 100% (3/3), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (3/3), 378 bytes | 2.00 KiB/s, done.
From ../work
 * branch            main       -> FETCH_HEAD
 * [new branch]      main       -> shared/main
Updating 0223813..243639b
Fast-forward
 README | 2 +-
 1 file changed, 1 insertion(+), 1 deletion(-)
```

 Перевірка вмісту ```README```:
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories/home (main)
$ cat README
This is the Hello World example from the Git tutorial.
(changed in the origin and pushed to shared)
```

![41](https://github.com/user-attachments/assets/98241202-9bbc-4785-a9b2-ec556d606df1)

# 42. Розміщення ваших Git репозиторіїв
Виконаємо наступну команду:

Запустимо наш Git-сервер
```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories
$ git daemon --verbose --export-all --base-path=.
[19148] Ready to rumble
[1572] Connection from [::1]:64741
[1572] unable to set SO_KEEPALIVE on socket: Input/output error
[1572] Extended attribute "host": localhost
[1572] Extended attribute "protocol": version=2
[1572] Request upload-pack for '/work.git'
```

В окремому вікні терміналу перейдемо до директорії ```repositories```:

```
dima2@DESKTOP-O8IIC2U MINGW64 /d/all you need/Общее/учеба/Git tutor/githowto/repositories
$ git clone git://localhost/work.git network_work
Cloning into 'network_work'...
remote: Enumerating objects: 36, done.
remote: Counting objects: 100% (36/36), done.
remote: Compressing objects: 100% (27/27), done.
remote: Total 36 (delta 4), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (36/36), done.
Resolving deltas: 100% (4/4), done.
```

Ми побачимо копію проекту ```work```.

![42](https://github.com/user-attachments/assets/879744e9-a8eb-4511-848c-1029a1f365e0)

Усе. Туторіал пройдений.

# Висновок
У ході виконання практичного завдання я ознайомився з основними командами Git, 
навчився працювати з локальним і віддаленим репозиторіями, створювати гілки, 
виконувати коміти, зливати зміни та вирішувати конфлікти. Інтерактивний курс Git How To 
допоміг закріпити ці навички на практиці та зрозуміти логіку роботи системи контролю версій Git.
