# PostgreSQL install

To install PostgreSQL server, update your computer's local package cache with the latest set of packages. Afterwards, install the postgresql package:

`sudo apt update`

`sudo apt install postgresql`

- By default, PostgreSQL is configured to use peer authentication, which allows users to log in if their operating system user name matches a PostgreSQL internal name.

- The installation process created an operating system user called postgres to match the postgres database administrative account. To log into PostgreSQL with the psql client, use sudo to run the command as the postgres user:
- `sudo -u postgres psql`

When you are finished, you can exit the psql session by typing:
`\quit`

## Changing the Password

```
postgres=# ALTER USER postgres PASSWORD 'myPassword';
ALTER ROLE
```

If successful, Postgres will output a confirmation of ALTER ROLE as seen above.

Finally, exit the psql client by using the \q command.

`postgres=# \q`


# DBeaver Install

Run this:
`sudo snap install dbeaver-ce`

## ⚠️ Use `ALT` + `X` to run CTEs
