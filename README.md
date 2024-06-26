# Домашнее задание к занятию "`GitLab`" - `Сологуб Евгений`


### Инструкция по выполнению домашнего задания

   1. Сделайте `fork` данного репозитория к себе в Github и переименуйте его по названию или номеру занятия, например, https://github.com/имя-вашего-репозитория/git-hw или  https://github.com/имя-вашего-репозитория/7-1-ansible-hw).
   2. Выполните клонирование данного репозитория к себе на ПК с помощью команды `git clone`.
   3. Выполните домашнее задание и заполните у себя локально этот файл README.md:
      - впишите вверху название занятия и вашу фамилию и имя
      - в каждом задании добавьте решение в требуемом виде (текст/код/скриншоты/ссылка)
      - для корректного добавления скриншотов воспользуйтесь [инструкцией "Как вставить скриншот в шаблон с решением](https://github.com/netology-code/sys-pattern-homework/blob/main/screen-instruction.md)
      - при оформлении используйте возможности языка разметки md (коротко об этом можно посмотреть в [инструкции  по MarkDown](https://github.com/netology-code/sys-pattern-homework/blob/main/md-instruction.md))
   4. После завершения работы над домашним заданием сделайте коммит (`git commit -m "comment"`) и отправьте его на Github (`git push origin`);
   5. Для проверки домашнего задания преподавателем в личном кабинете прикрепите и отправьте ссылку на решение в виде md-файла в вашем Github.
   6. Любые вопросы по выполнению заданий спрашивайте в чате учебной группы и/или в разделе “Вопросы по заданию” в личном кабинете.
   
Желаем успехов в выполнении домашнего задания!

[ДЗ условия](https://github.com/netology-code/sdvps-homeworks/blob/main/8-03.md)

   
### Дополнительные материалы, которые могут быть полезны для выполнения задания

1. [Руководство по оформлению Markdown файлов](https://gist.github.com/Jekins/2bf2d0638163f1294637#Code)

---

### Задание 1
bash:
   docker exec -it gitlab bash -c "echo \"external_url 'http://mynetology.docker'\" >> /etc/gitlab/gitlab.rb"  
   echo "172.17.0.2	mynetology.docker" >> /etc/hosts  

*172.17.0.2 - адрес контейнера с gitlab*

![alt text](https://github.com/SeSloup/gitlab-hw-gitlab/blob/main/screenshots/01-00.png)
![alt text](https://github.com/SeSloup/gitlab-hw-gitlab/blob/main/screenshots/01-01.png)


---

### Задание 2

`Приведите ответ в свободной форме........`

![alt text](https://github.com/SeSloup/gitlab-hw-gitlab/blob/main/screenshots/02-00.png)
![alt text](https://github.com/SeSloup/gitlab-hw-gitlab/blob/main/screenshots/02-01.png)
![alt text](https://github.com/SeSloup/gitlab-hw-gitlab/blob/main/screenshots/02-02.png)
![alt text](https://github.com/SeSloup/gitlab-hw-gitlab/blob/main/screenshots/02-03.png)

```
stages:
  - test
  - build

test:
  stage: test
  image: golang:1.17
  script: 
   - /usr/local/go/bin/go test .   

build:
  stage: build
  image: docker:latest
  script:
   - docker build .

```


---
 Спасибо за проверку !
