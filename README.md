--Create a Store Database

CREATE TABLE makeup (Id INTEGER PRIMARY KEY, Name TEXT, Quantity INTEGER, Type TEXT, Price INTEGER);

INSERT INTO makeup VALUES (1, "Foundation", 10, "caramel", 7);
INSERT INTO makeup VALUES (2, "Powder", 5, "Coco", 5);
INSERT INTO makeup VALUES (3, "Lipstick", 12, "Nude", 9);
INSERT INTO makeup VALUES (4, "Bronzer", 7, "Sunkissed", 8);
INSERT INTO makeup VALUES (5, "Contour", 10, "Deep", 5);
INSERT INTO makeup VALUES (6, "Highlighter", 3, "Golden", 8);
INSERT INTO makeup VALUES (7, "Lip gloss", 15, "Clear", 2);
INSERT INTO makeup VALUES (8, "Setting spray", 5, "Matte", 5);
INSERT INTO makeup VALUES (9, "Fixing spray", 6, "Shimmer", 11);
INSERT INTO makeup VALUES (10, "Lip oil", 20, "Rose", 5.50);
INSERT INTO makeup VALUES (11, "Eye liner", 16, "Black", 1.50);
INSERT INTO makeup VALUES (12, "Lip pencil", 13, "Brown", 3);
INSERT INTO makeup VALUES (13, "Blush", 4, "Deep Peach", 6.50);
INSERT INTO makeup VALUES (14, "Remover", 8, "Oil based", 4.99);
INSERT INTO makeup VALUES (15, "Wipes", 40, "Water based", 3);

--Show the quantity of each item group
SELECT Type, SUM(Quantity) FROM makeup GROUP BY Type;

--Show items where the price is greater than £1
SELECT * FROM makeup WHERE price > 1 ORDER BY price;
