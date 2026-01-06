# Laravel GiftShop Ecommerce

A full-featured e-commerce gift shop built with Laravel 12, featuring product management, shopping cart, order processing, and Stripe payment integration.

## Features

### Customer Features
- **Product Catalog**: Browse and search products with categories
- **Shopping Cart**: Add/remove items with real-time cart count
- **Order Management**: Place orders and track order history
- **User Authentication**: Registration, login, and profile management
- **Stripe Payments**: Secure online payment processing
- **Responsive Design**: Mobile-friendly interface using Tailwind CSS

### Admin Features
- **Dashboard**: Overview of users, products, orders, and deliveries
- **Product Management**: Add, edit, and delete products
- **Category Management**: Organize products by categories
- **Order Management**: View and manage customer orders
- **User Management**: Monitor registered users

### Technical Features
- **Laravel 12**: Latest Laravel framework with modern features
- **Tailwind CSS**: Utility-first CSS framework for styling
- **Alpine.js**: Lightweight JavaScript for interactivity
- **Stripe Integration**: Secure payment processing
- **PDF Generation**: Invoice generation using DOMPDF
- **Flash Notifications**: User-friendly toast notifications
- **Queue System**: Background job processing
- **Testing**: Pest PHP for unit and feature tests

## Installation

### Prerequisites
- PHP 8.2 or higher
- Composer
- Node.js and NPM
- MySQL or PostgreSQL database
- Stripe account (for payments)

### Setup Instructions

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd Laravel-GiftShop-Ecommerce
   ```

2. **Install dependencies**
   ```bash
   composer install
   npm install
   ```

3. **Environment setup**
   ```bash
   cp .env.example .env
   php artisan key:generate
   ```

4. **Configure database**
   Edit your `.env` file with your database credentials:
   ```env
   DB_CONNECTION=mysql
   DB_HOST=127.0.0.1
   DB_PORT=3306
   DB_DATABASE=your_database_name
   DB_USERNAME=your_username
   DB_PASSWORD=your_password
   ```

5. **Configure Stripe**
   Add your Stripe keys to `.env`:
   ```env
   STRIPE_SECRET=your_stripe_secret_key
   STRIPE_PUBLISHABLE_KEY=your_stripe_publishable_key
   ```

6. **Run migrations and seeders**
   ```bash
   php artisan migrate
   php artisan db:seed
   ```

7. **Build frontend assets**
   ```bash
   npm run build
   ```

8. **Start the development server**
   ```bash
   php artisan serve
   ```

## Available Scripts

### Composer Scripts
- `composer setup` - Complete project setup (install, migrate, build)
- `composer dev` - Start development server with queue and logs
- `composer test` - Run the test suite

### NPM Scripts
- `npm run dev` - Start Vite development server
- `npm run build` - Build production assets

## Database Structure

### Core Tables
- **users**: User authentication and profiles
- **categories**: Product categorization
- **products**: Product inventory and details
- **carts**: Shopping cart items
- **orders**: Customer orders and payment status

## Project Structure

```
app/
├── Http/Controllers/
│   ├── HomeController.php         # Main application logic
│   ├── AdminController.php        # Admin panel functionality
│   └── Auth/                      # Authentication controllers
├── Models/
│   ├── User.php                   # User model
│   ├── Product.php                # Product model
│   ├── Category.php               # Category model
│   ├── Cart.php                   # Shopping cart model
│   └── Order.php                  # Order model
└── View/Components/
    ├── AppLayout.php              # Main app layout
    └── GuestLayout.php            # Guest layout

resources/views/
├── home/                          # Customer-facing pages
├── admin/                         # Admin panel pages
└── auth/                          # Authentication pages
```

## Usage

### For Customers
1. Register an account or login as guest
2. Browse products in the shop
3. Add items to cart
4. Proceed to checkout
5. Choose payment method (Stripe or manual)
6. Track orders in your dashboard

### For Admins
1. Login with admin credentials
2. Access admin dashboard
3. Manage products and categories
4. View and process orders
5. Monitor user activity

## Testing

Run the test suite using Pest PHP:
```bash
php artisan test
```

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Run tests to ensure everything works
5. Submit a pull request

## Security

- Uses Laravel's built-in CSRF protection
- Input validation and sanitization
- Secure password hashing
- Environment-based configuration
- Stripe handles payment security

## License

This project is open-sourced software licensed under the MIT license.

## Support

For support and questions, please open an issue in the repository.

---

**Built with ❤️ using Laravel 12**