# Secure Login System Spring

A simple secure login system implemented with Spring Boot, Spring Security, and MySQL.

## Features
- User registration and authentication
- Password hashing using BCrypt
- Role-based access control
- Account activation via email
- Logout functionality
- Custom login and registration pages
- Security with Spring Security
- Google reCAPTCHA integration for registration
- Input validation with regular expressions for username, email, and password inputs

## Prerequisites
- Java 17 or higher
- MySQL 8 or higher
- Maven
- A MySQL database named `secure_login_system`
- A Google reCAPTCHA API key (site key and secret key)
- An email service for sending activation links (SMTP configuration)

## Technologies Used
- Spring Boot: Backend framework
- Spring Security: Authentication and authorization
- Thymeleaf: Template engine for UI
- MySQL: Database
- Hibernate: ORM framework
- BCrypt: Password hashing
- Google reCAPTCHA: Protection against bots
- JavaMailSender: Email service for account activation

## Installation

### 1. Clone the repository
```bash
git clone https://github.com/jabka1/SecureLoginSystemSpring
cd SecureLoginSystemSpring
```

### 2. Rename application.txt (src/main/resources/application.txt) to application.properties and fill your data
application.txt: [click here](src/main/resources/application.txt)

### 3. Configure the Database
Edit the application.properties file in src/main/resources:
```bash
spring.datasource.url=jdbc:mysql://localhost:3306/YOUR_DB
spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver
spring.datasource.username=YOUR_USERNAME
spring.datasource.password=YOUR_PASSWORD
```
Replace YOUR_USERNAME and YOUR_PASSWORD with your MySQL credentials.

### 4. Configure Google reCAPTCHA
To integrate Google reCAPTCHA into your registration form, follow these steps:
- Go to the Google reCAPTCHA website https://www.google.com/recaptcha/about/.
- Register your site and get your site key and secret key.
- Add your secret key to the application.properties file:
```bash
google.recaptcha.site.key=YOUR_SITE_KEY
google.recaptcha.secret.key=YOUR_SECRET_KEY
```
Replace YOUR_SITE_KEY and YOUR_SECRET_KEY with your Google reCAPTCHA site keys.

### 5. Configure Email Activation
To enable email-based activation, configure the SMTP server in the application.properties file:
```bash
spring.mail.host=smtp.YOUR_EMAIL_PROVIDER.com
spring.mail.port=587
spring.mail.username=YOUR_EMAIL
spring.mail.password=YOUR_EMAIL_PASSWORD
spring.mail.properties.mail.smtp.auth=true
spring.mail.properties.mail.smtp.starttls.enable=true
```
### 6. Build the Project
Use Maven to build the project:
```bash
mvn clean install
```

### 7. Run the Application
Run the application using:
```bash
mvn spring-boot:run
```

### 8. Access the Application
Open your browser and navigate to:
```bash
http://localhost:8080
```

## Screenshots
