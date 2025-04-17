# Web Infra Deployment

## 📦 Состав инфраструктуры:
- **NGINX** (веб-сервер)
- **PHP-FPM** (бэкенд)
- **PostgreSQL** (база данных)
- **Kafka + ZooKeeper** (брокеры сообщений)
- Всё разворачивается с помощью **Ansible + Docker Compose**

## 📂 Структура проекта:
```
web-infra/
├── inventory.ini        # Ansible inventory (локальный хост)
├── deploy.yml           # Ansible playbook
├── docker-compose.yml   # Инфраструктура
├── nginx.conf           # Конфигурация NGINX
├── index.html           # Простая веб-страница
└── kafka-data/          # Данные Kafka (автоматически создается)
```

## 🚀 Развёртывание
```bash
ansible-playbook -i inventory.ini deploy.yml
```

Проект поднимет все нужные сервисы на локальной машине.
