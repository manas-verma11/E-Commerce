# 🛒 E-Commerce Web Application

A full-stack **E-Commerce Web Application** built with **React.js** and **Spring Boot**. The project provides a modern shopping experience with product browsing, cart management, checkout functionality, and an admin interface for managing products.

The application is divided into a responsive React frontend and a RESTful Spring Boot backend.

---

## ✨ Features

### 👤 User Features

* 🏠 Modern and responsive home page
* 🛍️ Browse available products
* 🔎 View detailed product information
* 🛒 Add products to cart
* ➕ Increase or decrease product quantity
* ❌ Remove products from cart
* 💰 View cart total
* 📦 Checkout functionality
* 📱 Responsive design for different screen sizes

### 🔐 Admin Features

* ➕ Add new products
* ✏️ Update existing products
* 🗑️ Delete products
* 📋 Manage product information
* 🖼️ Product image management

### ⚙️ Application Features

* REST API architecture
* React Context API for frontend state management
* Axios for API communication
* Spring Boot backend
* Maven dependency management
* MySQL/database integration
* CORS configuration for frontend-backend communication
* Component-based React architecture

---

## 🏗️ Project Structure

```text
E-Commerce/
│
├── ecom-frontend/                 # React + Vite frontend
│   ├── public/
│   ├── src/
│   │   ├── components/
│   │   │   ├── AddProduct.jsx
│   │   │   ├── Cart.jsx
│   │   │   ├── CheckoutPopup.jsx
│   │   │   ├── Home.jsx
│   │   │   ├── Navbar.jsx
│   │   │   ├── Product.jsx
│   │   │   └── UpdateProduct.jsx
│   │   │
│   │   ├── Context/
│   │   │   └── Context.jsx
│   │   │
│   │   ├── App.jsx
│   │   ├── App.css
│   │   ├── axios.jsx
│   │   ├── index.css
│   │   └── main.jsx
│   │
│   ├── package.json
│   └── vite.config.js
│
├── ecom-project/                  # Spring Boot backend
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/
│   │   │   └── resources/
│   │   │       └── application.properties
│   │   │
│   │   └── test/
│   │
│   ├── pom.xml
│   └── mvnw
│
└── README.md
```

---

## 🛠️ Tech Stack

### Frontend

| Technology            | Purpose                             |
| --------------------- | ----------------------------------- |
| **React.js**          | Building the user interface         |
| **Vite**              | Frontend development and build tool |
| **React Context API** | Global state management             |
| **Axios**             | HTTP requests to backend APIs       |
| **CSS**               | Styling and responsive UI           |
| **JavaScript (ES6+)** | Application logic                   |

### Backend

| Technology        | Purpose                           |
| ----------------- | --------------------------------- |
| **Java**          | Backend programming language      |
| **Spring Boot**   | Backend framework                 |
| **Spring Web**    | REST API development              |
| **Maven**         | Dependency and project management |
| **MySQL**         | Database                          |
| **JPA/Hibernate** | Database interaction              |

---

## 🔄 Application Architecture

```text
                 ┌─────────────────────┐
                 │       User          │
                 └──────────┬──────────┘
                            │
                            ▼
                 ┌─────────────────────┐
                 │   React Frontend    │
                 │      (Vite)         │
                 └──────────┬──────────┘
                            │
                     HTTP / REST API
                            │
                            ▼
                 ┌─────────────────────┐
                 │   Spring Boot API   │
                 │      Backend        │
                 └──────────┬──────────┘
                            │
                         JPA / ORM
                            │
                            ▼
                 ┌─────────────────────┐
                 │       MySQL         │
                 │      Database       │
                 └─────────────────────┘
```

---

# 🚀 Getting Started

Follow the steps below to run the project locally.

## 📋 Prerequisites

Make sure you have the following installed:

* **Java JDK 17+**
* **Node.js 18+**
* **npm**
* **Maven** (optional because the project includes Maven Wrapper)
* **MySQL**
* **Git**

---

## 📥 1. Clone the Repository

```bash
git clone https://github.com/manas-verma11/E-Commerce.git
```

Navigate into the project:

```bash
cd E-Commerce
```

---

# 🎨 Frontend Setup

Open a terminal and navigate to the frontend:

```bash
cd ecom-frontend
```

Install dependencies:

```bash
npm install
```

Start the Vite development server:

```bash
npm run dev
```

The frontend will normally be available at:

```text
http://localhost:5173
```

---

# ☕ Backend Setup

Open another terminal and navigate to the backend:

```bash
cd ecom-project
```

### Using Maven Wrapper

On Windows:

```bash
mvnw.cmd spring-boot:run
```

On Linux/macOS:

```bash
./mvnw spring-boot:run
```

Alternatively, if Maven is installed:

```bash
mvn spring-boot:run
```

The Spring Boot server will run on the port configured in:

```text
src/main/resources/application.properties
```

---

# 🗄️ Database Configuration

Create a MySQL database for the application.

Example:

```sql
CREATE DATABASE ecommerce;
```

Then configure your database connection in:

```text
ecom-project/src/main/resources/application.properties
```

Example configuration:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/ecommerce
spring.datasource.username=YOUR_USERNAME
spring.datasource.password=YOUR_PASSWORD

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
```

> Replace `YOUR_USERNAME` and `YOUR_PASSWORD` with your local MySQL credentials.

**Do not commit real database passwords or other secrets to GitHub.**

---

# 🔌 API Communication

The React frontend communicates with the Spring Boot backend through REST APIs.

Axios is used on the frontend to send HTTP requests to the backend.

Typical flow:

```text
React Component
      │
      ▼
    Axios
      │
      ▼
Spring Boot REST API
      │
      ▼
    Service
      │
      ▼
 Repository / JPA
      │
      ▼
    MySQL
```

---

# 🛍️ Main Application Flow

### Product Browsing

```text
Home Page
    ↓
Products
    ↓
Product Details
    ↓
Add to Cart
```

### Shopping Cart

```text
Product
   ↓
Add to Cart
   ↓
Cart
   ├── Increase Quantity
   ├── Decrease Quantity
   └── Remove Product
   ↓
Checkout
```

### Product Management

```text
Admin
  ↓
Add Product
  ↓
Product Database
  ↓
Frontend Product Listing
```

---

# 📸 Screenshots

Add screenshots of your application here to make the repository more attractive to recruiters and other developers.

Example:

```markdown
## 📸 Screenshots

### Home Page

![Home Page](screenshots/home.png)

### Product Page

![Product Page](screenshots/product.png)

### Shopping Cart

![Shopping Cart](screenshots/cart.png)

### Admin Panel

![Admin Panel](screenshots/admin.png)
```

You can create a `screenshots/` folder in the root of the repository and place your images there.

---

# 🔮 Future Improvements

Some features that can be added in future versions:

* 🔐 User registration and login
* 🔑 JWT-based authentication
* 👥 Role-based authorization
* ❤️ Wishlist functionality
* 🔎 Product search
* 🏷️ Product categories and filtering
* ⭐ Product reviews and ratings
* 📦 Order history
* 🚚 Order tracking
* 💳 Online payment integration
* 📧 Email notifications
* 🖼️ Cloud-based image storage
* 📊 Admin dashboard and analytics
* 🐳 Docker support
* ☁️ Cloud deployment
* 🧪 More backend and frontend tests

---

# 🧪 Testing

The backend contains a test structure under:

```text
ecom-project/src/test/
```

Run backend tests with:

```bash
mvn test
```

Or using the Maven Wrapper on Windows:

```bash
mvnw.cmd test
```

---

# 🤝 Contributing

Contributions are welcome!

If you would like to improve this project:

1. Fork the repository
2. Create a new branch

```bash
git checkout -b feature/your-feature
```

3. Make your changes
4. Commit your changes

```bash
git commit -m "Add your feature"
```

5. Push your branch

```bash
git push origin feature/your-feature
```

6. Open a Pull Request

---

# 📄 License

This project is intended for **educational and development purposes**.

If you plan to use this project commercially, add an appropriate open-source license and update this section accordingly.

---

# 👨‍💻 Author

**Manas Verma**

GitHub: [@manas-verma11](https://github.com/manas-verma11?utm_source=chatgpt.com)

---

## ⭐ Support

If you find this project useful, consider giving the repository a ⭐ on GitHub!

**Repository:** [Manas Verma — E-Commerce](https://github.com/manas-verma11/E-Commerce?utm_source=chatgpt.com)

---

### 💡 About This Project

This project was built to demonstrate full-stack web development using a modern **React frontend** and **Spring Boot backend**, with RESTful communication between the client and server.

It is a practical project for learning and demonstrating concepts such as:

* Full-stack development
* REST API development
* React component architecture
* State management
* CRUD operations
* Database integration
* Frontend-backend communication
* Maven/Spring Boot application development
* E-commerce application architecture
