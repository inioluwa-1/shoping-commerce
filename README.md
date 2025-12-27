# 🛒 E-Commerce Store

A modern, responsive e-commerce web application built with HTML, CSS, JavaScript, and Bootstrap. Features include product management, shopping cart functionality, user authentication, and an admin panel for managing inventory.

![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)
![Bootstrap](https://img.shields.io/badge/Bootstrap-7952B3?logo=bootstrap&logoColor=white)

## ✨ Features

### Customer Features
- 🔐 **User Authentication** - Login and registration system with validation
- 🛍️ **Product Browsing** - Browse products with search and filter functionality
- 🛒 **Shopping Cart** - Add, remove, and manage cart items
- 💳 **Checkout Process** - Complete purchases with form validation
- 👤 **User Profile** - Personalized greeting and session management
- 📱 **Responsive Design** - Mobile-friendly interface

### Admin Features
- 🔧 **Product Management** - Add, edit, and delete products
- 📊 **Dashboard** - View total products and manage inventory
- 🖼️ **Image Upload** - Add product images with preview
- 💰 **Price Management** - Set and update product pricing
- 📝 **Product Details** - Manage descriptions and specifications

## 🚀 Demo

Visit the live demo: [E-Commerce Store](#)

### Demo Credentials
**Customer Account:**
- Email: `customer@example.com`
- Password: `customer123`

**Admin Account:**
- Email: `admin@example.com`
- Password: `admin123`

## 🛠️ Technologies Used

- **Frontend:**
  - HTML5
  - CSS3
  - JavaScript (ES6+)
  - Bootstrap 5.3.3
  - Font Awesome 6.4.0

- **Data Storage:**
  - LocalStorage API (for products, cart, and user sessions)

- **Libraries:**
  - Bootstrap (UI framework)
  - Font Awesome (icons)

## 📦 Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/inioluwa-1/shoping-commerce.git
   cd shoping-commerce
   ```

2. **Open the project**
   - Simply open `login.html` in your web browser
   - Or use a local server for better experience:
     ```bash
     # Using Python
     python -m http.server 8000
     
     # Using Node.js (http-server)
     npx http-server
     ```

3. **Access the application**
   - Navigate to `http://localhost:8000/login.html` (if using local server)
   - Or open `login.html` directly in your browser

## 📁 Project Structure

```
level 2/
├── index.html          # Main store/shopping page
├── admin.html          # Admin dashboard for product management
├── login.html          # Login and registration page
├── style.css           # Custom styles and animations
└── README.md           # Project documentation
```

## 🎯 Usage

### For Customers

1. **Register/Login**
   - Open `login.html`
   - Create a new account or login with existing credentials
   - Toggle between login and signup forms

2. **Browse Products**
   - View all available products on the main store page
   - Use search to find specific products
   - Filter by category or price range

3. **Shopping Cart**
   - Click "Add to Cart" on any product
   - View cart by clicking the cart icon
   - Adjust quantities or remove items
   - Proceed to checkout

4. **Checkout**
   - Fill in shipping information
   - Complete your order

### For Admins

1. **Access Admin Panel**
   - Login with admin credentials
   - Click "Admin Panel" from the navigation

2. **Manage Products**
   - **Add Products:** Fill in the form with product details and image URL
   - **Edit Products:** Click edit icon on any product card
   - **Delete Products:** Click delete icon to remove products
   - **View Statistics:** Monitor total product count

## 🔑 Key Functionalities

### Authentication System
- User registration with validation
- Login system with session management
- Password visibility toggle
- Persistent login sessions using LocalStorage

### Product Management
- CRUD operations for products
- Image upload and preview
- Form validation
- Real-time updates

### Shopping Cart
- Add/remove items
- Update quantities
- Calculate totals
- Persist cart data across sessions
- Visual cart counter badge

### Data Persistence
All data is stored in browser's LocalStorage:
- `users` - User accounts
- `products` - Product inventory
- `cart` - Shopping cart items
- `currentUser` - Active session

## 🎨 Customization

### Changing Colors
Edit the CSS variables in `style.css`:
```css
:root {
  --primary-color: #dc3545;
  --secondary-color: #212529;
  --success-color: #28a745;
}
```

### Adding New Features
The modular JavaScript structure makes it easy to extend:
- Add new product fields in the form handlers
- Implement payment gateway integration
- Add more filter options
- Include product reviews and ratings

## 🐛 Known Issues

- Data is stored locally (not persistent across devices)
- No backend integration (client-side only)
- Image URLs must be valid external links

## 🚧 Future Enhancements

- [ ] Backend API integration
- [ ] Database for data persistence
- [ ] Payment gateway integration
- [ ] Order history and tracking
- [ ] Product reviews and ratings
- [ ] Wishlist functionality
- [ ] Email notifications
- [ ] Advanced filtering and sorting
- [ ] Multi-language support
- [ ] Dark mode toggle

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👨‍💻 Author

**Inioluwa**
- GitHub: [@inioluwa-1](https://github.com/inioluwa-1)

## 🙏 Acknowledgments

- Bootstrap for the UI framework
- Font Awesome for icons
- SQI for the learning opportunity

## 📞 Support

For support, email your-email@example.com or open an issue in the repository.

---

⭐ Star this repository if you find it helpful!

Made with ❤️ by Inioluwa
