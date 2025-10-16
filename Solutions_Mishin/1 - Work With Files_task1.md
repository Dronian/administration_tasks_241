## Task 1 — Работа в консольке
```
1. Переместиться между директориями: 
[bob@host-3 ~]$ cd Видео
[bob@host-3 Видео]$

2. Вывести список файлов в директории:
[bob@host-3 Видео]$ cd ~  (Переместились в домашнюю директорию из-за отсутствия каких-либо файлов в директории Видео)
[bob@host-3 ~]$ ls
 Practice   Видео       Загрузки      Музыка         'Рабочий стол'
 Test       Документы   Изображения   Общедоступные   Шаблоны
[bob@host-3 ~]$

3. Вывести список Всех файлов в директории
[bob@host-3 ~]$ ls -a
 .               .mutt                                      .xprofile
 ..              Practice                                   .xsession.d
 .bash_history   .rpmmacros                                 Видео
 .bash_logout    .ssh                                       Документы
 .bash_profile   Test                                       Загрузки
 .bashrc         .vboxclient-clipboard-tty2-control.pid     Изображения
 .cache          .vboxclient-clipboard-tty2-service.pid     Музыка
 .config         .vboxclient-draganddrop-tty2-control.pid   Общедоступные
 .gnupg          .vboxclient-hostversion-tty2-control.pid  'Рабочий стол'
 .local          .vboxclient-seamless-tty2-control.pid      Шаблоны
 .lpoptions      .viminfo
[bob@host-3 ~]$

4. Создать папку с подпапками
[bob@host-3 ~]$ mkdir -p first_dir/second_dir/third_dir/fourth_dir 
[bob@host-3 ~]$ ls
 first_dir   Test    Документы   Изображения   Общедоступные   Шаблоны
 Practice    Видео   Загрузки    Музыка       'Рабочий стол'
[bob@host-3 ~]$ cd first_dir
[bob@host-3 first_dir]$ ls
second_dir
[bob@host-3 first_dir]$
И так далее...
(Можно было создать папку и в ней две папки на одном уровне одной командой: mkdir -p -- dir/dir_2 dir/dir_3 - просто пример)

5. Внутри папки создать файлик и записать в него что-нибудь
[bob@host-3 ~]$ cd Practice
[bob@host-3 Practice]$ touch practice.txt  (Можно было и так: touch Practice/practice_2.txt)
[bob@host-3 Practice]$ vim practice.txt (Можно было через echo и >)
В vim'e было проделано следующее: i -> ввели текст -> esc -> :wq
[bob@host-3 Practice]$ cat practice.txt
QuickSort - это база. Спасибо Хоару за победу!
[bob@host-3 Practice]$

6. Переместить файл из одно директории в другую
[bob@host-3 ~]$ mv Practice/practice.txt Документы  (Действия из домашней директории для удобства)
[bob@host-3 ~]$ cd Документы
[bob@host-3 Документы]$ ls
practice.txt
[bob@host-3 Документы]$

7. Скопировать файл из одной директории в другую
[bob@host-3 Документы]$ cp practice.txt /home/bob/Practice
[bob@host-3 Документы]$ cd ..
[bob@host-3 ~]$ cd Practice
[bob@host-3 Practice]$ ls
practice_2.txt  practice.txt  practice.txt~
[bob@host-3 Practice]$ cd ..
[bob@host-3 ~]$ cd Документы
[bob@host-3 Документы]$ ls
practice.txt
[bob@host-3 Документы]$

8. Переименовать файл
[bob@host-3 Документы]$ mv practice.txt new_practice.txt
[bob@host-3 Документы]$ ls
new_practice.txt
[bob@host-3 Документы]$ 

9. Сравнить содержимое файла
[bob@host-3 Документы]$ diff new_practice.txt /home/bob/Practice/practice.txt
[bob@host-3 Документы]$ (Ничего не вывелось - значит файлы равны)
[bob@host-3 Документы]$ diff -s new_practice.txt /home/bob/Practice/practice.txt
Файлы new_practice.txt и /home/bob/Practice/practice.txt идентичны  (Действительно! Флаг -s сообщает о идентичных файлах)
[bob@host-3 Документы]$

10. Отсортировать содержимое файла по возрастанию и убыванию (Можно были и короче, но для наглядности это того стоило)
[bob@host-3 Документы]$ touch example.txt
[bob@host-3 Документы]$ nano example.txt 
[bob@host-3 Документы]$ cat nano example.txt
QuickSort
-
это
база
.
Если
вы 
не 
согласны
...

[bob@host-3 Документы]$ sort example.txt -o sorted_example.txt (Можно было через > или так: sort -o sorted_example.txt example.txt)
[bob@host-3 Документы]$ cat sorted_example.txt

-
.
...
QuickSort
база
вы 
Если
не 
согласны
это
[bob@host-3 Документы]$ sort -r example.txt -o revsorted_example.txt (Аналогично пред. sort)
[bob@host-3 Документы]$ cat revsorted_example.txt 
это
согласны
не 
Если
вы 
база
QuickSort
...
.
-
[bob@host-3 Документы]$

11. Удалить все папки и файлы
[bob@host-3 Документы]$ cd ~
[bob@host-3 ~]$ rm -rf Practice  (Каталог Practice можно было увидеть до этого, в пред. пунктах. Теперь он удалён) 
[bob@host-3 ~]$ ls
 Test    Документы   Изображения   Общедоступные   Шаблоны
 Видео   Загрузки    Музыка       'Рабочий стол'
[bob@host-3 ~]$ rm -rf Test  (Для примера ещё один каталог)
[bob@host-3 ~]$ ls
 Видео       Загрузки      Музыка         'Рабочий стол'
 Документы   Изображения   Общедоступные   Шаблоны
[bob@host-3 ~]$ 
```
