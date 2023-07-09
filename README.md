# Тренировочный проект на django

Создать локальную папку будущего проекта ('my_first_project_on_django').

В терминале командой 'cd' перйти в папку проекта.

Командой 'python -m venv venv' создать виртуальное окружение 'venv'.

Командой '.\venv\Scripts\activate.ps1' активировать виртуальное окружение.

Создать файл '.gitignore' со строкой '/venv'.

Командой 'git init' создать репозиторий git.

Командой 'git add .gitignore' проиндексировать файл '.gitignore'.

Командой 'git commit -m "Добавить .gitignore"' закоммитить добавление .gitignore.

На GitHub создать репозиторий с названием проекта ('my_first_project_on_django').

Командой 'git remote add origin ССЫЛКА НА РЕПОЗИТОРИЙ ПРОЕКТА НА GITHAB' связать локальный и удаленный 
репозитории.

Командой 'git branch -M main' переименовать главную ветку с 'master' на 'main'.

Командой 'git push -u origin main' загрузить содержимое локального репозитория в удаленный репозиторий 
GitHub.

Командой 'django-admin startproject ИМЯ_ПРОЕКТА' создать проект ('coolsite').

Командой 'cd ИМЯ_ПРОЕКТА' перейти в папку проекта ('coolsite').

Командой 'python manage.py runserver' запустить локальный сервер.

Командой 'python manage.py startapp ИМЯ_ПРИЛОЖЕНИЯ' запустить приложение ('women') в проекте ('coolsite').

В файл ИМЯ_ПРОЕКТА/ИМЯ_ПРОЕКТА/settings.py в список INSTALLED_APPS добавить приложение 
'women.apps.WomenConfig' (из coolsite/coolsite/settings.py/INSTALLED_APPS вызывается класс
coolsite/women/apps.py/WomenConfig

Создать обработчик (функция или класс) главной страницы сайта: в файле coolsite/women/views.py создать 
функцию index (def index(request): return HttpResponse('Страница приложения women.')) и импортировать 
HttpResponse из модуля django.http.

В файл coolsite/coolsite/urls.py в список urlpatterns добавить путь path('women/', index) и импортировать
index из модуля women/views.

В coolsite/urls.py вместо импортирования всех функций из women/views импортировать include из модуля
django.urls, в список urlpatterns вместо всех путей добавить include('women.urls').

Создать файл women/urls.py, в который импортировать path из django.urls и все функции-обработчики из .views,
создать список urlpatterns.

Добавить в women/urls.py в urlpatterns путь 'cats/<int:catid>/' и шаблон пути 
r'^archive/(?P<year>[0-9]{4})', в views.py обработчик archive, отображающий словарь request.GET, и 
обработчик pageNotFound. Настроить settings.py на боевой режим (DEBUG = False, 
ALLOWED_HOSTS = ['127.0.0.1']).