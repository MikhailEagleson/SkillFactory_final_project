# SkillFactory_final_project
Итоговый проект по курсу тестировщик-автоматизатор на python от SkillFactory !!!!
 
ВНИМАНИЕ !!!! !! По условиям технического задания и при отсутствии тестовых данных (тестовая учетная запись от заказчика, 
тестовый номер телефона, адрес тестовой электронной почты, тестового логина и тестового номера личного счёта и тестовых паролей к выше перечисленным), 
разработанные автотесты проверяют UI часть web-сайта. Без проверок редиректа к основному продукту, без регистрации нового пользователя и без проверки 
корректного восстановления пароля. 
Тесты проверяют логику UI компонентов и корректную валидацию данных формы !! 

Для запуска автотестов необходимо склонировать содержимое репозитория, открыть проект и в командной консоли поочереди ввести следующие команды: 
"cd final_project/tests" и "pytest"

!! В случае, если на компьютере не установлены библиотеки для работы с Selenium необходимо ввести команду в терминале "python -m pip install selenium", 
а противном случае, тесты не запустятся. Список установленных модулей можно посмотреть командой "pip freeze" если ввести ее в терминале. Поочередно 
запустятся 3 файла тестов: test_rostelekom_auth.py, test_rostelekom_register.py и test_rostelekom_restore.py

- Первый файл проверяет элементы находящиеся непосредственно на страницы "Авторизация". Сценарии проверки:
Корректно изменяются поля ввода логина в соответствии с выбранным табом; корректно проходит валидация типа логина (мобилный телефон, почта, логин, личный счёт) 
в автоматическом режиме; выводится корректное сообщение об ошибке попытки авторизации (если на странице есть каптча, то проверяется что текст ошибки связан 
непосредственно с капчей, а не с ошибкой логина/пароля) при каждом возможном типе авторизации; при попытке авторизоваться через стороннее 
API (вк, ок, мэйл, гугл и яндекс), происходит редирект на API указанного метода авторизации; корректно происходит редирект на страницу восстановления пароля; 
корректно происходит редирект на страницу регистрации нового пользователя. 
- Второй файл проверяет элементы находящиеся непосредственно на страницы "Регистрация". 
Сценарий проверки содержит всего 1 тест который имитирует ручное тестирование по нескольким тест-кейсам.
- Третий файл проверяет элементы находящиеся непосредственно на страницы "Восстановление пароля". В проверки данного файла входят следующие тесты:
Корректно изменяются поля ввода логина в соответствии с выбранным табом; выводится корректное сообщение об ошибке попытки восстановить пароль 
(в случае если пользователь ввел не верное решение на капчу) для каждого способа восстановления пароля; корректно происходит обновление капчи, когда полтзователь 
нажимает на иконку "обновить капчу"; корректно происходит редирект обратно на страницу авторизации.
