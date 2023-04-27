Домашнее задание #2 на тему Git Bash  
Ознакомление с terminal и расширенное описание выполняемых команд

## 1. Сделать папку dir_1
Создадим каталог **dir_1**, для этого используем команду `mkdir`
```
nikol@DESKTOP-A1PNQL6 MINGW64 ~/git/terminal2
$ mkdir dir_1
```

## 2. Зайти в папку dir_1
Используем команду `сd имя_каталога`
```
nikol@DESKTOP-A1PNQL6 MINGW64 ~/git/terminal2
$ cd dir_1
```
## 3. Создать папку inner_dir_1
Создадим каталог **inner dir_1**, для этого используем команду `mkdir` 
```
nikol@DESKTOP-A1PNQL6 MINGW64 ~/git/terminal2/dir_1
$ mkdir inner_dir_1
```

## 4. Посмотреть где ты находишься 
Посмотреть где мы накходимся команда `pwd`
```
nikol@DESKTOP-A1PNQL6 MINGW64 ~/git/terminal2/dir_1
$ pwd
/c/Users/nikol/git/terminal2/dir_
```

## 5. Находясь в папке dir_1 создать пустой текстовый файл tf_1.txt
Для того чтобы создать пустой файл используется команда `touch`
```
nikol@DESKTOP-A1PNQL6 MINGW64 ~/git/terminal2/dir_1
$ touch tf_1.txt
```
## 6. Находясь в папке dir_1 через команду cat создать текстовый файл tf_2.txt со следующими строками 
Для того чтобы создать файл используется команду `cat` и запишем строки: 
- the first 1
- the second 2
- the third 3
```
$ cat >> tf_2.txt
the first 1
the second 2
the third 3
```
Нажать ctrl + C
## 7. Зайти в папку inner_dir_1
```
nikol@DESKTOP-A1PNQL6 MINGW64 ~/git/terminal2/dir_1
$ cd inner_dir_1
```
## 8. Через cat сделать текстовый файл tf_3.txt c любыми строками

```
$ cat >> tf_3.txt
Monday
Thusday
Wednesday
Thursday
```

## 9 Через cat добавить в текстовый файл tf_3.txt строку "the second 2"
```
nikol@DESKTOP-A1PNQL6 MINGW64 ~/git/terminal2/dir_1/inner_dir_1
$ cat >> tf_3.txt

```
```
the second 2

```

## 10. Через cat добавить в текстовый файл tf_3.txt строку "the sec 2"
```
nikol@DESKTOP-A1PNQL6 MINGW64 ~/git/terminal2/dir_1/inner_dir_1
$ cat >> tf_3.txt
```
```
the sec 2

```

## 11. Через cat добавить в текстовый файл tf_2.txt строку "the sec 3"
```
nikol@DESKTOP-A1PNQL6 MINGW64 ~/git/terminal2/dir_1/inner_dir_1
$ cat >> ..tf_2.txt
```
```
the sec 3

```
## 12. Через cat добавить в текстовый файл tf_3.txt строку "the SeCoNd 2"
```
nikol@DESKTOP-A1PNQL6 MINGW64 ~/git/terminal2/dir_1/inner_dir_1
$ cat >> tf_3.txt
```
```
the SeCoNd 2

```

## 13 Через cat добавить в текстовый файл tf_2.txt строку "the seConD 2".
```
nikol@DESKTOP-A1PNQL6 MINGW64 ~/git/terminal2/dir_1/inner_dir_1
$ cat >> ../tf_2.txt
```
```
the seConD 2

```
## 14. Создать текстовый файл tf_4.txt в котором будет 15 строк

```
nikol@DESKTOP-A1PNQL6 MINGW64 ~/git/terminal2/dir_1/inner_dir_1
$ seq 15 | cat > tf_4.txt
```
## 15 Создать текстовый файл tF_5.txt в котором будет 13 строк
```
nikol@DESKTOP-A1PNQL6 MINGW64 ~/git/terminal2/dir_1/inner_dir_1
$ seq 13 | cat > tF_5.txt
```


## 16. Вывести список всех файлов в папке

```
nikol@DESKTOP-A1PNQL6 MINGW64 ~/git/terminal2/dir_1/inner_dir_1
$ ls
tF_5.txt  tf_3.txt  tf_4.txt
```


## 17. Выйти из папки inner_dir_1
Для вывода первых строк используется команда `head`, синтаксис :
```
nikol@DESKTOP-A1PNQL6 MINGW64 ~/git/terminal2/dir_1/inner_dir_1
$ cd ..
```

## 18. Вывести содержимое файла tf_3.txt в терминал

```
nikol@DESKTOP-A1PNQL6 MINGW64 ~/git/terminal2/dir_1
$ cat */tf_3.txt
```
```
Monday
Thusday
Wensday
Thursday
the second 2
the sec 2
the SeCoNd 2
```


## 19. Найти путь к файлу tf_4.txt
```
nikol@DESKTOP-A1PNQL6 MINGW64 ~/git/terminal2/dir_1
$ find -name tf_4.txt
```
```
./inner_dir_1/tf_4.txt
```

## 20. Очистить файл tf_4.txt от содержимого без удаления самого файла

```
nikol@DESKTOP-A1PNQL6 MINGW64 ~/git/terminal2/dir_1
$ > */tf_4.txt

```

## 21. Найти путь к файлам у которых есть  “tf” в названии.
```
nikol@DESKTOP-A1PNQL6 MINGW64 ~/git/terminal2/dir_1
$ find -name 'tf*'

./inner_dir_1/tf_3.txt
./inner_dir_1/tf_4.txt
./tf_1.txt
./tf_2.txt
./tf_4.txt

```
## 22. Найти путь к файлам у которых есть "tf" в названии и буквы в любом регистре.


```
nikol@DESKTOP-A1PNQL6 MINGW64 ~/git/terminal2/dir_1
$ find -iname 'tf*'
```
```
./inner_dir_1/tf_3.txt
./inner_dir_1/tf_4.txt
./inner_dir_1/tF_5.txt
./tf_1.txt
./tf_2.txt
./tf_4.txt
./tf_6.txt


```
## 23. Найти строки в файлах где есть комбинация букв "sec" в текущей папке


```
nikol@DESKTOP-A1PNQL6 MINGW64 ~/git/terminal2/dir_1
$ grep -n 'sec' *.txt'

tf_2.txt:2:the second 2
tf_2.txt:4:the sec 3
```
## 24. Найти строки в файлах где есть комбинация букв "sec" в любом регистре в текущей папке.


```
$ grep -in 'sec' *.txt

tf_2.txt:2:the second 2
tf_2.txt:4:the sec 3
tf_2.txt:5:the seConD 2

```
## 25. Найти строки в файлах где есть только комбинация букв "sec" в текущей папке

```
nikol@DESKTOP-A1PNQL6 MINGW64 ~/git/terminal2/dir_1
$ grep -n '\<sec\>' *.txt

tf_2.txt:4:the sec 3

```
## 26. Найти строки в файлах где есть только комбинация букв "sec" в любом регистре в текущей папке

```
$ nikol@DESKTOP-A1PNQL6 MINGW64 ~/git/terminal2/dir_1
$ grep -in '\<sec\>' *.txt

tf_2.txt:4:the sec 3

```
## 27. Найти строки в файлах где есть комбинация букв "second" в текущей папке

```
nikol@DESKTOP-A1PNQL6 MINGW64 ~/git/terminal2/dir_1
$ grep -n 'second' *.txt

tf_2.txt:2:the second 

```
## 28. Найти строки в файлах где есть комбинация букв "second" в любом регистре в текущей папке

```
nikol@DESKTOP-A1PNQL6 MINGW64 ~/git/terminal2/dir_1
$ grep -in 'second' *.txt
tf_2.txt:2:the second 2
tf_2.txt:5:the seConD 2


```
## 29. Найти строки в файлах где есть комбинация букв "second" во всех папках ниже уровнем

```
nikol@DESKTOP-A1PNQL6 MINGW64 ~/git/terminal2/dir_1
$ grep -rn 'second' *
inner_dir_1/tf_3.txt:5:the second 2
tf_2.txt:2:the second 2


```
## 30. Найти только путь и название файла в строках которых есть комбинация букв "second" в текущей папке
```
nikol@DESKTOP-A1PNQL6 MINGW64 ~/git/terminal2/dir_1
$ grep -l 'second' *.*
tf_2.txt
```

## 31. Найти только путь и название файла в строках которых есть комбинация букв "second" в текущей папке
```
nikol@DESKTOP-A1PNQL6 MINGW64 ~/git/terminal2/dir_1
$ grep -rv 'second' *
```

```
inner_dir_1/tf_3.txt:Monday
inner_dir_1/tf_3.txt:Thusday
inner_dir_1/tf_3.txt:Wensday
inner_dir_1/tf_3.txt:Thursday
inner_dir_1/tf_3.txt:the sec 2
inner_dir_1/tf_3.txt:the SeCoNd 2
inner_dir_1/tF_5.txt:1
inner_dir_1/tF_5.txt:2
inner_dir_1/tF_5.txt:3
inner_dir_1/tF_5.txt:4
inner_dir_1/tF_5.txt:5
inner_dir_1/tF_5.txt:6
inner_dir_1/tF_5.txt:7
inner_dir_1/tF_5.txt:8
inner_dir_1/tF_5.txt:9
inner_dir_1/tF_5.txt:10
inner_dir_1/tF_5.txt:11
inner_dir_1/tF_5.txt:12
inner_dir_1/tF_5.txt:13
tf_2.txt:the first 1
tf_2.txt:the third 3
tf_2.txt:the sec 3
tf_2.txt:the seConD 2
tf_6.txt:

```
-v - исключает строки, содержащие шаблон

## 32. Найти только название и путь к файлам где нет комбинации "second"
```
nikol@DESKTOP-A1PNQL6 MINGW64 ~/git/terminal2/dir_1
$ grep -rlv 'second' *
inner_dir_1/tf_3.txt
inner_dir_1/tF_5.txt
tf_2.txt
tf_6.txt
```
-l атрибут котроый выводит имена файлов

## 33. Вывести в терминал 4 последних строк любого текстового файла
```
nikol@DESKTOP-A1PNQL6 MINGW64 ~/git/terminal2/dir_1
$ tail -n 4 inner_dir_1/tF_5.txt
10
11
12
13
```

## 34. Вывести в терминал 4 первые строки любого текстового файла.
```
nikol@DESKTOP-A1PNQL6 MINGW64 ~/git/terminal2/dir_1
$ head -n 4 inner_dir_1/tF_5.txt
1
2
3
4
```
## 35. Команда в одну строку. Создать папку и создать текстовый файл с содержиммым
```
nikol@DESKTOP-A1PNQL6 MINGW64 ~/git/terminal2/dir_1
$ mkdir inner_dir_2 && echo "test^C>> tf_8.txt
```
## 36. Команда в одну строку. Переместить в любую одну папку текстовые файлы у которых в содержимом есть слово “sec”
```
nikol@DESKTOP-A1PNQL6 MINGW64 ~/git/terminal2/dir_1
$ grep -lr sec * | xargs mv -t inner_dir_2/
```

## 37. Команда в одну строку. Скопировать в любую одну папку текстовые файлы у которых в содержимом есть слово “sec”
```
nikol@DESKTOP-A1PNQL6 MINGW64 ~/git/terminal2/dir_1
$ grep -lr sec * | xargs cp -t inner_dir_1/
```
## 38. Команда в одну строку. Найти все строки c "sec" во всех текстовых файлах, скопировать и вставить эти строки в один новый созданный текстовый файл.
```
nikol@DESKTOP-A1PNQL6 MINGW64 ~/git/terminal2/dir_1
$ grep -rh sec > tf_sec.txt
```
## 39. Команда в одну строку. Удалить текстовые файлы у которых в содержимом есть слово "sec"
```
nikol@DESKTOP-A1PNQL6 MINGW64 ~/git/terminal2/dir_1
$ grep -rlw sec | xargs rm
```
## 40. Просто вывести в терминал строку "Good job!!"
```
nikol@DESKTOP-A1PNQL6 MINGW64 ~/git/terminal2/dir_1
$ echo 'Good job!!'
Good job!!
```
