
# `Ecommerce` Project using `Go programing` with `gin` framework
# Here I'm follwing `clean-code architecture` for my project

# Used Packages 
1. [GIN](github.com/gin-gonic/gin) is a web framework written in Go (Golang). It features a martini-like API with performance that is up to 40 times faster thanks to httprouter. If you need performance and good productivity, you will love Gin.
2. [JWT](github.com/golang-jwt/jwt) A go (or 'golang' for search engine friendliness) implementation of JSON Web Tokens.
3. [GORM](https://gorm.io/index.html) with [PostgresSQL](https://gorm.io/docs/connecting_to_the_database.html#PostgreSQL)The fantastic ORM library for Golang aims to be developer friendly.
4. [Wire](https://github.com/google/wire) is a code generation tool that automates connecting components using dependency injection.
5. [Viper](https://github.com/spf13/viper) is a complete configuration solution for Go applications including 12-Factor apps. It is designed to work within an application, and can handle all types of configuration needs and formats.
6. [swag](https://github.com/swaggo/swag) converts Go annotations to Swagger Documentation 2.0 with [gin-swagger](https://github.com/swaggo/gin-swagger) and [swaggo files](github.com/swaggo/files)

# To Use and check my `ecommerce-gin-clean-arch` Project

# Follow these steps

1. clone my github `ecommerce-gin-clean-arch` repository to your system
2. use these bash commands

``` bash commands
## these bash comands are set-up on makefilie ##

# Step 1 :  Navigate into project directory
cd ./ecommerce-gin-clean-arch

# Step 2 : Install needed dependencies
make deps 
#or
go mod tidy

# Step 3 : Setup environment variables (directions given in the last of readme)

# Step 4 : if you want to use swagger for using the application the generate swagger files using given command
make swag

# Step 5 : Run the Server
make run

# if you are using postman then check : localhost:8000
 
# if you using swagger
#  Open any browser and visit localhost:8000/swagger/index.html (!you should generate swagger files use `make swag`)

For Test the Application

# step 1 : generate mock files
make generate
# step 2 : run the test 
make test

# values need to be in env(create your env in root directory)
# postgres databse details
DB_HOST="<your Datbase host name (localhost)>"
DB_NAME="<your database name>"
DB_USER="<your database user name>"
DB_PASSWORD="<your database owner password>"
DB_PORT="<your database running port number>"
#JWT
JWT_SECRET_ADMIN="<secret code that you want to use for signing admin jwt token>"
JWT_SECRET_USER="<secret code that you want to use for signing user jwt tokenr>"
# twillio
# create an account on twilio and setup messaging service
AUTH_TOKEN="<your twilio authenticatino token ( token)>"
ACCOUNT_SID="<your twilio account SID (account sid)>"
SERVICE_SID="<your twilio SID (messaging service sid)>"
#razorpay
# create an razorpay account and get api key
RAZOR_PAY_KEY="<your razorpay api test key>"
RAZOR_PAY_SECRET="<your razropay api test secret key>"
# stripe
STRIPE_SECRET="<your stripe accoutn secret key>"
STRIPE_PUBLISH_KEY="<your stripe account publish key>"
STRIPE_WEBHOOK="<your stripe accoutn webhook key>"
#google auth
GOAUTH_CLIENT_ID="<your google auth client id>"
GOAUTH_CLIENT_SECRET="<your google auth secret key>"
GOAUTH_CALL_BACK_URL="<call back url that you registered on google auth>"
```
