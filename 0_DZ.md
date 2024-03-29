# Классификация по теореме CAP

## ScyllaDB
ScyllaDB является AP-системой, что означает приоритетность Доступности и Устойчивости к Разделению за счет Согласованности. Она обеспечивает конечную согласованность и высокую доступность, поддерживая операции чтения и записи с низкой задержкой.
- **Доступность**: Высокая
- **Устойчивость к Разделению**: Поддерживается
- **Согласованность**: Конечная
- Источник: [ScyllaDB Docs](https://www.scylladb.com/docs/)&#8203;

## ArenadataDB
Для ArenadataDB предполагается классификация AC, исходя из её использования в аналитических целях и предполагаемого приоритета Согласованности и Доступности.
- **Доступность**: Предполагаемая
- **Согласованность**: Высокая
ArenadataDB предлагает масштабируемость без ухудшения производительности запросов на данных в петабайтах, обеспечивая высокую производительность аналитических задач. Эти характеристики подразумевают сбалансированное сочетание доступности и согласованности в контролируемой среде, характерное для систем типа AC.
- Источник: [Arenadata Docs](https://docs.arenadata.io)


## DragonFly
DragonFly, исходя из лозунга "Redis® with wings", предположительно может иметь характеристики, схожие с Redis, и может быть классифицирована как CP или AP система.
- **Доступность**: Предполагаемая (в случае AP)
- **Согласованность**: Предполагаемая (в случае CP)
- **Примечание**: Требуется дополнительное изучение для точной классификации
DragonFly, исходя из лозунга "Redis® with wings", предположительно может иметь характеристики, схожие с Redis. Redis как NoSQL база данных обеспечивает масштабируемость и доступность, что необходимо для микросервисной архитектуры. При этом, в распределенных системах, согласно теореме CAP, необходимо выбирать между доступностью и согласованностью. Если выбрать доступность, то данные будут консистентными, но лишь после определенного времени. Такой подход, предпочитающий доступность, подразумевает конечную согласованность данных.
- Источник: [Redis.com](https://redis.com/ebook/part-2-core-concepts-chapter-5-using-redis-for-application-support-caching-locking/)
