## Task 1 — Работа в консольке
---
```
1. Переместиться между директориями: 
[bob@host-3 ~]$ cd Видео
[bob@host-3 Видео]$
---
2. Вывести список файлов в директории:
[bob@host-3 Видео]$ cd ~  (переместились в домашнюю директорию из-за отсутствия каких-либо файлов в директории Видео)
[bob@host-3 ~]$ ls
 Practice   Видео       Загрузки      Музыка         'Рабочий стол'
 Test       Документы   Изображения   Общедоступные   Шаблоны
---
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
---
4. Создать папку с подпапками
[bob@host-3 ~]$ mkdir -p first_dir/second_dir/third_dir/fourth_dir 
[bob@host-3 ~]$ ls
 first_dir   Test    Документы   Изображения   Общедоступные   Шаблоны
 Practice    Видео   Загрузки    Музыка       'Рабочий стол'
[bob@host-3 ~]$ cd first_dir
[bob@host-3 first_dir]$ ls
second_dir
[bob@host-3 first_dir]$
(можно было создать папку и в ней две папки на одном уровне одной командой: mkdir -p -- dir/dir_2 dir/dir_3 - просто пример)

5. 
