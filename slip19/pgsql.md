# PostgreSQL Terminal Instructions (Ubuntu Style) - Slip 19

Follow these exact steps to setup authentication for your login program.

### 1. Switch to the Postgres User

```bash
sudo -i -u postgres
```

### 2. Enter the existing Database

```bash
psql testdb
```

### 3. Create the User Table

```sql
create table users(
    username varchar(50) primary key,
    password varchar(50)
);
```

### 4. Verify the Table

```sql
\d users;
```

### 5. Insert Sample Accounts

```sql
insert into users values('john', 'password123');
insert into users values('admin', 'admin@123');
```

### 6. View All Users

```sql
select * from users;
```

### 7. Exit and Logout

```sql
\q
```

```bash
exit
```
