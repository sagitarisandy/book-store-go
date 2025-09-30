# Book Store Go

A small RESTful book store API written in Go using GORM and MySQL.

## Prerequisites

- Go (1.13+ or newer)
- MySQL server running and accessible

## Environment variables

The app reads database configuration from these environment variables. Defaults are used when a variable is not set.

- DB_USER (default: `root`)
- DB_PASS (default: `root`)
- DB_HOST (default: `127.0.0.1`)
- DB_PORT (default: `3306`)
- DB_NAME (default: `simplerest`)

## How to run

From the project root you can run the main package directly:

```bash
# optional: set environment variables
export DB_USER=root
export DB_PASS=root
export DB_HOST=127.0.0.1
export DB_PORT=3306
export DB_NAME=simplerest

# run the app (option 1)
go run ./cmd/main

# or run the specific main file (option 2)
# go run cmd/main/main.go
```

When the application successfully connects to the database it will print:

```
success to connect db!
```

If the connection fails, the app currently panics and prints the underlying error.

## Notes

- This repository uses GORM (github.com/jinzhu/gorm) with the MySQL dialect.
- Update the environment variables to match your local MySQL credentials before running.

