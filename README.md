# Тест 
## Задание 1

<details>

Кейс
Крупная строительная компания, которая также занимается проектированием и девелопментом, решила создать правильную архитектуру для работы с данными. Ниже представлены задачи, которые необходимо решить для каждой предметной области.

Какие типы СУБД, на ваш взгляд, лучше всего подойдут для решения этих задач и почему?

1.1. Бюджетирование проектов с дальнейшим формированием финансовых аналитических отчётов и прогнозирования рисков. СУБД должна гарантировать целостность и чёткую структуру данных.

1.1.* Хеширование стало занимать длительно время, какое API можно использовать для ускорения работы?

1.2. Под каждый девелоперский проект создаётся отдельный лендинг, и все данные по лидам стекаются в CRM к маркетологам и менеджерам по продажам. Какой тип СУБД лучше использовать для лендингов и для CRM? СУБД должны быть гибкими и быстрыми.

1.2.* Можно ли эту задачу закрыть одной СУБД? И если да, то какой именно СУБД и какой реализацией?

1.3. Отдел контроля качества решил создать базу по корпоративным нормам и правилам, обучающему материалу и так далее, сформированную согласно структуре компании. СУБД должна иметь простую и понятную структуру.

1.3.* Можно ли под эту задачу использовать уже существующую СУБД из задач выше и если да, то как лучше это реализовать?

1.4. Департамент логистики нуждается в решении задач по быстрому формированию маршрутов доставки материалов по объектам и распределению курьеров по маршрутам с доставкой документов. СУБД должна уметь быстро работать со связями.

1.4.* Можно ли к этой СУБД подключить отдел закупок или для них лучше сформировать свою СУБД в связке с СУБД логистов?

1.5.* Можно ли все перечисленные выше задачи решить, используя одну СУБД? Если да, то какую именно?

Приведите ответ в свободной форме.
</details>

## Ответ:
1.1 Реляционные типы БД. Они обеспечивают наилучшую согласованность и доступность, данные организованы в табличной структуре. Например, Postgresql, MySQL, Oracle
1.2 Для лендингов можно использовать документо-ориентированные NOSQL, их недостаток в избыточности данных, но объем данных в примере будет небольшой. Например, MongoDB. Или же легковесную встраиваемую реляционную SQLite. Для CRM лучше использовать реляционную СУБД вроде Postgres, т.к. она обеспечивает наилучшую согласованность и доступность.
1.3 Если данные относительно небольшие и структура проекта простая, то можно использовать реляционную БД
При сложной и объемной структуре данных лучше применить NOSQL, вроде MongoDB, т.к. она обеспечит лучшую производительность. MongoDB рекомендуют использовать там, где существует потребность в сложных выборках.
1.4 Для такой задачи можно использовать NOSQL графовую БД, которая оптимизирована для работы со связями. Логистика часто имеет дело с сложными связями поставщиков, транспортных маршрутов, складов, клиентов. Графовая СУБД позволит эффективно моделировать и анализировать всё это.
1.5 Нет, задачи слишком разные (лендинг, CRM, логистика и т.п.). Лучше выбрать оптимальный вариант СУБД под каждую отдельную задачу.