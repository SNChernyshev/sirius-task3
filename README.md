Docker-контейнер запускается командой:
<pre>
docker-compose up -d
</pre>
---

Доступ к БД по адресу:
http://127.0.0.1/adminer.php
---

Запрос на получение списка книг, которые написаны 3-мя и более со-авторами:
<pre>
SELECT books.name, COUNT(authors.id) count_autors FROM books INNER JOIN authors_books ON books.id = book_id INNER JOIN authors ON authors.id = author_id GROUP BY books.id HAVING COUNT(authors.id) >= 3
</pre>

