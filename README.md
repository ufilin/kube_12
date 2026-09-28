# kube_12

## Задание. При деплое приложение web-consumer не может подключиться к auth-db. Необходимо это исправить

### Манифесты

**[deploy.yaml](https://github.com/ufilin/kube_11/blob/main/deploy.yaml)**  

### Решение и скриншоты
  
> Первоначально не было NS, добавлены вручную, но позже добавлены в манифест
  
<p align="center">
  <img src="task2/kube_12-1-1.png" width="800">
</p>
  
> Далее ошибка с image, замена на актуальный  
  
<p align="center">
  <img src="task2/kube_12-1-2.png" width="800">
</p>
  
> Ошибка доступа по имени из ns в ns  
  
<p align="center">
  <img src="task2/kube_12-1-3.png" width="800">
</p>
  
> Замена адреса в исполняемой команде, новый адрес "auth-db.data" 
  
Проверка из контейнера:  
  
<p align="center">
  <img src="task2/kube_12-1-5.png" width="800">
</p>
  
Проверка логов, чтобы проверить работоспособность всей схемы:
  
<p align="center">
  <img src="task2/kube_12-1-5.png" width="800">
</p>