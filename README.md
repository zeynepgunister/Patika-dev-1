# Patika-dev SQL-

## Ödev 1 - WHERE ve Mantıksal Operatörler

1. Soru Cevap:

```ruby
SELECT title, description FROM film;
```

2. Soru Cevap:

```ruby
SELECT * FROM film WHERE length > 60 AND length < 75;
```

3. Soru Cevap:

```ruby
SELECT * FROM film WHERE rental_rate = 0.99 AND replacement_cost = 12.99 OR replacement_cost = 28.99;
```

4. Soru Cevap:

```ruby
SELECT*FROM customer WHERE first_name='Mary';
```

5. Soru Cevap:
```ruby
SELECT*FROM film WHERE NOT (length > 50 AND rental_rate = 2.99 OR rental_rate = 4.99);
```

## Ödev 2 - Between ve In

1. SORU:
```ruby 
SELECT*FROM film WHERE replacement_cost BETWEEN 12.99 AND 16.99 
```

2. SORU:
```ruby
SELECT first_name, last_name FROM actor WHERE first_name IN ('Penelope','Nick','Ed')
```

3. SORU:
```ruby
SELECT * FROM film WHERE (rental_rate IN (0.99,2.99,4.99) AND replacement_cost IN(12.99, 15.99, 28.99))
```

## Ödev 3 - LIKE ve ILIKE

1. SORU:
```ruby 
SELECT*FROM country WHERE country LIKE 'A%a';
```

2. SORU:
```ruby 
SELECT*FROM country WHERE country LIKE '_____%n';
```

3. SORU:
```ruby 
SELECT*FROM film WHERE title ~~* '%T%T%T%T%'
```

4. SORU:
```ruby 
SELECT*FROM film WHERE title LIKE 'C%' AND length>90 AND rental_rate=2.99;
```

## Ödev 4

1. SORU:
   
```ruby 
SELECT DISTINCT replacement_cost FROM film;
```
2. SORU:
   
```ruby 
SELECT COUNT (DISTINCT replacement_cost) FROM film;
```
3. SORU:
   
```ruby 
SELECT COUNT(title LIKE 'T%' AND rating='G') FROM film;
```

4. SORU:
```ruby
SELECT COUNT(country LIKE '_____') FROM country;
```

5. SORU:
```ruby
SELECT COUNT (city) FROM city WHERE city ~~* 'R%';
```

## ÖDEV 5 

1. SORU:

```ruby
SELECT * FROM film
WHERE title LIKE '%n'
ORDER BY length DESC
LIMIT 5;
```
2. SORU:

```ruby
SELECT * FROM film
WHERE title LIKE '%n'
ORDER BY length 
OFFSET 5
LIMIT 5;
```

3. SORU:

```ruby
SELECT * FROM customer
WHERE store_id = '1'
ORDER BY last_name DESC
LIMIT 4;
```
## ÖDEV 6

1. SORU:

```ruby
SELECT AVG(rental_rate) FROM film;
```

2. SORU:

```ruby
SELECT COUNT(*) FROM film
WHERE title LIKE 'C%';
```

3. SORU:

```ruby
SELECT MAX(length) FROM film
WHERE rental_rate ='0.99';
```

4. SORU:

```ruby
SELECT COUNT(DISTINCT replacement_cost) FROM film
WHERE length > 150;
```

## ÖDEV 7:

1. SORU:

```ruby
SELECT rating, COUNT(*) FROM film
GROUP BY rating;
```

2. SORU:

```ruby
SELECT replacement_cost, COUNT(*) FROM film
GROUP BY replacement_cost
HAVING COUNT(*) > 50;
```

3. SORU:

```ruby
SELECT store_id,COUNT(*) FROM customer
GROUP BY store_id;
```

4. SORU:

```ruby
SELECT country_id, COUNT(*) FROM city
GROUP BY country_id
ORDER BY COUNT(*) DESC
LIMIT 1;
```
## ÖDEV 8:

1. Soru:
```ruby
CREATE TABLE employee(
	id int,
	name VARCHAR(50),
	birthday DATE,
	email VARCHAR(100)
);
```

2. SORU:

```ruby
insert into employee (id, name, birthday, email) values (1, 'Gartsyde', '2022-12-14', 'fgartsyde0@meetup.com');
insert into employee (id, name, birthday, email) values (2, 'Sandland', '2022-09-07', 'ssandland1@barnesandnoble.com');
insert into employee (id, name, birthday, email) values (3, 'Edens', '2023-02-01', 'ledens2@nydailynews.com');
insert into employee (id, name, birthday, email) values (4, 'De Rechter', '2023-06-07', 'nderechter3@imdb.com');
insert into employee (id, name, birthday, email) values (5, 'Morse', '2023-04-15', 'lmorse4@phpbb.com');
insert into employee (id, name, birthday, email) values (6, 'Featherston', '2022-09-17', 'dfeatherston5@printfriendly.com');
insert into employee (id, name, birthday, email) values (7, 'Pawlyn', '2023-04-18', 'rpawlyn6@vinaora.com');
insert into employee (id, name, birthday, email) values (8, 'Timmis', '2022-12-31', null);
insert into employee (id, name, birthday, email) values (9, 'Thombleson', '2023-02-14', 'athombleson8@diigo.com');
insert into employee (id, name, birthday, email) values (10, 'Tremolieres', '2022-08-16', null);
insert into employee (id, name, birthday, email) values (11, 'Adlem', '2023-01-10', 'ladlema@cloudflare.com');
insert into employee (id, name, birthday, email) values (12, 'Lux', '2022-10-27', 'gluxb@nba.com');
insert into employee (id, name, birthday, email) values (13, 'Shearsby', '2022-07-29', 'cshearsbyc@stumbleupon.com');
insert into employee (id, name, birthday, email) values (14, 'Lecordier', null, 'clecordierd@statcounter.com');
insert into employee (id, name, birthday, email) values (15, 'Collerd', '2022-10-23', 'gcollerde@bandcamp.com');
insert into employee (id, name, birthday, email) values (16, 'Dunican', '2023-05-27', 'cdunicanf@skype.com');
insert into employee (id, name, birthday, email) values (17, 'Peacocke', '2022-12-30', 'mpeacockeg@unblog.fr');
insert into employee (id, name, birthday, email) values (18, 'MacMenemy', '2023-01-05', 'mmacmenemyh@netlog.com');
insert into employee (id, name, birthday, email) values (19, 'Gershom', '2023-03-31', 'egershomi@businesswire.com');
insert into employee (id, name, birthday, email) values (20, 'Brazener', null, 'cbrazenerj@webmd.com');
insert into employee (id, name, birthday, email) values (21, 'Glaysher', '2023-06-04', 'mglaysherk@wisc.edu');
insert into employee (id, name, birthday, email) values (22, 'Alliott', '2022-09-17', 'salliottl@china.com.cn');
insert into employee (id, name, birthday, email) values (23, 'Calfe', '2022-08-31', 'kcalfem@rambler.ru');
insert into employee (id, name, birthday, email) values (24, 'Gascard', '2023-01-31', null);
insert into employee (id, name, birthday, email) values (25, 'McCosh', '2022-11-29', 'dmccosho@paypal.com');
insert into employee (id, name, birthday, email) values (26, 'Yitzhak', null, 'lyitzhakp@businessweek.com');
insert into employee (id, name, birthday, email) values (27, 'Dimitru', null, 'gdimitruq@jugem.jp');
insert into employee (id, name, birthday, email) values (28, 'Menaul', '2022-08-09', null);
insert into employee (id, name, birthday, email) values (29, 'Neeve', '2023-04-10', 'dneeves@goo.ne.jp');
insert into employee (id, name, birthday, email) values (30, 'Wabey', '2022-08-04', 'wwabeyt@nhs.uk');
insert into employee (id, name, birthday, email) values (31, 'Simeon', '2023-05-19', 'lsimeonu@t-online.de');
insert into employee (id, name, birthday, email) values (32, 'Willisch', '2022-08-19', 'nwillischv@list-manage.com');
insert into employee (id, name, birthday, email) values (33, 'Campanelli', '2022-12-04', 'kcampanelliw@posterous.com');
insert into employee (id, name, birthday, email) values (34, 'Napolitano', '2023-03-27', 'rnapolitanox@furl.net');
insert into employee (id, name, birthday, email) values (35, 'Blaylock', '2023-06-19', 'ablaylocky@elpais.com');
insert into employee (id, name, birthday, email) values (36, 'Acreman', '2023-01-01', 'tacremanz@nymag.com');
```
3. SORU:





