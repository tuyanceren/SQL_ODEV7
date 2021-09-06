# SQL_ODEV7
**Patika SQL eğitimi kapsamında yaptığım ödev7**
-------
1._film tablosunda bulunan filmleri rating değerlerine göre gruplayınız._
```sql
SELECT rating FROM film
GROUP BY rating;
```
2._film tablosunda bulunan filmleri replacement_cost sütununa göre grupladığımızda film sayısı 50 den fazla olan replacement_cost değerini ve karşılık gelen film sayısını sıralayınız._
```sql
SELECT replacement_cost, COUNT(*) FROM film
GROUP BY replacement_cost
HAVING COUNT(*)>50;
```
3._customer tablosunda bulunan store_id değerlerine karşılık gelen müşteri sayılarını nelerdir?_
```sql
SELECT store_id, COUNT(*) FROM customer
GROUP BY store_id;
```
4._city tablosunda bulunan şehir verilerini country_id sütununa göre gruplandırdıktan sonra en fazla şehir sayısı barındıra country_id bilgisini ve şehir sayısını paylaşınız._
```sql
SELECT country_id , COUNT(*) FROM city
GROUP BY country_id
ORDER BY COUNT(*) DESC
LIMIT 1;
```
--------
Sorgu senaryolarını [dvdrental.tar](https://www.postgresqltutorial.com/wp-content/uploads/2019/05/dvdrental.zip) isimli dosyayı indirerek gerçekleştirebilirsiniz.
