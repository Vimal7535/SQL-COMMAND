# SQL-COMMAND



------------------------------------------CREATE A DATABASE--------------------------------------------
create database Hospital
go
use Hospital
--------------------------------------------CREATE A TABLE-----------------------------------------------
create table clinic(P_id int not null identity, p_nmae varchar(50) not null,
p_address varchar(50) not null,p_mob bigint not null, p_age int not null)
--------------------------------------------INSERT DATA VALUES----------------------------------------------
insert into clinic values
('arvind','moradabad',7554764753,22),
('manoj','bijnor',754343553,20),
('sager','moradabad',755474533,10),
('jivan','nougawan',7754475253,30),
('ranjeet','noujawan',7554534753,30),
('piku','noorpur',7558752753,28),
('jeet','noorpur',7545354753,22),
('suhel','sela',4244764753,55),
('ram','kamri',02445764753,33),
('syam','dhampur',443454753,75),
('mohan','bilari',452354.364753,44),
('vimal','bijnor',75563543553,42),
('chavi','moradabad',47533435543,24)

----------------------------------------------DISPLAY THE TABLE------------------------------
select * from clinic
---------------------------------------------USING WHERE-----------------------------------
select p_name from clinic where p_address ='moradabad'
select * from clinic where p_address ='moradabad'
select * from clinic where p_age > 25
------------------------------------------------USING BETWEEN---------------------------------
select p_name from clinic where p_age between 25 and 50
--------------------------------------------------USING UPDATE-------------------------------------
update clinic set p_address='nougawan' where p_id =5
--------------------------------------------------USING ORDER BY-----------------------------------------
select * from clinic order by p_age desc
-------------------------------------------------USING DISTINCT---------------------------------------
select distinct  p_address from clinic 
-------------------------------------------------USING GROUP BY-------------------------------------------
select count(p_id),p_address from clinic group by p_address
------------------------------------------------------USING HAVING WITH ALIASES--------------------------------------
select count(p_id) as No_Of_Duplicate,p_address from clinic group by p_address 
having count (p_id) > 1 order by count (p_id) desc
--------------------------------------------------------SELECT INTO-------------------------------------
select * into p_age from clinic 
select * into p_address from clinic where  p_age=22

----------------------------------------------USING MIN() FINCTION-------------------------------------------
select min(p_age) from clinic
where p_address='noorpur'

select min(p_age) from clinic
---------------------------------------------USINNG MAX() FUNCTION--------------------------------------------
select max(p_age) from clinic 
----------------------------------------------USING COUNT() FUNCTION---------------------------------------
select count(p_age) from clinic

---------------------------------------------USING AVF() FUNCTION-------------------------------------

select avg(p_age) from clinic where p_id between 1 and 10

-----------------------------------------------------USING SUM() FUNCTION---------------------------------

select sum(p_age) from clinic where p_id between 1 and 10


