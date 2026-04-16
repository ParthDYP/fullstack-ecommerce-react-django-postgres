
# 🧾 Full-Stack E-Commerce Platform

_A scalable, full-stack shopping application featuring a Django REST API, React frontend, and robust PostgreSQL data management._

---

## 📌 Table of Contents
- <a href="#overview">Overview</a>
- <a href="#business-problem">Business Problem</a>
- <a href="#dataset">Dataset</a>
- <a href="#tools--technologies">Tools & Technologies</a>
- <a href="#project-structure">Project Structure</a>
- <a href="#Methods">Methods</a>
- <a href="#Key Insights">Key Insights</a>
- <a href="#dashboard">Dashboard</a>
- <a href="#how-to-run-this-project">How to Run This Project</a>
- <a href="#final-recommendations">Final Recommendations</a>
- <a href="#author--contact">Author & Contact</a>

---
<h2><a class="anchor" id="overview"></a>Overview</h2>

This project is a comprehensive e-commerce solution designed to handle the end-to-end user journey—from product discovery to secure checkout. It implements a decoupled architecture where a React-based frontend communicates with a Python/Django backend through secure API endpoints.

---
<h2><a class="anchor" id="business-problem"></a>Business Problem</h2>

Modern e-commerce requires seamless state management, secure user authentication, and real-time synchronization between the UI and the database. This project solves these challenges by implementing JWT authentication, React Context API for global cart management, and PostgreSQL for relational data integrity.

---
<h2><a class="anchor" id="dataset"></a>Dataset</h2>

- Categories: Electronics, Fashion, Home, etc.
- Products: Name, Description, Price, Stock Status, and Image Assets.
- Users: Customer profiles, Authentication logs.
- Orders: Transaction history and itemized order details.

---

<h2><a class="anchor" id="tools--technologies"></a>Tools & Technologies</h2>

- Frontend: React.js, Tailwind CSS, React Router DOM, Context API.
- Backend: Django, Django REST Framework (DRF).
- Database: PostgreSQL.
- Auth: SimpleJWT (JSON Web Tokens), CORS Middleware.
- Environment: Python Dotenv, Virtualenv.
- Version control: GitHub

---
<h2><a class="anchor" id="project-structure"></a>Project Structure</h2>

```
fullstack-ecommerce/
├── backend/                # Django Project Root
│   ├── core/               # Project settings (urls.py, settings.py)
│   ├── api/                # Apps for Products, Orders, etc.
│   ├── .env                # Environment variables (DB credentials, Secret Keys)
│   ├── manage.py
│   └── requirements.txt    # Python dependencies
├── frontend/               # React Project Root
│   ├── public/
│   ├── src/
│   │   ├── components/     # Reusable UI components
│   │   ├── pages/          # ProductListing, ProductDetail, CartPage
│   │   ├── context/        # Cart Context / Auth Context
│   │   └── App.js
│   ├── .env                # Frontend env vars (API base URL)
│   └── package.json
├── .gitignore              # Combined gitignore
├── README.md               # Project documentation
└── docker-compose.yml      # (Optional) To spin up Postgres, Django, and React
```

---
<h2><a class="anchor" id="Methods"></a>Methods</h2>

- Authentication: Token-based login/signup flow with JWT stored in localStorage.
- State Management: Context API to handle global cart updates (add/remove/increment).
- API Design: Functional serializers in DRF to expose relational data (Product-to-Category).
- Routing: Protected frontend routes ensuring only logged-in users access checkout.

---
<h2><a class="anchor" id="Key Insights"></a>Key Insights</h2>

**Decoupled Efficiency:**
- Separating the frontend and backend allows for independent scaling and easier debugging.

**Performance:**
- Fetching data via useEffect with optimized loading/error states significantly improves user retention.

**Data Integrity:**
- PostgreSQL functional dependencies ensure that orders remain consistent even if product prices update in the future.

---
<h2><a class="anchor" id="dashboard"></a>Dashboard</h2>

- Dashboard shows:
  - Product Grid: Responsive layout with Tailwind CSS.
  - Detail Page: Dynamic routing using :id to fetch specific product metadata.
  - Cart System: Real-time quantity updates synced via API.
  - Admin Panel: Django-integrated dashboard for inventory management.
  ![image alt] (https://github.com/ParthDYP/fullstack-ecommerce-react-django-postgres/blob/0674911b6f9703949c851ae43356f205013b4f96/Dashboard.png)

---
<h2><a class="anchor" id="how-to-run-this-project"></a>How to Run This Project</h2>

1. Clone the repository:
```bash
git clone git clone https://github.com/your-username/fullstack-ecommerce.git
```
3. Backend Setup
```bash
cd backend
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
pip install -r requirements.txt
# Update .env with your Postgres credentials
python manage.py migrate
python manage.py runserver
```
4. Frontend Setup
```bash
cd frontend
npm install
npm start
```

---
<h2><a class="anchor" id="final-recommendations"></a>Final Recommendations</h2>

- Payment Gateway: Integration with Stripe or PayPal for real transactions.
- Cloud Storage: Moving product images from local storage to AWS S3.
- Search & Filter: Implementing server-side search and category filtering for better performance on large datasets.

---
<h2><a class="anchor" id="author--contact"></a>Author & Contact</h2>

**Parth Ambale**    
📧 Email: parthambale0@gmail.com  
🔗 [LinkedIn](https://www.linkedin.com/in/parthambale1902/)  
