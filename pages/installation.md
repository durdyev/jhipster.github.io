---
layout: default
title: Установка JHipster
permalink: /installation/
sitemap:
    priority: 0.7
    lastmod: 2016-12-21T00:00:00-00:00
---

# <i class="fa fa-cloud-download"></i> Установка JHipster

## Шаги установки

Мы предоставляем 4 способа работы с JHipster:

*   Установка локально с помощью Yarn, является классическим способом работы с JHipster.
*   Установка с помощью NPM, так же является классическим способо установки, как и установка с Yarn, но используется NPM.
*   Установка Vagrant контейнера, со всеми необходимыми инструментами на виртуальную машину Ubuntu.
*   Установка Docker контейнера, который предоставит вам легкий виртуальный контейнер, с установленным JHipster.

## Локальная установка с помощью Yarn (рекомендуемый способ для нормального пользователя)

1.  Установите Java 8 с [официального сайта Oracle](http://www.oracle.com/technetwork/java/javase/downloads/index.html).
2.  (Опционально) Установить сборщик Java.
    *   Выбирая [Maven](http://maven.apache.org/) или [Gradle](http://www.gradle.org/), вам обычно не нужно ничего устанавливать, так как JHipster автоматически установит [Maven Wrapper](https://github.com/takari/maven-wrapper) или [Gradle Wrapper](http://gradle.org/docs/current/userguide/gradle_wrapper.html) для вас.
    *   Если вы хотите установить все вручную, скачайте и установите их с сайтов [Maven website](http://maven.apache.org/) или [Gradle website](http://www.gradle.org/).
3.  Установите Git с сайта [git-scm.com](http://git-scm.com/). Мы рекомендуем вам так же использовать инструмент [SourceTree](http://www.sourcetreeapp.com/), если вы только начинаете работу с Git.
4.  Установите Node.js с сайта [the Node.js website](http://nodejs.org/) (предпочтительно использовать LTS версию)
5.  Установите Yarn с сайта [the Yarn website](https://yarnpkg.com/en/docs/install)
6.  Установитье Yeoman: `yarn global add yo`
7.  Только для AngularJS 1, установите Bower: `yarn global add bower`
8.  Только для AngularJS 1, установите Gulp: `yarn global add gulp-cli`
9.  Установите JHipster: `yarn global add generator-jhipster`

Подсказка: Если у вас есть проблема с использованием этих инструментов глобально, будьте уверены, что у вас задана переменная 
`$HOME/.config/yarn/global/node_modules/.bin`.

На Mac или Linux: ```export PATH="$PATH:`yarn global bin`:$HOME/.config/yarn/global/node_modules/.bin"```

JHipster использует [Yeoman](http://yeoman.io/) для генерации кода.
Чтобы найти больше информации, пожалуйста посмотрите [Yeoman "Начало работы](http://yeoman.io/learning/index.html) и на сайте 
[Yarn документации](https://yarnpkg.com/), прежде чем [заводить bug](https://github.com/jhipster/generator-jhipster/issues?state=open).

Сейчас когда JHipster установлен, следующий шаг - [создать приложение]({{ site.url }}/creating-an-app/)

## Локальная установка с NPM (отличный способ от Yarn)

1.  Установить Java 8 с сайта [the Oracle website](http://www.oracle.com/technetwork/java/javase/downloads/index.html).
2.  (Опционально) Установить сборщик Java.
    *   Выбирая [Maven](http://maven.apache.org/) или [Gradle](http://www.gradle.org/), вам обычно не нужно ничего устанавливать, так как JHipster автоматически установит [Maven Wrapper](https://github.com/takari/maven-wrapper) или [Gradle Wrapper](http://gradle.org/docs/current/userguide/gradle_wrapper.html) для вас.
    *   Если вы хотите установить все вручную, скачайте и установите их с сайтов [Maven website](http://maven.apache.org/) или [Gradle website](http://www.gradle.org/).
3.  Установите Git с сайта [git-scm.com](http://git-scm.com/). Мы рекомендуем вам так же использовать инструмент [SourceTree](http://www.sourcetreeapp.com/), если вы только начинаете работу с Git.
4.  Установите Node.js с сайта [the Node.js website](http://nodejs.org/) (предпочтительно использовать LTS версию)
5.  (Рекомендовано) Обновить NPM: `npm install -g npm`
6.  Установить Yeoman: `npm install -g yo`
7.  Только для AngularJS 1, установить Bower: `npm install -g bower`
8.  Только для AngularJS 1, установить Gulp: `npm install -g gulp-cli` (если у вас уже установлен Gulp, запустите эту команду `npm rm -g gulp`, чтобы быть увереным, что старая версия gulp не будет конфликтовать с `gulp-cli`)
9.  Установите JHipster: `npm install -g generator-jhipster`
10.  (Опционально) Установить Yarn: `npm install -g yarn` (Если установили, то после генерации проекта, `yarn install` будет запущен, вместо `npm install`)

Здесь можно найти больше информации [NPM documentation](https://docs.npmjs.com/).

## Установка с помощью Vagrant box

[JHipster development box](https://github.com/jhipster/jhipster-devbox) предоставляет вам проект со всему необходимыми инструментами для разработки проекта JHipster.

Это самый простой, чтобы начать работу с JHipster.

Кроме JHipster, эта виртуальная машина включает в себя множество инструментов для разработки, так же как и Docker, у вас будет все необходимое для разработки.

Посетите сайт [JHipster development box page](https://github.com/jhipster/jhipster-devbox) для более подробной информации.

## Установка Docker (только для продвинутых пользователей)

_Пожалуйста помните: этот Docker образ для запуска JHipster generator внутри контейнера. Это полностью отличается от [Docker и Docker Compose configurations]({{ site.url }}/docker-compose/) этот JHipster сгенерирует приложение внутри контейнера_

### Информация

У JHipster есть специальный [Dockerfile](https://github.com/jhipster/generator-jhipster/blob/master/Dockerfile), который описывает [Docker](https://www.docker.io/) образ.

С помощью этого делаются автосборки, которые доступны здесь: [https://hub.docker.com/r/jhipster/jhipster/](https://hub.docker.com/r/jhipster/jhipster/)

Этот образо дает возможность запускать JHipster внутри Docker контейнера.

### Необходимые требования

Зависит от вашей операционной системы.

1.  **Linux:** Linux поддерживает Docker из коробки. Нужно только следовать инструкциям на этой странице [Docker](https://docs.docker.com/installation/#installation).
2.  **Mac & Windows:** установка [Docker Toolbox](https://www.docker.com/docker-toolbox) очень проста.

Сгенерированные файлы будут доступны в ващей общей директории, и вы не сможете их удалить, до тех пор, пока запущен контейнер. Если вы не хотите чтобы Docker скачивал все зависимости Maven и NPM каждый раз, вам необходимо закоммитить состяение или смонтировать образ.

<div class="alert alert-warning"><i>Осторожно: </i>

Зависит от ОС, ваш <code>DOCKER_HOST</code> будет разный. На Linux, это будет просто localhost.
Для Mac/Windows, вам нужно настроить IP, используя: <code>docker-machine ip default</code>

</div>

<div class="alert alert-info"><i>Подсказка: </i>

Kitematic это простой в использовании графический интерфейс Docker Toolbox, который сделает установки намного проще.

</div>

На Linux вам необходимо использовать команду запуска `docker` от имени root пользователя если ващ пользователь не принадлежит группе docker. Вы можете добавить вашего пользователя в группу docker и тогда использовать команды без root. Инструкция по настройке [http://askubuntu.com/a/477554](http://askubuntu.com/a/477554).

### Использование на Linux/Mac Windows (используя Docker Toolbox)

#### Загрузка образа

Загрузка последнего образа JHipster Docker:

`docker image pull jhipster/jhipster`

Загрузка образа для разработки JHipster Docker image:

`docker image pull jhipster/jhipster:master`

Вы можете посмотреть все доступные теги [here](https://hub.docker.com/r/jhipster/jhipster/tags/)

#### Запуска образа

<div class="alert alert-warning"><i>Warning: </i>

Если вы используете Docker Machine на Mac или Windows, ваш образ Docker daemon имеет ограниченный доступ к вашей OS X или Windows файловой системе. Docker Machine попытается автоматически получить общий доступ к директории /Users (OS X) или C:\Users\&lt;username&gt; (Windows) директории. Вам необходимо будет создать директорию проекта там, чтобы избежать автоматического монтирования.

</div>


Создайте дирекотрию "jhipster" в вашей домашней директории:

`mkdir ~/jhipster`

Запустите Docker со следующими параметрами:

*   Docker "/home/jhipster/app" директория расшарена с локальной "~/jhipster" директорией
*   Перенаправьте все порты Docker (8080 для Java приложения, 9000 для BrowserSync, 3001 для BrowserSync UI)

`docker container run --name jhipster -v ~/jhipster:/home/jhipster/app -v ~/.m2:/home/jhipster/.m2 -p 8080:8080 -p 9000:9000 -p 3001:3001 -d -t jhipster/jhipster`

<div class="alert alert-info"><i>Подсказка: </i>

Если вы уже запустили контейнер, вам не нужено еще раз запускать эту команду, просто используйте команды start/stop для существующего контейнера.

</div>

#### Проверьте что контейнера работает

Чтобы проверить это, используйте команду `docker container ps`:

    CONTAINER ID    IMAGE               COMMAND                 CREATED         STATUS          PORTS                                                       NAMES
    4ae16c0539a3    jhipster/jhipster   "tail -f /home/jhipst"  4 seconds ago   Up 3 seconds    0.0.0.0:9000-3001->9000-3001/tcp, 0.0.0.0:8080->8080/tcp    jhipster

#### Базовые операции

*   Чтобы остановить контейнер, используйте команду: `docker container stop jhipster`
*   Чтобы запустить контейнер, используйте команду: `docker container start jhipster`

Если вы обновили образ Docker (rebuild or pull from the Docker hub), лучше удалить существующий контейнер, и заново запустить новый. Чтобы сделать это, сначала остановите контейнер, запустите его и затем:

1.  `docker container stop jhipster`
2.  `docker container rm jhipster`
3.  `docker image pull jhipster/jhipster`
4.  `docker container run --name jhipster -v ~/jhipster:/home/jhipster/app -v ~/.m2:/home/jhipster/.m2 -p 8080:8080 -p 9000:9000 -p 3001:3001 -d -t jhipster/jhipster`

### Доступ к контейнеру

<div class="alert alert-warning"><i>Осторожно: </i>

На Windows, you need to execute the Docker Quick Terminal as Administrator to be able to create symlinks during the `yarn install` step.

</div>

The easiest way to log into the running container is by executing following command:

`docker container exec -it <container_name> bash`

If you copy-pasted the above command to run the container, notice that you have to specify `jhipster` as the container name:

`docker container exec -it jhipster bash`

You will log in as the "jhipster" user.

If you want to log in as "root", as the `sudo` command isn't available in Ubuntu Xenial, you need to run:

`docker container exec -it --user root jhipster bash`

### Your first project

You can then go to the /home/jhipster/app directory in your container, and start building your app inside Docker:

`cd /home/jhipster/app`

`jhipster`

<div class="alert alert-info"><i>Tip: </i>

If you are having issues with Yarn, you can use <code>jhipster --npm</code>, to use NPM instead of Yarn.

</div>

Once your application is created, you can run all the normal gulp/bower/maven commands, for example:

`./mvnw`

**Congratulations! You've launched your JHipster app inside Docker!**

On your host machine, you should be able to :

*   Access the running application at `http://DOCKER_HOST:8080`
*   Get all the generated files inside your shared folder

<div class="alert alert-warning"><i>Warning: </i>
    By default, Docker is not installed inside the <code>jhipster/jhipster</code> image.
    <br/>
    So you won't be able to:
    <ul>
        <li>use the docker-compose files</li>
        <li>build a Docker image (Maven goal: <code>docker:build</code> or Gradle task: <code>buildDocker</code>)</li>
    </ul>
</div>
