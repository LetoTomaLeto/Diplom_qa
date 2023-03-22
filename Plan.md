<p><strong>Планирование автоматизации тестирования</strong></p>
<p><strong> Перечень автоматизируемых сценариев</strong></p>
<p><strong>Ввод исходных данных:</strong> <strong>APPROVED</strong> карта &mdash;&nbsp;4444 4444 4444 4441; <strong>DECLINED</strong> карта &mdash;&nbsp;4444 4444 4444 4442.</p>
<p><strong>Валидные данные:</strong></p>
<ul>
<li>поле&nbsp;<strong><em>Номер карты</em></strong>- 4444 4444 4444 4441 (APPROVED карта);</li>
<li>поле&nbsp;<strong><em>Месяц</em></strong>- 2-х значное число (от 01 до 12);</li>
<li>поле&nbsp;<strong><em>Год</em></strong>- 2-х значное число от 23 до 28 (срок действия карты - 5 лет);</li>
<li>поле&nbsp;<strong><em>Владелец</em></strong>- имя и фамилия на латинице (имя может состоять из одного слова, из двух слов, написанных через дефис или пробел, фамилия также может состоять из одного слова или из двух слов);</li>
<li>поле&nbsp;<strong><em>CVC/CVV</em></strong>- 3-х значное число (от 001 до 999).</li>
</ul>
<p></p>
<p><strong>Невалидные данные: </strong></p>
<ul>
<li>поле&nbsp;<strong><em>Номер карты</em></strong>: 4444 4444 4444 4442 (DECLINED карта); пустое поле; нули (0000 0000 0000 0000); 1 цифра; 15 цифр; 17 цифр;</li>
<li>поле&nbsp;<strong><em>Месяц</em></strong>: пустое поле; нули (00); одна цифра; число больше 12-ти;</li>
<li>поле&nbsp;<strong><em>Год</em></strong>: 22 (прошлый год); 29 (текущий год + 6 лет); пустое поле; нули (00); 1 цифра;</li>
<li>поле&nbsp;<strong><em>Владелец</em></strong>: имя и фамилия на кирилице; спецсимволы, кроме дефиса; одно слово на латинице; цифры; пустое поле; нули (000 000);</li>
<li>поле&nbsp;<strong><em>CVC/CVV</em></strong>: пустое поле; нули (00); 1 цифра.</li>
</ul>
<p>&nbsp;</p>
<p><strong>Оплата тура по дебетовой карте</strong></p>
<p><strong>Предусловия:</strong></p>
<ol>
<li>Открыть в браузере страницу сервиса покупки тура&nbsp;<strong>&laquo;</strong><strong>Путешествие дня&raquo;</strong>&nbsp;<a href="http://localhost:8080/">http://localhost:8080</a>.</li>
<li>Нажать кнопку&nbsp;<strong>&laquo;</strong><strong>Купить&raquo;</strong>, ниже на этой же странице откроется форма&nbsp;Оплата по карте.</li>
</ol>
<p><strong>Позитивный сценарий</strong><strong>:</strong></p>
<p><strong>Кейс 1. Отправка формы с валидными данными</strong></p>
<p><strong>Шаги воспроизведения</strong><strong>:</strong></p>
<ul>
<li>Ввести в поле&nbsp;<strong>&laquo;</strong><strong>Номер карты&raquo;</strong> номер тестовой карты - 4444 4444 4444 4441</li>
<li>Ввести в поле&nbsp;<strong>&laquo;</strong><strong>Месяц&raquo;</strong>&nbsp;валидное значение</li>
<li>Ввести в поле&nbsp;<strong>&laquo;</strong><strong>Год&raquo;</strong>&nbsp;валидное значение</li>
<li>Ввести в поле&nbsp;<strong>&laquo;</strong><strong>Владелец&raquo;</strong>&nbsp;валидное значение</li>
<li>Ввести в поле&nbsp;<strong>&laquo;</strong><strong>CVC/CVV&raquo;</strong>&nbsp;валидное значение</li>
<li>Нажать кнопку&nbsp;<strong>&laquo;</strong><strong>Продолжить</strong><strong>&raquo;</strong></li>
</ul>
<p><strong>ОР:</strong></p>
<ul>
<li>отправлен запрос в банк</li>
<li>pop up с надписью: Успешно</li>
<li>Операция одобрена банком</li>
</ul>
<p></p>
<p><strong>Кейс 2. Покупка тура в кредит. Отправка формы с валидными данными</strong></p>
<p><strong>Шаги воспроизведения</strong><strong>:</strong></p> 
<ul>
<li>Ввести в поле <strong>Номер карты</strong> номер тестовой карты - 4444 4444 4444 4441</li>
<li>Ввести в поле&nbsp;<strong>&laquo;</strong><strong>Месяц&raquo;</strong>&nbsp;валидное значение</li>
<li>Ввести в поле&nbsp;<strong>&laquo;</strong><strong>Год&raquo;</strong>&nbsp;валидное значение</li>
<li>Ввести в поле&nbsp;<strong>&laquo;</strong><strong>Владелец&raquo;</strong>&nbsp;валидное значение</li>
<li>Ввести в поле&nbsp;<strong>&laquo;</strong><strong>CVC/CVV&raquo;</strong>&nbsp;валидное значение</li>
<li>Нажать кнопку&nbsp;<strong>&laquo;</strong><strong>Продолжить</strong><strong>&raquo;</strong></li>
</ul>
<p><strong>ОР:</strong></p>
<ul>
<li>отправлен запрос в банк</li>
<li>pop up с надписью: Успешно</li>
<li>Операция одобрена банком</li>
</ul>

<p><strong>Негативные сценарии:</strong></p>
Пользователь совершает покупку тура в кредит "Купить", заполнение полей невалидными данными
<p></p>
<p><strong>Кейс 1. Отправка формы с пустым полем "Номер карты"</strong></p>
<p><strong>Шаги воспроизведения</strong><strong>:</strong></p>
<ul>
<li>Ввести в поле&nbsp;<strong>&laquo;</strong><strong>Номер карты&raquo;</strong>оставить пустым</li>
<li>Ввести в поле&nbsp;<strong>&laquo;</strong><strong>Месяц&raquo;</strong>&nbsp;валидное значение</li>
<li>Ввести в поле&nbsp;<strong>&laquo;</strong><strong>Год&raquo;</strong>&nbsp;валидное значение</li>
<li>Ввести в поле&nbsp;<strong>&laquo;</strong><strong>Владелец&raquo;</strong>&nbsp;валидное значение</li>
<li>Ввести в поле&nbsp;<strong>&laquo;</strong><strong>CVC/CVV&raquo;</strong>&nbsp;валидное значение</li>
<li>Нажать кнопку&nbsp;<strong>&laquo;</strong><strong>Продолжить</strong><strong>&raquo;</strong></li>
</ul>
<p><strong>ОР: </strong></p>
<ul>
<li>форма не отправлена</li>
<li>под полем&nbsp;<strong>&laquo;</strong><strong>Год&raquo;</strong> появилась подсказка - Неверный формат</li>
</ul>
<p></p>
<p><strong>Кейс 2. Отправка формы с неполностью заполненным полем "Номер карты"</strong></p>
<p><strong>Шаги воспроизведения</strong><strong>:</strong></p>
<ul>
<li>Ввести в поле&nbsp;<strong>&laquo;</strong><strong>Номер карты&raquo;</strong>4444 4444 4444 444</li>
<li>Ввести в поле&nbsp;<strong>&laquo;</strong><strong>Месяц&raquo;</strong>&nbsp;валидное значение</li>
<li>Ввести в поле&nbsp;<strong>&laquo;</strong><strong>Год&raquo;</strong>&nbsp;валидное значение</li>
<li>Ввести в поле&nbsp;<strong>&laquo;</strong><strong>Владелец&raquo;</strong>&nbsp;валидное значение</li>
<li>Ввести в поле&nbsp;<strong>&laquo;</strong><strong>CVC/CVV&raquo;</strong>&nbsp;валидное значение</li>
<li>Нажать кнопку&nbsp;<strong>&laquo;</strong><strong>Продолжить</strong><strong>&raquo;</strong></li>
</ul>
<p><strong>ОР: </strong></p>
<ul>
<li>форма не отправлена</li>
<li>под полем&nbsp;<strong>&laquo;</strong><strong>Год&raquo;</strong> появилась подсказка - Неверный формат</li>
</ul>
<p></p>
<p><strong>Кейс 3. Отправка формы с полями, содержащими нули</strong></p>
<p><strong>Шаги воспроизведения</strong><strong>:</strong></p>
<ul>
<li>Ввести в поле&nbsp;&laquo;Номер карты&raquo;&nbsp;- 0000 0000 0000 0000;</li>
<li>Ввести в поле&nbsp;&laquo;Месяц&raquo;&nbsp;валидное значение</li>
<li>Ввести в поле&nbsp;&laquo;Год&raquo;&nbsp;валидное значение</li>
<li>Ввести в поле&nbsp;&laquo;Владелец&raquo;&nbsp;валидное значение</li>
<li>Ввести в поле&nbsp;&laquo;CVC/CVV&raquo;&nbsp;валидное значение</li>
<li>Нажать кнопку&nbsp;&laquo;Продолжить&raquo;</li>
</ul>
<p><strong>ОР: </strong></p>
<ul>
<li>форма не отправлена</li>
<li>под полем&nbsp;<strong>&laquo;</strong><strong>Год&raquo;</strong> появилась подсказка - Неверный формат</li>
</ul>
<p></p>
<p><strong>Кейс 4. Отправка формы с данными DECLINED карты</strong></p>
<p><strong>Шаги воспроизведения</strong><strong>:</strong></p>
<ul>
<li>Ввести в поле&nbsp;<strong>&laquo;</strong><strong>Номер карты&raquo;</strong> номер тестовой карты - 4444 4444 4444 4442</li>
<li>Ввести в поле&nbsp;<strong>&laquo;</strong><strong>Месяц&raquo;</strong>&nbsp;валидное значение</li>
<li>Ввести в поле&nbsp;<strong>&laquo;</strong><strong>Год&raquo;</strong>&nbsp;валидное значение</li>
<li>Ввести в поле&nbsp;<strong>&laquo;</strong><strong>Владелец&raquo;</strong>&nbsp;валидное значение</li>
<li>Ввести в поле&nbsp;<strong>&laquo;</strong><strong>CVC/CVV&raquo;</strong>&nbsp;валидное значение</li>
<li>Нажать кнопку&nbsp;<strong>&laquo;</strong><strong>Продолжить</strong><strong>&raquo;</strong></li>
</ul>
<p><strong>ОР: </strong></p>
<ul>
<li>запрос в банк отправлен</li>
<li>всплывает pop up: Ошибка!</li>
<li>Банк отказал в проведении операции</li>
</ul>
<p></p>
<p><strong>Кейс 5. Отправка формы с невалидным значением "Месяц"</strong></p>
<p><strong>Шаги воспроизведения</strong><strong>:</strong></p>
<ul>
<li>Ввести в поле&nbsp;<strong>&laquo;</strong><strong>Номер карты&raquo;</strong> номер тестовой карты - 4444 4444 4444 4441</li>
<li>Ввести в поле&nbsp;<strong>&laquo;</strong><strong>Месяц&raquo;</strong>&nbsp;невалидное значение - 13</li>
<li>Ввести в поле&nbsp;<strong>&laquo;</strong><strong>Год</strong>&raquo;&nbsp;валидное значение</li>
<li>Ввести в поле&nbsp;<strong>&laquo;</strong><strong>Владелец&raquo;</strong>&nbsp;валидное значение</li>
<li>Ввести в поле&nbsp;<strong>&laquo;</strong><strong>CVC/CVV&raquo;</strong>&nbsp;валидное значение</li>
<li>Нажать кнопку&nbsp;<strong>&laquo;</strong><strong>Продолжить&raquo;</strong></li>
</ul>
<p><strong>ОР:</strong></p>
<ul>
<li>форма не отправлена, под полем&nbsp;<strong>&laquo;</strong><strong>Месяц&raquo;</strong> появилась подсказка - Неверно указан срок действия карты</li>
</ul>
<p></p>
<p><strong>Кейс 6. Отправка формы с пустым полем "Месяц"</strong></p>
<p><strong>Шаги воспроизведения</strong><strong>:</strong></p>
<ul>
<li>Ввести в поле&nbsp;<strong>&laquo;</strong><strong>Номер карты&raquo;</strong> номер тестовой карты - 4444 4444 4444 4441</li>
<li>Ввести в поле&nbsp;<strong>&laquo;</strong><strong>Месяц&raquo;</strong>&nbsp;оставить пустым</li>
<li>Ввести в поле&nbsp;<strong>&laquo;</strong><strong>Год</strong>&raquo;&nbsp;валидное значение</li>
<li>Ввести в поле&nbsp;<strong>&laquo;</strong><strong>Владелец&raquo;</strong>&nbsp;валидное значение</li>
<li>Ввести в поле&nbsp;<strong>&laquo;</strong><strong>CVC/CVV&raquo;</strong>&nbsp;валидное значение</li>
<li>Нажать кнопку&nbsp;<strong>&laquo;</strong><strong>Продолжить&raquo;</strong></li>
</ul>
<p><strong>ОР:</strong></p>
<ul>
<li>форма не отправлена, под полем&nbsp;<strong>&laquo;</strong><strong>Месяц&raquo;</strong> появилась подсказка - Поле обязательно для заполнения</li>
</ul>
<p></p>
<p><strong>Кейс 7. Отправка формы с невалидным значением "Год"</strong></p>
<p><strong>Шаги воспроизведения</strong><strong>:</strong></p>
<ul>
<li>Ввести в поле&nbsp;<strong>&laquo;</strong><strong>Номер карты&raquo;</strong> номер тестовой карты - 4444 4444 4444 4441</li>
<li>Ввести в поле&nbsp;<strong>&laquo;</strong><strong>Месяц&raquo;</strong>&nbsp;валидное значение</li>
<li>Ввести в поле&nbsp;<strong>&laquo;</strong><strong>Год</strong>&raquo;&nbsp;невалидное значение - 22</li>
<li>Ввести в поле&nbsp;<strong>&laquo;</strong><strong>Владелец&raquo;</strong>&nbsp;валидное значение</li>
<li>Ввести в поле&nbsp;<strong>&laquo;</strong><strong>CVC/CVV&raquo;</strong>&nbsp;валидное значение</li>
<li>Нажать кнопку&nbsp;<strong>&laquo;</strong><strong>Продолжить&raquo;</strong></li>
</ul>
<p><strong>ОР:</strong></p>
<ul>
<li>форма не отправлена, под полем&nbsp;<strong>&laquo;</strong><strong>Год&raquo;</strong> появилась подсказка - Истёк срок действия карты</li>
</ul>
<p></p>
<p><strong>Кейс 8. Отправка формы с пустым полем "Год"</strong></p>
<p><strong>Шаги воспроизведения</strong><strong>:</strong></p>
<ul>
<li>Ввести в поле&nbsp;<strong>&laquo;</strong><strong>Номер карты&raquo;</strong> номер тестовой карты - 4444 4444 4444 4441</li>
<li>Ввести в поле&nbsp;<strong>&laquo;</strong><strong>Месяц&raquo;</strong>&nbsp;валидное значение</li>
<li>Ввести в поле&nbsp;<strong>&laquo;</strong><strong>Год</strong>&raquo;&nbsp;оставить пустым</li>
<li>Ввести в поле&nbsp;<strong>&laquo;</strong><strong>Владелец&raquo;</strong>&nbsp;валидное значение</li>
<li>Ввести в поле&nbsp;<strong>&laquo;</strong><strong>CVC/CVV&raquo;</strong>&nbsp;валидное значение</li>
<li>Нажать кнопку&nbsp;<strong>&laquo;</strong><strong>Продолжить&raquo;</strong></li>
</ul>
<p><strong>ОР:</strong></p>
<ul>
<li>форма не отправлена, под полем&nbsp;<strong>&laquo;</strong><strong>Год&raquo;</strong> появилась подсказка - Поле обязательно для заполнения</li>
</ul>
<p></p>
<p><strong>Кейс 9. Отправка формы с неполным именем владельца карты в поле "Владелец"</strong></p>
<p><strong>Шаги воспроизведения</strong><strong>:</strong></p>
<ul>
<li>Ввести в поле&nbsp;<strong>&laquo;</strong><strong>Номер карты&raquo;</strong> номер тестовой карты - 4444 4444 4444 4441</li>
<li>Ввести в поле&nbsp;<strong>&laquo;</strong><strong>Месяц&raquo;</strong>&nbsp;валидное значение</li>
<li>Ввести в поле&nbsp;<strong>&laquo;</strong><strong>Год</strong>&raquo;&nbsp;валидное значение</li>
<li>Ввести в поле&nbsp;<strong>&laquo;</strong><strong>Владелец&raquo;</strong>&nbsp;неполное данный имени владельца карты - ввести одну букву</li>
<li>Ввести в поле&nbsp;<strong>&laquo;</strong><strong>CVC/CVV&raquo;</strong>&nbsp;валидное значение</li>
<li>Нажать кнопку&nbsp;<strong>&laquo;</strong><strong>Продолжить&raquo;</strong></li>
</ul>
<p><strong>ОР:</strong></p>
<ul>
<li>форма не отправлена</li>
<li>под полем&nbsp;<strong>&laquo;</strong><strong>Год&raquo;</strong> появилась подсказка - Неверный формат</li>
</ul>
<p></p>
<p><strong>Кейс 10. Отправка формы с пустым полем "Владелец"</strong></p>
<p><strong>Шаги воспроизведения</strong><strong>:</strong></p>
<ul>
<li>Ввести в поле&nbsp;<strong>&laquo;</strong><strong>Номер карты&raquo;</strong> номер тестовой карты - 4444 4444 4444 4441</li>
<li>Ввести в поле&nbsp;<strong>&laquo;</strong><strong>Месяц&raquo;</strong>&nbsp;валидное значение</li>
<li>Ввести в поле&nbsp;<strong>&laquo;</strong><strong>Год</strong>&raquo;&nbsp;валидное значение</li>
<li>Ввести в поле&nbsp;<strong>&laquo;</strong><strong>Владелец&raquo;</strong>&nbsp;оставить пустым</li>
<li>Ввести в поле&nbsp;<strong>&laquo;</strong><strong>CVC/CVV&raquo;</strong>&nbsp;валидное значение</li>
<li>Нажать кнопку&nbsp;<strong>&laquo;</strong><strong>Продолжить&raquo;</strong></li>
</ul>
<ul>
<p><strong>ОР:</strong></p>
<li>форма не отправлена</li>
<li>всплывает pop up: Поле обязательно для заполнения</li>
</ul>
<p></p>
<p><strong>Кейс 11. Отправка формы с полем "Владелец" заполненным на кириллице</strong></p>
<p><strong>Шаги воспроизведения</strong><strong>:</strong></p>
<ul>
<li>Ввести в поле&nbsp;<strong>&laquo;</strong><strong>Номер карты&raquo;</strong> номер тестовой карты - 4444 4444 4444 4441</li>
<li>Ввести в поле&nbsp;<strong>&laquo;</strong><strong>Месяц&raquo;</strong>&nbsp;валидное значение</li>
<li>Ввести в поле&nbsp;<strong>&laquo;</strong><strong>Год</strong>&raquo;&nbsp;оставить пустым</li>
<li>Ввести в поле&nbsp;<strong>&laquo;</strong><strong>Владелец&raquo;</strong>&nbsp;ввести имя на кириллице (например Иванов Иван)</li>
<li>Ввести в поле&nbsp;<strong>&laquo;</strong><strong>CVC/CVV&raquo;</strong>&nbsp;валидное значение</li>
<li>Нажать кнопку&nbsp;<strong>&laquo;</strong><strong>Продолжить&raquo;</strong></li>
</ul>
<ul>
<p><strong>ОР:</strong></p>
<li>форма не отправлена</li>
<li>под полем&nbsp;<strong>&laquo;</strong><strong>Год&raquo;</strong> появилась подсказка - Неверный формат</li>
</ul>
<p></p>
<p><strong>Кейс 12. Отправка формы с пустым полем "CVC/CVV"</strong></p>
<p><strong>Шаги воспроизведения</strong><strong>:</strong></p>
<ul>
<li>Ввести в поле&nbsp;<strong>&laquo;</strong><strong>Номер карты&raquo;</strong> номер тестовой карты - 4444 4444 4444 4441</li>
<li>Ввести в поле&nbsp;<strong>&laquo;</strong><strong>Месяц&raquo;</strong>&nbsp;валидное значение</li>
<li>Ввести в поле&nbsp;<strong>&laquo;</strong><strong>Год</strong>&raquo;&nbsp;валидное значение</li>
<li>Ввести в поле&nbsp;<strong>&laquo;</strong><strong>Владелец&raquo;</strong>&nbsp;валидное значение</li>
<li>Ввести в поле&nbsp;<strong>&laquo;</strong><strong>CVC/CVV&raquo;</strong>&nbsp;оставить пустым</li>
<li>Нажать кнопку&nbsp;<strong>&laquo;</strong><strong>Продолжить&raquo;</strong></li>
</ul>
<p><strong>ОР:</strong></p>
<li>форма не отправлена, под полем&nbsp;<strong>&laquo;</strong><strong>Год&raquo;</strong> появилась подсказка - Поле обязательно для заполнения</li>
</ul>
<p></p>
<p><strong>Кейс 13. Отправка формы с невалидным значением "CVC/CVV"</strong></p>
<p><strong>Шаги воспроизведения</strong><strong>:</strong></p>
<ul>
<li>Ввести в поле&nbsp;<strong>&laquo;</strong><strong>Номер карты&raquo;</strong> номер тестовой карты - 4444 4444 4444 4441</li>
<li>Ввести в поле&nbsp;<strong>&laquo;</strong><strong>Месяц&raquo;</strong>&nbsp;валидное значение</li>
<li>Ввести в поле&nbsp;<strong>&laquo;</strong><strong>Год</strong>&raquo;&nbsp;валидное значение</li>
<li>Ввести в поле&nbsp;<strong>&laquo;</strong><strong>Владелец&raquo;</strong>&nbsp;валидное значение</li>
<li>Ввести в поле&nbsp;<strong>&laquo;</strong><strong>CVC/CVV&raquo;</strong>&nbsp;невалидно значение (например, ввести 1 цифру)</li>
<li>Нажать кнопку&nbsp;<strong>&laquo;</strong><strong>Продолжить&raquo;</strong></li>
</ul>
<ul>
<p><strong>ОР:</strong></p>
<li>форма не отправлена</li>
<li>под полем&nbsp;<strong>&laquo;</strong><strong>Год&raquo;</strong> появилась подсказка - Неверный формат</li>
</ul>
<p></p>
<p><strong>Кейс 14. Оплата тура в кредит</strong></p>
<p><strong>Предусловия:</strong></p>
<ul>
<li>Открыть в браузере страницу сервиса покупки тура&nbsp;<strong>&laquo;</strong><strong>Путешествие дня&raquo;</strong>&nbsp;<a href="http://localhost:8080/">http://localhost:8080</a>.</li>
<li>Нажать кнопку&nbsp;<strong>&laquo;</strong><strong>Купить в кредит&raquo;</strong>, ниже на этой же странице откроется форма&nbsp;<strong>&laquo;</strong><strong>Кредит по данным карты&raquo;</strong></li>
<li>Повторить сценарии для оплаты тура по дебетовой карте</li>
</ul>
<p><strong>Перечень используемых инструментов с обоснованием выбора</strong></p>
<ul>
<li><strong>IntelliJ IDEA</strong> - интегрированная среда разработки для Java.</li>
<li><strong>Gradle</strong> - инструмент автоматизации сборки и управления зависимостями, более быстрый, чем Maven.</li>
<li><strong>JUnit 5</strong> - тестовая среда, содержит необходимые аннотации и assert'ы.</li>
<li><strong>JavaFaker</strong> - генератор данных.</li>
<li><strong>Selenide</strong> - фреймворк для автоматизированного тестирования веб-приложений на основе Selenium WebDriver, имеет простую конфигурацию по сравнению с Selenium.</li>
<li><strong>Docker Desktop</strong> - наиболее распространенная система контейнеризации.</li>
<li><strong>MySQL</strong> - база данных.</li>
<li><strong>Allure</strong> - фрейворк для составления отчетов.</li>
<li><strong>Git и GitHub</strong> - хранение кода, автотестов.</li>
</ul>
<p><strong> Перечень и описание возможных рисков при автоматизации</strong></p>
<ul>
<li>Отсутствие технического задания.</li>
<li>Тесты могут не покрывать всех возможных сценариев.</li>
<li>Потеря актуальности автотестов при любом изменении дизайна.</li>
</ul>
<p><strong> Интервальная оценка с учётом рисков в часах</strong></p>
<ul>
<li>Написание плана - 4 часа</li>
<li>Написание автотестов - 30 часов</li>
<li>Выполнение автотестов с описанием процедуры запуска - 2 часа</li>
<li>Оформление issue - 4 часа</li>
</ul>
<p><strong> План сдачи работ: когда будут проведены автотесты, результаты их проведения и отчёт по автоматизации</strong></p>
<ul>
<li>Автоматизация - 18.03.23</li>
<li>Подготовка отчётных документов по итогам тестирования - 19.03.23</li>
<li>Подготовка отчётных документов по итогам автоматизации - 20.03.23</li>
</ul>
