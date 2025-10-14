<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400" alt="Laravel Logo"></a></p>

<p align="center">
<a href="https://github.com/laravel/framework/actions"><img src="https://github.com/laravel/framework/workflows/tests/badge.svg" alt="Build Status"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/dt/laravel/framework" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/v/laravel/framework" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/l/laravel/framework" alt="License"></a>
</p>

# 🎓 API Transkrip - Academic Transcript Request System

An elegant REST API system for managing academic transcript requests, built with Laravel. This system allows students to request transcripts and administrators to process these requests efficiently.

![Laravel](https://img.shields.io/badge/Laravel-10.x-red.svg)
![PHP](https://img.shields.io/badge/PHP-^8.1-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)

## 📋 Features

- **Authentication & Authorization**
  - JWT-based authentication
  - Role-based access control (Admin & User)
  - Secure endpoint protection

- **Request Management**
  - Create transcript requests
  - Track request status
  - Queue management
  - File attachments support

- **Response Handling**
  - Admin response management
  - File response capabilities
  - Status tracking system

## 🚀 Prerequisites

Before you begin, ensure you have met the following requirements:

- PHP >= 8.1
- Composer
- MySQL/MariaDB
- Node.js & NPM (for frontend assets)
- Laravel CLI

## ⚙️ Installation

1. Clone the repository
```bash
git clone https://github.com/yourusername/api-transkrip.git
cd api-transkrip
```

2. Install dependencies
```bash
composer install
```

3. Set up environment file
```bash
cp .env.example .env
php artisan key:generate
```

4. Configure database in `.env`
```
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=your_database
DB_USERNAME=your_username
DB_PASSWORD=your_password
```

5. Run migrations and seeders
```bash
php artisan migrate:fresh --seed
```

## 🔑 Default Users

After running seeders, you can use these default accounts:

- Admin Account
  - Username: admin
  - Password: password

- Test User Accounts
  - Username: user1 / user2
  - Password: password

## 🛣️ API Routes

### Authentication
- `POST /api/login` - Authenticate user
- `POST /api/logout` - Logout user

### Requests
- `GET /api/requests` - List all requests (Admin only)
- `POST /api/requests` - Create new request
- `GET /api/requests/{id}` - Get specific request
- `PUT /api/requests/{id}` - Update request (Admin only)
- `DELETE /api/requests/{id}` - Delete request (Admin only)

### Responses
- `GET /api/responses` - List all responses (Admin only)
- `POST /api/responses` - Create response (Admin only)
- `GET /api/responses/{id}` - Get specific response
- `PUT /api/responses/{id}` - Update response (Admin only)
- `DELETE /api/responses/{id}` - Delete response (Admin only)

## 🔒 Security

- All endpoints (except login) require authentication
- Role-based access control implementation
- Request validation and sanitization
- CORS protection
- Rate limiting

## 🧪 Testing

Run the test suite:
```bash
php artisan test
```

## 📝 License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.

## 👥 Contributors

- [Your Name](https://github.com/yourusername)

## 📮 Support

For support, email your-email@example.com or create an issue in this repository.

## About Laravel

Laravel is a web application framework with expressive, elegant syntax. We believe development must be an enjoyable and creative experience to be truly fulfilling. Laravel takes the pain out of development by easing common tasks used in many web projects, such as:

- [Simple, fast routing engine](https://laravel.com/docs/routing).
- [Powerful dependency injection container](https://laravel.com/docs/container).
- Multiple back-ends for [session](https://laravel.com/docs/session) and [cache](https://laravel.com/docs/cache) storage.
- Expressive, intuitive [database ORM](https://laravel.com/docs/eloquent).
- Database agnostic [schema migrations](https://laravel.com/docs/migrations).
- [Robust background job processing](https://laravel.com/docs/queues).
- [Real-time event broadcasting](https://laravel.com/docs/broadcasting).

Laravel is accessible, powerful, and provides tools required for large, robust applications.

## Learning Laravel

Laravel has the most extensive and thorough [documentation](https://laravel.com/docs) and video tutorial library of all modern web application frameworks, making it a breeze to get started with the framework.

You may also try the [Laravel Bootcamp](https://bootcamp.laravel.com), where you will be guided through building a modern Laravel application from scratch.

If you don't feel like reading, [Laracasts](https://laracasts.com) can help. Laracasts contains thousands of video tutorials on a range of topics including Laravel, modern PHP, unit testing, and JavaScript. Boost your skills by digging into our comprehensive video library.

## Laravel Sponsors

We would like to extend our thanks to the following sponsors for funding Laravel development. If you are interested in becoming a sponsor, please visit the [Laravel Partners program](https://partners.laravel.com).

### Premium Partners

- **[Vehikl](https://vehikl.com)**
- **[Tighten Co.](https://tighten.co)**
- **[Kirschbaum Development Group](https://kirschbaumdevelopment.com)**
- **[64 Robots](https://64robots.com)**
- **[Curotec](https://www.curotec.com/services/technologies/laravel)**
- **[DevSquad](https://devsquad.com/hire-laravel-developers)**
- **[Redberry](https://redberry.international/laravel-development)**
- **[Active Logic](https://activelogic.com)**

## Contributing

Thank you for considering contributing to the Laravel framework! The contribution guide can be found in the [Laravel documentation](https://laravel.com/docs/contributions).

## Code of Conduct

In order to ensure that the Laravel community is welcoming to all, please review and abide by the [Code of Conduct](https://laravel.com/docs/contributions#code-of-conduct).

## Security Vulnerabilities

Jika Anda menemukan kerentanan keamanan dalam aplikasi ini, silakan kirim e-mail ke taylor@laravel.com. Semua kerentanan keamanan akan segera ditangani.

## License

The Laravel framework is open-sourced software licensed under the [MIT license](https://opensource.org/licenses/MIT).
