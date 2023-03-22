Задание №1

1.
CREATE TABLE employees(
id BIGSERIAL NOT NULL PRIMARY KEY,
first_name VARCHAR(60) NOT NULL,
last_name VARCHAR(60) NOT NULL,
age INT NOT NULL
);
INSERT INTO employees(
first_name,last_name,age)
VALUES('Сергей','Петров',25);
INSERT INTO employees(
first_name,last_name,age)
VALUES('Иван','Васильев',40);
INSERT INTO employees(
first_name,last_name,age)
VALUES('Артем','Петров',33);
INSERT INTO employees(
first_name,last_name,age)
VALUES('Мирон','Федоров',55);
INSERT INTO employees(
first_name,last_name,age)
VALUES('Дмитрий','Сидоров',31);
INSERT INTO employees(
first_name,last_name,age)
VALUES('Феликс','Садовин',31);
2.
SELECT*FROM employees;
SELECT first_name,last_name
FROM employees;
3.
SELECT*FROM employees
WHERE age<30 OR age>50;
4.
SELECT* FROM employees
WHERE age
BETWEEN 30 AND 50;
5.
SELECT * FROM employees
ORDER BY last_name DESC;
6.
SELECT*FROM employees
WHERE length(first_name)>4;


Задание №2
1.
UPDATE employees SET first_name='Иван'
WHERE id=1;
UPDATE employees SET first_name='Александр'
WHERE id=3;
2.
SELECT first_name AS Имя,
SUM(age) AS Суммарный_возраст
FROM employees
GROUP BY Имя;
3.
SELECT first_name,age
FROM employees
WHERE age=(
SELECT MIN(age)
FROM employees
);
4.
SELECT first_name,age
FROM employees
WHERE NOT first_name='Иван'
ORDER BY age ASC;
