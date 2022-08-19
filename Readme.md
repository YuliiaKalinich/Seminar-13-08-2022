# Инструкция по работе с Git и с GitHub


## Что такое *Git*?
*Git* - одна из реализаций распределённых систем контроля версий, позволяющая организовать версионность, как локально, так и на удалённом серевере. Самая популярная платформа, реализующая *Git*,- [GitHub](https://github.com)

## Подготовка репозитория
Для создания в папке репозитория необходимо открыть эту папку в терминале и написать команду *git init*, после чего в этой папке создасться скрытая папка *.git*, и таким образом папка станет репозиторием


## Создание коммитов

### Просмотр состояния репозитория
Для просмотра состояния репозитория используется команда *git status*. В терминале с открытой папкой-репозиторием необходимо написать команду *git status*. В результате можно увидеть следующие выводы:
1. On branch *** nothing to commit - это означает нет активных изменений
2. Untracked file - это означает, что имеются файлы, не отслеживаемые системой контроля версий
...

### Добавление файла к коммиту
Для того, чтобы добавить файл к "сохранению", необходимо использовать команду *git add*. В терминале с открытой папкой-репозиторием необходимо написать *git add <название файла>*, и этот файл добавится к "сохранению"


### Создание фиксации
Для создания фиксации используется команда *git commit*. Для этого в терминале с папкой-репозиторием необходимо написать команду *git commit -m <сообщение к коммиту>*. Сообщение к коммиту писать **ОБЯЗАТЕЛЬНО**.


## Журнал изменений
Для просмотра истории изменений используется команда *git log*. Для этого в терминале с папкой-репозиторием необходимо написать *git log*, и Вы увидите список всех коммитов в этой ветке с описанием: имени, электронной почты, сообщением к коммиту и номер коммита.



## Ветки в git
### Создание ветки
Для того, чтобы создать новую ветку используется команда *git branch*. Для этого терминале с папкой-репозиторием необходимо написать *git branch <название вертки>* и таким образом создасться новая ветка, но вы останетесь в исходной.

## Просмотр списка веток
Для того, чтобы просмотреть список веток в локальном репозитории, используется команда *git branch*. Для этого в терминале с папкой-репозиторием, напишите *git branch*, и тогда Вы увидите список всех Ваших локальных веток. Зелёным цветом и звёздочкой будет выделена ветка, на которой Вы сейчас стоите. Фалг *-a* позволяет посмотреть все ветки в том числе и в удалённом репозитории.

### Переключение между ветками
Для того, чтобы переключиться на другую ветку, используется команда *git checkout*. Для этого в терминале с папкой-репозиторием необходимо написать *git checkout <название ветки>*, и тогда Вы перейдёте в указанную ветку. Для переключения между ветками, ветка должна **СУЩЕСТВОВАТЬ**, и в текущий ветке **НЕ ДОЛЖНО** быть активных изменений


## Слияние веток и решение конфликтов

Для слияния двух веток переходим в основную ветку к которой будем добавлять изменения. И используем комманду "git merge <name>". В процессе слияния могут произойти конфликты, программа может предложить варианты решения этих конфликтов, а также их можно решить в ручную. После внесения изменений нужно сохранить файл и создать коммит с сообщением.

## Удаление веток
Чтобы удалить ветку используем комманду "git branch -d <name>" . Вводим комманду в терминале открытой папки-репозитория.


## Просмотр списка веток

Для того, чтобы просмотреть список веток в локальном репозитории используется команда  *git branch*. Для этого в паке-репозитория в терминале вводим *git branch*. Тогда вы увидите список всех ваших локальных веток. Зеленым цветом и звездочкой будут выделенна ветка на которой вы сейчас стоите. Фалг *-а* позволяет посмотреть все ветки в том числе и в удаленном репозитории.

## Удаленный репозиторий
удаленный репозиторий- т.е. репозиторий на другом компьютере или в интернете. Локальный- на компьютере пользователя.

Для работы с удаленным репозиторием необходимо зарегистрироваться на сайте GitHub. Заходим на сайт гитхаб и копируем ссылку на чейто репозиторий. открываем новую папку у себя на компьютере. Далее терминал- вводим команды: 
* *git branch -M master*
* *git push origin master"
* *git add origin "ссылка на репозиторий с сайта GitHub"
И этот репозиторий появится у вас на компьютере и станет локальным. Теперь вы можете вносить в него свои изменения. Для того чтобы из локального репозитория передать изменения в удаленный репозиторий нужно набрать команду *git pull origin master*. Для того чтобы не создавать конфликты следует все изменнения вносить в новую ветку, а не в ветку master. В случае создания конфликтов- их придется решать вручную.
