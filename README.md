# Домашнє завдання #13

## Перша частина

У цьому домашньому завданні ми продовжуємо доопрацьовувати застосунок REST API із домашнього [завдання 12](https://github.com/Goit-Home-Works/Py_WEB_12).

### Завдання

- Реалізуйте механізм верифікації електронної пошти зареєстрованого користувача.
- Обмежуйте кількість запитів до своїх маршрутів контактів. Обов'язково обмежте швидкість - створення контактів для користувача.
- Увімкніть CORS для свого REST API.
- Реалізуйте можливість оновлення аватара користувача. Використовуйте сервіс Cloudinary.

### Загальні вимоги

- Усі змінні середовища повинні зберігатися у файлі .env. Всередині коду не повинно бути конфіденційних даних у «чистому» вигляді.
- Для запуску всіх сервісів і баз даних у застосунку використовується Docker Compose.

### Додаткове завдання

- Реалізуйте механізм кешування за допомогою бази даних Redis. Виконайте кешування поточного користувача під час авторизації.
- Реалізуйте механізм скидання паролю для застосунку REST API.

## Друга частина

У цьому домашньому завданні необхідно доопрацювати застосунок Django із [домашнього завдання 10](link_to_homework_10).

### Завдання

- Реалізуйте механізм скидання паролю для зареєстрованого користувача.
- Усі змінні середовища повинні зберігатися у файлі .env та використовуватися у файлі settings.py.

## Виконання

Remember to set your SendGrid API key in the SENDGRID_API_KEY environment variable before running the script. If you're using a Unix-like system, you can set it like this:

```bash
echo "export SENDGRID_API_KEY='YOUR_API_KEY'" > sendgrid.env
echo "sendgrid.env" >> .gitignore
source ./sendgrid.env
```
Replace 'YOUR_API_KEY' with your actual SendGrid API key.

Щоб запустити програму, скопіюйте та вставте наступну команду у термінал:

```bash
python3 src/main.py
```

Після цього, натиснить на кнопку API DOC.

##  АБО в докері:
## Встановлення та запуск
### Підготувати зміні оточення .env
На основі прикладу [.env_example](.env-example) створити файли з Вашими індивідуальними даними:
- .env  (визначає APP_ENV що визначає поточний робочий файл є prod, dev)
- .env-dev (Налаштування для dev)
- .env-prod (Налаштування для prod)

Виконати скрипт:

```
docker compose  --env-file .env-dev --file docker-compose-db.yml  up -d 
cd ./src && alembic upgrade head 
```

```
sudo chmod 777 /home/sergio/Desktop/Py_WEB_13/.postgres-data


sudo chown -R <username>:<group> /home/sergio/Desktop/Py_WEB_13/postgres-data

whoami

groups


sudo ls -l /home/sergio/Desktop/Custom_inst/postgres-data
sudo chown -R sergio:sergio /home/sergio/Desktop/Custom_inst/postgres-data



```



#### FastAPI server
Виконати скрипт:
```
cd ./src
uvicorn main:app --reload --port 9000
```
або
```
cd ./src
python3 ./main.py
```


### Відкрити сторінку браузера http://localhost:9000
