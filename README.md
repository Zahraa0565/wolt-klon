# Wolt-klon

Et fullstack-eksamensprojekt inspireret af Wolt. Webappen har restaurant- og menuvisning, kurv og bestillingsflow samt visninger til kunder, restauranter og administratorer.

Backend er skrevet i Python med Flask og MySQL. Frontend bruger HTML med Jinja-skabeloner, CSS og JavaScript. Flask-Session håndterer sessioner, og Compose indeholder også Redis til projektets Redis-testruter.

## Kør lokalt

1. Installér Docker med Docker Compose.
2. Kopiér `.env.example` til `.env`, og angiv værdier for `FLASK_SECRET_KEY`, `DB_PASSWORD` og `ARANGO_ROOT_PASSWORD`.
3. Start databasen med `docker compose up -d mysql`. Når MySQL er klar, opret demodata med `docker compose run --rm web python seed.py`. Brug kun seed-scriptet mod en lokal demodatabase.
4. Start webappen med `docker compose up --build -d web redis`. Åbn derefter [webappen lokalt](http://localhost).

E-mailfunktioner kræver SMTP-oplysninger i `.env`. Projektet er udviklet til lokal demonstration som en del af en eksamen.
