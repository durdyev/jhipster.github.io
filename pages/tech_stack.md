---
layout: default
title: Technology stack
permalink: /tech-stack/
redirect_from:
  - /tech_stack.html
sitemap:
    priority: 0.8
    lastmod: 2017-08-18T00:00:00-00:00
---

# <i class="fa fa-stack-overflow"></i> Стэк технологий

## Стэк технологий на клиентской стороне

Веб приложения с одной страницей (SPA):

*   [AngularJS v1.x](http://angularjs.org/) или [Angular 4](https://angular.io/)
*   Оптимизированный Веб дизайн с помощью [Twitter Bootstrap](http://getbootstrap.com/)
*   [HTML5 Boilerplate](http://html5boilerplate.com/)
*   Совместимый с IE11 и современными браузерами
*   Полная поддержка интернациализации
*   Опционально [Sass](https://www.npmjs.com/package/node-sass) поддержка CSS дизайна
*   Опционально поддержка вебсокетов с помощью Spring Websockets

С отличным процессом разработки:

*   Легко устанавливать новые Javascript библиотеки с помощью [Bower](http://bower.io/) или [Yarn](https://yarnpkg.com/)
*   Сборка, оптимизация и перегрузка страниц в реальном времени с [Gulp.js](http://www.gulpjs.com) or [Webpack](https://webpack.js.org/)
*   Тестирование с [Karma](http://karma-runner.github.io/), [PhantomJS](http://phantomjs.org/) and [Protractor](http://www.protractortest.org)

А что если вам не достаточно одностраничных приложений для ваших задач?

*   Поддержка движка [Thymeleaf](http://www.thymeleaf.org/), для генерации страниц на стороне сервера.

## Стэк технологий на стороне сервера

Полностью [Spring приложение](http://spring.io/):

*   [Spring Boot](http://projects.spring.io/spring-boot/) для легкой настройки приложения
*   [Maven](http://maven.apache.org/) или [Gradle](http://www.gradle.org/) для сборки, тестирования и запуска приложения
*   ["development" и "production" профили]({{ site.url }}/profiles/) (есть и для Maven, и для Gradle)
*   [Spring Security](http://docs.spring.io/spring-security/site/index.html)
*   [Spring MVC REST](http://spring.io/guides/gs/rest-service/) + [Jackson](https://github.com/FasterXML/jackson)
*   Опционально поддержка WebSocket с помощью Spring Websocket
*   [Spring Data JPA](http://projects.spring.io/spring-data-jpa/) + Bean Validation
*   Обновление базы данных с [Liquibase](http://www.liquibase.org/)
*   [Elasticsearch](https://github.com/elastic/elasticsearch) если вам нужны возможности поиска данных в вашей базе
*   [MongoDB](http://www.mongodb.org) если вам нужна поддержка документо-ориентированной NoSQL базы данных, вместо JPA
*   [Cassandra](http://cassandra.apache.org/) если вам нужна граф-ориентирвоанная база данных NoSQL, вместо JPA
*   [Kafka](http://kafka.apache.org/) Если вам нужны технологии публикации-чтения сообщений в вашей системе

Есть все для запуска в прод:

*   Мониторинг с [Metrics](http://metrics.dropwizard.io/)
*   Кэширование с [ehcache](http://ehcache.org/) (local cache), [hazelcast](http://www.hazelcast.com/) or [Infinispan](http://infinispan.org/)
*   Опционально кластеризация http сессий [hazelcast](http://www.hazelcast.com/)
*   Оптимизация статических ресурсов с (gzip фильтр, HTTP cache headers)
*   Управление логами с [Logback](http://logback.qos.ch/), возможнос настраивать во время работы приложения
*   Пул соединений с [HikariCP](https://github.com/brettwooldridge/HikariCP) для оптимальной производительности
*   Сборка стандартного WAR файла или исполняемого JAR файла
*   Поддержка всех известных облачных провайдеров: AWS, Cloud Foundry, Heroku, Kubernetes, Docker...
