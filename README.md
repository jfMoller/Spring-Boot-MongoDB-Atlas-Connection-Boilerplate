# **Spring-Boot-MongoDB-Atlas-Connection-Boilerplate**

## Introduction

I wanted to put together some boilerplate code for setting up a connection between Java Springboot and the MongoDB Atlas cluster.

## Description

This project provides a backend for setting up a connection to MongoDB Atlas with an example product repository, controller, and service. It could be useful as a starting point for creating noSQL full-stack apps.

## How to Run Locally

1. **Clone the project:**

    ```bash
    git clone https://github.com/jfMoller/Spring-Boot-MongoDB-Atlas-Connection-Boilerplate.git
    ```

2. [**Create an account and a free MongoDB Atlas cluster**](https://www.mongodb.com/cloud/atlas)
   

3. **Create a first database and collection in MongoDB Atlas**
```
   For example: "productDB" and "products"
```
4. **Get your connection string from your cluster**

    - Go to **connect**
    - **Connect to application**
      - Pick Drivers
      - Pick the Java driver
      - Copy the provided connection string
      - 

5. **Configure your application.properties file**

   Update your `application.properties` file with the following information:

    ```properties
    spring.data.mongodb.uri=YOUR_CONNECTION_STRING
    spring.data.mongodb.database=YOUR_DATABASE_NAME
    ```

   For example:
    ```properties
    spring.data.mongodb.uri=mongodb+srv://jfMoller:<password>@ExampleCluster.yeqqlzp.mongodb.net/?retryWrites=true&w=majority
    spring.data.mongodb.database=productDB
    ```
   Make sure to replace `<password>` with your own cluster password.


6. **Run the Spring Boot Application in your IDE**


7. **Verify that the endpoints are functioning as intended, for example by using [**Postman**](https://www.postman.com/downloads/)**

**GET**
```
Endpoint: `http://localhost:8080/api/products/all`
```
**POST**
```
Endpoint: `http://localhost:8080/api/products/insert`
JSON: `{"name": "Example", "price": 100, "quantity": 1}`
```
**PUT**
```
Endpoint: `http://localhost:8080/api/products/edit/{product_id}`
JSON: `{"_id": "{product_id}", "name": "test", "price": 100.0, "quantity": 1 }`
```
**DELETE**
```
Endpoint: `http://localhost:8080/api/products/delete/{product_id}`
```
    
  
    
