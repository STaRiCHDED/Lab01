## Laboratory work I

<a href="https://yandex.ru/efir/?stream_id=vsVJzkz4i9-s"><img src="https://raw.githubusercontent.com/tp-labs/lab01/master/preview.png" width="640"/></a>

Данная лабораторная работа посвещена изучению утилит для разработки проектов

## Tasks

- [X] 1. Ознакомиться со ссылками учебного материала
- [X] 2. Выполнить инструкцию учебного материала
- [X] 3. Составить отчет и отправить ссылку личным сообщением в **Slack**

## Tutorial

```bash
$ export GITHUB_USERNAME=STaRiCHDED
$ export GIST_TOKEN=d2ec6676c8442772309726a5c0cb4e1fc967f9f7
$ alias edit=subl
```

```sh
$ mkdir -p ${GITHUB_USERNAME}/workspace
$ cd ${GITHUB_USERNAME}/workspace
$ pwd
/home/nikitaklimov/STaRiCHDED/workspace
$ cd ..
$ pwd
/home/nikitaklimov/STaRiCHDED
```

```sh
$ mkdir -p workspace/tasks/
$ mkdir -p workspace/projects/
$ mkdir -p workspace/reports/
$ cd workspace
```

```sh
# Debian
$ wget https://nodejs.org/dist/v6.11.5/node-v6.11.5-linux-x64.tar.xz
--2020-06-01 18:42:26--  https://nodejs.org/dist/v6.11.5/node-v6.11.5-linux-x64.tar.xz
Распознаётся nodejs.org (nodejs.org)… 104.20.23.46, 104.20.22.46, 2606:4700:10::6814:172e, ...
Подключение к nodejs.org (nodejs.org)|104.20.23.46|:443... соединение установлено.
HTTP-запрос отправлен. Ожидание ответа… 200 OK
Длина: 9356460 (8,9M) [application/x-xz]
Сохранение в: «node-v6.11.5-linux-x64.tar.xz»

node-v6.11.5-linux- 100%[===================>]   8,92M  4,29MB/s    за 2,1s    

2020-06-01 18:42:28 (4,29 MB/s) - «node-v6.11.5-linux-x64.tar.xz» сохранён [9356460/9356460]

$ tar -xf node-v6.11.5-linux-x64.tar.xz
$ rm -rf node-v6.11.5-linux-x64.tar.xz
$ mv node-v6.11.5-linux-x64 node
```

```sh
$ ls node/bin
node  npm
$ echo ${PATH}
/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin
$ export PATH=${PATH}:`pwd`/node/bin
$ echo ${PATH}
/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin:/home/nikitaklimov/STaRiCHDED/workspace/node/bin
$ mkdir scripts
$ cat > scripts/activate<<EOF
export PATH=\${PATH}:`pwd`/node/bin
EOF
$ source scripts/activate
```

```sh
$ sudo apt install gist
```

```sh
$ (umask 0077 && echo ${GIST_TOKEN} > ~/.gist)
```

## Report

```sh
$ export LAB_NUMBER=01
$ git clone https://github.com/tp-labs/lab${LAB_NUMBER} tasks/lab${LAB_NUMBER}
Клонирование в «tasks/lab01»…
remote: Enumerating objects: 71, done.
remote: Total 71 (delta 0), reused 0 (delta 0), pack-reused 71
Распаковка объектов: 100% (71/71), готово.
$ mkdir reports/lab${LAB_NUMBER}
$ cp tasks/lab${LAB_NUMBER}/README.md reports/lab${LAB_NUMBER}/REPORT.md
$ cd reports/lab${LAB_NUMBER}
$ edit REPORT.md
$ gist REPORT.md
```

## Links

### Unix commands

- [ar](https://en.wikipedia.org/wiki/Ar_(Unix))
- [cat](https://en.wikipedia.org/wiki/Cat_(Unix))
- [cd](https://en.wikipedia.org/wiki/Cd_(command))
- [cp](https://en.wikipedia.org/wiki/Cp_(Unix))
- [cut](https://en.wikipedia.org/wiki/Cut_(Unix))
- [echo](https://en.wikipedia.org/wiki/Echo_(command))
- [env](https://en.wikipedia.org/wiki/Env_(shell))
- [ex](https://en.wikipedia.org/wiki/Ex_(editor))
- [file](https://en.wikipedia.org/wiki/File_(command))
- [find](https://en.wikipedia.org/wiki/Find)
- [ls](https://en.wikipedia.org/wiki/Ls)
- [man](https://en.wikipedia.org/wiki/Man_page)
- [mkdir](https://en.wikipedia.org/wiki/Mkdir)
- [mv](https://en.wikipedia.org/wiki/Mv)
- [nm](https://en.wikipedia.org/wiki/Nm_(Unix))
- [ps](https://en.wikipedia.org/wiki/Ps_(Unix))
- [pwd](https://en.wikipedia.org/wiki/Pwd)
- [rm](https://en.wikipedia.org/wiki/Rm_(Unix))
- [sed](https://en.wikipedia.org/wiki/Sed)
- [touch](https://en.wikipedia.org/wiki/Touch_(Unix))

### Package Managers

- [apt](http://help.ubuntu.ru/wiki/apt) | [dnf](https://en.wikipedia.org/wiki/DNF_(software)) | [yum](https://fedoraproject.org/wiki/Yum/ru)
- [brew](https://brew.sh) | [linuxbrew](http://linuxbrew.sh)
- [npm](https://docs.npmjs.com)

### Software

- [curl](https://www.gitbook.com/book/bagder/everything-curl/details)
- [wget](https://www.gnu.org/software/wget/manual/wget.pdf)
- [clang](https://clang.llvm.org)
- [g++](https://gcc.gnu.org/onlinedocs/gcc-4.0.2/gcc/G_002b_002b-and-GCC.html)
- [make](https://en.wikipedia.org/wiki/Make_(software))
- [open](https://developer.apple.com/legacy/library/documentation/Darwin/Reference/ManPages/man1/open.1.html)
- [openssl](https://www.openssl.org)
- [nano](https://www.nano-editor.org)
- [tree](https://linux.die.net/man/1/tree)
- [vim](http://www.vim.org)

## Homework

- [x] 1. Скачайте библиотеку *boost* с помощью утилиты **wget**. Адрес для скачивания `https://sourceforge.net/projects/boost/files/boost/1.69.0/boost_1_69_0.tar.gz`.
- [x] 2. Разархивируйте скаченный файл в директорию `~/boost_1_69_0`
- [x] 3. Подсчитайте количество файлов в директории `~/boost_1_69_0` **не включая** вложенные директории.
- [x] 4. Подсчитайте количество файлов в директории `~/boost_1_69_0` **включая** вложенные директории.
- [x] 5. Подсчитайте количество заголовочных файлов, файлов с расширением `.cpp`, сколько остальных файлов (не заголовочных и не `.cpp`).
- [x] 6. Найдите полный пусть до файла `any.hpp` внутри библиотеки *boost*.
- [x] 7. Выведите в консоль все файлы, где упоминается последовательность `boost::asio`.
- [x] 8. Скомпилирутйе *boost*. Можно воспользоваться [инструкцией](https://www.boost.org/doc/libs/1_61_0/more/getting_started/unix-variants.html#or-build-custom-binaries) или [ссылкой](https://codeyarns.com/2017/01/24/how-to-build-boost-on-linux/).
- [x] 9. Перенесите все скомпилированные на предыдущем шаге статические библиотеки в директорию `~/boost-libs`.
- [x] 10. Подсчитайте сколько занимает дискового пространства каждый файл в этой директории.
- [x] 11. Найдите *топ10* самых "тяжёлых".

#Homework
```sh
1.
$ wget https://sourceforge.net/projects/boost/files/boost/1.69.0/boost_1_69_0.tar.gz
2.
$ tar -xf boost_1_69_0.tar.gz
$ cd boost_1_69_0 
$ pwd
/home/nikitaklimov/boost_1_69_0
3.
$ ls -f . | wc -l # Считаем количество файлов в **boost**
20
4.
$ find . -type f | wc -l 
61191
5.
$ find . -type f -name '*.h' | wc -l # Находим все файлы с расширением '*.h' (заголовочный файл)
296
$ find . -type f -name '*.cpp' | wc -l # Находим все файлы с расширением '*.сpp' (файл C++)
13774
$ find . -type f '!' -name '*.cpp' -a '!' -name '*.cpp' | wc -l # Находим все остальные файлы
47417
6.
$ find . -type f -name 'any.hpp' # Полный путь до файла 'any.hpp'
./boost/hana/any.hpp
./boost/hana/fwd/any.hpp
./boost/fusion/include/any.hpp
./boost/fusion/algorithm/query/detail/any.hpp
./boost/fusion/algorithm/query/any.hpp
./boost/type_erasure/any.hpp
./boost/spirit/home/support/algorithm/any.hpp
./boost/any.hpp
./boost/proto/detail/any.hpp
./boost/xpressive/detail/utility/any.hpp
7.
$ find . -type f -exec grep -iH "boost::asio" {} \; # Выводит все файлы в которых упоминается последовательность "boost::asio"
8.
$ ./boost.sh
$ ./b2 —prefix=<DEST>
9.
$ find . -name "*.so.*" # Выведет все скомпилированные статические библиотеки
$ find . -name "*.so.*" -exec mv {} ../boost-libs \; # Переместит все скомпилированные статические библиотеки по адресу ../boost-libs
10.
$ find . type -f -exec du -h {} +; # Подсчитаем сколько занимает дискового пространства каждый файл в этой директории
100K ./libboost_stacktrace_basic.a
2,4M ./libboost_wave.dylib
7,8M ./libboost_math_tr1.a
5,4M ./libboost_python27.a 164K ./libboost_thread.dylib 100K ./libboost_math_c99f.dylib
480K ./libboost_$
1,9M ./libboost_math_c99f.a
1,8M ./libboost_math_c99l.a
1,3M ./libboost_iostreams.a
1,1M ./libboost_thread.a
7,3M ./libboost_program_options.a
188K ./libboost_iostreams.dylib
300K ./libboost_coroutine.a
276K ./libboost_timer.a
412K ./libboost_wserialization.dylib 940K ./libboost_contract.a
172K ./libboost_contract.dylib 892K ./libboost_numpy27.a
740K ./libboost_type_erasure.a
21M ./libboost_log_setup.a
16K ./libboost_atomic.a
208K ./libboost_random.a
104K ./libboost_prg_exec_monitor.dylib 528K ./libboost_date_time.a
648K ./libboost_graph.dylib
828K ./libboost_locale.dylib
11.
$ find . type -f -exec du -h {} +|sort -rh | head -n 10 # тoп 10 самых "тяжёлых"
28M ./libboost_wave.a
21M ./libboost_log_setup.a
20M ./libboost_log.a
16M ./libboost_test_exec_monitor.a
15M ./libboost_unit_test_framework.a
9,1M ./libboost_locale.a
8,9M ./libboost_regex.a
8,1M ./libboost_math_tr1f.a
7,8M ./libboost_math_tr1.a
7,7M ./libboost_math_tr1l.a
```

```sh
Copyright (c) 2015-2020 The ISC Authors
```
