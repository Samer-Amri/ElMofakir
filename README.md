# El Mofakir - Academic Journal Management System

A comprehensive Laravel-based academic journal management platform that enables publication of scholarly articles, announcements, and provides tools for researchers and professionals.

## ✨ Key Features

    📚 **Academic Journal Platform** - Complete scholarly article publication system
    📑 **Article Management** - Multi-language posts with categories, tags, and media attachments
    📢 **Announcements System** - Official journal announcements and news
    👥 **Role-Based Access** - Admin, Editor, Professional, and User roles with permissions
    📖 **Volume & Issue Management** - Organize articles by publication volumes and issues
    💾 **PDF Management** - Upload, manage, and bulk download research papers
    🔍 **Advanced Search** - Full-text search across articles and announcements
    🌐 **Multilingual Support** - Arabic and English content support
    📧 **Email Notifications** - Automated notifications for content management
    📊 **Admin Dashboard** - Comprehensive backend for content and user management
    📱 **RESTful API** - Complete API for mobile/frontend applications
    🔐 **Secure Authentication** - Laravel Passport OAuth2 implementation
    👤 **Professional Profiles** - CV uploads and researcher profile management

## 🧰 Tech Stack

    **Backend:** Laravel 8.x (PHP 7.3+)
    **Authentication:** Laravel Passport (OAuth2) + Role-based permissions (Entrust)
    **Frontend:** Blade Templates + Bootstrap 4 + Vue.js components
    **Database:** MySQL with advanced relationships
    **Search:** Laravel Scout with searchable traits
    **File Management:** Intervention Image for media processing
    **Real-time:** Laravel WebSockets + Pusher
    **Localization:** Multi-language support (Arabic/English)
    **Admin Panel:** Custom-built responsive admin interface
    **APIs:** RESTful API with resource transformers

## 📁 Project Structure

```
El_Mofakir/
│
├── app/
│   ├── Http/Controllers/
│   │   ├── Api/                    # API endpoints
│   │   ├── Backend/                # Admin panel controllers
│   │   └── Frontend/               # Public interface
│   ├── Models/                     # Eloquent models (User, Post, Category, etc.)
│   ├── Http/Resources/             # API resource transformers
│   └── Notifications/              # Email notification classes
├── resources/
│   ├── views/backend/              # Admin panel Blade templates
│   ├── lang/                       # Multi-language files (ar/en)
│   └── js/components/              # Vue.js components
├── database/
│   ├── migrations/                 # Database schema
│   └── seeders/                    # Sample data
├── routes/
│   ├── web.php                     # Web routes
│   └── api.php                     # API routes
├── public/assets/                  # Uploaded files (posts, users)
└── config/                         # Laravel configuration
```

## 🚀 Setup Instructions

### Prerequisites

-   PHP >= 7.3
-   Composer
-   Node.js & npm
-   MySQL
-   Redis (optional, for caching and queues)

### 1. Clone the Repository

```sh
git clone https://github.com/yourusername/el_mofakir.git
cd el_mofakir
```

### 2. Install Dependencies

```sh
composer install
npm install && npm run dev
```

### 3. Environment Setup

```sh
cp .env.example .env
php artisan key:generate
```

### 4. Database Configuration

Create a MySQL database named `elmofakir` and update your `.env` file:

```env
DB_DATABASE=elmofakir
DB_USERNAME=your_username
DB_PASSWORD=your_password
```

### 5. Run Migrations & Seeders

```sh
php artisan migrate --seed
```

### 6. Generate Passport Keys (for API)

```sh
php artisan passport:install
```

### 7. Start Development Server

```sh
php artisan serve
```

### 8. Optional: Start Redis & WebSocket Server

```sh
redis-server
php artisan websockets:serve
```

## 👤 Default Admin Access

-   **URL:** `localhost:8000/admin`
-   **Email:** `admin@elmofakir.test`
-   **Password:** `123123123`

## 📚 API Endpoints

The system provides a comprehensive REST API:

-   `GET /api/all_posts` - Retrieve all published articles
-   `GET /api/post/{slug}` - Get specific article details
-   `GET /api/all_announcements` - Fetch announcements
-   `GET /api/volumes` - Get publication volumes
-   `GET /api/authors` - List all authors
-   `GET /api/professionals` - Get professional researchers
-   `POST /api/contact-us` - Submit contact form

## 🌐 Multi-language Support

The platform supports both Arabic and English:

-   Dynamic content switching via `/change_locale/{locale}`
-   Separate slugs for both languages
-   Localized admin interface

## 👨‍💻 Author

**Samer Amri**  
FullStack Laravel Developer  
🔗 [LinkedIn](https://www.linkedin.com/in/samer-amri-1b1510225/)

## 📄 License

This project is open-sourced under the MIT license.
