# 💱 Currency Converter GUI (Java + Swing + MySQL)

This is a desktop-based Currency Converter application built using **Java Swing** for the graphical interface and **MySQL** for storing currency conversion history. It allows users to convert between Dollar, Pound, and Rupee using fixed conversion rates and records the results in a persistent database.

---

## 🧰 Features

* ✅ GUI interface with sleek design and user-friendly layout
* 🔁 Convert between Dollar, Pound, and Rupee
* 🧠 Input validation and error handling
* 💾 Persistent storage of conversion history using MySQL
* 🖨️ Displays clean and formatted output with two decimal precision

---

## 📂 Project Structure

```
CurrencyConverter.java       # Main class with GUI, conversion logic, and DB storage
README.md                    # Project documentation
currencydb.sql               # SQL script to create database and table
mysql-connector-java-x.x.x.jar  # MySQL JDBC driver (add to lib folder/classpath)
```

---

## 🚀 Getting Started

### 🔧 Prerequisites

* Java JDK 8 or higher
* MySQL Server installed and running
* MySQL Connector/J (JDBC driver)
* Java IDE (e.g., IntelliJ IDEA, Eclipse)

---

### 🗃️ Database Setup

Create a MySQL database and `conversions` table:

```sql
CREATE DATABASE currencydb;

USE currencydb;

CREATE TABLE conversions (
    id INT AUTO_INCREMENT PRIMARY KEY,
    from_currency VARCHAR(10),
    to_currency VARCHAR(10),
    amount DOUBLE,
    converted_amount DOUBLE,
    conversion_time TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```

Edit the database connection credentials inside the code if needed:

```java
String url = "jdbc:mysql://localhost:3306/currencydb";
String user = "root";
String password = "root";
```

---

### ▶️ Run the Application

1. Clone or download the project files.
2. Open the project in your preferred Java IDE.
3. Make sure MySQL server is running.
4. Add the MySQL JDBC `.jar` file to your classpath.
5. Run `CurrencyConverter.java`.

---

## 🖥️ Usage Instructions

1. **Select Currencies:** Choose the currency to convert *from* and *to* using the dropdowns.
2. **Enter Amount:** Input the amount to convert.
3. **Click Convert:** Press the `Convert` button.
4. **View Result:** The converted amount is displayed in the interface.
5. **Conversion Saved:** The transaction is stored in your MySQL database for record keeping.

---

## 🔄 Conversion Rates Used

| From \ To | Dollar | Pound | Rupee  |
|-----------|--------|-------|--------|
| **Dollar** |   -    | 0.78  | 82.47  |
| **Pound**  | 1.28   |   -   | 105.63 |
| **Rupee**  | 0.012  | 0.0095|   -    |

> These are hardcoded rates. For real-time conversion, consider using an API like [ExchangeRate-API](https://www.exchangerate-api.com/).

---

## 🧪 Testing

* Enter non-numeric values to check validation
* Try converting the same currency (e.g., Dollar to Dollar)
* Use zero and negative values to test error prompts
* Check database to confirm if conversions are being recorded

---

## 📦 Dependencies

* Java Swing (standard)
* JDBC (Java Database Connectivity)
* MySQL Connector/J

---


Enjoy converting and coding with this project! 💸🧠✨
