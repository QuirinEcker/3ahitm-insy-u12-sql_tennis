# Uebung 12 - Tennis

## A. Create Table Player

``` sql
CREATE TABLE PLAYER (
    membernr NUMBER(4, 0) NOT NULL,
    name VARCHAR2(15) NOT NULL,
    initials VARCHAR2(3),
    CONSTRAINT PK_PLAYER PRIMARY KEY (membernr)
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
    name VARCHAR2(45)
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
    playernr NUMBER(4, 0) NOT NULL,
    fine_date DATE NOT NULL,
    fine_money NUMBER(15, 2) NOT NULL,
    reasson VARCHAR(150) NULL,
    CONSTRAINT FK_FINE_PLAYER FOREIGN KEY (playernr) REFERENCES PLAYER (membernr),
    CONSTRAINT PK_FINE PRIMARY KEY (finenr)
);
```

## F. Delete Column reasson from table fine

```sql
ALTER TABLE FINE DROP COLUMN reasson;
```

## G. Copy Table Player

```sql
CREATE TABLE COPY_PLAYER (
    membernr,
    name
) AS SELECT membernr, name FROM PLAYER;
```

## H. Remove content of table Copy_Player


```sql
TRUNCATE TABLE COPY_PLAYER;
```

## I. Delete Table Copy_Player

```sql
DROP TABLE COPY_PLAYER;
```

