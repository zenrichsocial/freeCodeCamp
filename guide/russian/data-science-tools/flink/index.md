---
title: Flink
localeTitle: Flink
---
## Flink

Apache Flink - это платформа обработки потоков с открытым исходным кодом с мощными возможностями потоковой обработки и пакетной обработки.

Ядро Apache Flink - это распределенный потоковый поток данных, написанный на Java и Scala. Flink выполняет произвольные программы потока данных в параллельном и конвейерном режиме. Конвейерная система исполнения Flink позволяет выполнять программы обработки объемных / пакетных и потоковых данных. Кроме того, среда исполнения Flink поддерживает выполнение итеративных алгоритмов изначально. Flink обеспечивает высокопроизводительный, низкозатратный потоковый движок, а также поддержку обработки событий и управления состоянием. Приложения Flink являются отказоустойчивыми в случае сбоя машины и поддерживают точно-семантику. Программы могут быть написаны на Java, Scala, Python и SQL и автоматически скомпилированы и оптимизированы в программы потоков данных, которые выполняются в кластерной или облачной среде.

Flink не предоставляет свою собственную систему хранения данных и предоставляет соединители источника данных и приемника для таких систем, как Amazon Kinesis, Apache Kafka, HDFS, Apache Cassandra и ElasticSearch.

![Рабочий процесс Flink](https://flink.apache.org/img/flink-home-graphic-update.svg)

**Что нового в Apache Flink?**

*   Flink реализует фактическую поточную обработку и не имитирует ее с помощью микро-пакетной обработки. В Spark streaming - особый случай пакетной обработки, в то время как в Flink-пакете - частный случай потоковой передачи (поток конечного размера)
*   Flink имеет лучшую поддержку циклической и итеративной обработки
*   Flink имеет более низкую задержку и более высокую пропускную способность
*   Flink имеет более мощные операторы Windows
*   Flink реализует легкие распределенные снимки, которые имеют низкую накладную и только однократную гарантию обработки при обработке потока, без использования микробиблиотеки, поскольку Spark делает
*   Flink поддерживает изменяемое состояние при обработке потока

### Особенности

*   Первое время выполнения, которое поддерживает как пакетную обработку, так и программы потоковой передачи данных
*   Элегантные и плавные API-интерфейсы в Java и Scala
*   Время выполнения, которое поддерживает очень высокую пропускную способность и низкую задержку событий одновременно
*   Поддержка _времени события_ и обработки _вне порядка_ в API DataStream на основе модели _потока данных_
*   Гибкое оконное (время, счет, сеансы, пользовательские триггеры) по разной временной семантике (время события, время обработки)
*   Отказоустойчивость с гарантией _безотказной_ обработки
*   Естественное обратное давление в потоковых программах
*   Библиотеки для обработки графов (пакетные), машинное обучение (пакетные) и комплексная обработка событий (потоковая передача)
*   Встроенная поддержка итеративных программ (BSP) в API DataSet (пакетный)
*   Пользовательское управление памятью для эффективного и надежного переключения между встроенными и встроенными алгоритмами обработки данных
*   Уровни совместимости для Apache Hadoop MapReduce и Apache Storm
*   Интеграция с YARN, HDFS, HBase и другими компонентами экосистемы Apache Hadoop

### Использование Flink

Предпосылки для создания Flink:

*   Unix-подобная среда (мы используем Linux, Mac OS X, Cygwin)
*   мерзавец
*   Maven (рекомендуется версия 3.0.4)
*   Java 7 или 8
```
git clone https://github.com/apache/flink.git 
 cd flink 
 mvn clean package -DskipTests # this will take up to 10 minutes 
```

## Разработка Flink

Коммандеры Flink используют IntelliJ IDEA для разработки кодовой базы Flink. Мы рекомендуем IntelliJ IDEA для разработки проектов, связанных с кодом Scala.

Минимальными требованиями для IDE являются:

*   Поддержка Java и Scala (также смешанные проекты)
*   Поддержка Maven с Java и Scala

#### Дополнительная информация:

*   Сайт Flink: [Apache Flink](https://flink.apache.org/)
*   Документация Flink: [flinkdocs](https://ci.apache.org/projects/flink/flink-docs-release-1.3/)
*   Quick flink tutorial: [быстрый старт](https://www.linkedin.com/pulse/introduction-apache-flink-quickstart-tutorial-malini-shukla/)
*   Как руководство: [howto](https://data-artisans.com/blog/kafka-flink-a-practical-how-to)
*   Flink vs Spark: [сравнение](http://www.developintelligence.com/blog/2017/02/comparing-contrasting-apache-flink-vs-spark/)