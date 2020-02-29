# Uebung 12 - Tennis

## A. Create Table Player

``` sql
CREATE TABLE PLAYER (
    membernr NUMBER(4, 0) NOT NULL,
    name VARCHAR2(15) NOT NULL,
    initials VARCHAR2(3)
);
```

## B. Add a Column

```sql
ALTER TABLE PLAYER ADD (
    birth_date DATE
);
```

## C. Modify Column

```sql
ALTER TABLE PLAYER MODIFY (
    name VARCHAR2(45) NOT NULL
);

```

## D. Description of the Table

```sql
DESC PLAYER;
```

## E. Create table fine

```sql
CREATE TABLE FINE (
    finenr NUMBER(6, 0) NOT NULL,
    membernr NUMBER(4, 0) NOT NULL,
    date DATE NOT NULL,
    fine_money MONEY NOT NULL,
    reasson VARCHAR(150) NULL
);
```

## F. Delete Column reasson from table fine

```sql
ALTER TABLE FINE DROP COLUMN reasson;
```

## G. Copy Table Player

```sql
CREATE TABLE COPY_PLAYER [(
    membernr NUMBER(4, 0) NOT NULL,
    name VARCHAR2(45) NOT NULL
)] AS SELECT membernr, name
FROM TABLE PLAYER;
```

## H. Remove content of table Copy_Player


```sql
TRUNCATE TABLE COPY_PLAYER;
```

## I. Delete Table Copy_Player

```sql
DROP TABLE COPY_PLAYER;
```

