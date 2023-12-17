- Actor ve customer tablolarında bulunan first_name sütunları için tüm verileri sıralayalım.
```SQL
(SELECT first_name FROM actor
LIMIT 5)
UNION
(SELECT first_name FROM customer
LIMIT 5)
```
- Actor ve customer tablolarında bulunan first_name sütunları için kesişen verileri sıralayalım.
```SQL
(SELECT first_name FROM actor)
INTERSECT
(SELECT first_name FROM customer)
```
- Actor ve customer tablolarında bulunan first_name sütunları için ilk tabloda bulunan ancak ikinci tabloda bulunmayan verileri sıralayalım.
```SQL
(SELECT first_name FROM actor)
EXCEPT
(SELECT first_name FROM customer)

```