# Postgresql 14 on Linux (terminal)

## Installation
```
sudo apt update
sudo apt install postgresql-14
```

## Set your computer username as a user inside Postgres

### Login into psql as user "postgres" (the default superuser in Postgres)
```
sudo -u postgres psql
```

### Add your username to the psql users
```
postgres=# CREATE USER <your username>
```

### Add a password to your username
```
postgres=# ALTER USER <your username> WITH ENCRYPTED PASSWORD '<password>';
```

### Add login permission to your username
```
postgres=# ALTER USER <your username> WITH LOGIN;
```

### Exit psql
```
postgres=# \q
```

### Login into default database "postgres"
```
psql -U <your username> postgres
```

Now you have a working Postgres database for you to test and learn!
