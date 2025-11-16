# 🛒 Veridian Commerce

<div align="center">

![Next.js](https://img.shields.io/badge/Next.js-15.5-black?style=for-the-badge&logo=next.js)
![React](https://img.shields.io/badge/React-18.3-61DAFB?style=for-the-badge&logo=react)
![Node.js](https://img.shields.io/badge/Node.js-Express-339933?style=for-the-badge&logo=node.js)
![TypeScript](https://img.shields.io/badge/TypeScript-5.9-3178C6?style=for-the-badge&logo=typescript)
![MySQL](https://img.shields.io/badge/MySQL-8.0-4479A1?style=for-the-badge&logo=mysql)
![Prisma](https://img.shields.io/badge/Prisma-6.16-2D3748?style=for-the-badge&logo=prisma)
![Tailwind CSS](https://img.shields.io/badge/Tailwind-3.3-38B2AC?style=for-the-badge&logo=tailwind-css)

**A fully featured, production-ready electronics eCommerce platform with comprehensive admin dashboard**

[Features](#-features) • [Installation](#-installation) • [Usage](#-usage) • [Documentation](#-documentation)

</div>

---

## 📖 About

**Veridian Commerce** is a modern, full-stack e-commerce platform specifically designed for electronics retail. Built as a complete software engineering case study, this project demonstrates enterprise-level development practices with comprehensive requirements analysis, system design, and 350+ manually documented test cases.

The platform provides a seamless shopping experience for customers while offering powerful administrative tools for managing products, orders, users, and inventory through an intuitive dashboard interface.

---

## ✨ Features

### 🛍️ Customer Features
- **Product Catalog**: Browse and search through a comprehensive electronics catalog
- **Advanced Filtering**: Filter products by category, price range, and availability
- **Product Details**: Detailed product pages with multiple images, descriptions, and specifications
- **Shopping Cart**: Add to cart, quantity management, and cart persistence
- **Wishlist**: Save favorite products for later
- **Order Management**: Track order status and view order history
- **User Authentication**: Secure login and registration with NextAuth
- **Real-time Notifications**: Get notified about order updates, promotions, and system alerts
- **Responsive Design**: Fully responsive UI that works on all devices

### 👨‍💼 Admin Dashboard Features
- **Product Management**: Create, edit, delete, and bulk upload products via CSV
- **Category Management**: Organize products with hierarchical categories
- **Order Management**: View, process, and update order statuses
- **User Management**: Manage customer accounts and roles
- **Merchant Management**: Handle multiple merchants and their products
- **Bulk Upload**: Import hundreds of products at once with CSV upload
- **Upload History**: Track all bulk uploads with detailed statistics
- **Analytics Dashboard**: View sales statistics and product performance
- **Advanced Search**: Powerful search functionality with filters

### 🔒 Security & Performance
- **Rate Limiting**: Protection against abuse with configurable rate limits
- **Request Logging**: Comprehensive logging for security and debugging
- **Input Sanitization**: XSS and injection protection
- **Session Management**: Secure session handling with timeout
- **CSRF Protection**: Built-in CSRF protection
- **Error Handling**: Graceful error handling with user-friendly messages

---

## 🛠️ Tech Stack

### Frontend
- **Next.js 15.5** - React framework with App Router
- **React 18.3** - UI library
- **TypeScript** - Type safety
- **Tailwind CSS** - Utility-first CSS framework
- **DaisyUI** - Component library
- **Zustand** - State management
- **NextAuth** - Authentication
- **React Hot Toast** - Notifications
- **React Slick** - Carousel components

### Backend
- **Node.js** - Runtime environment
- **Express.js** - Web framework
- **Prisma** - ORM for database management
- **MySQL** - Relational database
- **Winston** - Logging
- **Express Rate Limit** - Rate limiting middleware
- **Bcrypt** - Password hashing

### Development Tools
- **Prisma Studio** - Database GUI
- **ESLint** - Code linting
- **TypeScript** - Type checking

---

## 📋 Prerequisites

Before you begin, ensure you have the following installed:

- **Node.js** (v18 or higher)
- **npm** or **yarn**
- **MySQL** (v8.0 or higher)
- **Git**

---

## 🚀 Installation

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/veridian-commerce.git
cd veridian-commerce
```

### 2. Install Frontend Dependencies

```bash
npm install
```

### 3. Install Backend Dependencies

```bash
cd server
npm install
cd ..
```

### 4. Set Up Environment Variables

Create a `.env` file in the root directory:

```env
# Database
DATABASE_URL="mysql://username:password@localhost:3306/veridian_commerce"

# Next.js
NEXT_PUBLIC_API_BASE_URL="http://localhost:3001"
NEXTAUTH_URL="http://localhost:3000"
NEXTAUTH_SECRET="your-secret-key-here"

# Optional: Add other environment variables as needed
```

**Note**: Replace `username`, `password`, and `veridian_commerce` with your MySQL credentials and database name.

### 5. Set Up the Database

```bash
# Generate Prisma Client
npm run db:generate

# Push the schema to your database
npm run db:push

# (Optional) Open Prisma Studio to view your database
npm run db:studio
```

### 6. Create Admin User

```bash
cd server
node createAdminUser.js
```

Follow the prompts to create your first admin user.

---

## 🎯 Usage

### Development Mode

1. **Start the Backend Server** (Terminal 1):

```bash
cd server
npm start
```

The backend API will run on `http://localhost:3001`

2. **Start the Frontend Development Server** (Terminal 2):

```bash
npm run dev
```

The frontend will run on `http://localhost:3000`

### Production Build

1. **Build the Frontend**:

```bash
npm run build
```

2. **Start Production Server**:

```bash
npm start
```

### Access the Application

- **Customer Frontend**: http://localhost:3000
- **Admin Dashboard**: http://localhost:3000/admin
- **API Endpoints**: http://localhost:3001/api
- **Prisma Studio**: Run `npm run db:studio` and access at http://localhost:5555

---

## 📁 Project Structure

```
veridian-commerce/
├── app/                      # Next.js app directory
│   ├── (dashboard)/         # Admin dashboard routes
│   │   └── admin/           # Admin pages
│   ├── api/                 # API routes
│   ├── actions/             # Server actions
│   └── ...                  # Other app routes
├── components/              # React components
│   └── modules/            # Feature modules
├── server/                  # Backend Express server
│   ├── controllers/        # Route controllers
│   ├── routes/             # API routes
│   ├── middleware/         # Express middleware
│   ├── services/           # Business logic
│   ├── prisma/             # Prisma schema
│   └── app.js              # Express app entry
├── lib/                    # Utility libraries
├── hooks/                  # Custom React hooks
├── types/                  # TypeScript type definitions
├── utils/                  # Utility functions
└── public/                 # Static assets
```

---

## 📚 Documentation

### Bulk Upload Guide

The platform supports bulk product uploads via CSV. See the detailed guides:

- **[Bulk Upload Guide](./BULK-UPLOAD-GUIDE.md)** - Complete guide to bulk uploading products
- **[Bulk Upload Quick Reference](./BULK-UPLOAD-QUICK-REFERENCE.md)** - Quick reference for bulk upload operations
- **[Bulk Upload Explanation](./BULK-UPLOAD-EXPLANATION.md)** - Detailed explanation of bulk upload functionality

### API Documentation

The backend API provides endpoints for:

- **Products**: `/api/products`
- **Categories**: `/api/category`
- **Orders**: `/api/customer_orders`
- **Users**: `/api/users`
- **Search**: `/api/search`
- **Bulk Upload**: `/api/bulk-upload`
- **Notifications**: `/api/notifications`
- **Merchants**: `/api/merchant`

### Database Schema

The database schema is defined in `server/prisma/schema.prisma`. Key models include:

- `Product` - Product catalog
- `Category` - Product categories
- `User` - User accounts
- `Customer_order` - Customer orders
- `Merchant` - Merchant information
- `Notification` - User notifications
- `Wishlist` - User wishlists
- `bulk_upload_batch` - Bulk upload tracking

---

## 🧪 Testing

This project includes 350+ manually documented test cases covering:

- User authentication and authorization
- Product CRUD operations
- Order processing
- Bulk upload functionality
- Search and filtering
- Admin dashboard features
- API endpoint validation

---

## 🔧 Available Scripts

### Frontend Scripts

```bash
npm run dev          # Start development server
npm run build        # Build for production
npm start            # Start production server
npm run lint         # Run ESLint
npm run db:generate  # Generate Prisma Client
npm run db:push      # Push schema to database
npm run db:studio    # Open Prisma Studio
```

### Backend Scripts

```bash
cd server
npm start            # Start Express server
npm run logs         # View all logs
npm run logs:access  # View access logs
npm run logs:error   # View error logs
npm run logs:security # View security logs
npm run db:backup    # Backup database
```

---

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request. For major changes, please open an issue first to discuss what you would like to change.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](./LICENSE) file for details.

---

## 👤 Author

**Your Name**

- GitHub: [@yourusername](https://github.com/yourusername)
- Email: your.email@example.com

---

## 🙏 Acknowledgments

- Built as a comprehensive software engineering case study
- Includes full requirements analysis and system design
- 350+ manually documented test cases
- Production-ready codebase with best practices

---

<div align="center">

**⭐ If you find this project helpful, please consider giving it a star! ⭐**

Made with ❤️ using Next.js, React, and Node.js

</div>
