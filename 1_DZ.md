1. Запустил wsl с бубунтой, начал добавлять mongo в список пакетов apt:
![Alt text](image.png)

2. Первые костыли, для 22 убунты не подходит дефолтная ссылка на монгу из гугла, приходится разбираться:
![Alt text](image-1.png) 

3. Оказывается mongo 6.0 забилдили для убунты 22.04 только в декабре 22 года, приходится использовать jammy ссылку:
![Alt text](image-2.png)

4. Аллилуя оно поставилось, прописываем sudo systemctl start mongod
sudo systemctl status mongod и начинаем упражнения с базой данных
![Alt text](image-3.png)


5. Скачаем данный датасет https://www.kaggle.com/datasets/decide-soluciones/air-quality-madrid?resource=download
И загрузим его в mongodb:
![Alt text](image-4.png)

6. Используем CRUD команды
В Mongo 6.0 в отличие от обычного интерфейса mongo следует использовать утилиту mongosh:
![Alt text](image-5.png)

Импортируем несколько таблиц с помощью mongoimport:
![Alt text](image-6.png)

CRUD:
C - Create
![Alt text](image-7.png)
R - Read
![Alt text](image-8.png)
U - Update
![Alt text](image-9.png)
D - Delete
![Alt text](image-10.png)

7. Перейдем к индексированию
Выберем значение через findOne:
![Alt text](image-12.png)

Его поиск занимает порядка 70 миллисекунд:
![Alt text](image-11.png)

Создадим индекс и попробуем снова:
![Alt text](image-13.png)
Ускорение более чем в 10 раз! (Sick!)