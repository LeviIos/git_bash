# Работа с командами в git_bash

## Задание 1.
1.Открыть домашнюю директорию через терминал

cd ~

2.Определить имя папки, в которой вы находитесь

pwd

3.Создать внутри этой папки каталог с именем test1

mkdir test1

4.Перейти в папку test1

cd test1

5.Создать файл 1,2 и 3 внутри каталога test1

touch 1.txt 2.txt 3.txt

6.Проверить содержимое каталога test1

ls

7.Перейти в домашнюю директорию

cd 

8.Создать папку test2 внутри домашней директории

mkdir test2 

9.Удалить папку test2

rmdir test2 

10.Удалить файл 2 из папки test1

cd test1

rm 2

11.Создать папку в домашней директории test3 и добавить в нее два файла

cd
mkdir test3
cd test3
touch file1 file2

12.Удалить папку test3

cd
rm -r test3

13.Создать папку test4 в домашней директории

mkdir test4

14.Переместить файлы 1 и 3 из папки test1 в папку test4

mv test1/1 test1/3 TEST4/

15.Добавить в файл 1 три строки со словами line

echo line >> 1.txt 
echo line >> 1.txt 
echo line >> 1.txt 

16.Посмотреть содержимое файла 1

cat 1.txt 

17.Добавьте в файл 3 три строки со словами line

echo line >> 3.txt 
echo line >> 3.txt 
echo line >> 3.txt

18.Просмотрите содержимое двух файлов (1 и 3) сразу

cat 3.txt

19.Используя один из редакторов замените все строки в файле 1

nano 1.txt 

1
2
3

CTRL+O
Enter
CTRL+X

## Задание 2.

1.Зайти в домашнюю директорию через терминал.

cd

2.Создать папку test 3

mkdir test3

3.Добавить в папку test 3 три файла 4, 5 и 6, в каждом из которых должно быть по 4 строки row1, row2, row3, row4

cd test3 
echo -e "row1\nrow2\nrow3\nrow4" > 4.txt 
echo -e "row1\nrow2\nrow3\nrow4" > 5.txt 
echo -e "row1\nrow2\nrow3\nrow4" > 6.txt

4.Найдите строку row2 в файле 5

grep "row2" 5.txt

5.Найдите строку row в папке test3

grep -r "row" 

6.Посчитайте сколько строк с содержимым row в файле 6

grep -c "row" 6

7.Найдите файл 5 внутри папки test3

find . -name "5"

8.Используя команду find, удалите файл 5

find . -name "5.txt" -delete 

9.Используя команду echo, добавьте слово test в файл 4 (без сохранения содержимого)

echo test > 4.txt

10.Замените слово test в файле 4 на fail

sed 's/test/fail/g' 4.txt

11.Добавьте в файл 4 слово test так, чтобы сохранилось содержимое

echo "test" >> 4

12.Просмотрите все процессы для юзеров не только в консоли, которые происходят в системе

ps aux 

13.Убейте процесс 666 в консоли (можно не убивать, а просто написать команду)

kill 666

14.Узнайте доступность ресурса rusau.net, используя ping

ping rusau.net

15.Отправьте 5 пакетов на сайт rusau.net

ping -c 5 rusau.net

16.Используя GET и команду curl, получите информацию о зарегистрированных питомцах с любым статусом на https://petstore.swagger.io/

curl -X GET "https://petstore.swagger.io/v2/pet/findByStatus?status=available&status=pending&status=sold" -H "accept: application/json"

17.Используя POST и команду curl, создайте нового пользователя на https://petstore.swagger.io/

curl -X POST "https://petstore.swagger.io/v2/user" \
  -H "accept: application/json" \
  -H "Content-Type: application/json" \
  -d '{
    "id": 1,
    "username": "Bacon",
    "firstName": "Bibi",
    "lastName": "Volkman",
    "email": "Darrel_Volkman80@gmail.com",
    "password": "g8kq2W1z_utLEBs",
    "phone": "7442783865",
    "userStatus": 0
}'
