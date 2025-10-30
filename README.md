# senior-java-roadmap

1. Core Java (недели 1-2)
R Пройти «Java 17 Complete» (JetBrains Academy) – 30 hrs
P Проект: консольный «Banking CLI» (lombok, records, NIO, BigDecimal)
A 2 недели, 1-2 ч/день
D Показываете код ревьюерам → демонстрируете владение новыми фичами
2. Алгоритмы + SQL (недели 3-6)
R LeetCode «Top 150» + SQL-50 (режим daily)
P Сохраняете решения в GitHub leetcode-tracker
A 1 час утром каждый день, 4 недели
D На собеседовании разбираете задачу «Top K Frequent Elements» за 3 минуты
3. Spring Ecosystem (недели 5-10)
R Курс «Spring Professional» (Ivanchuk, 35 hrs)
P Pet-project: micro-wallet

    Spring Boot 3, Spring Data JPA, Flyway, PostgreSQL
    REST + Swagger, MapStruct, DTO-validation
    Spring Security (JWT, refresh-token)
    Spring Cloud Config + Bus (Kafka)
    A 6 недель, 3 ч/день
    D Репо → 80 % покрытие тестами (Jacoco), CI green-badge

4. Test & Quality (недели 9-12)
R JUnit 5, Mockito, Testcontainers, AssertJ, ArchUnit
P Добавить в micro-wallet:

    интеграционные тесты (PostgreSQL container)
    layer-dependency tests (@ArchTest)
    mutation testing (PIT) ≥ 70 %
    A 3 недели
    D Показываете отчёт PIT на собеседовании → «мы убиваем 85 % мутантов»

5. High-load & Async (недели 11-14)
R Курс «High-Performance Java» (TechCenter, 25 000 ₽)
P Модуль «payment-gateway»

    Spring WebFlux + Reactor
    5 000 rps на k6, latency p95 < 150 мс
    Балансировка с помощью Spring Cloud LoadBalancer
    A 4 недели
    D Графики k6 в README → instant вау-эффект

6. Messaging & Persistence (недели 13-16)
R Apache Kafka, PostgreSQL partitioning, Redis (Lettuce)
P Feature: «cashback-calculation»

    продюсер/консюмер Kafka (exactly-once)
    шардированная таблица по user_id (pg_partman)
    кеш-аспект Redis (CacheAside)
    A 4 недели
    **D» На онлайн-интервью рисуете схему шардов + партиций

7. Containers & K8s (недели 15-18)
R Курс «Kubernetes for Java Devs» (Udemy) + CKA (по желанию)
P Добавить:

    multi-stage Dockerfile (jlink → 90 MB image)
    Helm-chart (deployment, hpa, pdb)
    GitHub Actions: build → test → docker push → deploy to k3s
    A 4 недели
    **D» Показываете helm get values и дашборд Grafana

8. Observability (недели 17-20)
R Prometheus, Grafana, Loki, Tempo (OpenTelemetry)
P Интегрировать Micrometer + OTLP exporter

    custom бизнес-метрика «payment_total»
    tracing across WebFlux → Kafka → DB
    **A» 3 недели
    **D» Ссылка на живой Grafana (логин demo/demo)

9. Cloud & DevOps-прокачка (недели 19-22)
R AWS Certified Solutions-Architect Associate (или Yandex-Cloud)
**P» Поднять в AWS:

    EKS-кластер, RDS (Multi-AZ), MSK (Kafka), ElastiCache
    Terraform-модули в отдельном репо terraform-awscoffee
    **A» 4 недели
    **D» Показываете terraform plan + смету AWS < 150 $/мес.

10. Архитектура & Soft (недели 21-24)
**R» Чистая архитектура (R.C.Martin), DDD, C4-model
**P» Перевести micro-wallet на Hexagonal (ports-adapter)

    отдельные модули: domain, application, infrastructure, boot
    **A» 3 недели
    **D» Диаграмма C4 в docs/ → легко показать на Zoom

11. Публикации + нетворкинг (недели 23-26)
**R» Хабр: 2 статьи

    «Как мы держим 5k rps на Spring WebFlux без блокировок»
    «Шардирование PostgreSQL на Java-проекте: pg_partman vs Citus»
    **P» Посты в LinkedIn (eng) + cross-post в Telegram-каналы
    **A» 4 недели
    **D» Метрика: 30k просмотров, 300+ апвоутов → соц-доказательство

12. Собеседования & офферы (недели 25-30)
**R» Цель: 30 откликов → 15 скринингов → 8 тех-интервью → 3 оффера
**P» Таблица Notion: компания, стек, з/п, фидбек, next action
**A» 6 недель
**D» Отказ — тоже результат, просим детальный фидбек и правим blind-spot
