# Lighthouse Role

Ansible роль для установки Lighthouse — веб-интерфейса для ClickHouse.

## Требования

- Ubuntu 20.04/22.04
- Ansible 2.10+

## Переменные

### defaults/main.yml (можно переопределить)

| Переменная | Описание | По умолчанию |
|------------|----------|--------------|
| `lighthouse_repo` | URL репозитория | `https://github.com/VKCOM/lighthouse.git` |
| `lighthouse_dir` | Директория установки | `/var/www/lighthouse` |
| `lighthouse_port` | Порт nginx | `80` |

### Внешние переменные

| Переменная | Описание | По умолчанию |
|------------|----------|--------------|
| `clickhouse_host` | IP адрес ClickHouse сервера | `127.0.0.1` |

## Зависимости

Роль устанавливает nginx и git автоматически.

## Пример использования
```yaml
- hosts: lighthouse
  roles:
    - lighthouse
  vars:
    clickhouse_host: "192.168.1.68"
```

## Лицензия

MIT

## Автор

Arthur Ishmakov
