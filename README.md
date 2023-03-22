## Дипломный проект «Тестировщик ПО»   

#### Веб-сервис "Путешествие дня"
Дипломная работа представляет собой автоматизацию тестирования комплексного сервиса, взаимодействующего с СУБД и API Банка.

Приложение предлагает покупку тура по попределеннйо цене с помощью дебетовой, или кредитной карты. Приложение сохраняет данным об успешности /не успешности операции покупки и том, каким способом она была совршенна в собственной СУБД.

### Документация
* План автоматизации
* Отчет по итогам тестирования
* Итоговый отчёт по автоматизации

### Начало Работы
Загрузка на ПК репозитория с проэктом. Запустить IntelliJ IDEA, Docker Desktop 


### Запуск
1. Запускаем команду в терминал: docker-compose up -d

2. Запуск <strong>SUT</strong> командой в терминале:   
<strong>MySQL:</strong>  java "-Dspring.datasource.url=jdbc:mysql://localhost:3306/app" -jar artifacts/aqa-shop.jar   
<strong>PostgreSQL:</strong>   java "-Dspring.datasource.url=jdbc:postgresql://localhost:5432/app" -jar artifacts/aqa-shop.jar

3. Запуск авто-тестов в терминале:   
<strong>MySQL:</strong>   ./gradlew clean test "-Ddb.url=jdbc:mysql://localhost:3306/app"   
<strong>PostgreSQL:</strong>   ./gradlew clean test "-Ddb.url=jdbc:postgresql://localhost:5432/app"   

Приложение запускается в браузере: http://localhost:8080/

4. Генерация отчётов в <strong>Allure</strong>: ./gradlew allureServe
