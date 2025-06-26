# API Testing with Postman & REST Assured (Java)

This project demonstrates API testing using two powerful tools:
- 🧪 **Postman**: for quick, GUI-based testing of HTTP requests
- 🧪 **REST Assured**: for automated and programmatic validation of APIs in Java

The tests use the public [ReqRes API](https://reqres.in/) as a mock backend.

## 🔧 Technologies Used
- Postman
- REST Assured
- Java
- JUnit
- JSON

## 📁 Project Structure

```
API-Testing-with-Postman-REST-Assured-Java-Based-Testing-Framework/
├── postman/
│   └── sample_collection.json       # Postman API collection
├── restassured/
│   └── src
│       └── test
│           └── java/
│               └── APITest.java     # REST Assured API test class
└── README.md                        # Project documentation
```

## ✅ Features

### Postman:
- Sends GET request to `/users?page=2`
- Easy to import and run inside the Postman app

### REST Assured:
- Validates the API status code (200)
- Asserts the size of the `data[]` array returned
- Uses JUnit for test structure and assertion

### Sample Code:
```java
given()
  .when()
  .get("/users?page=2")
  .then()
  .statusCode(200)
  .body("data.size()", greaterThan(0));
```

---

## 🚀 How to Use

### 📥 Postman
1. Open Postman
2. Import `sample_collection.json`
3. Run the request and view the response

### 💻 REST Assured
1. Clone the repo:
   ```
   git clone https://github.com/richie-qa-engineer/API-Testing-with-Postman-REST-Assured-Java-Based-Testing-Framework.git
   ```
2. Open in your Java IDE (like IntelliJ or Eclipse)
3. Run `APITest.java` as a JUnit test

---

🎯 **Ideal For:**
- Freelance QA portfolio showcase
- Sample for API test automation projects
- Learning REST API testing tools
