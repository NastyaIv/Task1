# Task1
## Инструкция
1. Открыть ivakhnenko_hw_1.ipynb с помощью Jupyter Notebook (https://jupyter.org/ он также встроен в Anaconda)
2. Данные поместить в папку с ivakhnenko_hw_1.ipynb (в распакованном виде)
3. Изменить переменную path в соответствии с директорией, куда Вы сохранили данные и тетрадку ivakhnenko_hw_1.ipynb
4. Установить MySQL (https://dev.mysql.com/downloads/installer/)
5. Обновить пакет pandas до последней версии командной строке anaconda (pip install --upgrade pandas)
6. Установить пакет MyqSQL connector в командной строке anaconda: pip install MySQL-connector-python
6. Создать БД в MySQL:
 + Открыть командную строку MySQL Command Line Client
 + Создать новую БД: CREATE DATABASE hw_db;
 + В ivakhnenko_hw_1.ipynb изменить переменную password на пароль от вашего root-пользователя, или также изменить переменную user, если используете другого пользователя.
8. Запустить код (Cell -> run all)

## Описание кода и результаты
1. В первой части данные по заявкам и контрактам загружаются из эксель файлов в питон, происходит их обработка (приведение дат к единому формату, получение переменной age вместо date_of_birth, удаление лишних столбцов, для текстовых полей NaN заменены на NULL)
2. Во второй части проверяются следующие типы ошибок в данных:
 + Отрицательные значения для числовых значений (с автоматическим исправлением на положительное число)
 + Проверены на адеватность минимальные и максимальные значения для дат.
 + Проверено единообразие для текстовых полей.
 + Поверено, что тело кредита не превышает сумму ежемесячных платежей
3. В третьей части текстовые поля перекодированы в числовые, удалены столбцы с текстовыми значениями, созданы таблицы с ключами для расшифровки чисел.
