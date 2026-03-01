# PostgreSQL Terminal Instructions (Ubuntu Style) - Slip 11

Follow these exact steps from your terminal to setup the database, as shown in your environment.

### 1. Switch to the Postgres User

```bash
sudo -i -u postgres
```

_(Enter your computer password when prompted)_

### 2. Create the Database

```bash
createdb testdb
```

### 3. Enter the Database Shell

```bash
psql testdb
```

### 4. Create the Table

```sql
create table DONAR(
    id int primary key,
    name varchar(50),
    blood_group varchar(5),
    last_donated date
);
```

### 5. Verify the Table Structure

```sql
\d DONAR;
```

### 6. Insert Sample Data

```sql
insert into DONAR values(1, 'Alice johnson', 'B+', '2023-12-05');
insert into DONAR values(2, 'john doe', 'O+', '2023-11-20');
insert into DONAR values(3, 'tony stark', 'B+', '2024-01-10');
```

### 7. View All Records

```sql
select * from DONAR;
```

### 8. Exit the Database Shell

```sql
\q
```

### 9. Return to your Normal User

```bash
exit
```
