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



