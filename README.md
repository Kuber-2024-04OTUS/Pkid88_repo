# Репозиторий для выполнения домашних заданий курса "Инфраструктурная платформа на основе Kubernetes-2024-02" 

**Описание:**

Создан namespace homework
Создан деплоймент my-deployment, создаётся 3 экземпляра пода(nginx-a, с конфигурацией из 1-ого ДЗ).
Добавлена readiness проба, проверка на наличие файла /homework/index.html/
Стратегия обновления RollingUpdate - может быть недоступен максимум 1-под
Добавлено правило запуска deployment-a только на нодах c меткой homework=true

![img_1.png](img_1.png)
![img_2.png](img_2.png)

Проверка ReadinessProbe HTTP
kubectl describe po my-deployment-7c87b597f-9qwbl
![3_img.png](3_img.png)

kubectl logs my-deployment-7c87b597f-9qwbl
![4_img.png](4_img.png)