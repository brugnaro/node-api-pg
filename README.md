## PostgreSQL - Green IT


## Installation

- App 
```bash
git clone git@github.com:clusson/node-api-pg
cd node-api-pg
yarn install
```

- Postgre SQL

*Windows* 
```bash
Get PostgreSQL  
[postgresql](https://www.postgresql.org/download/windows/)
pg_ctl start
```

*MacOS / Linux*
```bash
brew install postgresql
brew services start postgresql
psql postgres
```

## Database

```sql
CREATE ROLE patrick WITH LOGIN PASSWORD 'password';
ALTER ROLE patrick CREATEDB;
CREATE DATABASE greenIT;
GRANT ALL PRIVILEGES ON DATABASE greenIT TO patrick;
```
- #### Connection

```bash
psql -d greenIT -U patrick
```

- #### Create table
```sql
CREATE TABLE users (
  id SERIAL PRIMARY KEY,
  name VARCHAR(30),
  email VARCHAR(30)
);

INSERT INTO users (name, email)
  VALUES ('Johnny Bravo', 'johnny-bravo@contact.me'), ('George Bush', 'george-bush@gov.us');
```

## Launch the app

```bash
node index.js
```

  ## Commands

- GET: curl http://localhost:3000/users
- POST: curl --data "name=Jerry&email=jerry@example.com" http://localhost:3000/users
- PUT: curl -X PUT -d "name=George" -d "email=george@example.com" http://localhost:3000/users/1
- DELETE: curl -X "DELETE" http://localhost:3000/users/1




social : cron
financier : gain énergétique