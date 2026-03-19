# Two-Tier Flask App (Dockerized)

A simple two-tier web application built using Flask and MySQL, fully containerized using Docker.

---

##  Architecture

Client (Browser)
        ↓
Flask App (Container)
        ↓
MySQL Database (Container)

---

## Tech Stack

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

Step 2: Run MySQL Container

docker run -d \
  --name mysql-db \
  --network my-network \
  -e MYSQL_ROOT_PASSWORD=root \
  -e MYSQL_DATABASE=testdb \
  mysql:5.7

  Step 3: Wait for MySQL

  sleep 15

  Step 4: Run Flask App

  docker run -d \
  --name flask-app \
  --network my-network \
  -p 5000:5000 \
  -e MYSQL_HOST=mysql-db \
  -e MYSQL_USER=root \
  -e MYSQL_PASSWORD=root \
  -e MYSQL_DB=testdb \
  two-tier-flask-app

  Access Application : http://localhost:5000



