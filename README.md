# Patika+ Week6 SQL ile 3. Ödev Uygulaması
Merhaba,
Bu proje SQL ile Patika+ 6.hafta SQL komutları pratik için yapılmış bir uygulamadır.

## 📚 Proje Hakkında
Bu proje, aşağıdaki konuları öğrenmeye yardımcı olmak için tasarlanmıştır:
- Temel SQL komutları
- WHERE kullanımı
- AND ve OR kullanımı
- BETWEEN kullanımı
- IN kullanımı
- LIKE ve ILIKE


## İstenilen Görev
Aşağıdaki sorgu senaryolarını dvdrental örnek veri tabanı üzerinden gerçekleştiriniz.
   1. country tablosunda bulunan country sütunundaki ülke isimlerinden 'A' karakteri ile başlayıp 'a' karakteri ile sonlananları sıralayınız.
   2. country tablosunda bulunan country sütunundaki ülke isimlerinden en az 6 karakterden oluşan ve sonu 'n' karakteri ile sonlananları sıralayınız.
   3. film tablosunda bulunan title sütunundaki film isimlerinden en az 4 adet büyük ya da küçük harf farketmesizin 'T' karakteri içeren film isimlerini sıralayınız.
   4. film tablosunda bulunan tüm sütunlardaki verilerden title 'C' karakteri ile başlayan ve uzunluğu (length) 90 dan büyük olan ve rental_rate 2.99 olan verileri sıralayınız.


## Kod 
```sql
/*
Aşağıdaki sorgu senaryolarını dvdrental örnek veri tabanı üzerinden gerçekleştiriniz.

1. country tablosunda bulunan country sütunundaki ülke isimlerinden 'A' karakteri ile başlayıp 'a' karakteri 
ile sonlananları sıralayınız.

2. country tablosunda bulunan country sütunundaki ülke isimlerinden en az 6 karakterden oluşan ve sonu 'n' karakteri 
ile sonlananları sıralayınız.

3. film tablosunda bulunan title sütunundaki film isimlerinden en az 4 adet büyük ya da küçük harf farketmesizin 'T' karakteri 
içeren film isimlerini sıralayınız.

4. film tablosunda bulunan tüm sütunlardaki verilerden title 'C' karakteri ile başlayan ve uzunluğu (length) 90 dan büyük olan 
ve rental_rate 2.99 olan verileri sıralayınız.
*/

-- 1.SORU
SELECT * FROM country
WHERE country LIKE ('A%a');

-- 2.SORU
SELECT country FROM country
WHERE country LIKE ('______%m');

-- 3.SORU
SELECT title FROM film
WHERE title ILIKE ('%t%t%t%t');

-- 4.SORU
SELECT * FROM film
WHERE title LIKE('C%') AND length > 90 AND rental_rate IN(2.99);


```





