# 🧩 Django CRM — Customer Relationship Management System

A **modern Django-based CRM platform** designed to help you manage customers, track events, analyze engagement, and automate workflows.  
---

## 🚀 Project Overview

**Django CRM** is a full-stack web application built with **Django**, **Tailwind CSS**, and **TimescaleDB**.  
It focuses on teaching real-world backend development patterns, database relationships, user authentication, event analytics, and workflow automation.

### 🧱 Core Features

- 🔑 **Authentication & OAuth** — Secure login using Google OAuth  
- 👥 **Customer Management** — CRUD operations for contacts and organizations  
- 📈 **Event Tracking System** — Log and analyze user activity  
- 📊 **TimescaleDB Analytics** — Time-series event insights and visualization  
- 🔄 **Google Contacts Sync** — Bi-directional sync with Google People API  
- ⚙️ **CI/CD Automation** — GitHub Actions for scheduled sync and deployment  

---

## 🧰 Tech Stack

| Category | Technology |
|-----------|-------------|
| **Backend** | Django 5+, Python 3.12 |
| **Frontend** | Tailwind CSS, Flowbite, Chart.js |
| **Database** | PostgreSQL + TimescaleDB extension |
| **Auth** | Google OAuth (via Google Cloud Console) |
| **Deployment** | GitHub Actions, Whitenoise |
| **Automation** | Pre-commit hooks, management commands |
| **Analytics** | Time-series aggregation, Chart.js dashboards |

---

## ⚙️ Getting Started

### 1️⃣ Clone Repository

```bash
git clone
cd Django-CRM
````

### 2️⃣ Create Virtual Environment (using `uv`)

```bash
pip install uv
uv venv
source .venv/bin/activate  # (Linux/macOS)
.venv\Scripts\activate     # (Windows)
```

### 3️⃣ Install Dependencies

```bash
uv pip install -r requirements.txt
```

### 4️⃣ Configure Environment Variables

Create a `.env` file in the root directory:

```bash
DEBUG=True
SECRET_KEY=your-secret-key
DATABASE_URL=postgres://user:password@localhost:5432/django_crm
GOOGLE_CLIENT_ID=your-google-client-id
GOOGLE_CLIENT_SECRET=your-google-client-secret
```

### 5️⃣ Run Database Migrations

```bash
python manage.py makemigrations
python manage.py migrate
```

### 6️⃣ Create Superuser

```bash
python manage.py createsuperuser
```

### 7️⃣ Run Development Server

```bash
python manage.py runserver
```

App is now running at **[http://127.0.0.1:8000/](http://127.0.0.1:8000/)** 🎉

---

## 🧩 Project Modules Breakdown

### 1. Getting Started

* **Django Project Creation:** Project scaffolded with `uv` for fast dependency management
* **Pre-Commit Hooks:** Automate linting, formatting, and static checks using [pre-commit](https://pre-commit.com)
* **Creating Your First User:** Django admin user setup to manage CRM data

---

### 2. Django Fundamentals

* **Models & Database Design:** Define `Customer`, `Company`, and `Event` models
* **Foreign Key Relationships:** Connect customers to organizations and events
* **Migration Best Practices:** Use atomic migrations and maintain version control
* **Environment Variable Management:** Load environment settings using `python-dotenv`

---

### 3. Authentication & Views

* **Google OAuth Setup:** Integrate Google Cloud for secure authentication
* **Django Views & URL Routing:** Modular structure for clean URL mapping
* **Templates & Inheritance:** Use base templates and block inheritance for DRY design
* **Dynamic vs Static Content:** Serve user-specific data while caching static resources

---

### 4. Frontend & Static Files

* **Static File Handling:** Manage CSS/JS using [Whitenoise](http://whitenoise.evans.io)
* **Tailwind + Flowbite UI:** Build a responsive and modern CRM interface
* **Rendering Data:** Display live customer and analytics data dynamically
* **Custom Tailwind Theme (Optional):** Extend Tailwind configuration for brand-specific design

---

### 5. Event Tracking System

* **Event Model:** Log user actions (login, view, updates, etc.)
* **Generic Foreign Keys:** Allow events to relate to any model dynamically
* **Django Signals:** Automatically create events on user or model actions
* **Custom Signals & Analytics:** Track and visualize engagement over time

---

### 6. TimescaleDB Analytics

* **TimescaleDB Integration:** Extend PostgreSQL with time-series support
* **Event Tracking:** Record and query large volumes of time-based data efficiently
* **Time Bucket Analysis:** Aggregate data by minute, hour, or day
* **Chart.js Visualizations:** Display interactive graphs on dashboards

---

### 7. Google Contacts Integration

* **Google People API Setup:** Connect your Google Cloud project & enable APIs
* **Scope Management:** Request secure access for contacts read/write
* **Response Parsing:** Cleanly extract name, phone, and email data
* **Sync Service:** Implement a background task to sync contacts
* **Custom Management Commands:** Automate sync using `python manage.py sync_contacts`

---

### 8. Automation with GitHub Actions

* **CI/CD Workflow:** Deploy and test using GitHub Actions
* **Scheduled Workflows:** Auto-sync contacts daily/weekly
* **Production Sync:** Run periodic management commands in production environment
* **Environment Secrets:** Securely store API keys and credentials via GitHub Secrets

---

## 🧪 Development Utilities

### Pre-Commit Hook Setup

```bash
pre-commit install
```

Runs formatting & linting automatically on commit using `black`, `flake8`, and `isort`.

### Run Tests

```bash
python manage.py test
```

---

## 🧠 Learning Outcomes

By completing this project, you’ll master:

* Django fundamentals (models, migrations, views)
* Google OAuth authentication & API integrations
* Managing static assets with Tailwind CSS
* Event tracking and signal-based automation
* TimescaleDB time-series analytics
* CI/CD with GitHub Actions
* Real-world Django best practices

---

## 📜 License

This project is licensed under the **MIT License**.
Feel free to use, modify, and distribute under the same terms.

---

## 💬 Contributing

Contributions are welcome!
Fork the repo, create a new branch, and submit a pull request.

```bash
git checkout -b feature/new-feature
git commit -m "Add new feature"
git push origin feature/new-feature
```
---

**Made with ❤️ using Django + Tailwind + TimescaleDB(PostgreSQL)**

```