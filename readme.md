# Первоначальная настройка
Настройка информации о пользователе для всех локальных репозиториев

$ git config --global user.name "[имя]"

#Устанавливает имя, которое будет отображаться в поле автора у выполняемых вами коммитов

$ git config --global user.email "[адрес электронной почты]"

Устанавливает адрес электронной почты, который будет отображаться в информации о выполняемых вами коммитах

# Создание репозитория
Создание нового репозитория или получение его по существующему URL-адресу

$ git init [название проекта]

# Создаёт новый локальный репозиторий с заданным именем

$ git clone [url-адрес]

Скачивает репозиторий вместе со всей его историей изменений

# Внесение изменений
Просмотр изменений и создание коммитов (фиксация изменений)

$ git status

Перечисляет все новые или изменённые файлы, которые нуждаются в фиксации


$ git add [файл]

Индексирует указанный файл для последующего коммита


$ git commit -m "[сообщение с описанием]"

Фиксирует проиндексированные изменения и сохраняет их в историю версий


В первый раз эту команду нужно вызвать с флагом -u и параметрами origin (имя удалённого репозитория) и main или master (название текущей ветки). Флаг -u свяжет локальную ветку с одноимённой удалённой. Как вы связывали локальный и удалённый репозитории в предыдущем уроке, так же и здесь нужно дополнительно связать ветки.

$ git push -u origin main

Привязать удалённый репозиторий к локальному — git remote add

$ cd ~/dev/first-project
$ git remote add origin git@github.com:%ИМЯ_АККАУНТА%/first-project.git 

Убедиться, что репозитории связаны, — git remote -v

$ git remote -v
origin    git@github.com:%ИМЯ_АККАУНТА%/%ИМЯ-ПРОЕКТА%.git (fetch)
origin    git@github.com:%ИМЯ_АККАУНТА%/%ИМЯ-ПРОЕКТА%.git (push) 
