# StockWise — Smart Inventory Management

A full-stack inventory management system built with **Spring Boot** (Java 17) and a plain **HTML/CSS/JS** front-end.

## Features

- **Product Management** — Add, update, delete, and search products by name, category, or SKU
- **Store Management** — Create stores and manage per-store inventory
- **Inventory Tracking** — Track stock levels across multiple stores
- **Order Processing** — Place orders with automatic stock validation and deduction
- **Customer Management** — Auto-create customers on first order, track order history
- **Product Reviews** — Customer reviews stored in MongoDB, linked to products and stores

## Tech Stack

| Layer       | Technology                        |
|-------------|-----------------------------------|
| Back-end    | Spring Boot 3.4.3, Java 17       |
| SQL Database| MySQL (products, stores, orders)  |
| NoSQL Database | MongoDB (reviews)              |
| Front-end   | HTML, CSS, JavaScript (vanilla)   |

## Getting Started

### Prerequisites

- Java 17+
- Maven
- MySQL
- MongoDB

### Configuration

Update `back-end/src/main/resources/application.properties` with your database connection details:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/inventory
spring.datasource.username=root
spring.datasource.password=your_password
spring.data.mongodb.uri=mongodb://localhost:27017/reviews
```

### Run the Back-end

```bash
cd back-end
./mvnw spring-boot:run
```

### Open the Front-end

Open `front-end/index.html` in your browser. The front-end connects to the back-end at `http://localhost:8080`.

## Project Structure

```
StockWise/
├── back-end/
│   ├── src/main/java/com/project/code/
│   │   ├── Controller/    # REST API controllers
│   │   ├── Model/         # JPA entities & DTOs
│   │   ├── Repo/          # Spring Data repositories
│   │   ├── Service/       # Business logic
│   │   └── config/        # CORS configuration
│   └── pom.xml
├── front-end/
│   ├── index.html         # Main dashboard
│   ├── reviews.html       # Product reviews page
│   ├── script.js          # Application logic
│   └── frontend.css       # Styles
├── insert_data.sql        # Sample data
└── reviews.json           # Sample review data
```

## License

This project is licensed under the Apache License 2.0.
