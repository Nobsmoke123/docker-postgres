# Docker postgres with pgAdmin 4

This project provides a simple Docker Compose setup for running a PostgreSQL database alongside pgAdmin 4 for database management.

## Services

- **db**: Runs PostgreSQL 17.5 (alpine).  
  - Credentials:  
    - User: `<add_your_username>`  
    - Password: `<add_your_password>`  
    - Database: `<add_your_database>`
  - Data is persisted using a Docker volume (`db_data`).
  - Exposes port `5432` for database connections.

- **pgadmin**: Runs pgAdmin 4 for managing the PostgreSQL instance.
  - Access pgAdmin at [http://localhost:5050](http://localhost:5050)
  - Login credentials:  
    - Email: `snoww3b@gmail.com`  
    - Password: `donald123`
  - Depends on the `db` service.

## Usage

Start the services with:

```sh
docker compose up -d
```