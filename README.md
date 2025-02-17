## <img src="https://raw.githubusercontent.com/Tarikul-Islam-Anik/Animated-Fluent-Emojis/master/Emojis/Objects/Pager.png" alt="Pager" width="25" height="25" /> Работа с bash

Выполнил базовые команды, работая с терминалом в Visual Studio Code. Поработал над созданием, перемещением, редактированием, удалением файлов, а также доступ к веб-ресурсам.

### Артефакты:

#### Задача 1 [(команды в txt-файле)](https://github.com/khramovich/git_bash/blob/main/bash1.txt)
```bash
cd                                                                                 # Открываем домашнюю директорию

pwd                                                                                # Определяем имя папки, в которой находимся

mkdir test1                                                                        # Создаем в этой папке каталог test1

cd test1                                                                           # Переходим в папку test1

touch {1,2,3}.txt                                                                  # Создаем файлы 1, 2 и 3 внутри папки test1

ls                                                                                 # Проверяем содержимое папки test1

cd                                                                                 # Переходим в домашнюю директорию

mkdir test2                                                                        # Создаем в домашней директории папку test2

rmdir test2                                                                        # Удаляем папку

rm test1/2.txt                                                                     # Удаляем файл 2 из папки test1

mkdir test3 && touch test3/{1,2}.txt                                               # Создаем в домашней директории папку test3 и добавляем в нее два файла

rm -r test3                                                                        # Удаляем папку test3

mkdir test4                                                                        # Создаем в домашней директории папку test4

mv test1/{1,3}.txt test4                                                           # Перемещаем файлы 1 и 3 из папки test1 в папку test4

echo line > test4/1.txt && echo line >> test4/1.txt && echo line >> test4/1.txt    # Добавляем в файл 1 три строки со словами line

cat test4/1.txt                                                                    # Смотрим содержимое файла 1

echo line > test4/3.txt && echo line >> test4/3.txt && echo line >> test4/3.txt    # Добавляем в файл 3 три строки со словами line

cat {test4/1,test4/3}.txt                                                          # Смотрим содержимое двух файлов (1 и 3) сразу

echo "QA is my life" > test4/1.txt                                                 # Заменяем все строки в файле 1 
```

#### Задача 2 [(команды в txt-файле)](https://github.com/khramovich/git_bash/blob/main/bash2.txt)
```bash
cd                                                                                                 # Открываем домашнюю директорию

mkdir test3                                                                                        # Создаем в домашней директории папку test3

touch test3/{4,5,6}.txt && { echo row1; echo row2; echo row3; echo row4; } | tee test3/{4,5,6}.txt # Добавляем в папку test3 три файла (4, 5 и 6), в каждом из которых должно быть по 4 строки (row1, row2, row3, row4)

grep "row2" test3/5.txt                                                                            # Находим строку row2 в файле 5

grep -r "row" test3                                                                                # Находим строку row в папке test3

grep -c "row" test3/6.txt                                                                          # Считаем, сколько строк с содержимым row в файле 6

find test3 -name "5.txt"                                                                           # Находим файл 5 внутри папки test3

find test3 -name "5.txt" -exec rm {} \;                                                            # Используя команду find, удаляем файл 5

echo test > test3/4.txt                                                                            # Используя команду echo, добавляем слово test в файл 4

echo fail > test3/4.txt                                                                            # Заменяем слово test в файле 4 на fail

echo test >> test3/4.txt                                                                           # Добавляем в файл 4 слово test так, чтобы сохранилось содержимое

ps aux                                                                                             # Смотрим все процессы для юзеров, которые происходят в системе, не только в консоли

kill 666                                                                                           # Убиваем процесс 666 в консоли

ping rusau.net                                                                                     # Узнаем доступность ресурса rusau.net, используя команду ping

ping -c 5 rusau.net                                                                                # Отправляем 5 пакетов на сайт rusau.net

curl -X 'GET                                                                                       # Команда для получения информации о питомцах со всеми доступными статусами
'https://petstore.swagger.io/v2/pet/findByStatus?status=sold%2Cavailable%2Cpending'                

curl -X 'POST' \                                                                                   # Создаем нового пользователя через POST-запрос
  'https://petstore.swagger.io/v2/user' \
  -H 'accept: application/json' \
  -H 'Content-Type: application/json' \
  -d '{
  "id": 9999999999,
  "username": "khramovich",
  "firstName": "Roman",
  "lastName": "Khramovich",
  "email": "roman@khramovich.ru",
  "password": "p3tsTore*1",
  "phone": "777",
  "userStatus": 1
}'
```
