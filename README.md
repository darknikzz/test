# Ecommerce Project using Go Programming with Gin Framework

This project is an ecommerce application built using Go programming language and the Gin framework. It follows the clean code architecture, which promotes separation of concerns and maintainability.

## Project Overview

The ecommerce-gin-clean-arch project is designed to provide a performant and feature-rich ecommerce solution. It includes functionalities such as user authentication, product management, shopping cart, order processing, and payment integration.

## Used Packages

The project utilizes the following packages:

1. [GIN](github.com/gin-gonic/gin): A web framework written in Go that combines high performance with an API similar to Martini.
2. [JWT](github.com/golang-jwt/jwt): A Go implementation of JSON Web Tokens for secure authentication and authorization.
3. [GORM](https://gorm.io/index.html) with [PostgreSQL](https://gorm.io/docs/connecting_to_the_database.html#PostgreSQL): A powerful ORM library for Go that simplifies database operations.
4. [Wire](https://github.com/google/wire): A code generation tool for dependency injection, making it easier to connect components.
5. [Viper](https://github.com/spf13/viper): A configuration solution for Go applications, supporting various formats and 12-Factor app principles.
6. [swag](https://github.com/swaggo/swag) with [gin-swagger](https://github.com/swaggo/gin-swagger) and [swaggo files](github.com/swaggo/files): Converts Go annotations to Swagger Documentation 2.0 for API documentation.

## Setup Instructions

To use and test the ecommerce-gin-clean-arch project, please follow these steps:

### Prerequisites

Make sure you have the following installed on your system:

- Go (https://golang.org/doc/install)
- PostgreSQL (https://www.postgresql.org/download/)

### 1. Clone the Repository

Clone the ecommerce-gin-clean-arch repository to your local system:

```bash
git clone https://github.com/nikhilnarayanan623/ecommerce-gin-clean-arch.git
cd ecommerce-gin-clean-arch
```
### 2. Install Dependencies

Install the required dependencies using either the provided Makefile command or Go's built-in module management:

```bash
# Using Makefile
make deps

# OR using Go
go mod tidy
```
### 3. Configure Environment Variables
details provided the end of file
### 4. Make Swagger Files (If You Using Swagger)

```bash
make swag
```

### 5. Run The Application
```bash
make run
```
### To Use The API
1. visit [swagger](http://localhost:8000/swagger/index.html) to see all the api

### Set up Environment Variables
Set up the necessary environment variables in a .env file at the project's root directory. Below are the variables required:
# PostgreSQL database details
DB_HOST="<your database host name>"
DB_NAME="<your database name>"
DB_USER="<your database user name>"
DB_PASSWORD="<your database owner password>"
DB_PORT="<your database running port number>"

# JWT
JWT_SECRET_ADMIN="<secret code for signing admin JWT token>"
JWT_SECRET_USER="<secret code for signing user JWT token>"

# Twilio
AUTH_TOKEN="<your Twilio authentication token>"
ACCOUNT_SID="<your Twilio account SID>"
SERVICE_SID="<your Twilio messaging service SID>"

# Razorpay
RAZOR_PAY_KEY="<your Razorpay API test key>"
RAZOR_PAY_SECRET="<your Razorpay API test secret key>"

# Stripe
STRIPE_SECRET="<your Stripe account secret key>"
STRIPE_PUBLISH_KEY="<your Stripe account publish key>"
STRIPE_WEBHOOK="<your Stripe account webhook key>"

# Google Auth
GOAUTH_CLIENT_ID="<your Google Auth client ID>"
GOAUTH_CLIENT_SECRET="<your Google Auth secret key>"
GOAUTH_CALL_BACK_URL="<your registered callback URL for Google Auth>"

