michel@MichelUbuntu:~$ export GITHUB_USERNAME=MichelsonIU815
michel@MichelUbuntu:~$ export GIST_TOKEN=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
michel@MichelUbuntu:~$ alias edit=nano
michel@MichelUbuntu:~$ mkdir -p ${GITHUB_USERNAME}/workspace
michel@MichelUbuntu:~$ cd ${GITHUB_USERNAME}/workspace
michel@MichelUbuntu:~/MichelsonIU815/workspace$ pwd
/home/michel/MichelsonIU815/workspace
michel@MichelUbuntu:~/MichelsonIU815/workspace$ cd ..
michel@MichelUbuntu:~/MichelsonIU815$ pwd
/home/michel/MichelsonIU815
michel@MichelUbuntu:~/MichelsonIU815$ mkdir -p workspace/tasks/
michel@MichelUbuntu:~/MichelsonIU815$ mkdir -p workspace/projects/
michel@MichelUbuntu:~/MichelsonIU815$ mkdir -p workspace/reports/
michel@MichelUbuntu:~/MichelsonIU815$ cd workspace
michel@MichelUbuntu:~/MichelsonIU815/workspace$ wget https://nodejs.org/dist/v6.11.5/node-v6.11.5-linux-x64.tar.xz
--2025-02-21 20:14:41--  https://nodejs.org/dist/v6.11.5/node-v6.11.5-linux-x64.tar.xz
Распознаётся nodejs.org (nodejs.org)… 104.20.23.46, 104.20.22.46, 2606:4700:10::6814:172e, ...
Подключение к nodejs.org (nodejs.org)|104.20.23.46|:443... соединение установлено.
HTTP-запрос отправлен. Ожидание ответа… 200 OK
Длина: 9356460 (8,9M) [application/x-xz]
Сохранение в: ‘node-v6.11.5-linux-x64.tar.xz’

node-v6.11.5-linux-x64.t 100%[================================>]   8,92M  6,27MB/s    за 1,4s    

2025-02-21 20:14:43 (6,27 MB/s) - ‘node-v6.11.5-linux-x64.tar.xz’ сохранён [9356460/9356460]

michel@MichelUbuntu:~/MichelsonIU815/workspace$ tar -xf node-v6.11.5-linux-x64.tar.xz
michel@MichelUbuntu:~/MichelsonIU815/workspace$ rm -rf node-v6.11.5-linux-x64.tar.xz
michel@MichelUbuntu:~/MichelsonIU815/workspace$ mv node-v6.11.5-linux-x64 node
michel@MichelUbuntu:~/MichelsonIU815/workspace$ ls node/bin
node  npm
michel@MichelUbuntu:~/MichelsonIU815/workspace$ echo ${PATH}
/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin:/snap/bin
michel@MichelUbuntu:~/MichelsonIU815/workspace$ export PATH=${PATH}:`pwd`/node/bin
michel@MichelUbuntu:~/MichelsonIU815/workspace$ echo ${PATH}
/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin:/snap/bin:/home/michel/MichelsonIU815/workspace/node/bin
michel@MichelUbuntu:~/MichelsonIU815/workspace$ mkdir scripts
michel@MichelUbuntu:~/MichelsonIU815/workspace$ cat > scripts/activate<<EOF
> export PATH=\${PATH}:`pwd`/node/bin
> EOF
michel@MichelUbuntu:~/MichelsonIU815/workspace$ source scripts/activate
michel@MichelUbuntu:~/MichelsonIU815/workspace$ gem install gist
Successfully installed gist-6.0.0
1 gem installed
michel@MichelUbuntu:~/MichelsonIU815/workspace$ (umask 0077 && echo ${GIST_TOKEN} > ~/.gist)
michel@MichelUbuntu:~/MichelsonIU815/workspace$ export LAB_NUMBER=01
michel@MichelUbuntu:~/MichelsonIU815/workspace$ git clone https://github.com/tp-labs/lab${LAB_NUMBER} tasks/lab${LAB_NUMBER}
Клонирование в «tasks/lab01»...
remote: Enumerating objects: 74, done.
remote: Counting objects: 100% (3/3), done.
remote: Compressing objects: 100% (3/3), done.
remote: Total 74 (delta 0), reused 1 (delta 0), pack-reused 71 (from 1)
Получение объектов: 100% (74/74), 945.07 КиБ | 3.01 МиБ/с, готово.
Определение изменений: 100% (20/20), готово.
michel@MichelUbuntu:~/MichelsonIU815/workspace$ mkdir reports/lab${LAB_NUMBER}
michel@MichelUbuntu:~/MichelsonIU815/workspace$ cp tasks/lab${LAB_NUMBER}/README.md reports/lab${LAB_NUMBER}/REPORT.md
michel@MichelUbuntu:~/MichelsonIU815/workspace$ cd reports/lab${LAB_NUMBER}
michel@MichelUbuntu:~/MichelsonIU815/workspace/reports/lab01$ edit REPORT.md
michel@MichelUbuntu:~/MichelsonIU815/workspace/reports/lab01$ gist REPORT.md
Команда «gist» не найдена, но может быть установлена с помощью:
sudo apt install yorick
michel@MichelUbuntu:~/MichelsonIU815/workspace/reports/lab01$ sudo apt install yorick
[sudo] пароль для michel: 
Чтение списков пакетов… Готово
Построение дерева зависимостей… Готово
Чтение информации о состоянии… Готово         
Будут установлены следующие дополнительные пакеты:
  rlwrap yorick-data yorick-z
Предлагаемые пакеты:
  yorick-full yorick-mpy-openmpi | yorick-mpy-mpich2 emacsen curl
Следующие НОВЫЕ пакеты будут установлены:
  rlwrap yorick yorick-data yorick-z
Обновлено 0 пакетов, установлено 4 новых пакетов, для удаления отмечено 0 пакетов, и 0 пакетов не обновлено.
Необходимо скачать 1 443 kB архивов.
После данной операции объём занятого дискового пространства возрастёт на 4 538 kB.
Хотите продолжить? [Д/н] y
Пол:1 http://archive.ubuntu.com/ubuntu noble/universe amd64 rlwrap amd64 0.46.1-1build2 [107 kB]
Пол:2 http://archive.ubuntu.com/ubuntu noble/universe amd64 yorick-data all 2.2.04+dfsg1-12build3 [505 kB]
Пол:3 http://archive.ubuntu.com/ubuntu noble/universe amd64 yorick amd64 2.2.04+dfsg1-12build3 [795 kB]
Пол:4 http://archive.ubuntu.com/ubuntu noble/universe amd64 yorick-z amd64 1.2.0+cvs20080115-5.1build2 [36,7 kB]
Получено 1 443 kB за 3с (573 kB/s)         
Выбор ранее не выбранного пакета rlwrap.
(Чтение базы данных … на данный момент установлено 195360 файлов и каталогов.)
Подготовка к распаковке …/rlwrap_0.46.1-1build2_amd64.deb …
Распаковывается rlwrap (0.46.1-1build2) …
Выбор ранее не выбранного пакета yorick-data.
Подготовка к распаковке …/yorick-data_2.2.04+dfsg1-12build3_all.deb …
Распаковывается yorick-data (2.2.04+dfsg1-12build3) …
Выбор ранее не выбранного пакета yorick.
Подготовка к распаковке …/yorick_2.2.04+dfsg1-12build3_amd64.deb …
Распаковывается yorick (2.2.04+dfsg1-12build3) …
Выбор ранее не выбранного пакета yorick-z.
Подготовка к распаковке …/yorick-z_1.2.0+cvs20080115-5.1build2_amd64.deb …
Распаковывается yorick-z (1.2.0+cvs20080115-5.1build2) …
Настраивается пакет yorick-data (2.2.04+dfsg1-12build3) …
Настраивается пакет rlwrap (0.46.1-1build2) …
update-alternatives: используется /usr/bin/rlwrap для предоставления /usr/bin/readline-editor (rea
dline-editor) в автоматическом режиме
/usr/share/rlwrap/filters/ftp_filter.py:57: SyntaxWarning: invalid escape sequence '\s'
  results = [re.split('\s+', l)[dir_filename_column[where]] for l in lines]
/usr/share/rlwrap/filters/ftp_filter.py:100: SyntaxWarning: invalid escape sequence '\s'
  nwords = len(re.split('\s+', line))
/usr/share/rlwrap/filters/ftp_filter.py:108: SyntaxWarning: invalid escape sequence '\s'
  command = re.search('\s*(\S+)', line).group(1)
/usr/share/rlwrap/filters/rlwrapfilter.py:4: SyntaxWarning: invalid escape sequence '\s'
  """
/usr/share/rlwrap/filters/rlwrapfilter.py:211: SyntaxWarning: invalid escape sequence '\S'
  m = re.match("(\S+) (.*?)\r?\n", sys.stdin.readline())
Настраивается пакет yorick (2.2.04+dfsg1-12build3) …
Настраивается пакет yorick-z (1.2.0+cvs20080115-5.1build2) …
Обрабатываются триггеры для man-db (2.12.0-4build2) …
Обрабатываются триггеры для install-info (7.1-3build2) …
michel@MichelUbuntu:~/MichelsonIU815/workspace/reports/lab01$ gist REPORT.md
gist: (WARNING) fread failed (command) on CGM file REPORT.md
gist: (WARNING) BEGIN METAFILE element missing
gist: (WARNING) REPORT.md is not a binary CGM, cannot open
