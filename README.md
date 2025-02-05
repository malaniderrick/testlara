
**Server:** PHP, Laravel

**DataBase:** MySql

## Installation

```bash
composer install
```

Install NPM Dependencies

```bash
npm install && npm run dev
```

Create .env file

```bash
cp .env.example .env
```

Generate Application key

```bash
php artisan key:generate
```

Update .env File with Database credentials and run migration with seed.

```bash
php artisan migrate:fresh --seed
```

```bash
php artisan schedule:work

```


Login With 

```bash
Username - darshanm@yopmail.com
Password - Admin@123
```

crontab -e
* * * * * php /path-to-our-project/artisan schedule:run >> /dev/null 2>&1

php artisan schedule:work


php artisan schedule:run
php artisan queue:work
php artisan schedule:work


-------------------

API Demo Postman Collection Overview
This collection provides a set of API endpoints for managing posts. It demonstrates common actions like login, creating, updating, fetching, and deleting posts. It also includes examples for authentication with tokens and how to make requests with different HTTP methods.

Collection Information
Name: API_Demo
Postman Collection ID: cd16751b-ca79-47a1-a9d0-bfb32404286f

Endpoints Overview
Login (POST)

URL: {{url}}api/login
Description: Authenticates a user using their email and password. Returns a bearer token for subsequent requests.

{
  "email": "darshanm@yopmail.com",
  "password": "Admin@123"
}
Authentication
All endpoints except the login endpoint require Bearer token authentication. You can obtain the token by successfully calling the Login endpoint, and then use it for subsequent requests.
Request Body Format
All requests that involve creating or updating posts require JSON-formatted data, such as the title, content, and author fields.
Error Handling
The API handles common errors such as unauthorized access and resource not found, providing appropriate HTTP status codes and messages.
