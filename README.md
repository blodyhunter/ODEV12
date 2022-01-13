# ODEV12

1- select count(*) from film
where length >
(select avg (length) from film);

2- select count(*) from film
where rental_rate = 
(select max (rental_rate) from film);

3- select * from film
where 
(rental_rate = (select min (rental_rate) from film) 
 AND 
replacement_cost = (select max (replacement_cost) from film)
);

4-select first_name, last_name, amount from customer
inner join payment on payment.customer_id=customer.customer_id 
order by amount desc;
