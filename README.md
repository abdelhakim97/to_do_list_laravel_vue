# Laravel + Vue.js + JWT Todo List Application

A complete full-stack Todo List application with Laravel 9 backend, Vue.js 3 frontend, and JWT authentication.

## 🚀 Features

- ✅ User Registration & Login with JWT Authentication
- ✅ CRUD Operations for Todo Tasks
- ✅ Vue.js 3 Composition API
- ✅ Laravel 9 RESTful API
- ✅ JWT Token Management
- ✅ CORS Support
- ✅ Bootstrap 5 UI
- ✅ Responsive Design

## 📋 Prerequisites

- PHP 7.0 or higher
- Composer
- Node.js 16 or higher
- npm or yarn
- MySQL 5.7 or higher
- Git

## 🛠️ Installation Guide

### 1. Clone the Repository
```bash
git clone https://github.com/abdelhakim97/VUEJS_LARAVEL_JWT_AUTH.git
cd VUEJS_LARAVEL_JWT_AUTH
2. Backend Setup (Laravel)
bash
# Install PHP dependencies
composer install

# Create environment file
cp .env.example .env

# Generate application key
php artisan key:generate

# Configure database in .env file
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=your_database_name
DB_USERNAME=your_mysql_username
DB_PASSWORD=your_mysql_password

# Run database migrations
php artisan migrate

# Generate JWT secret key
php artisan jwt:secret

# Start Laravel development server
php artisan serve
3. Frontend Setup (Vue.js)
bash
# Install JavaScript dependencies
npm install

# Start development server
npm run dev

# Or build for production
npm run build
4. Environment Configuration
Update your .env file with these values:

env
APP_URL=http://localhost:8000
FRONTEND_URL=http://localhost:8080

BROADCAST_DRIVER=log
CACHE_DRIVER=file
QUEUE_CONNECTION=sync
SESSION_DRIVER=file

JWT_SECRET=your_generated_jwt_secret
🚀 Running the Application
Start Backend Server
bash
php artisan serve
Server runs on: http://localhost:8000

Start Frontend Development Server
bash
npm run dev
Frontend runs on: http://localhost:8080

📖 API Documentation
Authentication Endpoints
Method	Endpoint	Description
POST	/api/v1/auth/register	Register new user
POST	/api/v1/auth/login	User login
POST	/api/v1/auth/logout	User logout
GET	/api/v1/auth/user	Get current user
GET	/api/v1/auth/refresh	Refresh JWT token
User Endpoints (Protected)
Method	Endpoint	Description
GET	/api/v1/user	List all users
GET	/api/v1/user/{id}	Get specific user
🏗️ Project Structure
text
VUEJS_LARAVEL_JWT_AUTH/
├── app/
│   ├── Http/Controllers/
│   │   ├── AuthController.php     # JWT authentication
│   │   └── UserController.php     # User management
│   └── Models/
│       └── User.php              # User model
├── config/
│   ├── cors.php                  # CORS configuration
│   └── jwt.php                   # JWT settings
├── resources/
│   └── js/
│       ├── components/           # Vue components
│       ├── App.vue               # Main Vue component
│       └── bootstrap.js          # Vue initialization
├── routes/
│   └── api.php                   # API routes
└── database/
    └── migrations/               # Database migrations
⚙️ Configuration Files
CORS Configuration (config/cors.php)
php
'paths' => ['api/*'],
'allowed_methods' => ['*'],
'allowed_origins' => ['http://localhost:8080'],
'allowed_headers' => ['*'],
'exposed_headers' => ['Authorization'],
'max_age' => 0,
'supports_credentials' => false,
JWT Configuration (config/jwt.php)
JWT secret is automatically generated during installation.

🧪 Testing the Application
Open the application: http://localhost:8080

Register a new user:

Fill in name, email, and password

Confirm password

Login with credentials

Start managing your todos

🔧 Troubleshooting
Common Issues
CORS Errors: Ensure config/cors.php allows your frontend URL

JWT Errors: Run php artisan jwt:secret to generate new key

Database Errors: Check .env database configuration

Port Conflicts: Change ports in php artisan serve and npm run dev

Commands for Fixes
bash
# Clear configuration cache
php artisan config:clear

# Clear application cache
php artisan cache:clear

# Reinstall dependencies
composer install
npm install
🤝 Contributing
Fork the repository

Create a feature branch: git checkout -b feature/new-feature

Commit changes: git commit -m 'Add new feature'

Push to branch: git push origin feature/new-feature

Submit a pull request
