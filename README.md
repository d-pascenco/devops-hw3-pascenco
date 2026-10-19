# ДЗ 3 - мониторинг и Dockerfile (Пащенко Дмитрий)

Все команды, вывод и скрины - в ноуте hw3_Пащенко_Дмитрий.ipynb

## Мониторинг

- monitoring/prometheus/prometheus.yml - добавил job node, instance vm1 (vm1 это мой ноут)
- monitoring/grafana/dashboard.json - мой дашборд: CPU, RAM, диск, сеть + переменная instance
- цель сначала была down, пришлось открыть 9100 в ufw для докер-сетей

## Dockerfile

| образ | Dockerfile | размер | юзер |
|---|---|---|---|
| counter-backend:single | counter-backend/Dockerfile.single | 381 MB | root |
| counter-backend:multistage | counter-backend/Dockerfile.multistage | 234 MB | root |
| counter-backend:nonroot | counter-backend/Dockerfile.nonroot | 234 MB | user (1001) |

в poetry 2 export вынесли в плагин, поэтому везде доставил poetry-plugin-export
