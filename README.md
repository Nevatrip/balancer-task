Есть [docker-compose c nginx](./project1/docker-compose.yml), который слушает 80 и 443 порты и генерирует Let's encrypt-сертификаты. Нужен [балансер](./balancer/docker-compose.yml), который сохранит текущий «автоматизм» и позволит добавлять новые сервисы с новыми docker-compose-конфигами. Т. е. project1 и project2 должны быть запущены одновременно и доступны по адресу project1.nevatrip.ru и project2.nevatrip.ru.

Пробовали [traefik](https://github.com/Nevatrip/balancer-task/pull/1), но больше одного проекта запустить не удалось. Возможно «проблема» в том, что каждый проект подразумаевает несколько сервисом каждый со своим доменом.
