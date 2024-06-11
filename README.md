# Учебное web-приложение Docker Compose

- цель: для демонстрации запуска контейнерезированного web-приложения, отображающего экранные часы и функцию сохранения отметок времени.
Приложение состоит из 4 образов Docker:
- из них два пользовательских образа (frontend и backend(api)) с моего пользовательского репозитория на DockerHub:
1. https://hub.docker.com/repository/docker/dmay17/time-app-api-dev
2. https://hub.docker.com/repository/docker/dmay17/time-app-frontend-dev
- и двух официальных образов (базы данных и интерфейса базы данных) с DockerHub:
3. MySQL
4. Adminer

Инструкция по установке:
- запускается (после инсталляции на компьютере Docker Desktop для Windows или Docker Engine для Linux, и Docker compose): 
1) скачиванием в локальную папку файла docker-compose.pub.yml
2) перейдя в терминале ( cd <путь>) в эту папку и введением команды в терминале:    
docker-compose -f docker-compose.pub.yml up -d

После автоматического завершения процесса установки - приложение доступно в веб-браузере по адресу:     
http://localhost:3000/
После закрытия web-приложения - его контейнеры можно удалить командой в терминале:     
docker-compose -f docker-compose.pub.yml down

*По учебному курсу Б. Стащука по Docker и Docker Compose
