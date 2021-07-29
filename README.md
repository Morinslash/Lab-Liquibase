# Project to test Liquibase

To start docker-compose stack:

```bash
docker-compose up -d
```

To enter specific service shell:
```bash
docker-compose exec <service-name> sh
```

## PgAdmin

To access PgAdmin go to http://localhost:5050
```
username: pgadmin4@pgadmin.org
password: admin
```
### Add server in PgAdmin:
```
Hostname: postgres
Port: 5432
Username: <database.env-username>
Password: <database.env-password>
```

## Liquibase

To execute commands for Liquibase
```bash
docker-compose run --rm liquibase <command-name>
```

To perform update use this command:
```bash
docker-compose run --rm liquibase --defaultsFile=/liquibase/changelog/liquibase.properties update
```