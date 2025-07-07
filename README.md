# 🍽️ Little Lemon Booking System

![Django](https://img.shields.io/badge/Django-092e20?style=flat&logo=django&logoColor=white)
![PythonAnywhere](https://img.shields.io/badge/Deployed%20on-PythonAnywhere-green?style=flat&logo=python)

A Django-based restaurant booking and menu management system, deployed on [PythonAnywhere](https://ongunakay.pythonanywhere.com).

---

## 🌐 Live Site

🔗 [https://ongunakay.pythonanywhere.com](https://ongunakay.pythonanywhere.com)

---

## 📦 Tech Stack

- Python
- Django 4.2
- Django REST Framework
- MySQL (via `mysqlclient`)
- Gunicorn
- Pipenv
- PythonAnywhere (Hosting)

---

## ⚙️ Setup Instructions

### 1. Clone the repo

```
git clone https://github.com/ongunakaycom/pythonanywhere-littlelemon.git
cd pythonanywhere-littlelemon
```

```
Add a .env file in the root directory
```

```
SECRET_KEY="your-secret-key"
DB_NAME="your-db-name"
DB_HOST="127.0.0.1"
DB_PORT="3306"
DB_USER="your-db-user"
DB_PASSWORD="your-db-password"
```


```
Install dependencies and run migrations
```
```
pipenv install
pipenv run python manage.py makemigrations
pipenv run python manage.py migrate
```
## Run the development server
```
pipenv run python manage.py runserver
```

## 🔐 Authentication
Token-based authentication is used (via DRF authtoken).
See routes in authn/urls.py.


## 🧪 API Endpoints

| Endpoint            | Description         | Auth Required |
| ------------------- | ------------------- | ------------- |
| `/restaurant/`      | Homepage (HTML)     | ❌             |
| `/restaurant/menu/` | GET/POST Menu Items | ✅ Superuser   |
| `/restaurant/book/` | GET/POST Bookings   | ✅ User        |


## 🧑‍💼 Permissions
- Unauthenticated users can access the homepage.
- Authenticated users can book tables.
- Superusers can manage menu items and view all bookings.


## 🚀 Deployment
App is deployed using Gunicorn on PythonAnywhere:
🔗 ongunakay.pythonanywhere.com

To redeploy after code updates:

Push changes to GitHub.

Pull updates in your PythonAnywhere console.

Restart the web app from the PythonAnywhere dashboard.

## 🗂️ Folder Structure
```
/
│
├── authn/                # Custom auth views
├── restaurant/           # Menu & booking logic
├── templates/            # HTML templates
├── static/               # Static files
├── manage.py             # Django manager
├── Pipfile / Pipfile.lock
├── .env                  # Environment variables (not committed)
├── requirements.txt
└── README.md
```
## 👋 About Me

Ongun Akay, a Senior Full-Stack Developer with expertise across various technologies.

👀 I specialize in full-stack development with extensive experience in frontend and backend technologies.
🌱 Currently, I'm sharpening my skills in advanced concepts of web development.
💞️ I’m always open to exciting collaborations and projects that challenge my abilities.
📫 You can reach me at info@ongunakay.com.

🌐 Website: [ongunakay.com](https://ongunakay.com)<br>
💼 LinkedIn: [linkedin.com/in/ongunakay](https://linkedin.com/in/ongunakay)<br>
🧑‍💻 GitHub: [github.com/ongunakaycom](https://github.com/ongunakaycom)<br>
📬 Email: [info@ongunakay.com](mailto:info@ongunakay.com)

## 📝 License
This is a personal project built using Django for learning and experimentation.