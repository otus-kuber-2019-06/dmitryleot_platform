# dmitryleot_platform
dmitryleot Platform repository
# Выполнено ДЗ №1

 - [X] Основное ДЗ
 - [ ] Задание со *

## В процессе сделано:
 - kubectl уже был установлен через brew install kubernetes-cli
 - autocomplete для zsh также был установлен
 - virtualbox был установлен
 - установлен minikube через Homebrew
 - прометрена информация по кластеру kubectl cluster-info
 - установлен dashboard
 - опробовал k9s
 - подключился по ssh к minikube
 - Проверена отказоустойчивость кластера.
   Компоненты мастер ноды восстанавливаются т.к. запускаются из systemd
   CoreDNS запускается т.к. есть сущность deployment которая контролирует replicaset, а replicaset поды и т.д.
 - Создал докерфайл, запускающий докер на порту 8080 и манифест для пода.
 - Добавил init контейнер и подключил к нему volume empty dir
 - Установил Kube Forwarder, получил доступ к поду.  

## Как запустить проект:
 - Создать runtime из манифеста, например запустить команду kubectl apply -f kubernetes-intro/web-pod.yaml
 - при помощи форвард порта либо локально с mikikube curl. Например: port-forward pod/web 8080:8080

## Как проверить работоспособность:
 - Перейти по ссылке http://localhost:8000

## PR checklist:
 - [ ] Выставлен label с номером домашнего задания
 - [ ] Добавлены необходимые файлы для первого ПР
 - [ ] Указан Assignees

# Выполнено ДЗ №2
 - Создал SA bob и ClusterRoleBinding для bob к ClusterRole Admin
 - Добавил SA dave
 - Создал ns prometheus
 - Создал SA carol, ClusterRole "clusterview" ClusterRoleBinding "clusterview" для SA в NS prometheus
 - Создал NS "dev"
 - создал SA "jane" namespace "dev", создал RoleBinding где ClusterRole admin присваивается SA "jane"
 - Создал SA "ken" в ns "dev"
 - Создал RoleBinding для sa "ken" в ns "dev"
