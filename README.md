1. Используется:
- Ubuntu server
- Gitlab, gitlab-runner
- Docker Hub

2. Для работы terraform создать файл variables.tf с указанием переменных данных для подключения к облаку (cloud_id, folder_id, zone). Если доступ к облаку организован через сервисный аккаунт, то необходимо создать файл key.json с указанием данных сервисного аккаунта. Вариант использования token: закоментировать в main.tf service_account_key_file ... и раскоментировать token, данные token внести в файл variable.tf.

3. Как терраформ завершит создание серверов, актуализировать значения ip адресов в файле ansible/inventory.yml 

4. перееходим в папку ансибль и запускаем ansible-playbook play.yml

5. по заверешению работы ансибль, заходим на сервер srv под именем user

6. git clone https://gitlab.com/aorlov18/my_django.git
docker push alexorl/mydjango:tagname
https://hub.docker.com/r/alexorl/mydjango

7. запускаем 
gitlab-runner register
на вопрос Enter an executor: выбираем docker

gitlab-runner run

8. В настройках CI/CD Gitlab добавляем две переменные - DOCKER_USERNAME и DOCKER_PASSWORD. Соответственно, логин и пароль для прохождения валидации в репозитории Docker Hub.




8.



