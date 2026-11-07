# 💳 FinPay – Student Wallet, Payments & Cashback Platform

A modern campus payment platform that allows students to manage digital wallets, make payments to campus merchants, earn cashback, and track transactions. Administrators can monitor transactions and generate monthly reconciliation reports.

FinPay features a redesigned, modern fintech-inspired interface with an emerald and teal color palette, while retaining its existing backend functionality and business logic.

## ✨ Features

### 👨‍🎓 Student Dashboard
- Student registration and login.
- Digital wallet management.
- Add money to wallet.
- View wallet balance and transaction history.
- Make payments to registered merchants.
- Earn cashback on eligible transactions.
- View payment and cashback history.

### 🏪 Merchant Dashboard
- Merchant registration and authentication.
- Create and manage merchant profiles.
- View total payments received.
- Track payment transactions.

### 🛡️ Admin Dashboard
- Monthly transaction reconciliation.
- Monitor total sales and cashback.
- View merchant-wise settlement reports.
- Verify wallet and ledger consistency.

### 🎨 UI/UX Improvements
- Modern fintech-inspired design.
- Emerald, teal and white color palette.
- Clean dashboard layouts.
- Improved cards, buttons and input fields.
- Responsive layout for different screen sizes.
- Enhanced typography, shadows and spacing.

## 🛠️ Technology Stack

| Technology | Purpose |
|---|---|
| Python | Backend programming |
| FastAPI | REST API development |
| SQLAlchemy | Database ORM |
| SQLite | Database |
| HTML5 | Frontend structure |
| CSS3 | Frontend styling |
| JavaScript | Frontend functionality |
| JWT | Authentication |
| Pytest | Application testing |
| Uvicorn | ASGI server |

## 🏗️ System Architecture

FinPay follows a **Layered Architecture** to separate business logic, API handling and database operations.

```text
             Frontend
          HTML / CSS / JS
                 |
                 v
             FastAPI
                 |
                 v
              Routers
                 |
                 v
              Services
           (Business Logic)
                 |
                 v
            Repositories
           (Data Access)
                 |
                 v
              Models
                 |
                 v
              SQLite
              Database
```

### Project Structure

```text
FINPAY/
│
├── app/
│   ├── core/
│   │   ├── database.py
│   │   ├── security.py
│   │   ├── errors.py
│   │   └── utils.py
│   │
│   ├── models/
│   │   ├── user.py
│   │   ├── wallet.py
│   │   ├── merchant.py
│   │   ├── transaction.py
│   │   └── cashback.py
│   │
│   ├── repositories/
│   │   ├── user_repository.py
│   │   ├── wallet_repository.py
│   │   ├── merchant_repository.py
│   │   ├── transaction_repository.py
│   │   └── cashback_repository.py
│   │
│   ├── routers/
│   │   ├── auth_router.py
│   │   ├── wallet_router.py
│   │   ├── merchant_router.py
│   │   ├── payment_router.py
│   │   ├── cashback_router.py
│   │   └── reconciliation_router.py
│   │
│   ├── services/
│   │   ├── auth_service.py
│   │   ├── wallet_service.py
│   │   ├── merchant_service.py
│   │   ├── payment_service.py
│   │   ├── cashback_service.py
│   │   └── reconciliation_service.py
│   │
│   ├── static/
│   │   └── index.html
│   │
│   ├── main.py
│   └── schemas.py
│
├── tests/
│   └── test_flow.py
│
├── requirements.txt
└── README.md
```

## ⚙️ Installation and Setup

### 1. Clone the repository

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
```

### 2. Navigate to the project directory

```bash
cd FINPAY-main
```

### 3. Create a virtual environment

```bash
python -m venv venv
```

Activate it:

**Windows:**
```bash
venv\Scripts\activate
```

**Linux / macOS:**
```bash
source venv/bin/activate
```

### 4. Install dependencies

```bash
pip install -r requirements.txt
```

### 5. Run the application

```bash
python -m uvicorn app.main:app --reload
```

### 6. Open the application

| Service | URL |
|---|---|
| FinPay Web Application | http://127.0.0.1:8000/ |
| Swagger API Documentation | http://127.0.0.1:8000/docs |
| Health Check | http://127.0.0.1:8000/health |

The SQLite database is automatically created when the application starts.

## 💰 Cashback Rules

| Rule | Value |
|---|---|
| Cashback Rate | 2% |
| Minimum Eligible Payment | ₹100 |
| Maximum Cashback | ₹50 per transaction |

Example:

- Payment: ₹500
- Cashback: ₹10
- Total cashback credited: ₹10

## 🔐 Security Features

- JWT-based authentication.
- Password hashing.
- Role-based access control.
- Input validation.
- Wallet balance validation.
- Transaction consistency through database transactions.

## 🧪 Testing

Run the automated tests using:

```bash
python -m pytest -q
```

The tests cover authentication, wallet operations, merchant payments, cashback calculations, role permissions and monthly reconciliation.

## 📸 Screenshots

Add your application screenshots here.

Suggested screenshots:

- Login and Registration Page
- Student Dashboard
- Wallet and Transaction History
- Merchant Dashboard
- Admin Dashboard
- Monthly Reconciliation Report

Example:

```markdown
![FinPay Dashboard](screenshots/dashboard.png)
```

## 🚀 Future Enhancements

- QR-code-based payments.
- Payment notifications.
- Transaction export to PDF.
- Advanced analytics and visual reports.
- Integration with real payment gateways.
- PostgreSQL support for production deployment.
- Enhanced administrative controls.

## ⚠️ Disclaimer

FinPay is an educational project intended for demonstration and learning purposes. It is not a production-ready banking or payment system. Real financial transactions and deployment require additional security, compliance and payment gateway integrations.

## 👨‍💻 Project

**FinPay – Student Wallet, Payments & Cashback Platform**

Built using Python, FastAPI, SQLite, HTML, CSS and JavaScript.

---

⭐ If you find this project interesting, consider giving the repository a star!
