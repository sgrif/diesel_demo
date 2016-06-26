Diesel Demo
===========

This is the code from the [Diesel Getting Started
Guide](http://diesel.rs/guides/getting-started).

Quick start (Debian/Ubuntu)
===========================

Install postgres:
```
$ sudo apt-get install postgres
```

Setup postgres:
```
$ sudo -u postgres psql

postgres=# CREATE DATABASE test;
CREATE DATABASE

postgres=# CREATE USER test WITH PASSWORD 'pass';
CREATE ROLE

postgres=# GRANT ALL PRIVILEGES ON DATABASE test TO test;
GRANT
```

Try the demo:
```
$ cargo install diesel_cli

$ git clone https://github.com/sgrif/diesel_demo

$ cd diesel_demo

$ export DATABASE_URL=postgres://test:pass@localhost:5432/test

$ ~/.cargo/bin/diesel migration run

$ cargo build

$ ./target/debug/write_post
```
