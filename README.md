#  Two-Tier Flask App (Dockerized)

A simple two-tier web application built using Flask and MySQL, fully containerized using Docker.

---

##  Architecture

Client (Browser)
        ↓
Flask App (Container)
        ↓
MySQL Database (Container)

---

##  Tech Stack

-  Python (Flask)
-  MySQL
-  Docker
-  HTML (Frontend)

---

##  Features

- Add messages through UI
- Store messages in MySQL database
- Display stored messages on UI
- Fully containerized setup

---

##  Run Locally (Docker)

### Step 1: Create Network
```bash
docker network create my-network



