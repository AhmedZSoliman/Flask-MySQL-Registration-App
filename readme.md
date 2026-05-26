 # Flask + MySQL Registration App

## Prerequisites

Before you begin, make sure you have:

- Python 3.10 or higher
- pip installed
- MySQL Server installed and running
- virtualenv (recommended for isolated environments)

---

## Getting Started

### 1. Clone the Project

```bash
git clone <your-repo-url>
cd webapp
```

Make sure to configure your `.gitignore` file to exclude sensitive or unnecessary files (like `.env` and `.venv`).

---

### 2. Create and Activate a Virtual Environment

```bash
python3 -m venv .venv
source .venv/bin/activate  # On Linux/macOS
```

On Windows:

```bash
.venv\Scripts\activate
```

---

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

---

### 4. Configure Environment Variables

Create a `.env` file in the project root directory:

```env
DB_HOST=localhost
DB_USER=flaskuser
DB_PASSWORD=StrongPassword123!
DB_NAME=froshims
```

> **Note:** Make sure `.env` is added to your `.gitignore` file to keep credentials secure.

---

### 5. Install and Configure MySQL

If MySQL is not installed:

```bash
sudo apt update
sudo apt install mysql-server
```

Start and enable the MySQL service:

```bash
sudo systemctl start mysql
sudo systemctl enable mysql
```

Create the database and user:

```bash
sudo mysql
```

Inside the MySQL prompt:

```sql
CREATE DATABASE froshims;
CREATE USER 'flaskuser'@'localhost' IDENTIFIED BY 'StrongPassword123!';
GRANT ALL PRIVILEGES ON froshims.* TO 'flaskuser'@'localhost';
FLUSH PRIVILEGES;
EXIT;
```

---

### 6. Run the Application

```bash
flask run
```

Or:

```bash
python app.py
```

The app runs by default at: http://127.0.0.1:5000

Open it in your browser to access the application.
