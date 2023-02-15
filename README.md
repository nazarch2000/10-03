# Домашнее задание к занятию 10.3 «Pacemaker» - Рыженко Назарий

---

### Задание 1

Опишите основные функции и назначение Pacemaker.

Pacemaker — менеджер ресурсов кластера. Он позволяет использовать `службы и объекты` в рамках одного кластера из двух или более нод.

* позволяет находить и устранять сбои на уровне нод и служб;
* не зависит от подсистемы хранения: можем забыть общий накопитель, как страшный сон;
* не зависит от типов ресурсов: все, что можно прописать в скрипты, можно кластеризовать;
* поддерживает STONITH (Shoot-The-Other-Node-In-The-Head), то есть умершая нода изолируется и запросы к ней не поступают, пока нода не отправит сообщение о том, что она снова в рабочем состоянии;
* поддерживает кворумные и ресурсозависимые кластеры любого размера;
* поддерживает практически любую избыточную конфигурацию;
* может автоматически реплицировать конфиг на все узлы кластера — не придется править все вручную;
* можно задать порядок запуска ресурсов, а также их совместимость на одном узле;
* поддерживает расширенные типы ресурсов: клоны (когда ресурс запущен на множестве узлов) и дополнительные состояния (master/slave и подобное) — актуально для СУБД (MySQL, MariaDB, PostgreSQL, Oracle);
* имеет единую кластерную оболочку CRM с поддержкой скриптов.
*Приведите ответ в свободной форме.*

---

### Задание 2

Опишите основные функции и назначение Corosync.

Corosync — программный продукт, который позволяет создавать единый кластер из нескольких `аппаратных или виртуальных серверов`. Corosync отслеживает и передает состояние всех участников (нод) в кластере.

* мониторить статус приложений;
* оповещать приложения о смене активной ноды в кластере;
* отправлять идентичные сообщения процессам на всех нодах;
* предоставлять доступ к общей базе данных с конфигурацией и статистикой;
* отправлять уведомления об изменениях, произведенных в базе.

---

### Задание 3

Соберите модель, состоящую из двух виртуальных машин. Установите Pacemaker, Corosync, Pcs. Настройте HA кластер.

Необходимо, чтобы на всех нодах было одинаковое время.
![image](https://user-images.githubusercontent.com/106932460/218745295-a089fc83-03f4-43e9-9a47-1f7e3d7adad3.png)

![image](https://user-images.githubusercontent.com/106932460/218766575-ed6970c0-3c59-4bb3-b88b-faa175483e18.png)

![image](https://user-images.githubusercontent.com/106932460/218767513-f8f0d21c-02b8-4e54-8623-b7c90c3689c0.png)

![image](https://user-images.githubusercontent.com/106932460/219016784-4cb81c81-e247-4129-84d2-0ba7cea15da1.png)

---

### Задания со звёздочкой*
Эти задания дополнительные. Выполнять их не обязательно. Это не повлияет на зачёт. Вы можете их выполнить, если хотите глубже разобраться в материале.
 
---

### Задание 4

Установите и настройте DRBD-сервис для настроенного кластера.

*Пришлите скриншот рабочей конфигурации и состояние сервиса для каждого нода.*

![image](https://user-images.githubusercontent.com/106932460/219014041-95752bc9-c99c-4e68-a296-bcdc1fde1439.png)

![image](https://user-images.githubusercontent.com/106932460/219015145-791b9b38-e4a0-4b38-9cdb-614cb6a92bf2.png)

![image](https://user-images.githubusercontent.com/106932460/219015365-626036f3-e651-4adb-92a3-3c2f04a6cf80.png)
