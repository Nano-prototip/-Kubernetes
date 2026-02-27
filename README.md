# Практическое задание к занятию «Настройка приложений и управление доступом в Kubernetes»

## Задание 1: Работа с ConfigMaps
Задача
Развернуть приложение (nginx + multitool), решить проблему конфигурации через ConfigMap и подключить веб-страницу.

Шаги выполнения

1. Создать Deployment с двумя контейнерами

Манифест: [deployment.yaml](https://github.com/Nano-prototip/-Kubernetes/blob/main/deployment.yaml)

<img width="452" height="123" alt="image" src="https://github.com/user-attachments/assets/97f15e95-e360-4d56-b2b9-6ee30585d539" />


3. Подключить веб-страницу через ConfigMap

 Манифест: [configmap-web.yaml](https://github.com/Nano-prototip/-Kubernetes/blob/main/configmap-web.yaml)  

<img width="422" height="135" alt="image" src="https://github.com/user-attachments/assets/aaafcecf-4661-41ca-8419-95b5492079a1" />


3.Проверить доступность

<img width="624" height="242" alt="image" src="https://github.com/user-attachments/assets/d7cdb566-c456-4348-aa43-d338f2ee160c" />



## Задание 2: Настройка HTTPS с Secrets
Задача
Развернуть приложение с доступом по HTTPS, используя самоподписанный сертификат.

Манифесты:

[secret-tls.yaml](https://github.com/Nano-prototip/-Kubernetes/blob/main/secret-tls.yaml)

<img width="385" height="46" alt="image" src="https://github.com/user-attachments/assets/9c9a2eca-28cf-47e7-9106-460996ec047d" />

[ingress-tls.yaml](https://github.com/Nano-prototip/-Kubernetes/blob/main/ingress-tls.yaml)

<img width="384" height="47" alt="image" src="https://github.com/user-attachments/assets/eddc9170-dd4b-44cf-8900-e88e76f1661c" />

[myservice.yaml](https://github.com/Nano-prototip/-Kubernetes/blob/main/myservice.yaml)

<img width="355" height="33" alt="image" src="https://github.com/user-attachments/assets/37729d99-e3d8-4c71-8a20-7e23f7816de0" />

Скриншот вывода curl -k

<img width="472" height="175" alt="image" src="https://github.com/user-attachments/assets/1d3f0de6-63e6-4908-8466-a00f1010a863" />


## Задание 3: Настройка RBAC
Задача
Создать пользователя с ограниченными правами (только просмотр логов и описания подов).

Манифесты:

[role-pod-reader.yaml](https://github.com/Nano-prototip/-Kubernetes/blob/main/role-pod-reader.yaml)

<img width="400" height="46" alt="image" src="https://github.com/user-attachments/assets/fddda464-aadd-4782-8ceb-86704fa6b1cc" />


[rolebinding-developer.yaml](https://github.com/Nano-prototip/-Kubernetes/blob/main/rolebinding-developer.yaml)

<img width="486" height="48" alt="image" src="https://github.com/user-attachments/assets/4898d695-4066-4183-9bf6-9cc19a4bea53" />

Команды генерации сертификатов

<img width="659" height="30" alt="image" src="https://github.com/user-attachments/assets/f02d8b87-a95f-49fd-be48-845178bc7d77" />

Скриншот проверки прав (kubectl get pods --as=developer)

<img width="450" height="62" alt="image" src="https://github.com/user-attachments/assets/2e2a738e-152c-4a35-8c54-089c7308864a" />
