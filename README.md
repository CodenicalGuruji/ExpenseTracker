# ExpenseTracker - Personal Finance Manager

![Project Banner](https://via.placeholder.com/1024x300.png?text=Expense+Tracker+-+Smart+Financial+Management) <!-- Add your own banner image -->

A full-stack web application for tracking personal finances, managing expenses/income across multiple bank accounts, and visualizing spending patterns.

## 🚀 Features

### Core Functionality

- 🔐 **JWT Authentication & User Management**
  - Secure user registration/login
  - Password encryption with BCrypt
- 💸 **Transaction Management**
  - Create expenses/income records
  - Categorize transactions (Food, Travel, Bills, etc.)
  - Tagging system for transactions
- 🏦 **Multi-Bank Account Support**
  - Track balances across different accounts
  - Assign transactions to specific accounts
- 📅 **Date Filtering & Reporting**
  - Filter transactions by date ranges
  - Daily/Weekly/Monthly views
- 📊 **Budget Management**
  - Set category-specific budgets
  - Monthly budget tracking

### Technical Highlights

- RESTful API with proper status codes
- Database migration with Flyway
- MapStruct for DTO-Entity mapping
- Spring Boot Actuator for monitoring
- H2 Database (Dev) + PostgreSQL ready (Prod)

## 🛠 Tech Stack

### Backend

| Component         | Technology                          |
| ----------------- | ----------------------------------- |
| Framework         | Spring Boot 3.4.3                   |
| Language          | Java 21                             |
| Build Tool        | Maven                               |
| Security          | Spring Security + JWT               |
| ORM               | Spring Data JPA (Hibernate)         |
| Database          | H2 (Development), PostgreSQL (Prod) |
| API Documentation | Postman                             |
| Testing           | JUnit 5, Mockito                    |
| Utilities         | Lombok, MapStruct                   |

### Frontend (Planned)

| Component        | Technology              |
| ---------------- | ----------------------- |
| Framework        | React 19                |
| Build Tool       | Vite                    |
| State Management | Redux Toolkit / Zustand |
| Styling          | Tailwind CSS            |
| Charts           | Chart.js                |
| UI Components    | Shadcn/ui               |
| HTTP Client      | Axios                   |

## ⚙️ Installation & Setup

### Prerequisites

- Java 21 JDK
- Maven 3.9+
- Node.js 20+ (for frontend)
- PostgreSQL (optional for production)

### Backend Setup

1. **Clone Repository**
   ```
   git clone https://github.com/CodenicalGuruji/ExpenseTracker.git
   cd ExpenseTracker/backend
   ```
2. **Build Application**
   ```
   mvn clean install
   ```
3. **Run Application**
   ```
   mvn spring-boot:run
   ```
4. **Access H2 DB Console**
   ```
   URL: http://localhost:8080/h2-console
   JDBC URL: jdbc:h2:mem:expensetracker
   Username: sa
   Password: [leave empty]
   ```

### Frontend Setup (Coming Soon)

    cd expensetracker/frontend
    npm install
    npm run dev

## 📚 API Documentation

[![Run in Postman](https://run.pstmn.io/button.svg)](https://documenter.getpostman.com/view/12345678/2s9YJZbTqE) <!-- Replace with your Postman link -->

Sample API Endpoints:

- `POST /api/auth/signup` - User registration
- `POST /api/auth/login` - User authentication
- `GET /api/transactions` - Get filtered transactions
- `POST /api/categories` - Create spending category

## 🔍 Testing

Run all tests:
mvn test

## ⚙️ Configuration

Update `src/main/resources/application.properties`:

    # H2 Configuration
    spring.datasource.url=jdbc:h2:mem:expensetracker

    # JWT Configuratons
    jwt.secret=your-strong-secret-key
    jwt.expiration.ms=86400000 # 24 hours

## 🤝 Contribution Guidelines

1.  Fork the repository
2.  Create your feature branch:
         git checkout -b feature/amazing-feature
3.  Commit your changes:
        git commit -m 'Add some amazing feature'
4.  Push to the branch:

        git push origin feature/amazing-feature

5.  Open a Pull Request
