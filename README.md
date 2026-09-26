# libreplan

This repo uses the official `libreplan/libreplan:1.6.1` image with
PostgreSQL 16 and the official LibrePlan `install.sql` initializer.

## Start

```bash
cp .env.example .env
```

Edit `.env`, set a strong `LIBREPLAN_DBPASSWORD`, then run:

```bash
docker compose up -d
```

Open:

```text
http://localhost:8080
```

Default first login from the official package:

```text
Username: admin
Password: admin
```

Change that password immediately after first login.

## Operations

```bash
docker compose ps
docker compose logs -f libreplan
docker compose down
```

To remove all data:

```bash
docker compose down -v
```

That last command is irreversible because it deletes the PostgreSQL volume.
