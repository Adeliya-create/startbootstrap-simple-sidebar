# Simple Sidebar — Docker + Nginx + CI/CD

Форк [StartBootstrap/startbootstrap-simple-sidebar](https://github.com/StartBootstrap/startbootstrap-simple-sidebar) с добавленной Docker-инфраструктурой.

## Что добавлено

- `Dockerfile` — упаковывает сайт в Nginx контейнер
- `docker-compose.yml` — запуск одной командой
- GitHub Actions CI/CD — автосборка образа при каждом пуше

## Как запустить

### Вариант 1 — через docker compose (для разработки)
git clone https://github.com/Adeliya-create/startbootstrap-simple-sidebar.git
cd startbootstrap-simple-sidebar
docker compose up --build

### Вариант 2 — скачать готовый образ (без клонирования)
docker run -p 8080:80 ТВОЙ_ЛОГИН/simple-sidebar:latest

Открой http://localhost:8080

## Как это работает

браузер → localhost:8080 → Nginx внутри Docker → файлы сайта

При каждом git push → GitHub Actions → docker build → Docker Hub