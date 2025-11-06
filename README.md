# Django Hello World 🌍

A minimal **Django** project demonstrating the core concepts of Django’s architecture — projects, apps, views, and URL dispatching.  
This is a perfect starting point for beginners learning how to build a web application with Django.

---

## 🏗️ Project Structure

```
django_project/
├── django_project/
│   ├── __init__.py
│   ├── asgi.py
│   ├── settings.py
│   ├── urls.py
│   └── wsgi.py
├── pages/
│   ├── __init__.py
│   ├── admin.py
│   ├── apps.py
│   ├── migrations/
│   │   └── __init__.py
│   ├── models.py
│   ├── tests.py
│   ├── views.py
│   └── urls.py
├── manage.py
```

---

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/gatwirival/Django-HelloWorld.git
cd Django-HelloWorld
```

### 2. Create and activate a virtual environment

```bash
python3 -m venv .venv
source .venv/bin/activate     # On Windows: .venv\Scripts\activate
```

### 3. Install dependencies

```bash
pip install django
```

### 4. Apply initial migrations

```bash
python manage.py migrate
```

### 5. Run the development server

```bash
python manage.py runserver
```

Then open your browser and visit:

👉 **http://127.0.0.1:8000/**

You should see:

> “Hello, World!”

---

## 🧠 How It Works

### **`views.py`**
```python
from django.http import HttpResponse

def home_page_view(request):
    return HttpResponse("Hello, World!")
```

### **`pages/urls.py`**
```python
from django.urls import path
from .views import home_page_view

urlpatterns = [
    path("", home_page_view),
]
```

### **`django_project/urls.py`**
```python
from django.contrib import admin
from django.urls import path, include

urlpatterns = [
    path("admin/", admin.site.urls),
    path("", include("pages.urls")),
]
```

---

## ⚙️ Key Django Concepts Learned

- **Project vs App:**  
  The project (`django_project`) acts as the container for configuration.  
  The app (`pages`) handles specific functionality (in this case, rendering a homepage).

- **Views:**  
  Handle logic for what gets displayed when a URL is requested.

- **URL Dispatcher:**  
  Maps URLs to views using the `path()` and `include()` functions.

---

## 🧩 Next Steps

- Add templates and static files (HTML, CSS)
- Create more views and link them to different URLs
- Learn about models, admin, and databases

---

## 🪪 License

This project is open source and available under the [MIT License](LICENSE).

 
📧 [your.email@example.com]  
🌐 [your-portfolio-or-linkedin](https://www.linkedin.com/in/your-profile)
