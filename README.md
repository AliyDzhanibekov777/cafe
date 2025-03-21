# Программа для автоматизации заказов кафе, ресторанов.


## Описание программы
Данная программа разработана для автоматизации заказов в заведениях общественного питания
Был реализован функционал:
1. Добавление/Удаление блюд в меню
2. Создания заказа выбором блюд в меню и указание номера стола
3. Управление состоянием заказа (В ожидании/Готово/Оплачено)
4. Автоматическим подсчетом итоговой выручки


## Устанорвка
1. Клонирование репозитория:
    git clone https://github.com/AliyDzhanibekov777/cafe.git

2. Установка виртуального окружения:
    python -m venv .venv

3. Активация виртуального окружения:
    .venv\Scripts\Activate.ps1

4. Переход в каталог проекта:
    cd cafe

5. Установка зависимости:
   pip install -r requirements.txt
   

## Настройка
1. Создайте файл .env и добавьте необходимые переменные окружения:
    DEBUG=True
    SECRET_KEY='your-secret-key'

2. Выполнение миграций:
   python manage.py migrate
   
3. Запуск сервера разработки
   python manage.py runserver

4. Теперь вы можете зайти на http://127.0.0.1:8000/.


## Использование API
1. Получение списка заказов:
    GET 'api/v1/order/'

2. Добавление заказа:
    POST 'api/v1/order/'
    Пример:
        {
        "id": 2,
        "table_number": 3,
        "status": "Оплачено",
        "items": [2, 3, 5]
        },
   
3. Получение заказа по id
    GET 'v1/order/<int:pk>/'

4. Удаление заказа:
    DELETE 'v1/order/delete/<int:pk>/'


## Тестирование
1. python manage.py test


# Автор
Алий Джанибеков
