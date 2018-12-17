### Тестовое задание

Напиши скрипт на Python или bash.

Скрипт / приложение должны уметь:
1. Запуститься и выкачать репозиторий с файлом index.js (либо другим простейшим http.server'ом).
2. В заданный интервал времени проверять наличие изменений во всех ветках репозитория.
3. При обнаружении изменений в ветке выкачать их и собрать приложение в Docker-образ (требуется написать подходящий Dockerfile).
4. Придумать версионирование для образа и назначать версию в качестве тега образа.
5. Docker-образ должен содержать метаданные:
  * branch: ветка, из которой собран образ;
  * сommit: хеш последнего коммита;
  * maintainer: автор коммита.
6. После сборки образа скрипт должен остановить старый контейнер и запустить новый.
В контейнере должен запуститься http-сервис (на 80 порту), который будет доступен снаружи контейнера.

Задания со звездочкой: 
  a. Сделать так, чтобы вывод приложения сохранялся в лог-файл и этот файл не удалялся вместе с контейнером.
  b. Передавать вместе с запуском контейнера параметр, который будет указывать на путь к лог-файлу.
  c. Образ должен быть небольшого размера.
  d. Реализовать откат к предыдущей версии в случае неудачного запуска новой версии.
