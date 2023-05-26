# Ansible playbook для развертывания отказоустойчивого кластера Kubernetes 
=========

* kube-install - Подготовка Linux серверов для установки kubernetes. Установка kubernetes на сервер с CentOS/Fedora.
* kube-init - Инициирует мастер ноду кластера kubernetes. Устанавливает CNI. Генерирует токены для пресоединения рабочих нод и мастеров.
* kube-join  - Добавляет ноды в кластер.


Требуется
-----------

Ansible 2.10 и новее 

ОС семейства Linux (CentOS, Fedora).


Переменные
-----------

LOAD_BALANCER_IP - IP балансировщика нагрузки

POD_NETWORK_CIDR - подсеть для подов

USER_ADM - пользователь, которому будет скопирован конфиг для kubectl

CNI_POD - Версия CNI

JOIN_MASTER - токен для добавления Control-Plane ноды

JOIN_WORKER - токен для добавления worker ноды
