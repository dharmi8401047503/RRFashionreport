
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>RR Fashion - Richa & Rudri Fashion</title>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
    <style>
        body {
            box-sizing: border-box;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Poppins', sans-serif;
            line-height: 1.6;
            color: #333;
            background-color: #F7F6F3;
        }

        /* Navigation */
        .navbar {
            background: linear-gradient(135deg, #FADCD9 0%, #EAF3F9 100%);
            padding: 1rem 0;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        .nav-container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
        }

        .logo {
            font-size: 2rem;
            font-weight: 700;
            color: #2c3e50;
            text-decoration: none;
            background: linear-gradient(45deg, #e74c3c, #3498db);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 2rem;
            align-items: center;
            flex-wrap: wrap;
        }

        .nav-links a {
            text-decoration: none;
            color: #2c3e50;
            font-weight: 500;
            transition: color 0.3s ease;
            position: relative;
        }

        .nav-links a:hover {
            color: #e74c3c;
        }

        .nav-links a::after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            bottom: -5px;
            left: 0;
            background-color: #e74c3c;
            transition: width 0.3s ease;
        }

        .nav-links a:hover::after {
            width: 100%;
        }

        .search-bar {
            display: flex;
            align-items: center;
            background: white;
            border-radius: 25px;
            padding: 0.5rem 1rem;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
            margin: 0 1rem;
        }

        .search-bar input {
            border: none;
            outline: none;
            padding: 0.5rem;
            font-size: 1rem;
            width: 200px;
        }

        .search-bar button {
            background: none;
            border: none;
            color: #666;
            cursor: pointer;
            font-size: 1.1rem;
        }

        .cart-icon {
            position: relative;
            font-size: 1.5rem;
            color: #2c3e50;
            cursor: pointer;
        }

        .cart-count {
            position: absolute;
            top: -8px;
            right: -8px;
            background: #e74c3c;
            color: white;
            border-radius: 50%;
            width: 20px;
            height: 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 0.8rem;
            font-weight: bold;
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(135deg, #FADCD9 0%, #EAF3F9 50%, #F7F6F3 100%);
            padding: 4rem 0;
            text-align: center;
        }

        .hero-content {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
        }

        .hero h1 {
            font-size: 3.5rem;
            font-weight: 700;
            margin-bottom: 1rem;
            background: linear-gradient(45deg, #2c3e50, #e74c3c);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .hero p {
            font-size: 1.3rem;
            color: #666;
            margin-bottom: 2rem;
        }

        .cta-button {
            display: inline-block;
            background: linear-gradient(45deg, #e74c3c, #c0392b);
            color: white;
            padding: 1rem 2rem;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 600;
            font-size: 1.1rem;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            box-shadow: 0 4px 15px rgba(231, 76, 60, 0.3);
        }

        .cta-button:hover {
            transform: translateY(-2px);
            box-shadow: 0 6px 20px rgba(231, 76, 60, 0.4);
        }

        /* Shop by Season */
        .shop-by-season {
            padding: 4rem 0;
            background: white;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
        }

        .section-title {
            text-align: center;
            font-size: 2.5rem;
            font-weight: 600;
            margin-bottom: 3rem;
            color: #2c3e50;
        }

        .season-cards {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-bottom: 3rem;
        }

        .season-card {
            background: linear-gradient(135deg, #FADCD9 0%, #EAF3F9 100%);
            border-radius: 20px;
            padding: 2rem;
            text-align: center;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            cursor: pointer;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }

        .season-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0,0,0,0.15);
        }

        .season-icon {
            font-size: 4rem;
            margin-bottom: 1rem;
        }

        .summer-icon {
            color: #f39c12;
        }

        .winter-icon {
            color: #3498db;
        }

        .season-card h3 {
            font-size: 1.8rem;
            font-weight: 600;
            margin-bottom: 1rem;
            color: #2c3e50;
        }

        .season-card p {
            color: #666;
            margin-bottom: 1.5rem;
        }

        .season-button {
            background: linear-gradient(45deg, #3498db, #2980b9);
            color: white;
            padding: 0.8rem 1.5rem;
            border: none;
            border-radius: 25px;
            font-weight: 600;
            cursor: pointer;
            transition: transform 0.3s ease;
        }

        .season-button:hover {
            transform: scale(1.05);
        }

        /* Featured Products */
        .featured-products {
            padding: 4rem 0;
            background: #F7F6F3;
        }

        .products-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2rem;
        }

        .product-card {
            background: white;
            border-radius: 20px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            cursor: pointer;
        }

        .product-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0,0,0,0.15);
        }

        .product-image {
            width: 100%;
            height: 250px;
            background: linear-gradient(45deg, #FADCD9, #EAF3F9);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 4rem;
            color: #666;
            position: relative;
        }

        .discount-badge {
            position: absolute;
            top: 10px;
            right: 10px;
            background: #e74c3c;
            color: white;
            padding: 0.3rem 0.8rem;
            border-radius: 15px;
            font-size: 0.8rem;
            font-weight: 600;
        }

        .product-info {
            padding: 1.5rem;
        }

        .product-title {
            font-size: 1.2rem;
            font-weight: 600;
            margin-bottom: 0.5rem;
            color: #2c3e50;
        }

        .product-price {
            display: flex;
            align-items: center;
            gap: 0.5rem;
            margin-bottom: 1rem;
        }

        .current-price {
            font-size: 1.3rem;
            font-weight: 700;
            color: #e74c3c;
        }

        .original-price {
            font-size: 1rem;
            color: #999;
            text-decoration: line-through;
        }

        .add-to-cart {
            width: 100%;
            background: linear-gradient(45deg, #27ae60, #2ecc71);
            color: white;
            border: none;
            padding: 0.8rem;
            border-radius: 10px;
            font-weight: 600;
            cursor: pointer;
            transition: transform 0.3s ease;
        }

        .add-to-cart:hover {
            transform: scale(1.02);
        }

        /* Footer */
        .footer {
            background: linear-gradient(135deg, #2c3e50 0%, #34495e 100%);
            color: white;
            padding: 3rem 0 1rem;
        }

        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-bottom: 2rem;
        }

        .footer-section h3 {
            font-size: 1.3rem;
            font-weight: 600;
            margin-bottom: 1rem;
            color: #FADCD9;
        }

        .footer-section ul {
            list-style: none;
        }

        .footer-section ul li {
            margin-bottom: 0.5rem;
        }

        .footer-section ul li a {
            color: #bdc3c7;
            text-decoration: none;
            transition: color 0.3s ease;
        }

        .footer-section ul li a:hover {
            color: #FADCD9;
        }

        .social-icons {
            display: flex;
            gap: 1rem;
            margin-top: 1rem;
        }

        .social-icons a {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            background: rgba(255,255,255,0.1);
            border-radius: 50%;
            color: white;
            text-decoration: none;
            transition: background 0.3s ease;
        }

        .social-icons a:hover {
            background: #FADCD9;
            color: #2c3e50;
        }

        .footer-bottom {
            text-align: center;
            padding-top: 2rem;
            border-top: 1px solid #34495e;
            color: #bdc3c7;
        }

        /* Mobile Menu */
        .mobile-menu-toggle {
            display: none;
            background: none;
            border: none;
            font-size: 1.5rem;
            color: #2c3e50;
            cursor: pointer;
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .nav-container {
                flex-direction: column;
                gap: 1rem;
            }

            .mobile-menu-toggle {
                display: block;
                position: absolute;
                right: 2rem;
                top: 1rem;
            }

            .nav-links {
                display: none;
                width: 100%;
                flex-direction: column;
                gap: 1rem;
                margin-top: 1rem;
            }

            .nav-links.active {
                display: flex;
            }

            .search-bar {
                margin: 0;
                width: 100%;
                max-width: 300px;
            }

            .search-bar input {
                width: 100%;
            }

            .hero h1 {
                font-size: 2.5rem;
            }

            .hero p {
                font-size: 1.1rem;
            }

            .season-cards {
                grid-template-columns: 1fr;
            }

            .products-grid {
                grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            }
        }

        /* Cart Sidebar */
        .cart-sidebar {
            position: fixed;
            right: -400px;
            top: 0;
            width: 400px;
            height: 100%;
            background: white;
            box-shadow: -5px 0 15px rgba(0,0,0,0.1);
            transition: right 0.3s ease;
            z-index: 2000;
            overflow-y: auto;
        }

        .cart-sidebar.active {
            right: 0;
        }

        .cart-header {
            padding: 2rem;
            border-bottom: 1px solid #eee;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .cart-header h3 {
            font-size: 1.5rem;
            color: #2c3e50;
        }

        .close-cart {
            background: none;
            border: none;
            font-size: 1.5rem;
            cursor: pointer;
            color: #666;
        }

        .cart-items {
            padding: 1rem;
        }

        .cart-item {
            display: flex;
            align-items: center;
            gap: 1rem;
            padding: 1rem;
            border-bottom: 1px solid #eee;
        }

        .cart-item-image {
            width: 60px;
            height: 60px;
            background: #FADCD9;
            border-radius: 10px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.5rem;
        }

        .cart-item-info {
            flex: 1;
        }

        .cart-item-title {
            font-weight: 600;
            margin-bottom: 0.5rem;
        }

        .cart-item-price {
            color: #e74c3c;
            font-weight: 600;
        }

        .quantity-controls {
            display: flex;
            align-items: center;
            gap: 0.5rem;
            margin-top: 0.5rem;
        }

        .quantity-btn {
            width: 30px;
            height: 30px;
            border: 1px solid #ddd;
            background: white;
            border-radius: 5px;
            cursor: pointer;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .quantity {
            padding: 0.3rem 0.8rem;
            border: 1px solid #ddd;
            border-radius: 5px;
            text-align: center;
            width: 50px;
        }

        .cart-total {
            padding: 2rem;
            border-top: 2px solid #eee;
            background: #f8f9fa;
        }

        .total-amount {
            font-size: 1.5rem;
            font-weight: 700;
            color: #2c3e50;
            margin-bottom: 1rem;
        }

        .checkout-btn {
            width: 100%;
            background: linear-gradient(45deg, #e74c3c, #c0392b);
            color: white;
            border: none;
            padding: 1rem;
            border-radius: 10px;
            font-weight: 600;
            font-size: 1.1rem;
            cursor: pointer;
            transition: transform 0.3s ease;
        }

        .checkout-btn:hover {
            transform: scale(1.02);
        }

        .overlay {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0,0,0,0.5);
            z-index: 1500;
            display: none;
        }

        .overlay.active {
            display: block;
        }

        @media (max-width: 480px) {
            .cart-sidebar {
                width: 100%;
                right: -100%;
            }
        }

        /* About Section Styles */
        .about-section {
            padding: 4rem 0;
            background: linear-gradient(135deg, #F7F6F3 0%, #EAF3F9 100%);
        }

        .about-content {
            max-width: 1000px;
            margin: 0 auto;
        }

        .about-hero {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 3rem;
            align-items: center;
            margin-bottom: 4rem;
        }

        .about-text h3 {
            font-size: 2rem;
            color: #2c3e50;
            margin-bottom: 1.5rem;
            font-weight: 600;
        }

        .about-text p {
            font-size: 1.1rem;
            line-height: 1.8;
            color: #666;
        }

        .founder-cards {
            display: flex;
            gap: 1.5rem;
            justify-content: center;
        }

        .founder-card {
            background: white;
            padding: 2rem;
            border-radius: 20px;
            text-align: center;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            transition: transform 0.3s ease;
        }

        .founder-card:hover {
            transform: translateY(-5px);
        }

        .founder-avatar {
            font-size: 3rem;
            margin-bottom: 1rem;
        }

        .founder-card h4 {
            font-size: 1.3rem;
            color: #2c3e50;
            margin-bottom: 0.5rem;
        }

        .founder-card p {
            color: #666;
            font-size: 0.9rem;
        }

        .mission-vision {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 2rem;
            margin-bottom: 4rem;
        }

        .mission-card, .vision-card {
            background: white;
            padding: 2.5rem;
            border-radius: 20px;
            text-align: center;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }

        .card-icon {
            font-size: 3rem;
            margin-bottom: 1.5rem;
        }

        .mission-card h4, .vision-card h4 {
            font-size: 1.5rem;
            color: #2c3e50;
            margin-bottom: 1rem;
        }

        .mission-card p, .vision-card p {
            color: #666;
            line-height: 1.6;
        }

        .values-section {
            margin-bottom: 4rem;
        }

        .values-section h3 {
            text-align: center;
            font-size: 2rem;
            color: #2c3e50;
            margin-bottom: 2rem;
        }

        .values-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
            gap: 2rem;
        }

        .value-item {
            background: white;
            padding: 2rem;
            border-radius: 15px;
            text-align: center;
            box-shadow: 0 3px 10px rgba(0,0,0,0.1);
            transition: transform 0.3s ease;
        }

        .value-item:hover {
            transform: translateY(-3px);
        }

        .value-icon {
            font-size: 2.5rem;
            margin-bottom: 1rem;
        }

        .value-item h5 {
            font-size: 1.2rem;
            color: #2c3e50;
            margin-bottom: 0.8rem;
        }

        .value-item p {
            color: #666;
            font-size: 0.9rem;
            line-height: 1.5;
        }

        .stats-section h3 {
            text-align: center;
            font-size: 2rem;
            color: #2c3e50;
            margin-bottom: 2rem;
        }

        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 2rem;
        }

        .stat-item {
            background: linear-gradient(45deg, #e74c3c, #c0392b);
            color: white;
            padding: 2rem;
            border-radius: 15px;
            text-align: center;
            box-shadow: 0 5px 15px rgba(231, 76, 60, 0.3);
        }

        .stat-number {
            font-size: 2.5rem;
            font-weight: 700;
            margin-bottom: 0.5rem;
        }

        .stat-label {
            font-size: 1rem;
            opacity: 0.9;
        }

        /* Login Section Styles */
        .login-section {
            padding: 4rem 0;
            background: linear-gradient(135deg, #FADCD9 0%, #EAF3F9 100%);
            min-height: 80vh;
            display: flex;
            align-items: center;
        }

        .auth-container {
            max-width: 500px;
            margin: 0 auto;
            background: white;
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            overflow: hidden;
        }

        .auth-tabs {
            display: flex;
            background: #f8f9fa;
        }

        .auth-tab {
            flex: 1;
            padding: 1rem;
            border: none;
            background: transparent;
            font-size: 1.1rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            color: #666;
        }

        .auth-tab.active {
            background: white;
            color: #2c3e50;
            box-shadow: 0 -2px 10px rgba(0,0,0,0.1);
        }

        .auth-form {
            padding: 3rem;
        }

        .auth-form h2 {
            font-size: 2rem;
            color: #2c3e50;
            margin-bottom: 0.5rem;
            text-align: center;
        }

        .auth-form > p {
            text-align: center;
            color: #666;
            margin-bottom: 2rem;
        }

        .form-row {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 1rem;
        }

        .form-group {
            margin-bottom: 1.5rem;
        }

        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            color: #2c3e50;
            font-weight: 500;
        }

        .form-group input {
            width: 100%;
            padding: 0.8rem 1rem;
            border: 2px solid #e1e8ed;
            border-radius: 10px;
            font-size: 1rem;
            transition: border-color 0.3s ease;
            background: #f8f9fa;
        }

        .form-group input:focus {
            outline: none;
            border-color: #3498db;
            background: white;
        }

        .form-options {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 2rem;
        }

        .checkbox-label {
            display: flex;
            align-items: center;
            cursor: pointer;
            font-size: 0.9rem;
            color: #666;
        }

        .checkbox-label input[type="checkbox"] {
            margin-right: 0.5rem;
        }

        .forgot-password {
            color: #3498db;
            text-decoration: none;
            font-size: 0.9rem;
        }

        .forgot-password:hover {
            text-decoration: underline;
        }

        .auth-button {
            width: 100%;
            background: linear-gradient(45deg, #3498db, #2980b9);
            color: white;
            border: none;
            padding: 1rem;
            border-radius: 10px;
            font-size: 1.1rem;
            font-weight: 600;
            cursor: pointer;
            transition: transform 0.3s ease;
            margin-bottom: 2rem;
        }

        .auth-button:hover {
            transform: translateY(-2px);
        }

        .social-login {
            text-align: center;
            border-top: 1px solid #eee;
            padding-top: 2rem;
        }

        .social-login p {
            color: #666;
            margin-bottom: 1rem;
        }

        .social-buttons {
            display: flex;
            gap: 1rem;
        }

        .social-btn {
            flex: 1;
            padding: 0.8rem;
            border: 2px solid #e1e8ed;
            background: white;
            border-radius: 10px;
            cursor: pointer;
            transition: all 0.3s ease;
            font-weight: 500;
        }

        .social-btn.google:hover {
            border-color: #db4437;
            color: #db4437;
        }

        .social-btn.facebook:hover {
            border-color: #4267B2;
            color: #4267B2;
        }

        /* Responsive styles for About and Login */
        @media (max-width: 768px) {
            .about-hero {
                grid-template-columns: 1fr;
                text-align: center;
            }

            .founder-cards {
                flex-direction: column;
                align-items: center;
            }

            .mission-vision {
                grid-template-columns: 1fr;
            }

            .values-grid {
                grid-template-columns: 1fr;
            }

            .stats-grid {
                grid-template-columns: repeat(2, 1fr);
            }

            .auth-container {
                margin: 0 1rem;
            }

            .auth-form {
                padding: 2rem;
            }

            .form-row {
                grid-template-columns: 1fr;
            }

            .social-buttons {
                flex-direction: column;
            }
        }
    </style>
</head>
<body>
    <!-- Navigation -->
    <nav class="navbar">
        <div class="nav-container">
            <a href="#" class="logo">RR Fashion</a>
            
            <button class="mobile-menu-toggle" onclick="toggleMobileMenu()">
                <i class="fas fa-bars"></i>
            </button>
            
            <div class="search-bar">
                <input type="text" placeholder="Search products..." id="searchInput">
                <button onclick="searchProducts()">
                    <i class="fas fa-search"></i>
                </button>
            </div>
            
            <ul class="nav-links" id="navLinks">
                <li><a href="#" onclick="showHome()">Home</a></li>
                <li><a href="#categories">Categories</a></li>
                <li><a href="#" onclick="showAbout()">About</a></li>
                <li><a href="#contact">Contact</a></li>
                <li><a href="#" onclick="showLogin()">Login</a></li>
            </ul>
            
            <div class="cart-icon" onclick="toggleCart()">
                <i class="fas fa-shopping-cart"></i>
                <span class="cart-count" id="cartCount">0</span>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="hero-content">
            <h1>Shop the Latest Trends</h1>
            <p>For Every Season - Discover Fashion for Boys & Girls</p>
            <a href="#categories" class="cta-button">Start Shopping</a>
        </div>
    </section>

    <!-- Shop by Season -->
    <section class="shop-by-season" id="categories">
        <div class="container">
            <h2 class="section-title">Shop by Season</h2>
            <div class="season-cards">
                <div class="season-card" onclick="showSeason('summer')">
                    <div class="season-icon summer-icon">
                        <i class="fas fa-sun"></i>
                    </div>
                    <h3>Summer Collection</h3>
                    <p>Light, comfortable clothing perfect for warm weather</p>
                    <button class="season-button">Shop Summer</button>
                </div>
                
                <div class="season-card" onclick="showSeason('winter')">
                    <div class="season-icon winter-icon">
                        <i class="fas fa-snowflake"></i>
                    </div>
                    <h3>Winter Collection</h3>
                    <p>Cozy, warm clothing to keep you comfortable</p>
                    <button class="season-button">Shop Winter</button>
                </div>
            </div>
        </div>
    </section>

    <!-- Featured Products -->
    <section class="featured-products">
        <div class="container">
            <h2 class="section-title">Featured Products</h2>
            <div class="products-grid" id="productsGrid">
                <!-- Products will be loaded here -->
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section class="about-section" id="about" style="display: none;">
        <div class="container">
            <h2 class="section-title">About RR Fashion</h2>
            
            <div class="about-content">
                <div class="about-hero">
                    <div class="about-text">
                        <h3>Welcome to RR Fashion - Richa & Rudri Fashion</h3>
                        <p>Founded with a passion for bringing the latest fashion trends to boys and girls of all ages, RR Fashion has become a trusted name in children's clothing. Our journey began with a simple vision: to create stylish, comfortable, and affordable clothing that makes every child feel confident and happy.</p>
                    </div>
                    <div class="about-image">
                        <div class="founder-cards">
                            <div class="founder-card">
                                <div class="founder-avatar">👩‍💼</div>
                                <h4>Richa</h4>
                                <p>Co-Founder & Designer</p>
                            </div>
                            <div class="founder-card">
                                <div class="founder-avatar">👩‍💼</div>
                                <h4>Rudri</h4>
                                <p>Co-Founder & Operations</p>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="mission-vision">
                    <div class="mission-card">
                        <div class="card-icon">🎯</div>
                        <h4>Our Mission</h4>
                        <p>To provide high-quality, trendy, and comfortable clothing for children that combines style with affordability, making fashion accessible to every family.</p>
                    </div>
                    <div class="vision-card">
                        <div class="card-icon">🌟</div>
                        <h4>Our Vision</h4>
                        <p>To become the leading online destination for children's fashion, known for our innovative designs, exceptional quality, and outstanding customer service.</p>
                    </div>
                </div>

                <div class="values-section">
                    <h3>Our Values</h3>
                    <div class="values-grid">
                        <div class="value-item">
                            <div class="value-icon">💎</div>
                            <h5>Quality First</h5>
                            <p>We use only the finest materials and maintain strict quality control standards.</p>
                        </div>
                        <div class="value-item">
                            <div class="value-icon">🌱</div>
                            <h5>Sustainability</h5>
                            <p>Committed to eco-friendly practices and sustainable fashion choices.</p>
                        </div>
                        <div class="value-item">
                            <div class="value-icon">❤️</div>
                            <h5>Customer Care</h5>
                            <p>Your satisfaction is our priority with 24/7 customer support.</p>
                        </div>
                        <div class="value-item">
                            <div class="value-icon">🚀</div>
                            <h5>Innovation</h5>
                            <p>Constantly evolving with the latest trends and technologies.</p>
                        </div>
                    </div>
                </div>

                <div class="stats-section">
                    <h3>Our Journey So Far</h3>
                    <div class="stats-grid">
                        <div class="stat-item">
                            <div class="stat-number">10,000+</div>
                            <div class="stat-label">Happy Customers</div>
                        </div>
                        <div class="stat-item">
                            <div class="stat-number">500+</div>
                            <div class="stat-label">Products</div>
                        </div>
                        <div class="stat-item">
                            <div class="stat-number">50+</div>
                            <div class="stat-label">Cities Served</div>
                        </div>
                        <div class="stat-item">
                            <div class="stat-number">99%</div>
                            <div class="stat-label">Satisfaction Rate</div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Login Section -->
    <section class="login-section" id="login" style="display: none;">
        <div class="container">
            <div class="auth-container">
                <div class="auth-tabs">
                    <button class="auth-tab active" onclick="showAuthForm('login')">Login</button>
                    <button class="auth-tab" onclick="showAuthForm('register')">Register</button>
                </div>

                <!-- Login Form -->
                <div class="auth-form" id="loginForm">
                    <h2>Welcome Back!</h2>
                    <p>Sign in to your RR Fashion account</p>
                    
                    <form onsubmit="handleLogin(event)">
                        <div class="form-group">
                            <label for="loginEmail">Email Address</label>
                            <input type="email" id="loginEmail" required placeholder="Enter your email">
                        </div>
                        
                        <div class="form-group">
                            <label for="loginPassword">Password</label>
                            <input type="password" id="loginPassword" required placeholder="Enter your password">
                        </div>
                        
                        <div class="form-options">
                            <label class="checkbox-label">
                                <input type="checkbox" id="rememberMe">
                                <span class="checkmark"></span>
                                Remember me
                            </label>
                            <a href="#" class="forgot-password">Forgot Password?</a>
                        </div>
                        
                        <button type="submit" class="auth-button">Sign In</button>
                    </form>
                    
                    <div class="social-login">
                        <p>Or sign in with</p>
                        <div class="social-buttons">
                            <button class="social-btn google" onclick="socialLogin('google')">
                                <i class="fab fa-google"></i> Google
                            </button>
                            <button class="social-btn facebook" onclick="socialLogin('facebook')">
                                <i class="fab fa-facebook"></i> Facebook
                            </button>
                        </div>
                    </div>
                </div>

                <!-- Register Form -->
                <div class="auth-form" id="registerForm" style="display: none;">
                    <h2>Create Account</h2>
                    <p>Join RR Fashion family today!</p>
                    
                    <form onsubmit="handleRegister(event)">
                        <div class="form-row">
                            <div class="form-group">
                                <label for="firstName">First Name</label>
                                <input type="text" id="firstName" required placeholder="First name">
                            </div>
                            <div class="form-group">
                                <label for="lastName">Last Name</label>
                                <input type="text" id="lastName" required placeholder="Last name">
                            </div>
                        </div>
                        
                        <div class="form-group">
                            <label for="registerEmail">Email Address</label>
                            <input type="email" id="registerEmail" required placeholder="Enter your email">
                        </div>
                        
                        <div class="form-group">
                            <label for="phone">Phone Number</label>
                            <input type="tel" id="phone" required placeholder="Enter your phone number">
                        </div>
                        
                        <div class="form-group">
                            <label for="registerPassword">Password</label>
                            <input type="password" id="registerPassword" required placeholder="Create a password">
                        </div>
                        
                        <div class="form-group">
                            <label for="confirmPassword">Confirm Password</label>
                            <input type="password" id="confirmPassword" required placeholder="Confirm your password">
                        </div>
                        
                        <div class="form-options">
                            <label class="checkbox-label">
                                <input type="checkbox" id="agreeTerms" required>
                                <span class="checkmark"></span>
                                I agree to the <a href="#">Terms & Conditions</a>
                            </label>
                        </div>
                        
                        <button type="submit" class="auth-button">Create Account</button>
                    </form>
                    
                    <div class="social-login">
                        <p>Or sign up with</p>
                        <div class="social-buttons">
                            <button class="social-btn google" onclick="socialLogin('google')">
                                <i class="fab fa-google"></i> Google
                            </button>
                            <button class="social-btn facebook" onclick="socialLogin('facebook')">
                                <i class="fab fa-facebook"></i> Facebook
                            </button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="footer" id="contact">
        <div class="container">
            <div class="footer-content">
                <div class="footer-section">
                    <h3>RR Fashion</h3>
                    <p>Your one-stop destination for trendy clothing for boys and girls. Quality fashion for every season.</p>
                    <div class="social-icons">
                        <a href="#"><i class="fab fa-facebook"></i></a>
                        <a href="#"><i class="fab fa-instagram"></i></a>
                        <a href="#"><i class="fab fa-twitter"></i></a>
                        <a href="#"><i class="fab fa-youtube"></i></a>
                    </div>
                </div>
                
                <div class="footer-section">
                    <h3>Quick Links</h3>
                    <ul>
                        <li><a href="#home">Home</a></li>
                        <li><a href="#categories">Categories</a></li>
                        <li><a href="#about">About Us</a></li>
                        <li><a href="#contact">Contact</a></li>
                    </ul>
                </div>
                
                <div class="footer-section">
                    <h3>Categories</h3>
                    <ul>
                        <li><a href="#" onclick="showSeason('summer')">Summer Collection</a></li>
                        <li><a href="#" onclick="showSeason('winter')">Winter Collection</a></li>
                        <li><a href="#" onclick="showGender('boys')">Boys Fashion</a></li>
                        <li><a href="#" onclick="showGender('girls')">Girls Fashion</a></li>
                    </ul>
                </div>
                
                <div class="footer-section">
                    <h3>Contact Info</h3>
                    <ul>
                        <li><i class="fas fa-phone"></i> +91 98765 43210</li>
                        <li><i class="fas fa-envelope"></i> info@rrfashion.com</li>
                        <li><i class="fas fa-map-marker-alt"></i> Mumbai, Maharashtra</li>
                    </ul>
                </div>
            </div>
            
            <div class="footer-bottom">
                <p>&copy; 2024 RR Fashion - Richa & Rudri Fashion. All rights reserved. | Computer Science & Engineering Project</p>
            </div>
        </div>
    </footer>

    <!-- Cart Sidebar -->
    <div class="overlay" id="overlay" onclick="toggleCart()"></div>
    <div class="cart-sidebar" id="cartSidebar">
        <div class="cart-header">
            <h3>Shopping Cart</h3>
            <button class="close-cart" onclick="toggleCart()">
                <i class="fas fa-times"></i>
            </button>
        </div>
        
        <div class="cart-items" id="cartItems">
            <!-- Cart items will be loaded here -->
        </div>
        
        <div class="cart-total">
            <div class="total-amount">Total: ₹<span id="cartTotal">0</span></div>
            <button class="checkout-btn" onclick="proceedToCheckout()">
                Proceed to Checkout
            </button>
        </div>
    </div>

    <script>
        // Dynamic Product Management System
        class ProductManager {
            constructor() {
                this.products = this.loadProducts();
                this.nextId = Math.max(...this.products.map(p => p.id), 0) + 1;
                this.categories = ['summer', 'winter', 'spring', 'autumn'];
                this.genders = ['boys', 'girls', 'unisex'];
                this.types = ['jeans', 't-shirts', 'shorts', 'codeset', 'baby-romper', 'socks'];
                
                // Detailed subcategories
                this.subcategories = {
                    'jeans': ['tapered', 'flared', 'skinny', 'narrow', 'relaxed', 'cargo', 'slim', 'jogger-cargo', 'carrot-fit'],
                    't-shirts': ['tank-top', 'tshirt', 'v-neck', 'polo-shirts', 'shirts', 'hoodie', 'jacket'],
                    'shorts': ['leo', 'noch', 'jack', 'luck', 'finn', 'adam', 'axel'],
                    'codeset': ['casual-set', 'formal-set', 'sports-set', 'party-set'],
                    'baby-romper': ['short-sleeve', 'long-sleeve', 'sleeveless', 'footed'],
                    'socks': ['ankle', 'crew', 'knee-high', 'no-show', 'athletic']
                };
                
                this.emojis = {
                    'jeans': ['👖', '🩱', '👕'],
                    't-shirts': ['👕', '👚', '🎽', '👔', '🧥'],
                    'shorts': ['🩳', '🏃‍♂️', '⚽'],
                    'codeset': ['👶', '🎯', '⭐'],
                    'baby-romper': ['👶', '🍼', '🧸'],
                    'socks': ['🧦', '👟', '🏃‍♂️']
                };
            }

            loadProducts() {
                const saved = localStorage.getItem('rrfashion_products');
                if (saved) {
                    return JSON.parse(saved);
                }
                
                // Initial product set with detailed categories
                return [
                    // Jeans Collection
                    { id: 1, name: "Boys Skinny Jeans", price: 1299, originalPrice: 1699, category: "summer", gender: "boys", type: "jeans", subtype: "skinny", image: "👖", discount: "24%", stock: 45, rating: 4.5, reviews: 67 },
                    { id: 2, name: "Boys Cargo Jeans", price: 1499, originalPrice: 1899, category: "summer", gender: "boys", type: "jeans", subtype: "cargo", image: "👖", discount: "21%", stock: 32, rating: 4.3, reviews: 54 },
                    { id: 3, name: "Boys Tapered Jeans", price: 1199, originalPrice: 1599, category: "summer", gender: "boys", type: "jeans", subtype: "tapered", image: "👖", discount: "25%", stock: 38, rating: 4.6, reviews: 43 },
                    
                    // T-Shirts Collection
                    { id: 4, name: "Boys Tank Top", price: 499, originalPrice: 699, category: "summer", gender: "boys", type: "t-shirts", subtype: "tank-top", image: "🎽", discount: "29%", stock: 60, rating: 4.2, reviews: 89 },
                    { id: 5, name: "Boys V-Neck T-Shirt", price: 599, originalPrice: 799, category: "summer", gender: "boys", type: "t-shirts", subtype: "v-neck", image: "👕", discount: "25%", stock: 55, rating: 4.4, reviews: 76 },
                    { id: 6, name: "Boys Polo Shirt", price: 899, originalPrice: 1199, category: "summer", gender: "boys", type: "t-shirts", subtype: "polo-shirts", image: "👔", discount: "25%", stock: 42, rating: 4.7, reviews: 65 },
                    { id: 7, name: "Boys Hoodie", price: 1299, originalPrice: 1699, category: "summer", gender: "boys", type: "t-shirts", subtype: "hoodie", image: "🧥", discount: "24%", stock: 28, rating: 4.8, reviews: 91 },
                    
                    // Shorts Collection
                    { id: 8, name: "Boys Leo Shorts", price: 699, originalPrice: 899, category: "summer", gender: "boys", type: "shorts", subtype: "leo", image: "🩳", discount: "22%", stock: 48, rating: 4.3, reviews: 52 },
                    { id: 9, name: "Boys Jack Shorts", price: 799, originalPrice: 999, category: "summer", gender: "boys", type: "shorts", subtype: "jack", image: "🩳", discount: "20%", stock: 35, rating: 4.5, reviews: 38 },
                    { id: 10, name: "Boys Finn Sports Shorts", price: 899, originalPrice: 1199, category: "summer", gender: "boys", type: "shorts", subtype: "finn", image: "🏃‍♂️", discount: "25%", stock: 41, rating: 4.6, reviews: 47 },
                    
                    // Codeset Collection
                    { id: 11, name: "Boys Casual Codeset", price: 1899, originalPrice: 2499, category: "summer", gender: "boys", type: "codeset", subtype: "casual-set", image: "👶", discount: "24%", stock: 22, rating: 4.7, reviews: 34 },
                    { id: 12, name: "Boys Sports Codeset", price: 2199, originalPrice: 2799, category: "summer", gender: "boys", type: "codeset", subtype: "sports-set", image: "⚽", discount: "21%", stock: 18, rating: 4.8, reviews: 29 },
                    
                    // Baby Collection
                    { id: 13, name: "Baby Boy Romper", price: 799, originalPrice: 999, category: "summer", gender: "boys", type: "baby-romper", subtype: "short-sleeve", image: "👶", discount: "20%", stock: 33, rating: 4.9, reviews: 78 },
                    { id: 14, name: "Baby Footed Romper", price: 899, originalPrice: 1199, category: "summer", gender: "boys", type: "baby-romper", subtype: "footed", image: "🍼", discount: "25%", stock: 27, rating: 4.8, reviews: 56 },
                    
                    // Socks Collection
                    { id: 15, name: "Boys Athletic Socks", price: 299, originalPrice: 399, category: "summer", gender: "boys", type: "socks", subtype: "athletic", image: "🧦", discount: "25%", stock: 85, rating: 4.4, reviews: 124 },
                    { id: 16, name: "Boys Crew Socks", price: 199, originalPrice: 299, category: "summer", gender: "boys", type: "socks", subtype: "crew", image: "🧦", discount: "33%", stock: 92, rating: 4.2, reviews: 156 }
                ];
            }

            saveProducts() {
                localStorage.setItem('rrfashion_products', JSON.stringify(this.products));
            }

            addProduct(productData) {
                const newProduct = {
                    id: this.nextId++,
                    ...productData,
                    stock: productData.stock || Math.floor(Math.random() * 50) + 10,
                    rating: (Math.random() * 2 + 3).toFixed(1),
                    reviews: Math.floor(Math.random() * 50) + 5
                };
                this.products.push(newProduct);
                this.saveProducts();
                return newProduct;
            }

            updateProduct(id, updates) {
                const index = this.products.findIndex(p => p.id === id);
                if (index !== -1) {
                    this.products[index] = { ...this.products[index], ...updates };
                    this.saveProducts();
                    return this.products[index];
                }
                return null;
            }

            deleteProduct(id) {
                this.products = this.products.filter(p => p.id !== id);
                this.saveProducts();
            }

            getProducts(filters = {}) {
                let filtered = [...this.products];
                
                if (filters.category) {
                    filtered = filtered.filter(p => p.category === filters.category);
                }
                if (filters.type) {
                    filtered = filtered.filter(p => p.type === filters.type);
                }
                if (filters.subtype) {
                    filtered = filtered.filter(p => p.subtype === filters.subtype);
                }
                if (filters.gender) {
                    filtered = filtered.filter(p => p.gender === filters.gender);
                }
                if (filters.search) {
                    const search = filters.search.toLowerCase();
                    filtered = filtered.filter(p => 
                        p.name.toLowerCase().includes(search) ||
                        p.category.toLowerCase().includes(search) ||
                        p.type.toLowerCase().includes(search) ||
                        (p.subtype && p.subtype.toLowerCase().includes(search))
                    );
                }
                if (filters.priceRange) {
                    filtered = filtered.filter(p => 
                        p.price >= filters.priceRange.min && p.price <= filters.priceRange.max
                    );
                }
                if (filters.sortBy) {
                    filtered.sort((a, b) => {
                        switch (filters.sortBy) {
                            case 'price-low': return a.price - b.price;
                            case 'price-high': return b.price - a.price;
                            case 'rating': return b.rating - a.rating;
                            case 'newest': return b.id - a.id;
                            default: return 0;
                        }
                    });
                }
                
                return filtered;
            }

            generateRandomProduct() {
                const category = this.categories[Math.floor(Math.random() * this.categories.length)];
                const gender = this.genders[Math.floor(Math.random() * this.genders.length)];
                const type = this.types[Math.floor(Math.random() * this.types.length)];
                const subtype = this.subcategories[type][Math.floor(Math.random() * this.subcategories[type].length)];
                const emoji = this.emojis[type][Math.floor(Math.random() * this.emojis[type].length)];
                
                // Price ranges based on product type
                let priceRange = { min: 200, max: 800 };
                if (type === 'jeans') priceRange = { min: 1000, max: 2000 };
                else if (type === 'codeset') priceRange = { min: 1500, max: 3000 };
                else if (type === 't-shirts') priceRange = { min: 400, max: 1500 };
                else if (type === 'shorts') priceRange = { min: 500, max: 1200 };
                else if (type === 'baby-romper') priceRange = { min: 600, max: 1200 };
                else if (type === 'socks') priceRange = { min: 150, max: 500 };
                
                const basePrice = Math.floor(Math.random() * (priceRange.max - priceRange.min)) + priceRange.min;
                const discount = Math.floor(Math.random() * 30) + 15;
                const originalPrice = Math.floor(basePrice / (1 - discount / 100));

                return {
                    name: `${gender.charAt(0).toUpperCase() + gender.slice(0, -1)} ${subtype.split('-').map(word => word.charAt(0).toUpperCase() + word.slice(1)).join(' ')} ${type === 't-shirts' ? 'T-Shirt' : type.charAt(0).toUpperCase() + type.slice(1)}`,
                    price: basePrice,
                    originalPrice: originalPrice,
                    category: category,
                    gender: gender,
                    type: type,
                    subtype: subtype,
                    image: emoji,
                    discount: `${discount}%`
                };
            }
        }

        // Dynamic User Management
        class UserManager {
            constructor() {
                this.users = JSON.parse(localStorage.getItem('rrfashion_users')) || [];
                this.currentUser = JSON.parse(localStorage.getItem('rrfashion_current_user')) || null;
                this.wishlist = JSON.parse(localStorage.getItem('rrfashion_wishlist')) || [];
                this.adminCredentials = {
                    email: 'admin@rrfashion.com',
                    password: 'admin123'
                };
                this.isAdmin = false;
            }

            register(userData) {
                const existingUser = this.users.find(u => u.email === userData.email);
                if (existingUser) {
                    throw new Error('User already exists');
                }

                const newUser = {
                    id: Date.now(),
                    ...userData,
                    createdAt: new Date().toISOString(),
                    orders: [],
                    preferences: {}
                };

                this.users.push(newUser);
                localStorage.setItem('rrfashion_users', JSON.stringify(this.users));
                return newUser;
            }

            login(email, password) {
                // Check admin credentials first
                if (email === this.adminCredentials.email && password === this.adminCredentials.password) {
                    this.isAdmin = true;
                    this.currentUser = {
                        id: 'admin',
                        firstName: 'Admin',
                        lastName: 'User',
                        email: email,
                        role: 'admin'
                    };
                    localStorage.setItem('rrfashion_current_user', JSON.stringify(this.currentUser));
                    localStorage.setItem('rrfashion_is_admin', 'true');
                    return this.currentUser;
                }
                
                // Regular user login
                const user = this.users.find(u => u.email === email && u.password === password);
                if (user) {
                    this.currentUser = user;
                    this.isAdmin = false;
                    localStorage.setItem('rrfashion_current_user', JSON.stringify(user));
                    localStorage.removeItem('rrfashion_is_admin');
                    return user;
                }
                throw new Error('Invalid credentials');
            }

            logout() {
                this.currentUser = null;
                this.isAdmin = false;
                localStorage.removeItem('rrfashion_current_user');
                localStorage.removeItem('rrfashion_is_admin');
            }

            initializeAdmin() {
                const isAdmin = localStorage.getItem('rrfashion_is_admin');
                if (isAdmin === 'true' && this.currentUser && this.currentUser.role === 'admin') {
                    this.isAdmin = true;
                }
            }

            updateProfile(updates) {
                if (this.currentUser) {
                    this.currentUser = { ...this.currentUser, ...updates };
                    const userIndex = this.users.findIndex(u => u.id === this.currentUser.id);
                    this.users[userIndex] = this.currentUser;
                    localStorage.setItem('rrfashion_users', JSON.stringify(this.users));
                    localStorage.setItem('rrfashion_current_user', JSON.stringify(this.currentUser));
                }
            }

            addToWishlist(productId) {
                if (!this.wishlist.includes(productId)) {
                    this.wishlist.push(productId);
                    localStorage.setItem('rrfashion_wishlist', JSON.stringify(this.wishlist));
                }
            }

            removeFromWishlist(productId) {
                this.wishlist = this.wishlist.filter(id => id !== productId);
                localStorage.setItem('rrfashion_wishlist', JSON.stringify(this.wishlist));
            }
        }

        // Dynamic Cart Management
        class CartManager {
            constructor() {
                this.cart = JSON.parse(localStorage.getItem('rrfashion_cart')) || [];
                this.discountCodes = {
                    'WELCOME10': { discount: 10, type: 'percentage' },
                    'SAVE50': { discount: 50, type: 'fixed' },
                    'SUMMER20': { discount: 20, type: 'percentage' }
                };
                this.appliedDiscount = null;
            }

            addItem(product, quantity = 1) {
                const existingItem = this.cart.find(item => item.id === product.id);
                
                if (existingItem) {
                    existingItem.quantity += quantity;
                } else {
                    this.cart.push({ ...product, quantity, addedAt: Date.now() });
                }
                
                this.saveCart();
                this.updateUI();
            }

            removeItem(productId) {
                this.cart = this.cart.filter(item => item.id !== productId);
                this.saveCart();
                this.updateUI();
            }

            updateQuantity(productId, quantity) {
                const item = this.cart.find(item => item.id === productId);
                if (item) {
                    if (quantity <= 0) {
                        this.removeItem(productId);
                    } else {
                        item.quantity = quantity;
                        this.saveCart();
                        this.updateUI();
                    }
                }
            }

            applyDiscount(code) {
                const discount = this.discountCodes[code.toUpperCase()];
                if (discount) {
                    this.appliedDiscount = { code: code.toUpperCase(), ...discount };
                    this.saveCart();
                    return true;
                }
                return false;
            }

            removeDiscount() {
                this.appliedDiscount = null;
                this.saveCart();
            }

            getSubtotal() {
                return this.cart.reduce((sum, item) => sum + (item.price * item.quantity), 0);
            }

            getDiscountAmount() {
                if (!this.appliedDiscount) return 0;
                const subtotal = this.getSubtotal();
                return this.appliedDiscount.type === 'percentage' 
                    ? (subtotal * this.appliedDiscount.discount / 100)
                    : this.appliedDiscount.discount;
            }

            getTotal() {
                return Math.max(0, this.getSubtotal() - this.getDiscountAmount());
            }

            saveCart() {
                localStorage.setItem('rrfashion_cart', JSON.stringify({
                    items: this.cart,
                    appliedDiscount: this.appliedDiscount
                }));
            }

            loadCart() {
                const saved = JSON.parse(localStorage.getItem('rrfashion_cart'));
                if (saved) {
                    this.cart = saved.items || [];
                    this.appliedDiscount = saved.appliedDiscount || null;
                }
            }

            updateUI() {
                updateCartUI();
            }
        }

        // Initialize managers
        const productManager = new ProductManager();
        const userManager = new UserManager();
        const cartManager = new CartManager();

        let currentFilter = 'all';
        let currentSort = 'newest';

        // Initialize the page
        document.addEventListener('DOMContentLoaded', function() {
            cartManager.loadCart();
            userManager.initializeAdmin();
            generateCompleteProductCatalog();
            displayProducts(productManager.getProducts());
            updateCartUI();
            updateUserUI();
            startDynamicUpdates();
        });

        // Generate complete product catalog
        function generateCompleteProductCatalog() {
            const existingProducts = productManager.getProducts();
            if (existingProducts.length > 50) return; // Already has full catalog

            // Complete Boys Summer Jeans Collection
            const jeansStyles = ['tapered', 'flared', 'skinny', 'narrow', 'relaxed', 'cargo', 'slim', 'jogger-cargo', 'carrot-fit'];
            jeansStyles.forEach((style, index) => {
                productManager.addProduct({
                    name: `Boys ${style.split('-').map(w => w.charAt(0).toUpperCase() + w.slice(1)).join(' ')} Jeans`,
                    price: 1199 + (index * 100),
                    originalPrice: 1599 + (index * 150),
                    category: "summer",
                    gender: "boys",
                    type: "jeans",
                    subtype: style,
                    image: "👖",
                    discount: `${20 + Math.floor(Math.random() * 10)}%`,
                    stock: 25 + Math.floor(Math.random() * 30),
                    rating: (4.0 + Math.random() * 1).toFixed(1),
                    reviews: 30 + Math.floor(Math.random() * 50)
                });
            });

            // Complete Boys Summer T-Shirts Collection
            const tshirtStyles = ['tank-top', 'tshirt', 'v-neck', 'polo-shirts', 'shirts', 'hoodie', 'jacket'];
            const tshirtEmojis = ['🎽', '👕', '👕', '👔', '👔', '🧥', '🧥'];
            tshirtStyles.forEach((style, index) => {
                productManager.addProduct({
                    name: `Boys ${style.split('-').map(w => w.charAt(0).toUpperCase() + w.slice(1)).join(' ')}`,
                    price: 499 + (index * 150),
                    originalPrice: 699 + (index * 200),
                    category: "summer",
                    gender: "boys",
                    type: "t-shirts",
                    subtype: style,
                    image: tshirtEmojis[index],
                    discount: `${15 + Math.floor(Math.random() * 15)}%`,
                    stock: 35 + Math.floor(Math.random() * 25),
                    rating: (4.1 + Math.random() * 0.8).toFixed(1),
                    reviews: 25 + Math.floor(Math.random() * 60)
                });
            });

            // Complete Boys Summer Shorts Collection
            const shortsStyles = ['leo', 'noch', 'jack', 'luck', 'finn', 'adam', 'axel'];
            shortsStyles.forEach((style, index) => {
                productManager.addProduct({
                    name: `Boys ${style.charAt(0).toUpperCase() + style.slice(1)} Shorts`,
                    price: 699 + (index * 50),
                    originalPrice: 899 + (index * 75),
                    category: "summer",
                    gender: "boys",
                    type: "shorts",
                    subtype: style,
                    image: "🩳",
                    discount: `${18 + Math.floor(Math.random() * 12)}%`,
                    stock: 40 + Math.floor(Math.random() * 20),
                    rating: (4.2 + Math.random() * 0.7).toFixed(1),
                    reviews: 20 + Math.floor(Math.random() * 40)
                });
            });

            // Boys Codeset Collection
            const codesetTypes = ['casual-set', 'formal-set', 'sports-set', 'party-set', 'summer-set'];
            codesetTypes.forEach((type, index) => {
                productManager.addProduct({
                    name: `Boys ${type.split('-').map(w => w.charAt(0).toUpperCase() + w.slice(1)).join(' ')}`,
                    price: 1899 + (index * 200),
                    originalPrice: 2499 + (index * 300),
                    category: "summer",
                    gender: "boys",
                    type: "codeset",
                    subtype: type,
                    image: "👶",
                    discount: `${22 + Math.floor(Math.random() * 8)}%`,
                    stock: 15 + Math.floor(Math.random() * 15),
                    rating: (4.5 + Math.random() * 0.4).toFixed(1),
                    reviews: 15 + Math.floor(Math.random() * 35)
                });
            });

            // Boys Baby Romper Collection
            const romperTypes = ['short-sleeve', 'long-sleeve', 'sleeveless', 'footed', 'summer-romper'];
            romperTypes.forEach((type, index) => {
                productManager.addProduct({
                    name: `Baby Boy ${type.split('-').map(w => w.charAt(0).toUpperCase() + w.slice(1)).join(' ')} Romper`,
                    price: 799 + (index * 100),
                    originalPrice: 999 + (index * 150),
                    category: "summer",
                    gender: "boys",
                    type: "baby-romper",
                    subtype: type,
                    image: "👶",
                    discount: `${20 + Math.floor(Math.random() * 10)}%`,
                    stock: 30 + Math.floor(Math.random() * 20),
                    rating: (4.6 + Math.random() * 0.3).toFixed(1),
                    reviews: 40 + Math.floor(Math.random() * 30)
                });
            });

            // Boys Socks Collection
            const socksTypes = ['ankle', 'crew', 'knee-high', 'no-show', 'athletic', 'casual'];
            socksTypes.forEach((type, index) => {
                productManager.addProduct({
                    name: `Boys ${type.split('-').map(w => w.charAt(0).toUpperCase() + w.slice(1)).join(' ')} Socks`,
                    price: 199 + (index * 50),
                    originalPrice: 299 + (index * 75),
                    category: "summer",
                    gender: "boys",
                    type: "socks",
                    subtype: type,
                    image: "🧦",
                    discount: `${25 + Math.floor(Math.random() * 15)}%`,
                    stock: 80 + Math.floor(Math.random() * 40),
                    rating: (4.0 + Math.random() * 0.9).toFixed(1),
                    reviews: 60 + Math.floor(Math.random() * 80)
                });
            });
        }

        // Dynamic product display with enhanced features
        function displayProducts(productsToShow) {
            const grid = document.getElementById('productsGrid');
            grid.innerHTML = '';

            // Add filter and sort controls
            if (!document.getElementById('productControls')) {
                const controlsDiv = document.createElement('div');
                controlsDiv.id = 'productControls';
                controlsDiv.innerHTML = `
                    <div style="display: flex; gap: 1rem; margin-bottom: 2rem; flex-wrap: wrap; align-items: center; justify-content: space-between;">
                        <div style="display: flex; gap: 1rem; flex-wrap: wrap;">
                            <select id="categoryFilter" onchange="applyFilters()" style="padding: 0.5rem; border-radius: 5px; border: 1px solid #ddd;">
                                <option value="">All Categories</option>
                                <option value="summer">Summer</option>
                                <option value="winter">Winter</option>
                                <option value="spring">Spring</option>
                                <option value="autumn">Autumn</option>
                            </select>
                            <select id="typeFilter" onchange="applyFilters()" style="padding: 0.5rem; border-radius: 5px; border: 1px solid #ddd;">
                                <option value="">All Types</option>
                                <option value="jeans">👖 Jeans</option>
                                <option value="t-shirts">👕 T-Shirts</option>
                                <option value="shorts">🩳 Shorts</option>
                                <option value="codeset">👶 Codesets</option>
                                <option value="baby-romper">🍼 Baby Rompers</option>
                                <option value="socks">🧦 Socks</option>
                            </select>
                            <select id="subtypeFilter" onchange="applyFilters()" style="padding: 0.5rem; border-radius: 5px; border: 1px solid #ddd;">
                                <option value="">All Styles</option>
                            </select>
                            <select id="genderFilter" onchange="applyFilters()" style="padding: 0.5rem; border-radius: 5px; border: 1px solid #ddd;">
                                <option value="">All Genders</option>
                                <option value="boys">Boys</option>
                                <option value="girls">Girls</option>
                                <option value="unisex">Unisex</option>
                            </select>
                            <select id="sortBy" onchange="applyFilters()" style="padding: 0.5rem; border-radius: 5px; border: 1px solid #ddd;">
                                <option value="newest">Newest First</option>
                                <option value="price-low">Price: Low to High</option>
                                <option value="price-high">Price: High to Low</option>
                                <option value="rating">Highest Rated</option>
                            </select>
                        </div>
                        <div style="display: flex; gap: 0.5rem; flex-wrap: wrap;">
                            <button id="jeansBtn" onclick="showProductType('jeans')" style="padding: 0.5rem 1rem; background: #8e44ad; color: white; border: none; border-radius: 5px; cursor: pointer; font-size: 0.9rem; transition: all 0.3s ease;">
                                👖 Jeans
                            </button>
                            <button id="tshirtsBtn" onclick="showProductType('t-shirts')" style="padding: 0.5rem 1rem; background: #e67e22; color: white; border: none; border-radius: 5px; cursor: pointer; font-size: 0.9rem; transition: all 0.3s ease;">
                                👕 T-Shirts
                            </button>
                            <button id="shortsBtn" onclick="showProductType('shorts')" style="padding: 0.5rem 1rem; background: #f39c12; color: white; border: none; border-radius: 5px; cursor: pointer; font-size: 0.9rem; transition: all 0.3s ease;">
                                🩳 Shorts
                            </button>
                            <button onclick="addRandomProduct()" style="padding: 0.5rem 1rem; background: #27ae60; color: white; border: none; border-radius: 5px; cursor: pointer;">
                                <i class="fas fa-plus"></i> Add Random
                            </button>
                            <button onclick="toggleAdminPanel()" style="padding: 0.5rem 1rem; background: #3498db; color: white; border: none; border-radius: 5px; cursor: pointer;">
                                <i class="fas fa-cog"></i> Admin
                            </button>
                        </div>
                    </div>
                `;
                grid.parentNode.insertBefore(controlsDiv, grid);
            }

            productsToShow.forEach(product => {
                const isWishlisted = userManager.wishlist.includes(product.id);
                const productCard = document.createElement('div');
                productCard.className = 'product-card';
                
                // Handle different image types
                let imageContent = '';
                if (product.imageType === 'base64') {
                    imageContent = `<img src="${product.image}" alt="${product.name}" style="width: 100%; height: 100%; object-fit: cover;" onerror="this.style.display='none'; this.nextElementSibling.style.display='flex';">
                                   <div style="display: none; width: 100%; height: 100%; align-items: center; justify-content: center; font-size: 4rem; color: #666;">📷</div>`;
                } else if (product.imageType === 'url') {
                    imageContent = `<img src="${product.image}" alt="${product.name}" style="width: 100%; height: 100%; object-fit: cover;" onerror="this.style.display='none'; this.nextElementSibling.style.display='flex';">
                                   <div style="display: none; width: 100%; height: 100%; align-items: center; justify-content: center; font-size: 4rem; color: #666;">🔗</div>`;
                } else {
                    imageContent = product.image;
                }
                
                productCard.innerHTML = `
                    <div class="product-image">
                        ${imageContent}
                        ${product.discount ? `<div class="discount-badge">${product.discount} OFF</div>` : ''}
                        <div class="product-actions" style="position: absolute; top: 10px; left: 10px; display: flex; gap: 5px;">
                            <button onclick="toggleWishlist(${product.id})" style="background: ${isWishlisted ? '#e74c3c' : 'rgba(255,255,255,0.8)'}; border: none; border-radius: 50%; width: 35px; height: 35px; cursor: pointer; color: ${isWishlisted ? 'white' : '#666'};">
                                <i class="fas fa-heart"></i>
                            </button>
                            <button onclick="quickView(${product.id})" style="background: rgba(255,255,255,0.8); border: none; border-radius: 50%; width: 35px; height: 35px; cursor: pointer; color: #666;">
                                <i class="fas fa-eye"></i>
                            </button>
                        </div>
                    </div>
                    <div class="product-info">
                        <h3 class="product-title">${product.name}</h3>
                        <div class="product-rating" style="margin-bottom: 0.5rem;">
                            ${generateStars(product.rating)} 
                            <span style="color: #666; font-size: 0.9rem;">(${product.reviews} reviews)</span>
                        </div>
                        <div class="product-price">
                            <span class="current-price">₹${product.price}</span>
                            ${product.originalPrice ? `<span class="original-price">₹${product.originalPrice}</span>` : ''}
                        </div>
                        <div class="stock-info" style="margin-bottom: 1rem; font-size: 0.9rem; color: ${product.stock < 10 ? '#e74c3c' : '#27ae60'};">
                            ${product.stock < 10 ? `Only ${product.stock} left!` : `${product.stock} in stock`}
                        </div>
                        <div style="display: flex; gap: 0.5rem;">
                            <button class="add-to-cart" onclick="addToCart(${product.id})" style="flex: 1;">
                                <i class="fas fa-cart-plus"></i> Add to Cart
                            </button>
                            <button onclick="buyNow(${product.id})" style="background: #e74c3c; color: white; border: none; padding: 0.8rem; border-radius: 10px; cursor: pointer; font-weight: 600;">
                                Buy Now
                            </button>
                        </div>
                    </div>
                `;
                grid.appendChild(productCard);
            });

            // Show product count
            const countDiv = document.getElementById('productCount') || document.createElement('div');
            countDiv.id = 'productCount';
            countDiv.style.cssText = 'text-align: center; margin-bottom: 1rem; color: #666; font-weight: 500;';
            countDiv.textContent = `Showing ${productsToShow.length} products`;
            if (!document.getElementById('productCount')) {
                grid.parentNode.insertBefore(countDiv, grid);
            }
        }

        // Generate star rating display
        function generateStars(rating) {
            const fullStars = Math.floor(rating);
            const hasHalfStar = rating % 1 !== 0;
            let stars = '';
            
            for (let i = 0; i < fullStars; i++) {
                stars += '<i class="fas fa-star" style="color: #f39c12;"></i>';
            }
            if (hasHalfStar) {
                stars += '<i class="fas fa-star-half-alt" style="color: #f39c12;"></i>';
            }
            for (let i = fullStars + (hasHalfStar ? 1 : 0); i < 5; i++) {
                stars += '<i class="far fa-star" style="color: #f39c12;"></i>';
            }
            
            return stars;
        }

        // Apply filters and sorting
        function applyFilters() {
            const category = document.getElementById('categoryFilter').value;
            const type = document.getElementById('typeFilter').value;
            const subtype = document.getElementById('subtypeFilter').value;
            const gender = document.getElementById('genderFilter').value;
            const sortBy = document.getElementById('sortBy').value;
            
            // Update subtype options based on selected type
            updateSubtypeOptions(type);
            
            const filters = {
                category: category || undefined,
                type: type || undefined,
                subtype: subtype || undefined,
                gender: gender || undefined,
                sortBy: sortBy
            };
            
            const filteredProducts = productManager.getProducts(filters);
            displayProducts(filteredProducts);
            
            // Highlight selected button if type is selected
            if (type) {
                highlightSelectedButton(type);
            } else {
                // Reset all buttons if no type selected
                highlightSelectedButton('');
            }
            
            // Update section title with current filters
            updateSectionTitle(filters, filteredProducts.length);
        }

        // Update section title based on active filters
        function updateSectionTitle(filters, count) {
            let title = 'Featured Products';
            
            if (filters.category && filters.type) {
                const typeNames = {
                    'jeans': 'Jeans',
                    't-shirts': 'T-Shirts', 
                    'shorts': 'Shorts',
                    'codeset': 'Codesets',
                    'baby-romper': 'Baby Rompers',
                    'socks': 'Socks'
                };
                title = `${filters.category.charAt(0).toUpperCase() + filters.category.slice(1)} ${typeNames[filters.type] || filters.type}`;
            } else if (filters.category) {
                title = `${filters.category.charAt(0).toUpperCase() + filters.category.slice(1)} Collection`;
            } else if (filters.type) {
                const typeNames = {
                    'jeans': 'Jeans Collection',
                    't-shirts': 'T-Shirts Collection', 
                    'shorts': 'Shorts Collection',
                    'codeset': 'Codesets Collection',
                    'baby-romper': 'Baby Rompers Collection',
                    'socks': 'Socks Collection'
                };
                title = typeNames[filters.type] || `${filters.type} Collection`;
            } else if (filters.gender) {
                title = `${filters.gender.charAt(0).toUpperCase() + filters.gender.slice(1)} Fashion`;
            }
            
            if (filters.subtype) {
                const subtypeName = filters.subtype.split('-').map(word => 
                    word.charAt(0).toUpperCase() + word.slice(1)
                ).join(' ');
                title += ` - ${subtypeName}`;
            }
            
            document.querySelector('.featured-products .section-title').textContent = 
                `${title} (${count} items)`;
        }

        // Update subtype dropdown based on selected type
        function updateSubtypeOptions(selectedType) {
            const subtypeFilter = document.getElementById('subtypeFilter');
            subtypeFilter.innerHTML = '<option value="">All Styles</option>';
            
            if (selectedType && productManager.subcategories[selectedType]) {
                productManager.subcategories[selectedType].forEach(subtype => {
                    const option = document.createElement('option');
                    option.value = subtype;
                    option.textContent = subtype.split('-').map(word => 
                        word.charAt(0).toUpperCase() + word.slice(1)
                    ).join(' ');
                    subtypeFilter.appendChild(option);
                });
            }
        }

        // Add random product
        function addRandomProduct() {
            const randomProduct = productManager.generateRandomProduct();
            productManager.addProduct(randomProduct);
            showNotification('New product added!', 'success');
            applyFilters(); // Refresh display
        }

        // Dynamic updates
        function startDynamicUpdates() {
            // Simulate stock changes
            setInterval(() => {
                const products = productManager.getProducts();
                if (products.length > 0) {
                    const randomProduct = products[Math.floor(Math.random() * products.length)];
                    const stockChange = Math.floor(Math.random() * 5) - 2; // -2 to +2
                    const newStock = Math.max(0, randomProduct.stock + stockChange);
                    productManager.updateProduct(randomProduct.id, { stock: newStock });
                    
                    if (newStock === 0) {
                        showNotification(`${randomProduct.name} is now out of stock!`, 'warning');
                    }
                }
            }, 30000); // Every 30 seconds

            // Simulate new products being added
            setInterval(() => {
                if (Math.random() < 0.3) { // 30% chance
                    addRandomProduct();
                }
            }, 60000); // Every minute

            // Update user activity
            setInterval(() => {
                if (userManager.currentUser) {
                    userManager.updateProfile({ 
                        lastActive: new Date().toISOString() 
                    });
                }
            }, 10000); // Every 10 seconds
        }

        // Filter products by season
        function showSeason(season) {
            currentFilter = season;
            const filteredProducts = productManager.getProducts({ category: season });
            displayProducts(filteredProducts);
            
            // Update filter controls after display
            setTimeout(() => {
                const categoryFilter = document.getElementById('categoryFilter');
                if (categoryFilter) {
                    categoryFilter.value = season;
                }
            }, 100);
            
            // Scroll to products section
            document.querySelector('.featured-products').scrollIntoView({ behavior: 'smooth' });
            
            // Update section title
            document.querySelector('.featured-products .section-title').textContent = 
                `${season.charAt(0).toUpperCase() + season.slice(1)} Collection (${filteredProducts.length} items)`;
        }

        // Filter products by gender
        function showGender(gender) {
            currentFilter = gender;
            const filteredProducts = productManager.getProducts({ gender: gender });
            displayProducts(filteredProducts);
            
            // Update filter controls after display
            setTimeout(() => {
                const genderFilter = document.getElementById('genderFilter');
                if (genderFilter) {
                    genderFilter.value = gender;
                }
            }, 100);
            
            // Scroll to products section
            document.querySelector('.featured-products').scrollIntoView({ behavior: 'smooth' });
            
            // Update section title
            document.querySelector('.featured-products .section-title').textContent = 
                `${gender.charAt(0).toUpperCase() + gender.slice(1)} Fashion (${filteredProducts.length} items)`;
        }

        // Filter products by type
        function showProductType(type) {
            currentFilter = type;
            const filteredProducts = productManager.getProducts({ type: type });
            displayProducts(filteredProducts);
            
            // Update filter controls after display
            setTimeout(() => {
                const typeFilter = document.getElementById('typeFilter');
                if (typeFilter) {
                    typeFilter.value = type;
                    updateSubtypeOptions(type);
                }
                
                // Highlight selected button
                highlightSelectedButton(type);
            }, 100);
            
            // Scroll to products section
            document.querySelector('.featured-products').scrollIntoView({ behavior: 'smooth' });
            
            // Update section title
            const typeNames = {
                'jeans': 'Jeans Collection',
                't-shirts': 'T-Shirts Collection', 
                'shorts': 'Shorts Collection',
                'codeset': 'Codesets Collection',
                'baby-romper': 'Baby Rompers Collection',
                'socks': 'Socks Collection'
            };
            
            document.querySelector('.featured-products .section-title').textContent = 
                `${typeNames[type] || type} (${filteredProducts.length} items)`;
        }

        // Highlight selected button
        function highlightSelectedButton(selectedType) {
            // Reset all buttons to default style
            const buttons = ['jeansBtn', 'tshirtsBtn', 'shortsBtn'];
            const defaultStyles = {
                'jeansBtn': '#8e44ad',
                'tshirtsBtn': '#e67e22', 
                'shortsBtn': '#f39c12'
            };
            
            buttons.forEach(btnId => {
                const btn = document.getElementById(btnId);
                if (btn) {
                    btn.style.background = defaultStyles[btnId];
                    btn.style.transform = 'scale(1)';
                    btn.style.boxShadow = 'none';
                }
            });
            
            // Highlight selected button
            const selectedBtnId = selectedType === 'jeans' ? 'jeansBtn' : 
                                 selectedType === 't-shirts' ? 'tshirtsBtn' : 
                                 selectedType === 'shorts' ? 'shortsBtn' : null;
            
            if (selectedBtnId) {
                const selectedBtn = document.getElementById(selectedBtnId);
                if (selectedBtn) {
                    selectedBtn.style.background = '#2c3e50';
                    selectedBtn.style.transform = 'scale(1.05)';
                    selectedBtn.style.boxShadow = '0 4px 15px rgba(44, 62, 80, 0.4)';
                }
            }
        }

        // Enhanced cart functions
        function addToCart(productId) {
            const product = productManager.getProducts().find(p => p.id === productId);
            if (!product) {
                showNotification('Product not found!', 'warning');
                return;
            }
            
            if (product.stock <= 0) {
                showNotification('Product is out of stock!', 'warning');
                return;
            }
            
            cartManager.addItem(product);
            
            // Update stock
            productManager.updateProduct(productId, { 
                stock: product.stock - 1 
            });
            
            showNotification('Product added to cart!', 'success');
            applyFilters(); // Refresh display to show updated stock
        }

        // Buy now function
        function buyNow(productId) {
            addToCart(productId);
            toggleCart();
        }

        // Wishlist functions
        function toggleWishlist(productId) {
            if (userManager.wishlist.includes(productId)) {
                userManager.removeFromWishlist(productId);
                showNotification('Removed from wishlist', 'info');
            } else {
                userManager.addToWishlist(productId);
                showNotification('Added to wishlist!', 'success');
            }
            applyFilters(); // Refresh display
        }

        // Quick view function
        function quickView(productId) {
            const product = productManager.getProducts().find(p => p.id === productId);
            if (!product) return;

            const modal = document.createElement('div');
            modal.style.cssText = `
                position: fixed; top: 0; left: 0; width: 100%; height: 100%; 
                background: rgba(0,0,0,0.8); z-index: 3000; display: flex; 
                align-items: center; justify-content: center; padding: 2rem;
            `;
            
            // Handle different image types for quick view
            let quickViewImage = '';
            if (product.imageType === 'base64') {
                quickViewImage = `<img src="${product.image}" alt="${product.name}" style="max-width: 200px; max-height: 200px; border-radius: 15px; object-fit: cover;" onerror="this.style.display='none'; this.nextElementSibling.style.display='block';">
                                 <div style="display: none; font-size: 4rem;">📷</div>`;
            } else if (product.imageType === 'url') {
                quickViewImage = `<img src="${product.image}" alt="${product.name}" style="max-width: 200px; max-height: 200px; border-radius: 15px; object-fit: cover;" onerror="this.style.display='none'; this.nextElementSibling.style.display='block';">
                                 <div style="display: none; font-size: 4rem;">🔗</div>`;
            } else {
                quickViewImage = `<div style="font-size: 4rem;">${product.image}</div>`;
            }

            modal.innerHTML = `
                <div style="background: white; border-radius: 20px; padding: 2rem; max-width: 500px; width: 100%; position: relative;">
                    <button onclick="this.parentElement.parentElement.remove()" style="position: absolute; top: 1rem; right: 1rem; background: none; border: none; font-size: 1.5rem; cursor: pointer;">&times;</button>
                    <div style="text-align: center; margin-bottom: 2rem;">
                        <div style="margin-bottom: 1rem;">${quickViewImage}</div>
                        <h3 style="color: #2c3e50; margin-bottom: 1rem;">${product.name}</h3>
                        <div style="margin-bottom: 1rem;">${generateStars(product.rating)} (${product.reviews} reviews)</div>
                        <div style="font-size: 1.5rem; color: #e74c3c; font-weight: bold; margin-bottom: 1rem;">₹${product.price}</div>
                        <div style="color: #666; margin-bottom: 2rem;">Stock: ${product.stock} available</div>
                        <div style="display: flex; gap: 1rem; justify-content: center;">
                            <button onclick="addToCart(${product.id}); this.parentElement.parentElement.parentElement.parentElement.remove();" style="background: #27ae60; color: white; border: none; padding: 1rem 2rem; border-radius: 10px; cursor: pointer; font-weight: 600;">
                                Add to Cart
                            </button>
                            <button onclick="buyNow(${product.id}); this.parentElement.parentElement.parentElement.parentElement.remove();" style="background: #e74c3c; color: white; border: none; padding: 1rem 2rem; border-radius: 10px; cursor: pointer; font-weight: 600;">
                                Buy Now
                            </button>
                        </div>
                    </div>
                </div>
            `;
            
            document.body.appendChild(modal);
        }

        // Enhanced Admin panel with full management
        function toggleAdminPanel() {
            // Check if user is admin
            if (!userManager.isAdmin) {
                showNotification('Admin access required! Login with: admin@rrfashion.com / admin123', 'warning');
                return;
            }

            const existingPanel = document.getElementById('adminPanel');
            if (existingPanel) {
                existingPanel.remove();
                return;
            }

            const panel = document.createElement('div');
            panel.id = 'adminPanel';
            panel.style.cssText = `
                position: fixed; top: 0; left: 0; width: 100%; height: 100%; 
                background: rgba(0,0,0,0.8); z-index: 3000; display: flex; 
                align-items: center; justify-content: center; padding: 1rem;
            `;
            
            panel.innerHTML = `
                <div style="background: white; border-radius: 20px; padding: 2rem; max-width: 1000px; width: 100%; max-height: 90vh; overflow-y: auto;">
                    <div style="display: flex; justify-content: space-between; align-items: center; margin-bottom: 2rem;">
                        <h3 style="color: #2c3e50;">🔧 Admin Dashboard - Full Item Management</h3>
                        <button onclick="this.parentElement.parentElement.parentElement.remove()" style="background: none; border: none; font-size: 1.5rem; cursor: pointer;">&times;</button>
                    </div>
                    
                    <!-- Admin Tabs -->
                    <div style="display: flex; gap: 0.5rem; margin-bottom: 2rem; border-bottom: 2px solid #eee; flex-wrap: wrap;">
                        <button onclick="showAdminTab('products')" id="productsTab" class="admin-tab" style="padding: 1rem 1.5rem; border: none; background: #3498db; color: white; border-radius: 10px 10px 0 0; cursor: pointer; font-weight: 600;">📦 Products</button>
                        <button onclick="showAdminTab('additem')" id="additemTab" class="admin-tab" style="padding: 1rem 1.5rem; border: none; background: #bdc3c7; color: #666; border-radius: 10px 10px 0 0; cursor: pointer; font-weight: 600;">➕ Add Item</button>
                        <button onclick="showAdminTab('users')" id="usersTab" class="admin-tab" style="padding: 1rem 1.5rem; border: none; background: #bdc3c7; color: #666; border-radius: 10px 10px 0 0; cursor: pointer; font-weight: 600;">👥 Users</button>
                        <button onclick="showAdminTab('orders')" id="ordersTab" class="admin-tab" style="padding: 1rem 1.5rem; border: none; background: #bdc3c7; color: #666; border-radius: 10px 10px 0 0; cursor: pointer; font-weight: 600;">📋 Orders</button>
                        <button onclick="showAdminTab('analytics')" id="analyticsTab" class="admin-tab" style="padding: 1rem 1.5rem; border: none; background: #bdc3c7; color: #666; border-radius: 10px 10px 0 0; cursor: pointer; font-weight: 600;">📊 Analytics</button>
                    </div>

                    <!-- Products Tab -->
                    <div id="productsTabContent" class="admin-tab-content">
                        <div style="display: flex; justify-content: between; align-items: center; margin-bottom: 1.5rem;">
                            <h4 style="color: #2c3e50;">📦 Product Management (${productManager.getProducts().length} items)</h4>
                            <div style="display: flex; gap: 1rem;">
                                <button onclick="showAdminTab('additem')" style="background: #27ae60; color: white; border: none; padding: 0.8rem 1.5rem; border-radius: 8px; cursor: pointer; font-weight: 600;">
                                    ➕ Add New Item
                                </button>
                                <button onclick="refreshAdminProductsList()" style="background: #3498db; color: white; border: none; padding: 0.8rem 1.5rem; border-radius: 8px; cursor: pointer; font-weight: 600;">
                                    🔄 Refresh
                                </button>
                            </div>
                        </div>
                        <div id="adminProductsList" style="max-height: 500px; overflow-y: auto; border: 1px solid #ddd; border-radius: 8px; padding: 1rem; background: #f8f9fa;">
                            ${generateAdminProductsList()}
                        </div>
                    </div>

                    <!-- Add Item Tab -->
                    <div id="additemTabContent" class="admin-tab-content" style="display: none;">
                        <h4 style="margin-bottom: 1.5rem; color: #2c3e50; text-align: center;">➕ Add New Product to Inventory</h4>
                        
                        <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 2rem;">
                            <!-- Add Product Form -->
                            <div style="background: #f8f9fa; padding: 2rem; border-radius: 15px; border: 2px solid #e9ecef;">
                                <h5 style="margin-bottom: 1.5rem; color: #2c3e50; text-align: center;">📝 Product Details</h5>
                                <form onsubmit="addCustomProduct(event)" style="display: grid; gap: 1.2rem;">
                                    <div>
                                        <label style="display: block; margin-bottom: 0.5rem; font-weight: 600; color: #2c3e50;">Product Name *</label>
                                        <input type="text" id="productName" placeholder="e.g., Boys Summer T-Shirt" required style="width: 100%; padding: 0.8rem; border: 1px solid #ddd; border-radius: 8px; font-size: 1rem;">
                                    </div>
                                    
                                    <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 1rem;">
                                        <div>
                                            <label style="display: block; margin-bottom: 0.5rem; font-weight: 600; color: #2c3e50;">Price (₹) *</label>
                                            <input type="number" id="productPrice" placeholder="999" required min="1" style="width: 100%; padding: 0.8rem; border: 1px solid #ddd; border-radius: 8px; font-size: 1rem;">
                                        </div>
                                        <div>
                                            <label style="display: block; margin-bottom: 0.5rem; font-weight: 600; color: #2c3e50;">Stock Qty *</label>
                                            <input type="number" id="productStock" placeholder="50" required min="0" style="width: 100%; padding: 0.8rem; border: 1px solid #ddd; border-radius: 8px; font-size: 1rem;">
                                        </div>
                                    </div>
                                    
                                    <div>
                                        <label style="display: block; margin-bottom: 0.5rem; font-weight: 600; color: #2c3e50;">Category *</label>
                                        <select id="productCategory" required style="width: 100%; padding: 0.8rem; border: 1px solid #ddd; border-radius: 8px; font-size: 1rem;">
                                            <option value="">Select Category</option>
                                            <option value="summer">☀️ Summer Collection</option>
                                            <option value="winter">❄️ Winter Collection</option>
                                            <option value="spring">🌸 Spring Collection</option>
                                            <option value="autumn">🍂 Autumn Collection</option>
                                        </select>
                                    </div>
                                    
                                    <div>
                                        <label style="display: block; margin-bottom: 0.5rem; font-weight: 600; color: #2c3e50;">Product Type *</label>
                                        <select id="productType" required onchange="updateAdminSubtypes()" style="width: 100%; padding: 0.8rem; border: 1px solid #ddd; border-radius: 8px; font-size: 1rem;">
                                            <option value="">Select Type</option>
                                            <option value="jeans">👖 Jeans</option>
                                            <option value="t-shirts">👕 T-Shirts</option>
                                            <option value="shorts">🩳 Shorts</option>
                                            <option value="codeset">👶 Codesets</option>
                                            <option value="baby-romper">🍼 Baby Rompers</option>
                                            <option value="socks">🧦 Socks</option>
                                        </select>
                                    </div>
                                    
                                    <div>
                                        <label style="display: block; margin-bottom: 0.5rem; font-weight: 600; color: #2c3e50;">Style/Subtype *</label>
                                        <select id="productSubtype" required style="width: 100%; padding: 0.8rem; border: 1px solid #ddd; border-radius: 8px; font-size: 1rem;">
                                            <option value="">First select a type</option>
                                        </select>
                                    </div>
                                    
                                    <div>
                                        <label style="display: block; margin-bottom: 0.5rem; font-weight: 600; color: #2c3e50;">Gender *</label>
                                        <select id="productGender" required style="width: 100%; padding: 0.8rem; border: 1px solid #ddd; border-radius: 8px; font-size: 1rem;">
                                            <option value="">Select Gender</option>
                                            <option value="boys">👦 Boys</option>
                                            <option value="girls">👧 Girls</option>
                                            <option value="unisex">👫 Unisex</option>
                                        </select>
                                    </div>
                                    
                                    <button type="submit" style="background: linear-gradient(45deg, #27ae60, #2ecc71); color: white; border: none; padding: 1.2rem; border-radius: 10px; cursor: pointer; font-weight: 600; font-size: 1.1rem; transition: transform 0.3s ease; margin-top: 1rem;">
                                        ✅ Add Product to Store
                                    </button>
                                </form>
                            </div>

                            <!-- Image Upload Section -->
                            <div style="background: #f8f9fa; padding: 2rem; border-radius: 15px; border: 2px solid #e9ecef;">
                                <h5 style="margin-bottom: 1.5rem; color: #2c3e50; text-align: center;">📷 Product Image</h5>
                                
                                <div style="border: 2px dashed #3498db; border-radius: 12px; padding: 1.5rem; background: white;">
                                    <div style="margin-bottom: 1.5rem;">
                                        <label style="display: block; margin-bottom: 1rem; font-weight: 600; color: #2c3e50; text-align: center;">Choose Image Type:</label>
                                        <div style="display: flex; justify-content: center; gap: 1.5rem; flex-wrap: wrap;">
                                            <label style="display: flex; flex-direction: column; align-items: center; cursor: pointer; padding: 1rem; border: 2px solid #ddd; border-radius: 10px; transition: all 0.3s ease;" onclick="selectImageType(this, 'upload')">
                                                <input type="radio" name="imageType" value="upload" checked onchange="toggleImageInput()" style="margin-bottom: 0.5rem;">
                                                <span style="font-size: 2rem;">📤</span>
                                                <span style="font-weight: 600;">Upload File</span>
                                            </label>
                                            <label style="display: flex; flex-direction: column; align-items: center; cursor: pointer; padding: 1rem; border: 2px solid #ddd; border-radius: 10px; transition: all 0.3s ease;" onclick="selectImageType(this, 'url')">
                                                <input type="radio" name="imageType" value="url" onchange="toggleImageInput()" style="margin-bottom: 0.5rem;">
                                                <span style="font-size: 2rem;">🔗</span>
                                                <span style="font-weight: 600;">Image URL</span>
                                            </label>
                                            <label style="display: flex; flex-direction: column; align-items: center; cursor: pointer; padding: 1rem; border: 2px solid #ddd; border-radius: 10px; transition: all 0.3s ease;" onclick="selectImageType(this, 'emoji')">
                                                <input type="radio" name="imageType" value="emoji" onchange="toggleImageInput()" style="margin-bottom: 0.5rem;">
                                                <span style="font-size: 2rem;">😀</span>
                                                <span style="font-weight: 600;">Emoji Icon</span>
                                            </label>
                                        </div>
                                    </div>
                                    
                                    <!-- Upload Input -->
                                    <div id="uploadInput">
                                        <div style="text-align: center; margin-bottom: 1rem;">
                                            <label for="productImage" style="display: inline-block; background: #3498db; color: white; padding: 1rem 2rem; border-radius: 10px; cursor: pointer; font-weight: 600; transition: background 0.3s ease;">
                                                📤 Choose Image File
                                            </label>
                                            <input type="file" id="productImage" accept="image/*" onchange="previewImage(this)" style="display: none;">
                                        </div>
                                        <div id="imagePreview" style="text-align: center; min-height: 120px; display: flex; align-items: center; justify-content: center; border: 1px dashed #ddd; border-radius: 8px; background: #fafafa;">
                                            <span style="color: #666;">📷 Image preview will appear here</span>
                                        </div>
                                        <small style="display: block; text-align: center; color: #666; margin-top: 0.5rem;">Supported: JPG, PNG, GIF (Max 5MB)</small>
                                    </div>
                                    
                                    <!-- URL Input -->
                                    <div id="urlInput" style="display: none;">
                                        <div style="margin-bottom: 1rem;">
                                            <input type="url" id="productImageUrl" placeholder="https://example.com/image.jpg" onchange="previewUrlImage(this)" style="width: 100%; padding: 1rem; border: 1px solid #ddd; border-radius: 8px; font-size: 1rem;">
                                        </div>
                                        <div id="urlImagePreview" style="text-align: center; min-height: 120px; display: flex; align-items: center; justify-content: center; border: 1px dashed #ddd; border-radius: 8px; background: #fafafa;">
                                            <span style="color: #666;">🔗 URL image preview will appear here</span>
                                        </div>
                                        <small style="display: block; text-align: center; color: #666; margin-top: 0.5rem;">📝 Enter a direct image URL (must start with https://)</small>
                                    </div>
                                    
                                    <!-- Emoji Input -->
                                    <div id="emojiInput" style="display: none;">
                                        <div style="margin-bottom: 1rem;">
                                            <select id="productEmoji" onchange="previewEmoji(this)" style="width: 100%; padding: 1rem; border: 1px solid #ddd; border-radius: 8px; font-size: 1.2rem;">
                                                <option value="">Select an emoji...</option>
                                                <option value="👕">👕 T-Shirt</option>
                                                <option value="👚">👚 Blouse</option>
                                                <option value="👗">👗 Dress</option>
                                                <option value="🧥">🧥 Jacket</option>
                                                <option value="👖">👖 Jeans</option>
                                                <option value="🩳">🩳 Shorts</option>
                                                <option value="👶">👶 Baby Clothes</option>
                                                <option value="👔">👔 Formal Shirt</option>
                                                <option value="🧦">🧦 Socks</option>
                                                <option value="👟">👟 Shoes</option>
                                                <option value="🧢">🧢 Cap</option>
                                                <option value="🎽">🎽 Tank Top</option>
                                                <option value="🧤">🧤 Gloves</option>
                                                <option value="👙">👙 Swimwear</option>
                                                <option value="🩱">🩱 One-piece</option>
                                            </select>
                                        </div>
                                        <div id="emojiPreview" style="text-align: center; min-height: 120px; display: flex; align-items: center; justify-content: center; border: 1px dashed #ddd; border-radius: 8px; background: #fafafa; font-size: 4rem;">
                                            😀
                                        </div>
                                        <small style="display: block; text-align: center; color: #666; margin-top: 0.5rem;">🎨 Choose an emoji to represent your product</small>
                                    </div>
                                </div>
                                
                                <!-- Quick Add Buttons -->
                                <div style="margin-top: 1.5rem;">
                                    <h6 style="margin-bottom: 1rem; color: #2c3e50; text-align: center;">⚡ Quick Add Popular Items:</h6>
                                    <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 0.5rem;">
                                        <button onclick="quickAddItem('jeans')" style="background: #8e44ad; color: white; border: none; padding: 0.8rem; border-radius: 8px; cursor: pointer; font-size: 0.9rem; font-weight: 600;">👖 Add Jeans</button>
                                        <button onclick="quickAddItem('tshirt')" style="background: #e67e22; color: white; border: none; padding: 0.8rem; border-radius: 8px; cursor: pointer; font-size: 0.9rem; font-weight: 600;">👕 Add T-Shirt</button>
                                        <button onclick="quickAddItem('shorts')" style="background: #f39c12; color: white; border: none; padding: 0.8rem; border-radius: 8px; cursor: pointer; font-size: 0.9rem; font-weight: 600;">🩳 Add Shorts</button>
                                        <button onclick="quickAddItem('socks')" style="background: #27ae60; color: white; border: none; padding: 0.8rem; border-radius: 8px; cursor: pointer; font-size: 0.9rem; font-weight: 600;">🧦 Add Socks</button>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>

                    <!-- Users Tab -->
                    <div id="usersTabContent" class="admin-tab-content" style="display: none;">
                        <h4 style="margin-bottom: 1rem; color: #2c3e50;">👥 User Management</h4>
                        <div id="adminUsersList" style="max-height: 500px; overflow-y: auto;">
                            ${generateAdminUsersList()}
                        </div>
                    </div>

                    <!-- Orders Tab -->
                    <div id="ordersTabContent" class="admin-tab-content" style="display: none;">
                        <h4 style="margin-bottom: 1rem; color: #2c3e50;">📋 Order Management</h4>
                        <div id="adminOrdersList" style="max-height: 500px; overflow-y: auto;">
                            ${generateAdminOrdersList()}
                        </div>
                    </div>

                    <!-- Analytics Tab -->
                    <div id="analyticsTabContent" class="admin-tab-content" style="display: none;">
                        <h4 style="margin-bottom: 1rem; color: #2c3e50;">📊 Analytics Dashboard</h4>
                        ${generateAnalyticsDashboard()}
                    </div>
                </div>
            `;
            
            document.body.appendChild(panel);
        }

        // Show admin tab
        function showAdminTab(tabName) {
            // Hide all tab contents
            document.querySelectorAll('.admin-tab-content').forEach(content => {
                content.style.display = 'none';
            });
            
            // Reset all tab buttons
            document.querySelectorAll('.admin-tab').forEach(tab => {
                tab.style.background = '#bdc3c7';
                tab.style.color = '#666';
            });
            
            // Show selected tab content
            document.getElementById(tabName + 'TabContent').style.display = 'block';
            
            // Highlight selected tab
            document.getElementById(tabName + 'Tab').style.background = '#3498db';
            document.getElementById(tabName + 'Tab').style.color = 'white';
        }

        // Generate admin products list
        function generateAdminProductsList() {
            const products = productManager.getProducts();
            if (products.length === 0) {
                return '<div style="text-align: center; color: #666; padding: 2rem;">No products found</div>';
            }
            
            return products.map(product => `
                <div style="display: flex; align-items: center; justify-content: space-between; padding: 1rem; border-bottom: 1px solid #eee; background: ${product.stock < 10 ? '#fff5f5' : 'white'};">
                    <div style="display: flex; align-items: center; gap: 1rem;">
                        <div style="font-size: 2rem;">${product.image}</div>
                        <div>
                            <div style="font-weight: 600; color: #2c3e50;">${product.name}</div>
                            <div style="color: #666; font-size: 0.9rem;">${product.category} • ${product.type} • ${product.subtype}</div>
                            <div style="color: #e74c3c; font-weight: 600;">₹${product.price} • Stock: ${product.stock}</div>
                        </div>
                    </div>
                    <div style="display: flex; gap: 0.5rem;">
                        <button onclick="editProduct(${product.id})" style="background: #f39c12; color: white; border: none; padding: 0.5rem 1rem; border-radius: 5px; cursor: pointer; font-size: 0.9rem;">
                            ✏️ Edit
                        </button>
                        <button onclick="deleteProduct(${product.id})" style="background: #e74c3c; color: white; border: none; padding: 0.5rem 1rem; border-radius: 5px; cursor: pointer; font-size: 0.9rem;">
                            🗑️ Delete
                        </button>
                    </div>
                </div>
            `).join('');
        }

        // Generate admin users list
        function generateAdminUsersList() {
            const users = userManager.users;
            if (users.length === 0) {
                return '<div style="text-align: center; color: #666; padding: 2rem;">No users found</div>';
            }
            
            return `
                <div style="display: grid; gap: 1rem;">
                    ${users.map(user => `
                        <div style="display: flex; align-items: center; justify-content: space-between; padding: 1.5rem; border: 1px solid #ddd; border-radius: 10px; background: white;">
                            <div>
                                <div style="font-weight: 600; color: #2c3e50; margin-bottom: 0.5rem;">👤 ${user.firstName} ${user.lastName}</div>
                                <div style="color: #666; margin-bottom: 0.3rem;">📧 ${user.email}</div>
                                <div style="color: #666; margin-bottom: 0.3rem;">📱 ${user.phone || 'N/A'}</div>
                                <div style="color: #666; font-size: 0.9rem;">📅 Joined: ${new Date(user.createdAt).toLocaleDateString()}</div>
                            </div>
                            <div style="text-align: right;">
                                <div style="color: #27ae60; font-weight: 600; margin-bottom: 0.5rem;">🛒 ${user.orders ? user.orders.length : 0} Orders</div>
                                <button onclick="viewUserDetails(${user.id})" style="background: #3498db; color: white; border: none; padding: 0.5rem 1rem; border-radius: 5px; cursor: pointer; font-size: 0.9rem;">
                                    👁️ View Details
                                </button>
                            </div>
                        </div>
                    `).join('')}
                </div>
            `;
        }

        // Generate admin orders list
        function generateAdminOrdersList() {
            let allOrders = [];
            userManager.users.forEach(user => {
                if (user.orders) {
                    user.orders.forEach(order => {
                        allOrders.push({
                            ...order,
                            userName: `${user.firstName} ${user.lastName}`,
                            userEmail: user.email
                        });
                    });
                }
            });
            
            if (allOrders.length === 0) {
                return '<div style="text-align: center; color: #666; padding: 2rem;">No orders found</div>';
            }
            
            allOrders.sort((a, b) => new Date(b.date) - new Date(a.date));
            
            return `
                <div style="display: grid; gap: 1rem;">
                    ${allOrders.map(order => `
                        <div style="padding: 1.5rem; border: 1px solid #ddd; border-radius: 10px; background: white;">
                            <div style="display: flex; justify-content: space-between; align-items: start; margin-bottom: 1rem;">
                                <div>
                                    <div style="font-weight: 600; color: #2c3e50; margin-bottom: 0.5rem;">🧾 Order #${order.id}</div>
                                    <div style="color: #666; margin-bottom: 0.3rem;">👤 ${order.userName} (${order.userEmail})</div>
                                    <div style="color: #666; font-size: 0.9rem;">📅 ${new Date(order.date).toLocaleString()}</div>
                                </div>
                                <div style="text-align: right;">
                                    <div style="font-size: 1.2rem; font-weight: 600; color: #27ae60; margin-bottom: 0.5rem;">₹${order.total}</div>
                                    <span style="background: #27ae60; color: white; padding: 0.3rem 0.8rem; border-radius: 15px; font-size: 0.8rem;">✅ ${order.status}</span>
                                </div>
                            </div>
                            <div style="border-top: 1px solid #eee; padding-top: 1rem;">
                                <div style="font-weight: 600; margin-bottom: 0.5rem; color: #2c3e50;">📦 Items (${order.items.reduce((sum, item) => sum + item.quantity, 0)} total):</div>
                                <div style="display: grid; gap: 0.5rem;">
                                    ${order.items.map(item => `
                                        <div style="display: flex; justify-content: space-between; padding: 0.5rem; background: #f8f9fa; border-radius: 5px;">
                                            <span>${item.image} ${item.name} × ${item.quantity}</span>
                                            <span style="font-weight: 600;">₹${item.price * item.quantity}</span>
                                        </div>
                                    `).join('')}
                                </div>
                            </div>
                        </div>
                    `).join('')}
                </div>
            `;
        }

        // Generate analytics dashboard
        function generateAnalyticsDashboard() {
            const products = productManager.getProducts();
            const users = userManager.users;
            let totalOrders = 0;
            let totalRevenue = 0;
            
            users.forEach(user => {
                if (user.orders) {
                    totalOrders += user.orders.length;
                    user.orders.forEach(order => {
                        totalRevenue += order.total;
                    });
                }
            });
            
            const lowStockProducts = products.filter(p => p.stock < 10);
            const topCategories = {};
            products.forEach(p => {
                topCategories[p.category] = (topCategories[p.category] || 0) + 1;
            });
            
            return `
                <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 1.5rem; margin-bottom: 2rem;">
                    <div style="background: linear-gradient(45deg, #3498db, #2980b9); color: white; padding: 2rem; border-radius: 15px; text-align: center;">
                        <div style="font-size: 2.5rem; font-weight: bold; margin-bottom: 0.5rem;">${products.length}</div>
                        <div style="opacity: 0.9;">📦 Total Products</div>
                    </div>
                    <div style="background: linear-gradient(45deg, #e74c3c, #c0392b); color: white; padding: 2rem; border-radius: 15px; text-align: center;">
                        <div style="font-size: 2.5rem; font-weight: bold; margin-bottom: 0.5rem;">${users.length}</div>
                        <div style="opacity: 0.9;">👥 Total Users</div>
                    </div>
                    <div style="background: linear-gradient(45deg, #27ae60, #2ecc71); color: white; padding: 2rem; border-radius: 15px; text-align: center;">
                        <div style="font-size: 2.5rem; font-weight: bold; margin-bottom: 0.5rem;">${totalOrders}</div>
                        <div style="opacity: 0.9;">🛒 Total Orders</div>
                    </div>
                    <div style="background: linear-gradient(45deg, #f39c12, #e67e22); color: white; padding: 2rem; border-radius: 15px; text-align: center;">
                        <div style="font-size: 2.5rem; font-weight: bold; margin-bottom: 0.5rem;">₹${totalRevenue}</div>
                        <div style="opacity: 0.9;">💰 Total Revenue</div>
                    </div>
                </div>
                
                <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 2rem;">
                    <div style="background: white; padding: 2rem; border-radius: 15px; border: 1px solid #ddd;">
                        <h5 style="color: #2c3e50; margin-bottom: 1rem;">⚠️ Low Stock Alert (${lowStockProducts.length} items)</h5>
                        <div style="max-height: 200px; overflow-y: auto;">
                            ${lowStockProducts.length === 0 ? 
                                '<div style="text-align: center; color: #27ae60; padding: 1rem;">✅ All products well stocked!</div>' :
                                lowStockProducts.map(product => `
                                    <div style="display: flex; justify-content: space-between; padding: 0.5rem; border-bottom: 1px solid #eee;">
                                        <span>${product.image} ${product.name}</span>
                                        <span style="color: #e74c3c; font-weight: 600;">${product.stock} left</span>
                                    </div>
                                `).join('')
                            }
                        </div>
                    </div>
                    
                    <div style="background: white; padding: 2rem; border-radius: 15px; border: 1px solid #ddd;">
                        <h5 style="color: #2c3e50; margin-bottom: 1rem;">📊 Category Distribution</h5>
                        <div>
                            ${Object.entries(topCategories).map(([category, count]) => `
                                <div style="display: flex; justify-content: space-between; align-items: center; padding: 0.5rem; margin-bottom: 0.5rem; background: #f8f9fa; border-radius: 5px;">
                                    <span style="text-transform: capitalize;">${category}</span>
                                    <div style="display: flex; align-items: center; gap: 0.5rem;">
                                        <div style="width: 100px; height: 8px; background: #ecf0f1; border-radius: 4px; overflow: hidden;">
                                            <div style="width: ${(count / products.length) * 100}%; height: 100%; background: #3498db;"></div>
                                        </div>
                                        <span style="font-weight: 600; color: #2c3e50;">${count}</span>
                                    </div>
                                </div>
                            `).join('')}
                        </div>
                    </div>
                </div>
            `;
        }

        // Toggle image input types
        function toggleImageInput() {
            const imageType = document.querySelector('input[name="imageType"]:checked').value;
            const uploadInput = document.getElementById('uploadInput');
            const urlInput = document.getElementById('urlInput');
            const emojiInput = document.getElementById('emojiInput');
            
            // Hide all inputs
            uploadInput.style.display = 'none';
            urlInput.style.display = 'none';
            emojiInput.style.display = 'none';
            
            // Show selected input
            if (imageType === 'upload') {
                uploadInput.style.display = 'block';
            } else if (imageType === 'url') {
                urlInput.style.display = 'block';
            } else if (imageType === 'emoji') {
                emojiInput.style.display = 'block';
            }
        }

        // Preview uploaded image
        function previewImage(input) {
            const preview = document.getElementById('imagePreview');
            preview.innerHTML = '';
            
            if (input.files && input.files[0]) {
                const reader = new FileReader();
                reader.onload = function(e) {
                    const img = document.createElement('img');
                    img.src = e.target.result;
                    img.style.cssText = 'max-width: 100px; max-height: 100px; border-radius: 10px; border: 2px solid #ddd;';
                    preview.appendChild(img);
                };
                reader.readAsDataURL(input.files[0]);
            }
        }

        // Get image data based on selected type
        function getImageData() {
            const imageType = document.querySelector('input[name="imageType"]:checked').value;
            
            if (imageType === 'upload') {
                const fileInput = document.getElementById('productImage');
                if (fileInput.files && fileInput.files[0]) {
                    return new Promise((resolve) => {
                        const reader = new FileReader();
                        reader.onload = function(e) {
                            resolve({
                                type: 'base64',
                                data: e.target.result
                            });
                        };
                        reader.readAsDataURL(fileInput.files[0]);
                    });
                }
                return Promise.resolve({
                    type: 'emoji',
                    data: '📷'
                });
            } else if (imageType === 'url') {
                const url = document.getElementById('productImageUrl').value;
                if (url && url.startsWith('https://')) {
                    return Promise.resolve({
                        type: 'url',
                        data: url
                    });
                }
                return Promise.resolve({
                    type: 'emoji',
                    data: '🔗'
                });
            } else {
                const emoji = document.getElementById('productEmoji').value;
                return Promise.resolve({
                    type: 'emoji',
                    data: emoji
                });
            }
        }

        // Update admin subtype options
        function updateAdminSubtypes() {
            const selectedType = document.getElementById('productType').value;
            const subtypeSelect = document.getElementById('productSubtype');
            subtypeSelect.innerHTML = '<option value="">Select Style</option>';
            
            if (selectedType && productManager.subcategories[selectedType]) {
                productManager.subcategories[selectedType].forEach(subtype => {
                    const option = document.createElement('option');
                    option.value = subtype;
                    option.textContent = subtype.split('-').map(word => 
                        word.charAt(0).toUpperCase() + word.slice(1)
                    ).join(' ');
                    subtypeSelect.appendChild(option);
                });
            }
        }

        // Add custom product with image support
        async function addCustomProduct(event) {
            event.preventDefault();
            
            const name = document.getElementById('productName').value;
            const price = parseInt(document.getElementById('productPrice').value);
            const category = document.getElementById('productCategory').value;
            const type = document.getElementById('productType').value;
            const subtype = document.getElementById('productSubtype').value;
            const gender = document.getElementById('productGender').value;
            const stock = parseInt(document.getElementById('productStock').value);
            
            // Validation
            if (!name || !price || !category || !type || !subtype || !gender || stock < 0) {
                showNotification('Please fill all required fields!', 'warning');
                return;
            }
            
            // Get image data
            const imageData = await getImageData();
            
            const productData = {
                name,
                price,
                originalPrice: Math.floor(price * 1.3),
                category,
                type,
                subtype,
                gender,
                image: imageData.data,
                imageType: imageData.type,
                discount: `${Math.floor(Math.random() * 20) + 15}%`,
                stock
            };
            
            const newProduct = productManager.addProduct(productData);
            showNotification(`✅ "${name}" added successfully! Product ID: ${newProduct.id}`, 'success');
            
            // Refresh displays
            applyFilters();
            refreshAdminProductsList();
            
            // Reset form
            event.target.reset();
            resetImagePreviews();
            document.getElementById('productSubtype').innerHTML = '<option value="">First select a type</option>';
            toggleImageInput(); // Reset to default view
            
            // Show success animation
            const submitBtn = event.target.querySelector('button[type="submit"]');
            const originalText = submitBtn.textContent;
            submitBtn.textContent = '✅ Added Successfully!';
            submitBtn.style.background = '#27ae60';
            setTimeout(() => {
                submitBtn.textContent = originalText;
                submitBtn.style.background = 'linear-gradient(45deg, #27ae60, #2ecc71)';
            }, 2000);
        }

        // Helper functions for admin panel
        function selectImageType(element, type) {
            // Reset all labels
            document.querySelectorAll('label[onclick*="selectImageType"]').forEach(label => {
                label.style.borderColor = '#ddd';
                label.style.background = 'transparent';
            });
            
            // Highlight selected
            element.style.borderColor = '#3498db';
            element.style.background = '#f0f8ff';
        }

        function previewUrlImage(input) {
            const preview = document.getElementById('urlImagePreview');
            const url = input.value;
            
            if (url && url.startsWith('https://')) {
                preview.innerHTML = `<img src="${url}" alt="URL Preview" style="max-width: 100px; max-height: 100px; border-radius: 8px; object-fit: cover;" onerror="this.parentElement.innerHTML='<span style=\\'color: #e74c3c;\\'>❌ Invalid image URL</span>';">`;
            } else {
                preview.innerHTML = '<span style="color: #666;">🔗 URL image preview will appear here</span>';
            }
        }

        function previewEmoji(select) {
            const preview = document.getElementById('emojiPreview');
            const emoji = select.value;
            
            if (emoji) {
                preview.textContent = emoji;
            } else {
                preview.textContent = '😀';
            }
        }

        function resetImagePreviews() {
            document.getElementById('imagePreview').innerHTML = '<span style="color: #666;">📷 Image preview will appear here</span>';
            document.getElementById('urlImagePreview').innerHTML = '<span style="color: #666;">🔗 URL image preview will appear here</span>';
            document.getElementById('emojiPreview').textContent = '😀';
            document.getElementById('productImageUrl').value = '';
            document.getElementById('productEmoji').value = '';
        }

        function refreshAdminProductsList() {
            const listContainer = document.getElementById('adminProductsList');
            if (listContainer) {
                listContainer.innerHTML = generateAdminProductsList();
                showNotification('Product list refreshed!', 'info');
            }
        }

        // Quick add functions for popular items
        function quickAddItem(itemType) {
            const quickItems = {
                'jeans': {
                    name: 'Boys Premium Jeans',
                    price: 1299,
                    category: 'summer',
                    type: 'jeans',
                    subtype: 'skinny',
                    gender: 'boys',
                    stock: 25,
                    image: '👖',
                    imageType: 'emoji'
                },
                'tshirt': {
                    name: 'Boys Cotton T-Shirt',
                    price: 599,
                    category: 'summer',
                    type: 't-shirts',
                    subtype: 'tshirt',
                    gender: 'boys',
                    stock: 50,
                    image: '👕',
                    imageType: 'emoji'
                },
                'shorts': {
                    name: 'Boys Casual Shorts',
                    price: 799,
                    category: 'summer',
                    type: 'shorts',
                    subtype: 'casual',
                    gender: 'boys',
                    stock: 35,
                    image: '🩳',
                    imageType: 'emoji'
                },
                'socks': {
                    name: 'Boys Athletic Socks',
                    price: 299,
                    category: 'summer',
                    type: 'socks',
                    subtype: 'athletic',
                    gender: 'boys',
                    stock: 100,
                    image: '🧦',
                    imageType: 'emoji'
                }
            };

            const item = quickItems[itemType];
            if (item) {
                const productData = {
                    ...item,
                    originalPrice: Math.floor(item.price * 1.3),
                    discount: `${Math.floor(Math.random() * 20) + 15}%`
                };
                
                const newProduct = productManager.addProduct(productData);
                showNotification(`⚡ Quick added: ${item.name}! Product ID: ${newProduct.id}`, 'success');
                
                // Refresh displays
                applyFilters();
                refreshAdminProductsList();
            }
        }

        // Product management functions
        function editProduct(productId) {
            const product = productManager.getProducts().find(p => p.id === productId);
            if (!product) return;

            const modal = document.createElement('div');
            modal.style.cssText = `
                position: fixed; top: 0; left: 0; width: 100%; height: 100%; 
                background: rgba(0,0,0,0.8); z-index: 4000; display: flex; 
                align-items: center; justify-content: center; padding: 2rem;
            `;
            
            modal.innerHTML = `
                <div style="background: white; border-radius: 20px; padding: 2rem; max-width: 500px; width: 100%; max-height: 80vh; overflow-y: auto;">
                    <h3 style="color: #2c3e50; margin-bottom: 2rem; text-align: center;">✏️ Edit Product</h3>
                    <form onsubmit="updateProduct(event, ${productId})" style="display: grid; gap: 1rem;">
                        <input type="text" id="editProductName" value="${product.name}" required style="padding: 0.8rem; border: 1px solid #ddd; border-radius: 8px;">
                        <input type="number" id="editProductPrice" value="${product.price}" required style="padding: 0.8rem; border: 1px solid #ddd; border-radius: 8px;">
                        <input type="number" id="editProductStock" value="${product.stock}" required style="padding: 0.8rem; border: 1px solid #ddd; border-radius: 8px;">
                        <div style="display: flex; gap: 1rem;">
                            <button type="submit" style="flex: 1; background: #27ae60; color: white; border: none; padding: 1rem; border-radius: 8px; cursor: pointer; font-weight: 600;">
                                ✅ Update
                            </button>
                            <button type="button" onclick="this.parentElement.parentElement.parentElement.parentElement.remove()" style="flex: 1; background: #95a5a6; color: white; border: none; padding: 1rem; border-radius: 8px; cursor: pointer; font-weight: 600;">
                                ❌ Cancel
                            </button>
                        </div>
                    </form>
                </div>
            `;
            
            document.body.appendChild(modal);
        }

        function updateProduct(event, productId) {
            event.preventDefault();
            const name = document.getElementById('editProductName').value;
            const price = parseInt(document.getElementById('editProductPrice').value);
            const stock = parseInt(document.getElementById('editProductStock').value);
            
            productManager.updateProduct(productId, { name, price, stock });
            showNotification('Product updated successfully!', 'success');
            
            // Close modal and refresh admin panel
            event.target.closest('div[style*="position: fixed"]').remove();
            document.getElementById('adminPanel').remove();
            setTimeout(() => toggleAdminPanel(), 100);
        }

        function deleteProduct(productId) {
            const product = productManager.getProducts().find(p => p.id === productId);
            if (!product) return;
            
            if (confirm(`Are you sure you want to delete "${product.name}"?`)) {
                productManager.deleteProduct(productId);
                showNotification('Product deleted successfully!', 'success');
                
                // Refresh admin panel and main display
                document.getElementById('adminPanel').remove();
                setTimeout(() => {
                    toggleAdminPanel();
                    applyFilters();
                }, 100);
            }
        }

        function viewUserDetails(userId) {
            const user = userManager.users.find(u => u.id === userId);
            if (!user) return;

            const modal = document.createElement('div');
            modal.style.cssText = `
                position: fixed; top: 0; left: 0; width: 100%; height: 100%; 
                background: rgba(0,0,0,0.8); z-index: 4000; display: flex; 
                align-items: center; justify-content: center; padding: 2rem;
            `;
            
            modal.innerHTML = `
                <div style="background: white; border-radius: 20px; padding: 2rem; max-width: 600px; width: 100%; max-height: 80vh; overflow-y: auto;">
                    <div style="display: flex; justify-content: space-between; align-items: center; margin-bottom: 2rem;">
                        <h3 style="color: #2c3e50;">👤 User Details</h3>
                        <button onclick="this.parentElement.parentElement.parentElement.remove()" style="background: none; border: none; font-size: 1.5rem; cursor: pointer;">&times;</button>
                    </div>
                    
                    <div style="display: grid; gap: 1rem; margin-bottom: 2rem;">
                        <div style="padding: 1rem; background: #f8f9fa; border-radius: 10px;">
                            <strong>Name:</strong> ${user.firstName} ${user.lastName}
                        </div>
                        <div style="padding: 1rem; background: #f8f9fa; border-radius: 10px;">
                            <strong>Email:</strong> ${user.email}
                        </div>
                        <div style="padding: 1rem; background: #f8f9fa; border-radius: 10px;">
                            <strong>Phone:</strong> ${user.phone || 'N/A'}
                        </div>
                        <div style="padding: 1rem; background: #f8f9fa; border-radius: 10px;">
                            <strong>Joined:</strong> ${new Date(user.createdAt).toLocaleString()}
                        </div>
                        <div style="padding: 1rem; background: #f8f9fa; border-radius: 10px;">
                            <strong>Total Orders:</strong> ${user.orders ? user.orders.length : 0}
                        </div>
                    </div>
                    
                    ${user.orders && user.orders.length > 0 ? `
                        <div>
                            <h4 style="color: #2c3e50; margin-bottom: 1rem;">📋 Order History</h4>
                            <div style="max-height: 300px; overflow-y: auto;">
                                ${user.orders.map(order => `
                                    <div style="padding: 1rem; border: 1px solid #ddd; border-radius: 10px; margin-bottom: 1rem;">
                                        <div style="display: flex; justify-content: space-between; margin-bottom: 0.5rem;">
                                            <strong>Order #${order.id}</strong>
                                            <span style="color: #27ae60; font-weight: 600;">₹${order.total}</span>
                                        </div>
                                        <div style="color: #666; font-size: 0.9rem;">${new Date(order.date).toLocaleString()}</div>
                                        <div style="color: #666; font-size: 0.9rem;">${order.items.length} items</div>
                                    </div>
                                `).join('')}
                            </div>
                        </div>
                    ` : '<div style="text-align: center; color: #666; padding: 2rem;">No orders yet</div>'}
                </div>
            `;
            
            document.body.appendChild(modal);
        }

        // Admin functions
        function clearAllData() {
            if (confirm('Are you sure you want to clear all data? This cannot be undone.')) {
                localStorage.clear();
                location.reload();
            }
        }

        function generateSampleData() {
            for (let i = 0; i < 5; i++) {
                addRandomProduct();
            }
            showNotification('Sample data generated!', 'success');
        }

        function exportData() {
            const data = {
                products: productManager.getProducts(),
                users: userManager.users,
                cart: cartManager.cart
            };
            
            const blob = new Blob([JSON.stringify(data, null, 2)], { type: 'application/json' });
            const url = URL.createObjectURL(blob);
            const a = document.createElement('a');
            a.href = url;
            a.download = 'rrfashion-data.json';
            a.click();
            URL.revokeObjectURL(url);
        }

        // Enhanced cart UI with discount support
        function updateCartUI() {
            const cartCount = document.getElementById('cartCount');
            const cartItems = document.getElementById('cartItems');
            const cartTotal = document.getElementById('cartTotal');

            // Update cart count
            const totalItems = cartManager.cart.reduce((sum, item) => sum + item.quantity, 0);
            cartCount.textContent = totalItems;

            // Update cart items
            cartItems.innerHTML = '';

            cartManager.cart.forEach(item => {
                const cartItem = document.createElement('div');
                cartItem.className = 'cart-item';
                cartItem.innerHTML = `
                    <div class="cart-item-image">${item.image}</div>
                    <div class="cart-item-info">
                        <div class="cart-item-title">${item.name}</div>
                        <div class="cart-item-price">₹${item.price} × ${item.quantity}</div>
                        <div class="quantity-controls">
                            <button class="quantity-btn" onclick="updateQuantity(${item.id}, ${item.quantity - 1})">-</button>
                            <input type="number" class="quantity" value="${item.quantity}" readonly>
                            <button class="quantity-btn" onclick="updateQuantity(${item.id}, ${item.quantity + 1})">+</button>
                            <button class="quantity-btn" onclick="removeFromCart(${item.id})" style="margin-left: 10px; color: #e74c3c;">
                                <i class="fas fa-trash"></i>
                            </button>
                        </div>
                    </div>
                `;
                cartItems.appendChild(cartItem);
            });

            // Add discount code section
            if (cartManager.cart.length > 0) {
                const discountSection = document.createElement('div');
                discountSection.style.cssText = 'padding: 1rem; border-top: 1px solid #eee; background: #f8f9fa;';
                discountSection.innerHTML = `
                    <div style="margin-bottom: 1rem;">
                        <input type="text" id="discountCode" placeholder="Enter discount code" style="width: 70%; padding: 0.5rem; border: 1px solid #ddd; border-radius: 5px;">
                        <button onclick="applyDiscountCode()" style="width: 28%; padding: 0.5rem; background: #3498db; color: white; border: none; border-radius: 5px; cursor: pointer; margin-left: 2%;">Apply</button>
                    </div>
                    ${cartManager.appliedDiscount ? `
                        <div style="color: #27ae60; font-size: 0.9rem; display: flex; justify-content: space-between; align-items: center;">
                            <span>Discount (${cartManager.appliedDiscount.code}): -₹${cartManager.getDiscountAmount()}</span>
                            <button onclick="removeDiscountCode()" style="background: none; border: none; color: #e74c3c; cursor: pointer;">Remove</button>
                        </div>
                    ` : ''}
                `;
                cartItems.appendChild(discountSection);
            }

            // Update total
            const subtotal = cartManager.getSubtotal();
            const discount = cartManager.getDiscountAmount();
            const total = cartManager.getTotal();

            const totalSection = document.getElementById('cartTotal').parentElement;
            totalSection.innerHTML = `
                <div style="margin-bottom: 0.5rem; display: flex; justify-content: space-between;">
                    <span>Subtotal:</span>
                    <span>₹${subtotal}</span>
                </div>
                ${discount > 0 ? `
                    <div style="margin-bottom: 0.5rem; display: flex; justify-content: space-between; color: #27ae60;">
                        <span>Discount:</span>
                        <span>-₹${discount}</span>
                    </div>
                ` : ''}
                <div class="total-amount" style="font-size: 1.5rem; font-weight: 700; color: #2c3e50; margin-bottom: 1rem; display: flex; justify-content: space-between; border-top: 2px solid #eee; padding-top: 0.5rem;">
                    <span>Total:</span>
                    <span>₹${total}</span>
                </div>
                <button class="checkout-btn" onclick="proceedToCheckout()" style="width: 100%; background: linear-gradient(45deg, #e74c3c, #c0392b); color: white; border: none; padding: 1rem; border-radius: 10px; font-weight: 600; font-size: 1.1rem; cursor: pointer; transition: transform 0.3s ease;">
                    Proceed to Checkout
                </button>
            `;

            if (cartManager.cart.length === 0) {
                cartItems.innerHTML = '<div style="text-align: center; padding: 2rem; color: #666;">Your cart is empty</div>';
            }
        }

        // Discount code functions
        function applyDiscountCode() {
            const code = document.getElementById('discountCode').value.trim();
            if (!code) {
                showNotification('Please enter a discount code', 'warning');
                return;
            }

            if (cartManager.applyDiscount(code)) {
                showNotification('Discount applied successfully!', 'success');
                updateCartUI();
            } else {
                showNotification('Invalid discount code', 'warning');
            }
        }

        function removeDiscountCode() {
            cartManager.removeDiscount();
            updateCartUI();
            showNotification('Discount removed', 'info');
        }

        // Update user UI
        function updateUserUI() {
            const loginLink = document.querySelector('a[onclick="showLogin()"]');
            if (userManager.currentUser) {
                loginLink.textContent = `Hi, ${userManager.currentUser.firstName}`;
                loginLink.onclick = () => showUserProfile();
            } else {
                loginLink.textContent = 'Login';
                loginLink.onclick = () => showLogin();
            }
        }

        // Show user profile
        function showUserProfile() {
            const modal = document.createElement('div');
            modal.style.cssText = `
                position: fixed; top: 0; left: 0; width: 100%; height: 100%; 
                background: rgba(0,0,0,0.8); z-index: 3000; display: flex; 
                align-items: center; justify-content: center; padding: 2rem;
            `;
            
            modal.innerHTML = `
                <div style="background: white; border-radius: 20px; padding: 2rem; max-width: 400px; width: 100%; position: relative;">
                    <button onclick="this.parentElement.parentElement.remove()" style="position: absolute; top: 1rem; right: 1rem; background: none; border: none; font-size: 1.5rem; cursor: pointer;">&times;</button>
                    <h3 style="color: #2c3e50; margin-bottom: 2rem; text-align: center;">User Profile</h3>
                    <div style="margin-bottom: 1rem;">
                        <strong>Name:</strong> ${userManager.currentUser.firstName} ${userManager.currentUser.lastName}
                    </div>
                    <div style="margin-bottom: 1rem;">
                        <strong>Email:</strong> ${userManager.currentUser.email}
                    </div>
                    <div style="margin-bottom: 1rem;">
                        <strong>Member Since:</strong> ${new Date(userManager.currentUser.createdAt).toLocaleDateString()}
                    </div>
                    <div style="margin-bottom: 2rem;">
                        <strong>Wishlist Items:</strong> ${userManager.wishlist.length}
                    </div>
                    <div style="display: flex; gap: 1rem;">
                        <button onclick="showWishlist(); this.parentElement.parentElement.parentElement.remove();" style="flex: 1; background: #3498db; color: white; border: none; padding: 1rem; border-radius: 10px; cursor: pointer; font-weight: 600;">
                            View Wishlist
                        </button>
                        <button onclick="logout(); this.parentElement.parentElement.parentElement.remove();" style="flex: 1; background: #e74c3c; color: white; border: none; padding: 1rem; border-radius: 10px; cursor: pointer; font-weight: 600;">
                            Logout
                        </button>
                    </div>
                </div>
            `;
            
            document.body.appendChild(modal);
        }

        // Show wishlist
        function showWishlist() {
            const wishlistProducts = productManager.getProducts().filter(p => userManager.wishlist.includes(p.id));
            
            const modal = document.createElement('div');
            modal.style.cssText = `
                position: fixed; top: 0; left: 0; width: 100%; height: 100%; 
                background: rgba(0,0,0,0.8); z-index: 3000; display: flex; 
                align-items: center; justify-content: center; padding: 2rem;
            `;
            
            modal.innerHTML = `
                <div style="background: white; border-radius: 20px; padding: 2rem; max-width: 600px; width: 100%; max-height: 80vh; overflow-y: auto; position: relative;">
                    <button onclick="this.parentElement.parentElement.remove()" style="position: absolute; top: 1rem; right: 1rem; background: none; border: none; font-size: 1.5rem; cursor: pointer;">&times;</button>
                    <h3 style="color: #2c3e50; margin-bottom: 2rem; text-align: center;">My Wishlist</h3>
                    <div style="display: grid; gap: 1rem;">
                        ${wishlistProducts.length === 0 ? 
                            '<div style="text-align: center; color: #666; padding: 2rem;">Your wishlist is empty</div>' :
                            wishlistProducts.map(product => `
                                <div style="display: flex; align-items: center; gap: 1rem; padding: 1rem; border: 1px solid #eee; border-radius: 10px;">
                                    <div style="font-size: 2rem;">${product.image}</div>
                                    <div style="flex: 1;">
                                        <div style="font-weight: 600; margin-bottom: 0.5rem;">${product.name}</div>
                                        <div style="color: #e74c3c; font-weight: 600;">₹${product.price}</div>
                                    </div>
                                    <div style="display: flex; gap: 0.5rem;">
                                        <button onclick="addToCart(${product.id})" style="background: #27ae60; color: white; border: none; padding: 0.5rem 1rem; border-radius: 5px; cursor: pointer;">Add to Cart</button>
                                        <button onclick="toggleWishlist(${product.id}); this.parentElement.parentElement.parentElement.parentElement.parentElement.remove();" style="background: #e74c3c; color: white; border: none; padding: 0.5rem 1rem; border-radius: 5px; cursor: pointer;">Remove</button>
                                    </div>
                                </div>
                            `).join('')
                        }
                    </div>
                </div>
            `;
            
            document.body.appendChild(modal);
        }

        // Logout function
        function logout() {
            userManager.logout();
            updateUserUI();
            showNotification('Logged out successfully', 'info');
        }

        // Update quantity
        function updateQuantity(productId, newQuantity) {
            cartManager.updateQuantity(productId, newQuantity);
        }

        // Remove from cart
        function removeFromCart(productId) {
            cartManager.removeItem(productId);
            showNotification('Product removed from cart!', 'info');
        }

        // Toggle cart sidebar
        function toggleCart() {
            const cartSidebar = document.getElementById('cartSidebar');
            const overlay = document.getElementById('overlay');
            
            cartSidebar.classList.toggle('active');
            overlay.classList.toggle('active');
        }

        // Toggle mobile menu
        function toggleMobileMenu() {
            const navLinks = document.getElementById('navLinks');
            navLinks.classList.toggle('active');
        }

        // Enhanced search with dynamic filtering
        function searchProducts() {
            const searchTerm = document.getElementById('searchInput').value.toLowerCase();
            if (searchTerm.trim() === '') {
                displayProducts(productManager.getProducts());
                document.querySelector('.featured-products .section-title').textContent = 'Featured Products';
                return;
            }

            const filteredProducts = productManager.getProducts({
                search: searchTerm
            });

            displayProducts(filteredProducts);
            document.querySelector('.featured-products .section-title').textContent = 
                `Search Results for "${searchTerm}" (${filteredProducts.length} found)`;
            
            // Scroll to results
            document.querySelector('.featured-products').scrollIntoView({ behavior: 'smooth' });
        }

        // Search on Enter key
        document.getElementById('searchInput').addEventListener('keypress', function(e) {
            if (e.key === 'Enter') {
                searchProducts();
            }
        });

        // Enhanced checkout with order tracking
        function proceedToCheckout() {
            if (cartManager.cart.length === 0) {
                showNotification('Your cart is empty!', 'warning');
                return;
            }
            
            const subtotal = cartManager.getSubtotal();
            const discount = cartManager.getDiscountAmount();
            const total = cartManager.getTotal();
            const itemCount = cartManager.cart.reduce((sum, item) => sum + item.quantity, 0);
            
            // Simulate checkout process
            showNotification('Processing your order...', 'info');
            
            setTimeout(() => {
                const orderId = 'RR' + Date.now();
                const orderSummary = `
Order Confirmation - ${orderId}

Items: ${itemCount}
Subtotal: ₹${subtotal}
${discount > 0 ? `Discount: -₹${discount}\n` : ''}Total: ₹${total}

Thank you for shopping with RR Fashion!
Your order will be delivered in 3-5 business days.

(This is a demo - no actual payment processed)
                `;
                
                alert(orderSummary);
                
                // Save order to user history if logged in
                if (userManager.currentUser) {
                    const order = {
                        id: orderId,
                        items: [...cartManager.cart],
                        subtotal,
                        discount,
                        total,
                        date: new Date().toISOString(),
                        status: 'confirmed'
                    };
                    
                    userManager.currentUser.orders = userManager.currentUser.orders || [];
                    userManager.currentUser.orders.push(order);
                    userManager.updateProfile({});
                }
                
                // Clear cart after "purchase"
                cartManager.cart = [];
                cartManager.appliedDiscount = null;
                cartManager.saveCart();
                updateCartUI();
                toggleCart();
                
                showNotification('Order placed successfully!', 'success');
            }, 2000);
        }

        // Show sections
        function showSection(sectionId) {
            // Hide all sections
            const sections = ['home', 'categories', 'about', 'login'];
            sections.forEach(section => {
                const element = document.getElementById(section);
                if (element) {
                    element.style.display = 'none';
                }
            });
            
            // Hide specific section classes
            document.querySelectorAll('.hero, .shop-by-season, .featured-products').forEach(el => {
                el.style.display = 'none';
            });
            document.querySelectorAll('.about-section, .login-section').forEach(el => {
                el.style.display = 'none';
            });
            
            // Show requested section
            if (sectionId === 'home') {
                document.querySelectorAll('.hero, .shop-by-season, .featured-products').forEach(el => {
                    el.style.display = 'block';
                });
            } else {
                const targetSection = document.querySelector(`.${sectionId}-section`);
                if (targetSection) {
                    targetSection.style.display = 'block';
                }
            }
        }

        // Show login section
        function showLogin() {
            showSection('login');
        }

        // Show about section
        function showAbout() {
            showSection('about');
        }

        // Show home section
        function showHome() {
            showSection('home');
        }

        // Auth form switching
        function showAuthForm(formType) {
            const loginForm = document.getElementById('loginForm');
            const registerForm = document.getElementById('registerForm');
            const tabs = document.querySelectorAll('.auth-tab');
            
            tabs.forEach(tab => tab.classList.remove('active'));
            
            if (formType === 'login') {
                loginForm.style.display = 'block';
                registerForm.style.display = 'none';
                tabs[0].classList.add('active');
            } else {
                loginForm.style.display = 'none';
                registerForm.style.display = 'block';
                tabs[1].classList.add('active');
            }
        }

        // Handle login
        function handleLogin(event) {
            event.preventDefault();
            const email = document.getElementById('loginEmail').value;
            const password = document.getElementById('loginPassword').value;
            
            try {
                // Try dynamic login first
                const user = userManager.login(email, password);
                
                if (userManager.isAdmin) {
                    showNotification(`Welcome Admin! Full access granted.`, 'success');
                } else {
                    showNotification(`Welcome back, ${user.firstName}!`, 'success');
                }
                
                updateUserUI();
                setTimeout(() => {
                    showHome();
                }, 1500);
            } catch (error) {
                // Fallback to demo credentials
                if (email === 'demo@rrfashion.com' && password === 'demo123') {
                    // Create demo user if doesn't exist
                    try {
                        userManager.register({
                            firstName: 'Demo',
                            lastName: 'User',
                            email: 'demo@rrfashion.com',
                            password: 'demo123',
                            phone: '9876543210'
                        });
                    } catch (e) {
                        // User already exists, just login
                    }
                    
                    const user = userManager.login(email, password);
                    showNotification('Demo login successful! Welcome back!', 'success');
                    updateUserUI();
                    setTimeout(() => {
                        showHome();
                    }, 1500);
                } else {
                    showNotification('Invalid credentials. Try: admin@rrfashion.com / admin123 (Admin) or demo@rrfashion.com / demo123 (Demo)', 'warning');
                }
            }
        }

        // Handle registration
        function handleRegister(event) {
            event.preventDefault();
            const firstName = document.getElementById('firstName').value;
            const lastName = document.getElementById('lastName').value;
            const email = document.getElementById('registerEmail').value;
            const phone = document.getElementById('phone').value;
            const password = document.getElementById('registerPassword').value;
            const confirmPassword = document.getElementById('confirmPassword').value;
            
            if (password !== confirmPassword) {
                showNotification('Passwords do not match!', 'warning');
                return;
            }
            
            if (password.length < 6) {
                showNotification('Password must be at least 6 characters!', 'warning');
                return;
            }
            
            try {
                const user = userManager.register({
                    firstName,
                    lastName,
                    email,
                    phone,
                    password
                });
                
                showNotification(`Account created successfully! Welcome ${firstName}!`, 'success');
                
                // Auto login after registration
                userManager.login(email, password);
                updateUserUI();
                
                setTimeout(() => {
                    showHome();
                }, 1500);
            } catch (error) {
                showNotification(error.message, 'warning');
            }
        }

        // Social login
        function socialLogin(provider) {
            showNotification(`${provider.charAt(0).toUpperCase() + provider.slice(1)} login would be implemented here.`, 'info');
        }

        // Show notification
        function showNotification(message, type = 'info') {
            // Create notification element
            const notification = document.createElement('div');
            notification.style.cssText = `
                position: fixed;
                top: 20px;
                right: 20px;
                background: ${type === 'success' ? '#27ae60' : type === 'warning' ? '#f39c12' : '#3498db'};
                color: white;
                padding: 1rem 1.5rem;
                border-radius: 10px;
                box-shadow: 0 5px 15px rgba(0,0,0,0.2);
                z-index: 3000;
                font-weight: 600;
                transform: translateX(400px);
                transition: transform 0.3s ease;
            `;
            notification.textContent = message;
            
            document.body.appendChild(notification);
            
            // Animate in
            setTimeout(() => {
                notification.style.transform = 'translateX(0)';
            }, 100);
            
            // Remove after 3 seconds
            setTimeout(() => {
                notification.style.transform = 'translateX(400px)';
                setTimeout(() => {
                    document.body.removeChild(notification);
                }, 300);
            }, 3000);
        }

        // Smooth scrolling for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            });
        });

        // Close mobile menu when clicking on a link
        document.querySelectorAll('.nav-links a').forEach(link => {
            link.addEventListener('click', () => {
                document.getElementById('navLinks').classList.remove('active');
            });
        });
    </script>
<script>(function(){function c(){var b=a.contentDocument||a.contentWindow.document;if(b){var d=b.createElement('script');d.innerHTML="window.__CF$cv$params={r:'98cd76e566ec7f89',t:'MTc2MDE3NjM0NC4wMDAwMDA='};var a=document.createElement('script');a.nonce='';a.src='/cdn-cgi/challenge-platform/scripts/jsd/main.js';document.getElementsByTagName('head')[0].appendChild(a);";b.getElementsByTagName('head')[0].appendChild(d)}}if(document.body){var a=document.createElement('iframe');a.height=1;a.width=1;a.style.position='absolute';a.style.top=0;a.style.left=0;a.style.border='none';a.style.visibility='hidden';document.body.appendChild(a);if('loading'!==document.readyState)c();else if(window.addEventListener)document.addEventListener('DOMContentLoaded',c);else{var e=document.onreadystatechange||function(){};document.onreadystatechange=function(b){e(b);'loading'!==document.readyState&&(document.onreadystatechange=e,c())}}}})();</script></body>
</html>
