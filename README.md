# web-infra
```bash
sudo apt update
sudo apt install -y ansible
```
После выполнения:

Веб-приложение будет доступно на http://localhost:8080
PostgreSQL будет доступен внутри Docker-сети
Kafka будет доступна на порту 9092
5. Запуск с принудительным пересозданием
bash
Copy

docker-compose -f /tmp/docker-compose.yml up -d --force-recreate


    Остановите и удалите все текущие контейнеры:

bash
Copy

docker-compose -f /tmp/docker-compose.yml down --remove-orphans
docker rm -f $(docker ps -aq)