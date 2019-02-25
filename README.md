* Data base -> collection of data
* Databases run the world
* Nearly everything runs with DB
* Examples - Facebook, Twitter, etc
* Not only storing data - but also how to store it so you can access it easily

* Today talking about one of the most common DBs, one that has been around for quite a while
* Relational databases

* Relational databases are kind of like Excel, big tables of data


Example: cities
---------------
    (city, country_id, population, area)
    ("Zürich",  "Switzerland",  391359,  87.88),
    ("Vienna",  "Austria",     1867960, 414.65),
    ("Berlin",  "Germany",     3520031, 891.68),
    ("Geneva",  1,  194565,  15.93),
    ("Bern",    1,  130015,  51.62),
    ("Linz",    2,  198181, 196.05),
    ("Graz",    2,  273838, 127.56),
    ("Hamburg", 3, 1787408, 755.30),
    ("Munich",  3, 1450381, 310.70)

-> Each column usually has a data type. 
TEXT
NUMERIC
INTEGER
REAL
BLOB

-> There is one special column ID
-> Identifier, that uniquely identifies one row 

-> There is one problem with this database
-> Imagine you want to put every city and village from DACH in here
-> What could it be?

* Redundancy. We have to store the name over and over again
* Why is redundancy bad? 
1. Needs a lot of space. Switzerland takes up 11 bytes, not so good
2. Finding all cities of Switzerland takes a lot of time - need to compare 11 bytes
3. What if somebody has typos? Switserland for examample
4. If Switzerland changes to Schweiz --> need to change a lot of entries

Let's see if we can do better

Alternative: new table countries:
---------------------------------
    (country, population, area)
    ("Switzerland", 8401120, 41285),
    ("Austria", 8794267, 83879),
    ("Germany", 82349400, 357168),
    ("Liechtenstein", 37341, 160)


-> Remember ID? 
-> We can now use ID to clean up the cities DB
--> Normalized form


=================================

- SQL
- Sequel

- Not really a DB, more a language.
- It's a database programming language, if you want
- Commands to create tables - excel sheets
- Commands to find entries, sort,etc

- It's become the quasi standard for relational databases

- A lot of Relational Dagtabases uses it. MySQL, MS Access, Oracle, Postgres - just to nae a few very prominent ones
database language.

- We'll use SQLlite today
- More to get our hands dirty quick
- Nobody would use that in production
- Concept is the same
- Postgres -> remainder of the course



Note: Be careful when updating records in a table! Notice the WHERE clause in the UPDATE statement. The WHERE clause specifies which record(s) that should be updated. If you omit the WHERE clause, all records in the table will be updated

!# notes
