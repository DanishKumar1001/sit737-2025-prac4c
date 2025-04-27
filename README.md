# Calculator Microservice

Calculator Microservice with expanded features exponentiation, square root, and modulo operations in basic calculator from Task 4.1P. Supports RESTful API endpoints with input validation and error handling. Created for SIT737 Cloud Native App Dev – Task 4.2C (T1 2025).

## Steps to Run Microservice:

### 1. Clone the Repository

git clone https://github.com/DanishKumar1001/SIT737-2025-prac4c.git
cd SIT737-2025-prac4c

### 2. Install Dependencies

npm install

### 3. Run the Application

node calculator.js
The service will run on http://localhost:3000. 

* Either use browser or postman

### Available Endpoints

### 1. Addition

GET /add?num1=10&num2=5

### 2. Subtraction

GET /subtract?num1=10&num2=5
Returns error if num1 < num2.

### 3. Multiplication

GET /multiply?num1=10&num2=5

### 4. Division

GET /divide?num1=10&num2=5
Returns error if num2 == 0.

### 5. Exponentiation(Power)

GET /power?num1=2&num2=3

### 6. Modulo 

GET /modulo?num1=10&num2=3
Returns error if num2 == 0.

### 7. Square Root:

GET /sqrt?num1=16
Returns error if num1 is negative.

## Error Handling

**Missing Parameters:** Returns 400 Bad Request
**Invalid Numbers:** Returns 400 Bad Request
**Subtraction Edge Case:** num1 must be greater than num2
**Division by Zero:** Not allowed
**Modulo by Zero:** Not allowed
**Square Root of Negative Number:** Not allowed
**Invalid Endpoint:** Returns 404 Not Found

## 📊 Logging with Winston

**Winston Logs Include:**

1. All incoming requests
2. Success logs for each operation
3. Error logs for invalid operations and endpoints

**Log Files:**

1. logs/combined.log – all logs
2. logs/error.log – only errors
