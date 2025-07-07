# 🍽️ Restaurant Booking API – Django + Python + CI/CD

![Django](https://img.shields.io/badge/Django-092e20?style=flat&logo=django&logoColor=white)
![PythonAnywhere](https://img.shields.io/badge/Deployed%20on-PythonAnywhere-green?style=flat&logo=python)

A Django-based restaurant booking and menu management system, deployed on [PythonAnywhere](https://ongunakay.pythonanywhere.com).

---

## 🌐 Live Site

🔗 [https://ongunakay.pythonanywhere.com](https://ongunakay.pythonanywhere.com)

---

## 📦 Tech Stack

- Python 3
- Django 4.2
- Django REST Framework
- MySQL (via `mysqlclient`)
- Gunicorn
- Pipenv
- PythonAnywhere (Hosting)

---

## ⚙️ Setup Instructions

### 1. Clone the repository

```
git clone https://github.com/ongunakaycom/pythonanywhere-littlelemon.git
cd pythonanywhere-littlelemon
```

## 2. Create a .env file in the root directory
```
SECRET_KEY="your-secret-key"
DB_NAME="your-db-name"
DB_HOST="127.0.0.1"
DB_PORT="3306"
DB_USER="your-db-user"
DB_PASSWORD="your-db-password"
```

#3. Install dependencies and run migrations
```
pipenv install
pipenv run python manage.py makemigrations
pipenv run python manage.py migrate
```

# 4. Run the development server
```
pipenv run python manage.py runserver
```

# 🔐 Authentication
Token-based authentication is used via Django REST Framework's authtoken.

See route definitions in authn/urls.py.

Obtain tokens via the login endpoint.

# 🧪 API Endpoints

| Endpoint            | Description         | Auth Required   |
| ------------------- | ------------------- | --------------- |
| `/restaurant/`      | Homepage (HTML)     | ❌               |
| `/restaurant/menu/` | GET/POST menu items | ✅ Superuser     |
| `/restaurant/book/` | GET/POST bookings   | ✅ Authenticated |

## 🧑‍💼 Permissions
- Unauthenticated users: Can view the homepage.
- Authenticated users: Can make bookings.
- Superusers: Can manage menu items and view all bookings.

# 🚀 Deployment

App is deployed on PythonAnywhere using Gunicorn.

To redeploy after changes:
Push updates to GitHub.

SSH into PythonAnywhere and pull latest changes.

Restart the web app via the PythonAnywhere dashboard.

# 🗂️ Project Structure
```
/
├── authn/                # Custom authentication
├── restaurant/           # Booking & menu logic
├── templates/            # HTML templates
├── static/               # Static assets
├── staticfiles/          # Collected static files
├── manage.py             # Django management script
├── Pipfile / Pipfile.lock
├── .env                  # Environment variables (not tracked)
├── requirements.txt
└── README.md
```
## 👋 About Me
Ongun Akay, a Senior Full-Stack Developer with expertise across various technologies.

👀 I specialize in full-stack development with extensive experience in frontend and backend technologies. 🌱 Currently, I'm sharpening my skills in advanced concepts of web development. 💞️ I’m always open to exciting collaborations and projects that challenge my abilities. 📫 You can reach me at info@ongunakay.com.

🌐 Website: ongunakay.com <br>
💼 LinkedIn: linkedin.com/in/ongunakay<br>
🧑‍💻 GitHub: github.com/ongunakaycom <br>
📬 Email: info@ongunakay.com<br>

## 📝 License
This is a personal project built using Django for learning and experimentation.