\dg

\dt

SELECT * FROM owners;     

INSERT INTO owners
(name, age)
VALUES
('Donald', 56), ('Elaine', 24), ('Emma', 36);

SELECT name FROM owners

SELECT name, age FROM owners ORDER BY age;

SELECT * FROM owners WHERE name = 'Donald';

SELECT * FROM owners WHERE age > 30

SELECT * FROM owners WHERE name LIKE 'E%'

INSERT INTO owners
(name, age) 
VALUES
('John', 33), ('Jane', 43);

UPDATE owners 
SET age = 30
WHERE name = 'Jane';

DELETE FROM owners
WHERE name = 'Janet';

INSERT INTO properties
(name, num_units)
VALUES
('Archstone', 20);

INSERT INTO properties
(name, num_units)
VALUES
('Tara', 10), ('Kara', 5);

SELECT * FROM properties WHERE name <> 'Archstone' ORDER BY name;

SELECT COUNT (*) FROM properties;

SELECT MAX (age) FROM owners;

SELECT name FROM owners LIMIT 3;

SELECT * FROM owners
FULL OUTER JOIN properties
ON owners.id = properties.owner_id
;

UPDATE properties
SET owner_id = 1
WHERE name = 'Archstone';

SELECT * FROM owners
CROSS JOIN properties
WHERE owners.id = 1;