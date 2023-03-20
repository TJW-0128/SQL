--Create a camping outfitter database

CREATE TABLE camping_gear (id INTEGER PRIMARY KEY, item TEXT, cost INTEGER, status TEXT, amount INTEGER);

INSERT INTO camping_gear VALUES (1, "tent", 400, "new", 10);
INSERT INTO camping_gear VALUES (2, "backpack", 150, "new", 15);
INSERT INTO camping_gear VALUES (3, "sleeping_bag", 200, "new", 8);
INSERT INTO camping_gear VALUES (4, "sleeping_pad", 150, "new", 8);
INSERT INTO camping_gear VALUES (5, "hiking_pant", 100, "new", 25);
INSERT INTO camping_gear VALUES (6, "hiking_shirt", 60, "new", 25);
INSERT INTO camping_gear VALUES (7, "socks", 15, "new", 11);
INSERT INTO camping_gear VALUES (8, "hiking_boots", 275, "new", 30);
INSERT INTO camping_gear VALUES (9, "sunglasses", 80, "new", 50);
INSERT INTO camping_gear VALUES (10, "trekking_poles", 95, "new", 12);
INSERT INTO camping_gear VALUES (11, "hydration_bladder", 65, "new", 8);
INSERT INTO camping_gear VALUES (12, "hat", 25.99, "new", 30);
INSERT INTO camping_gear VALUES (13, "gloves", 30, "new", 15);
INSERT INTO camping_gear VALUES (14, "climbing_harness", 86, "new", 20);
INSERT INTO camping_gear VALUES (15, "hiking_boots", 99, "used", 2);

--display the datebase ordered by cost, least expensive to most expensive.
SELECT * FROM camping_gear 
ORDER BY cost asc;

--how many of each item is currently in stock, from least to greatest?
SELECT item, amount FROM camping_gear
ORDER BY amount asc;

--how many items are priced at or under 100 dollars?
SELECT item,cost FROM camping_gear 
WHERE cost <= 100
ORDER BY cost asc;
