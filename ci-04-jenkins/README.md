# Домашнее задание к занятию 10 «Jenkins»

## Подготовка к выполнению

1. Создать двe VM: для jenkins-master и jenkins-agent.
![image](screenshots/1_1.jpg)
2. Установить Jenkins при помощи playbook.
3. Запустить и проверить работоспособность.
4. Сделать первоначальную настройку.
![image](screenshots/1_4.jpg)

## Основная часть

1. Сделать Freestyle Job, который будет запускать `molecule test` из любого вашего репозитория с ролью.
![image](screenshots/2_1.jpg)
![image](screenshots/2_1_1.jpg)
![image](screenshots/2_1_2.jpg)
2. Сделать Declarative Pipeline Job, который будет запускать `molecule test` из любого вашего репозитория с ролью.
![image](screenshots/2_2.jpg)
![image](screenshots/2_2_1.jpg)
3. Перенести Declarative Pipeline в репозиторий в файл `Jenkinsfile`.
![image](screenshots/2_3.jpg)
![image](screenshots/2_3_1.jpg)
![image](screenshots/2_3_2.jpg)
4. Создать Multibranch Pipeline на запуск `Jenkinsfile` из репозитория.
![image](screenshots/2_4.jpg)
5. Создать Scripted Pipeline, наполнить его скриптом из [pipeline](./pipeline).
6. Внести необходимые изменения, чтобы Pipeline запускал `ansible-playbook` без флагов `--check --diff`, если не установлен параметр при запуске джобы (prod_run = True). По умолчанию параметр имеет значение False и запускает прогон с флагами `--check --diff`.
![image](screenshots/2_6.jpg)
7. Проверить работоспособность, исправить ошибки, исправленный Pipeline вложить в репозиторий в файл `ScriptedJenkinsfile`.
![image](screenshots/2_7.jpg)
8. Отправить ссылку на репозиторий с ролью и Declarative Pipeline и Scripted Pipeline.
https://github.com/anmiroshnichenko/vector_role
9. Сопроводите процесс настройки скриншотами для каждого пункта задания!!

## Необязательная часть

1. Создать скрипт на groovy, который будет собирать все Job, завершившиеся хотя бы раз неуспешно. Добавить скрипт в репозиторий с решением и названием `AllJobFailure.groovy`.
2. Создать Scripted Pipeline так, чтобы он мог сначала запустить через Yandex Cloud CLI необходимое количество инстансов, прописать их в инвентори плейбука и после этого запускать плейбук. Мы должны при нажатии кнопки получить готовую к использованию систему.

---

### Как оформить решение задания

Выполненное домашнее задание пришлите в виде ссылки на .md-файл в вашем репозитории.

---
