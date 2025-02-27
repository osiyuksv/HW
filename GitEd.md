# Работа с Git
## Работа с удалёнными репозиториями в git
### Создание нового удалённого репозитория в GitHub и перенос в него наш локальный репозиторий
1.	Создаём новую папку с локальным репозиторием в git
2.	git status – проверяем, что в локальном репозитории ничего нет
3.	git init – инициализируем наш локальный репозиторий
4.	Создаём в локальном репозитории файл с раширением md
5.	Вносим контент в файл на git, и коммитимся
6.	Создаём свой новый виртуальный репо через плюс на GitHub
7.	Даём в GitHub имя удалённому репозиторию как вариант Test1
8.	Выбираем в GitHub вариант 2 …or push an existing repository from the command line
9.	git remote add origin https://github.com/osiyuksv/Test_Seminar3_HW.git – вводим команду в git (копируем строку отдельно, не все строки)
10.	git branch -M main – вводим команду в git (копируем строку отдельно, не все строки)
11.	git push -u origin main – вводим команду в git (копируем строку отдельно, не все строки)
12.	Обновляем удаленный репозиторий на GitHub и видим в нём наш файл перенесённый с локального репозитория из git, где отражена вся информация из последнего актуального коммита в git


### Обмен коммитами между локальным репозиторием в git и удалённым репозиторием в GitHub
#### Перенос коммита с GitHub в git
1.	В удалённом репозитории на GitHub вносим актуальные уточнения и коммитимся (напрямую или через другого пользователя)
2.	Открываем git c папкой с нашим локальным репозиторием, которая дружит с удалённым репозиторием в GitHub
3.	git pull – скачиваем актуальный commit из удаленного репо в локальный
4.	Видим в git наш файл с перенесёнными с удалённого репозитория из GitHub изменениями, где отражена вся информация из последнего актуального коммита в GitHub
#### Перенос коммита с git в GitHub
1.	В локальном репозитории в git вносим актуальные уточнения и коммитимся
2.	git push – пушим наш локальный репозиторий в удалённый на GitHub
3.	Открываем GitHub c папкой с нашим удалённым репозиторием, которая дружит с локальным репозиторием в git
4.	Обновляем в GitHub наш файл  и видим в нём перенесённые с удалённого репозитория из git изменения, где отражена вся информация из последнего актуального коммита в git
### Перенос удаленного актуального для нас репозитория из GitHub в наш локальный репозиторий в git (способ создание репозитория через git clone – аналог способу создания через git init)
1.	Создаём новую папку на нашем рабочем столе и называем её как вариант Seminar_3_HW
2.	Открываем её в git, но без init
3.	Открываем GitHub c папкой с удалённым репозиторием, который нам актуален, как вариант Test_Seminar3_HW
4.	Копируем в GitHub в этом удалённом репозитории ссылку / строку в кнопке Код
5.	Перед клонированием вызываем в терминале команду git status и убеждаемся, что у нас не настроен гит и мы без инита и локальный репозитоий пустой
6.	git clone link – открываем терминал в git и в нашем локальном репозитории (созданной пустой без инита папке) даём команду в git (git clone link (с скопированной ссылкой))
7.	Далее появилась новая папка после клонирования, в git мы видим перенесённую папку с файлом из GitHub
8.	При этом через гит статус по появившейся папке по-прежнему ошибка, потому что эта папка из GitHub с названием как в GitHub (Test_Seminar3_HW) и она находится внутри нашей локальной созданной на старте папке (Seminar_3_HW)
9.	cd Test_Seminar3_HW – change directory, меняем местоположение / дирректорию, чтобы перейти из созданной на старте папки Seminar_3_HW в директорию / папку Test_Seminar3_HW, перенесённую из удалённого репозитория в GitHub
10.	Проверяем через гит статус, что дирректория поменялась и ошибки больше нет, и здесь же поменялась выдача терминала – вместо ранее (Seminar_3_HW) сейчас стало (Test_Seminar3_HW)
11.	Теперь в (Test_Seminar3_HW) через гит лог можем посмотреть все сделанные ранее коммиты и можем перемещаться по каждому из этих коммитов, здесь же можем посмотреть лог графа, чтобы увидеть всю историю работы над этим файлом
12.	Мы можем продолжить работу в Test_Seminar3_HW и вносить изменения и делать коммиты, это будет всё локально, в виртуальной версии ничего не будет при этом меняться
### Работа с pull request запросами – запрос на вливание наших изменений в какой-то удалённый репозиторий
1.	Находим актуальный для нас удалённый репозиторий по интересному для нас проекту в GitHub, это аккаут другого человека, поэтому у нас нет доступа в нём редактировать
2.	Для того, чтобы мы могли поучаствоать в этом проекте то, нам нужно создать свою копию этог репозитория у на в аккаунте в GitHub
3.	Нажимаем на кнопку fork (снимаем при актуальности галочку копировать только ветку мастер)  и делаем у нас в аккаунте копию этого репозитория, он появляется у нас в аккаунте и там отражается инфо на исходный репозиторий, с которым у нас в аккаунте мы можем делать всё что хотим
4.	В нашем аккаунте в GitHub мы забираем этот удалённый репозиторий к себе в локальный репозиторий в git путём клонирования в наши локальные папки, например, которые уже у нас есть
5.	Для этого открываем в git актуальную папку и рядом с уже существующим репозиторием положим тот репозиторий, который только что форкнули
6.	git clone link
7.	У нас появился в нашем локальном репозитории склонированный форкнутый репозиторий из GitHub в виде доп папки (folder_name)
8.	cd folder_name – переходим в эту папку, она внутри нашей локальной папки
9.	Внутри этой папки есть проект, где есть файлы и мы можем помочь этому проекту. На GitHub принято, чтобы у каждого проекта был файл README.md с описанием того, что происходит внутри этого проекта
10.	Важно понимать, если мы хотим внести изменения в чей-то проект, то это всегда делается в отельной ветке
11.	Создаём эту ветку и в ней создадим файл с описанием этого проекта
12.	git branch – смотрим какие ветки существуют (пока только мастер)
13.	git branch description – создаём рядом новую ветку description
14.	git branch + git checkout description +git branch – смотрим что она действительно создана и переключаемся на неё и убеждаемся, что мы перешли на неё, после чего продолжаем на ней работу
15.	создаём новый файл внутри нашей папки README.md – этот файл принято называть капсулой, и мы здесь дедаем какое-то описание, сохраняемся, эддимся и коммитимся на ветке дескрипшн  с сообщением “добавили описание проекта, как вариант”
16.	У нас это файл на ветке дискрипшн, которую мы создали и которой не было изначально в проекте
17.	Мы сощдали новую ветку произвели в ней какие-то изменения и эти изменения мы хотим предложить тому человек, который владеет основным репозиторием в GitHub и для этого см. далее
18.	git push – направляем, то что у нас сделано в наш репозиторий в GitHub и получаем подсказку от git
19.	git push –set-upstream origin description – git нам услужливо подсказывает, что у нас изменения сделаны в другой ветки, поэтому следует ввести другую команду
20.	Обновляем наш удалённый репозиторий в GitHub и видим что у нас появляется новая ветка description, которой раньше не было и самой главное появляется кнопка Compare & pull request (сравни и отправь изначальному репозиторию (с которого форкали) запрос на вливание того, что мы только что сделали)
21.	Нажимаем на кнопку Compare & pull request – GitHub проанализировал и показывает, что мы можем без проблем слить, что никаких конфликтов не обнаружено и предлагает нам добавить некоторое описание по сделанному
22.	Далее отправляем от нас этот пул реквест через кнопку Create pull request
23.	После этого в аккаунте, с которого мы делали копию появляется новое поле и с ним уже будет работать хозяин этого аккуанта, он посмотрит на те изменения которые мы сделали и если они его устроят то он может влить эту ветку в сой основной репозиторий
