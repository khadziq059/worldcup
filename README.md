# World Cup Database

A relational database project developed as part of the **Relational Database Certification** from [freeCodeCamp](https://www.freecodecamp.org/).

This project uses **PostgreSQL** and **Bash** to build a database of World Cup games from a CSV file and query it for statistics.

---

## Project Overview

A Bash script reads World Cup match data from `games.csv`, inserts it into a normalized database, and a second script runs queries to answer questions such as total goals, winners by year, and top teams.

---

## Technologies Used

- **PostgreSQL** – Relational database management system
- **SQL** – Table creation, queries, and data manipulation
- **Bash** – Scripting for data insertion and queries

---

## Database Structure

The database is named `worldcup` and has two tables:

- **`teams`** – Stores `team_id` (primary key) and a unique team `name`.
- **`games`** – Stores `game_id` (primary key), `year`, `round`, `winner_goals`, `opponent_goals`, and foreign keys `winner_id` and `opponent_id` referencing `teams`.

---

## Repository Structure

| File | Description |
|------|-------------|
| `insert_data.sh` | Reads `games.csv` and inserts teams and games into the database |
| `queries.sh` | Runs SQL queries and prints the results |
| `worldcup.sql` | SQL dump of the database |
| `games.csv` | Source data for World Cup games |

---

## How to Run

1. **Clone this repository:**

   ```bash
   git clone https://github.com/khadziq059/worldcup.git
   cd worldcup
   ```

2. **Restore the database:**

   ```bash
   psql -U postgres < worldcup.sql
   ```

3. **Run the scripts:**

   ```bash
   chmod +x insert_data.sh queries.sh
   ./insert_data.sh
   ./queries.sh
   ```

---

## What I Learned

- Designing a normalized schema with primary and foreign keys.
- Inserting data from a CSV file using a Bash script.
- Writing SQL queries with `JOIN`, aggregate functions, and filtering.
- Connecting Bash scripts to PostgreSQL.

---

## Certification

This project is part of the **Relational Database Certification** curriculum by freeCodeCamp.

[View my freeCodeCamp Certification](https://www.freecodecamp.org/certification/fccaf2a963f-74a0-49ac-90af-8087b20f3047/relational-databases-v9)
