# SQLQ-ODV5

## SQL Ödev 5 | ORDER BY | LIMIT ve OFFSET

Aşağıdaki sorgu senaryolarını dvdrental örnek veri tabanı üzerinden gerçekleştiriniz.

1-) film tablosunda bulunan ve film ismi (title) 'n' karakteri ile biten en uzun (length) 5 filmi sıralayınız.
SELECT title FROM film
WHERE title LIKE '%n'
ORDER BY length DESC
LIMIT 5;

![image](https://github.com/CYazar12/SQLQ-ODV5/assets/109551508/80f72bca-bbdb-429b-8120-604531e8359b)


2-) film tablosunda bulunan ve film ismi (title) 'n' karakteri ile biten en kısa (length) ikinci(6,7,8,9,10) 5 filmi(6,7,8,9,10) sıralayınız.

SELECT title FROM film
WHERE title LIKE '%n'
ORDER BY length ASC
LIMIT 5 
OFFSET 5;

![image](https://github.com/CYazar12/SQLQ-ODV5/assets/109551508/6828447c-b09e-4c3e-a4ec-d3b7af93ed45)

3-) customer tablosunda bulunan last_name sütununa göre azalan yapılan sıralamada store_id 1 olmak koşuluyla ilk 4 veriyi sıralayınız.

SELECT *
FROM customer
WHERE store_id = 1
ORDER BY last_name DESC
LIMIT 4

![image](https://github.com/CYazar12/SQLQ-ODV5/assets/109551508/5db8e887-b36d-4b04-a3ca-63c05dcd5bd2)

