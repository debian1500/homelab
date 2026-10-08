# Homelab Services

Набор сервисов, развёрнутых на домашнем сервере (Debian + Docker).

## Стек

- Debian
- Docker / Docker Compose
- PostgreSQL 14 (Invidious)
- Nginx
- Samba
- Minidlna
- Tor

## Сервисы

- **Invidious** — YouTube-фронтенд (Docker + PostgreSQL)
- **SearXNG** — метапоисковик (Docker + Tor)
- **Nginx** — реверс-прокси + статика
- **Samba** — файловый сервер
- **Minidlna** — DLNA для медиа

## Как развернуть

1. `cp invidious/.env.example invidious/.env` и заполнить
2. `cd invidious && docker compose up -d`
3. `cd ../searxng && docker compose up -d`
4. Nginx: скопировать конфиги в `/etc/nginx/`

## Что демонстрирует

- Docker Compose для многоконтейнерных приложений
- PostgreSQL (через Invidious)
- Nginx как реверс-прокси
- Samba с открытыми и закрытыми шарами
- Tor для анонимности
- Безопасность через `.env.example`
