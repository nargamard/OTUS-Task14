# Задание: настроить дашборд

## Решение:

---
### Описание доски:
В качестве решения хотел бы продемонстрировать доску, которую в прикладных и образоватеьных целях сейчас создаю на текущем рабочем месте для мониторинга узлов сети с ОС разных типов (linux и windows).
Сейчас в общей таблице отображаются ip адрес, имя хоста, uptime, название ОС и её версией, всего ОЗУ на машине, колчество ядер ЦПУ, максимальная частота ЦПУ, процент использования ЦПУ, памяти, диска, использование swap, процент iowait и температура ЦПУ. 
Сейчас, вечером, показывается лишь несколько включенных узлов (фермы виртуальных машин, серверы мониторнга, 1С, nextcloud и несколько иных узлов).

---
### Описание объекта мониторинга:

В инфраструктуре имеется порядка 40 узлов, в том числе 2 фермы виртуальных машин.
Я решил настроить систему мониторинга для решения следующих задач:

1. Оперативно реагировать на проблемы с высокой загрузкой узлов или недостатком свободного места. А такое бывает из-за утечек памяти на сервере 1С, на узлаз, где работает Контур.Плагин для КриптоПро для сервиса отправки налоговой отчетности;
2. Своевременно узнавать, что необходимо гдето провести профилактику и очистку системного блока, т.к. часть узлов находится в других городах и физически редко доступна; 
3. Увидеть и решить проблему производительности, в частности с помощью системы были найдены узлы, где часто возникают высокие значения ipwait, на них HDD были заменены на SSD, были выявлены узлы с недостатком памяти и меделнными ЦПУ. Т.к. всё оборудование приобреталось организацией в разное время по принципу "лишь бы подешевле", было несколько переездов из офиса в офис, никто не знал, в каком блоке какая начинка. В общем, мониторинг уже помог часть вопросов закрыть.

---
### Что планируется сделать далее:
1. Добавить данные о сетевом траффике;
2. Добавить более подробную детализацию по выбранной машине;
3. Сделать схематичную карту сети и смотреть на ней, какие узлы включены, какие нет;
4. Настроить alert manager, чтобы получатьт уведомления в Телеграмм.

