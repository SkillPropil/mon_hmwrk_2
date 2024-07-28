# mon_hmwrk_2
Преподам привет! Хорошего дня и настроения:) 


## Задание 1
Подключил data source по имени контейнера \
<img width="1470" alt="datasource" src="https://github.com/user-attachments/assets/2d9d7fc7-e816-4bed-bb37-4cad2c395c26">
## Задание 2
cpu usage by nodeexporter
```
(avg by (instance) (irate(node_cpu_seconds_total{job="nodeexporter",mode="idle"}[5m])) * 100)
```
LA1/5/15
```
# Цифры переменной являются значением времени, все сделано в рамках трех разных запросов
node_load{1,5,15}{instance="nodeexporter:9100"}
```

Free mem
```
100 * (1 - ((avg_over_time(node_memory_MemFree_bytes[5m]) + avg_over_time(node_memory_Cached_bytes[5m]) + avg_over_time(node_memory_Buffers_bytes[5m])) / avg_over_time(node_memory_MemTotal_bytes[5m])))
```

Free disk space
```
node_filesystem_free_bytes{fstype=~"ext4|xfs"})
```
<img width="1318" alt="metrics" src="https://github.com/user-attachments/assets/b1323414-7a1f-49e6-8154-43c6e5da9d2c">


## Задание 3
Скриншот выше валиден

## Задание 4
model.json
