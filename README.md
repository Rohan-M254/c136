# Astronomy Data API

A small Flask API that exposes a static catalogue of stars and selected numeric properties. This repository is an early learning project and a starting point for a future backend-focused rebuild.

## What it currently does

- Returns the complete star catalogue from the root endpoint.
- Looks up a star by its exact name through a query parameter.
- Returns JSON responses with a simple success message.

## Technology

- Python
- Flask
- JSON responses

## Project structure

```text
c136/
├── README.md
└── c136/
    ├── flask.py
    └── data.py
```

## Run locally

1. Install Python 3.
2. Install Flask:

   ```bash
   python -m pip install Flask
   ```

3. From the repository root, start the application:

   ```bash
   python c136/flask.py
   ```

4. Open the local address printed by Flask.

## API endpoints

### `GET /`

Returns the full catalogue.

### `GET /star?name=Vega`

Looks up a star by exact name. The `name` query parameter is required by the current implementation.

## Current limitations

This is not a production-ready service yet:

- Data is stored in a Python module rather than a database.
- Star-name matching is exact and case-sensitive.
- Missing or unknown names are not handled with a deliberate 400/404 response yet.
- Automated tests, pagination, filtering, authentication and deployment configuration have not been added.

These limitations are documented intentionally; they are the next engineering improvements, not features this repository currently claims to have.

## Roadmap

- [ ] Validate query parameters and return clear 400/404 responses.
- [ ] Add automated tests for successful and unsuccessful lookups.
- [ ] Add search, filtering and pagination.
- [ ] Move the catalogue into PostgreSQL.
- [ ] Add API documentation and deployment configuration.

## Project status

Educational Flask API. The current branch documents the existing implementation; it does not claim the planned improvements are already complete.
