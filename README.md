<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>TechDrop - Premium Gaming Gear</title>
    <link rel="icon" type="image/x-icon" href="/static/favicon.ico">
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        primary: '#0066FF',
                        dark: '#0A0A0A',
                        accent: '#00FFE0',
                    },
                    fontFamily: {
                        'sans': ['"Inter"', 'sans-serif'],
                        'display': ['"Bebas Neue"', 'sans-serif'],
                    },
                }
            }
        }
    </script>
    <link href="https://unpkg.com/aos@2.3.1/dist/aos.css" rel="stylesheet">
    <script src="https://unpkg.com/aos@2.3.1/dist/aos.js"></script>
    <script src="https://unpkg.com/feather-icons"></script>
    <link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&family=Bebas+Neue&display=swap">
    <style>
        .product-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0, 102, 255, 0.2);
        }
        .cart-drawer {
            transform: translateX(100%);
            transition: transform 0.3s ease-in-out;
        }
        .cart-drawer.open {
            transform: translateX(0);
        }
        .badge-new {
            background: linear-gradient(135deg, #00FFE0 0%, #0066FF 100%);
        }
        .badge-promo {
            background: linear-gradient(135deg, #FF2D55 0%, #FF9500 100%);
        }
    </style>
</head>
<body class="bg-dark text-white font-sans min-h-screen">
    <!-- Header -->
    <header class="sticky top-0 z-50 bg-dark/90 backdrop-blur border-b border-gray-800">
        <div class="container mx-auto px-4 py-3 flex items-center justify-between">
            <div class="flex items-center space-x-4">
                <a href="#" class="text-3xl font-display tracking-wider text-primary">TECHDROP</a>
                <nav class="hidden md:block">
                    <ul class="flex space-x-6">
                        <li><a href="#" class="hover:text-primary transition">Home</a></li>
                        <li><a href="#" class="hover:text-primary transition">Xbox</a></li>
                        <li><a href="#" class="hover:text-primary transition">PlayStation 5</a></li>
                        <li><a href="#" class="hover:text-primary transition">PCs</a></li>
                        <li><a href="#" class="hover:text-primary transition">Peripherals</a></li>
                    </ul>
                </nav>
            </div>
            <div class="flex items-center space-x-4">
                <div class="relative hidden md:block">
                    <input type="text" placeholder="Search products..." 
                           class="bg-gray-900 rounded-full py-2 pl-10 pr-4 w-64 focus:outline-none focus:ring-2 focus:ring-primary">
                    <i data-feather="search" class="absolute left-3 top-2.5 text-gray-400"></i>
                </div>
                <button id="cart-toggle" class="relative p-2 rounded-full hover:bg-gray-800">
                    <i data-feather="shopping-cart"></i>
                    <span id="cart-count" class="absolute -top-1 -right-1 bg-primary text-xs font-bold rounded-full h-5 w-5 flex items-center justify-center">0</span>
                </button>
                <button class="md:hidden p-2 rounded-full hover:bg-gray-800" id="mobile-menu-toggle">
                    <i data-feather="menu"></i>
                </button>
            </div>
        </div>
        <!-- Mobile Menu -->
        <div id="mobile-menu" class="hidden md:hidden bg-gray-900 px-4 py-2 border-t border-gray-800">
            <div class="relative mb-3">
                <input type="text" placeholder="Search products..." 
                       class="bg-gray-800 rounded-full py-2 pl-10 pr-4 w-full focus:outline-none focus:ring-2 focus:ring-primary">
                <i data-feather="search" class="absolute left-3 top-2.5 text-gray-400"></i>
            </div>
            <nav>
                <ul class="space-y-2">
                    <li><a href="#" class="block py-2 hover:text-primary transition">Home</a></li>
                    <li><a href="#" class="block py-2 hover:text-primary transition">Xbox</a></li>
                    <li><a href="#" class="block py-2 hover:text-primary transition">PlayStation 5</a></li>
                    <li><a href="#" class="block py-2 hover:text-primary transition">PCs</a></li>
                    <li><a href="#" class="block py-2 hover:text-primary transition">Peripherals</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="relative overflow-hidden">
        <div class="absolute inset-0 bg-gradient-to-r from-dark to-transparent z-10"></div>
        <img src="http://static.photos/technology/1200x630/1" alt="Gaming setup with consoles and PC" class="w-full h-auto md:h-[500px] object-cover">
        <div class="container mx-auto px-4 relative z-20">
            <div class="py-16 md:py-24 max-w-xl">
                <h1 class="text-4xl md:text-6xl font-display tracking-wide mb-4" data-aos="fade-right">GAME LIKE A PRO</h1>
                <p class="text-lg md:text-xl text-gray-300 mb-8" data-aos="fade-right" data-aos-delay="100">
                    Premium gaming gear for competitive advantage. Shop the latest consoles, PCs, and accessories.
                </p>
                <div class="flex space-x-4" data-aos="fade-right" data-aos-delay="200">
                    <button class="bg-primary hover:bg-blue-700 text-white px-6 py-3 rounded font-bold transition">
                        Shop Now
                    </button>
                    <button class="border border-primary text-primary hover:bg-primary hover:text-white px-6 py-3 rounded font-bold transition">
                        View Deals
                    </button>
                </div>
            </div>
        </div>
    </section>

    <!-- Featured Categories -->
    <section class="py-12 bg-gray-900">
        <div class="container mx-auto px-4">
            <h2 class="text-3xl md:text-4xl font-display tracking-wide mb-8 text-center" data-aos="fade-up">Shop By Platform</h2>
            <div class="grid grid-cols-2 md:grid-cols-4 gap-4 md:gap-8">
                <a href="#" class="group" data-aos="zoom-in" data-aos-delay="100">
                    <div class="bg-gray-800 rounded-lg overflow-hidden transition-all duration-300 group-hover:scale-105">
                        <img src="http://static.photos/technology/640x360/10" alt="Xbox Series X" class="w-full h-40 md:h-48 object-cover">
                        <div class="p-4">
                            <h3 class="text-xl font-bold group-hover:text-primary transition">Xbox</h3>
                            <p class="text-gray-400 text-sm">Series X|S & Accessories</p>
                        </div>
                    </div>
                </a>
                <a href="#" class="group" data-aos="zoom-in" data-aos-delay="200">
                    <div class="bg-gray-800 rounded-lg overflow-hidden transition-all duration-300 group-hover:scale-105">
                        <img src="http://static.photos/technology/640x360/11" alt="PlayStation 5" class="w-full h-40 md:h-48 object-cover">
                        <div class="p-4">
                            <h3 class="text-xl font-bold group-hover:text-primary transition">PlayStation 5</h3>
                            <p class="text-gray-400 text-sm">Consoles & Controllers</p>
                        </div>
                    </div>
                </a>
                <a href="#" class="group" data-aos="zoom-in" data-aos-delay="300">
                    <div class="bg-gray-800 rounded-lg overflow-hidden transition-all duration-300 group-hover:scale-105">
                        <img src="http://static.photos/technology/640x360/12" alt="Gaming PC" class="w-full h-40 md:h-48 object-cover">
                        <div class="p-4">
                            <h3 class="text-xl font-bold group-hover:text-primary transition">Gaming PCs</h3>
                            <p class="text-gray-400 text-sm">Pre-built & Components</p>
                        </div>
                    </div>
                </a>
                <a href="#" class="group" data-aos="zoom-in" data-aos-delay="400">
                    <div class="bg-gray-800 rounded-lg overflow-hidden transition-all duration-300 group-hover:scale-105">
                        <img src="http://static.photos/technology/640x360/13" alt="Gaming peripherals" class="w-full h-40 md:h-48 object-cover">
                        <div class="p-4">
                            <h3 class="text-xl font-bold group-hover:text-primary transition">Peripherals</h3>
                            <p class="text-gray-400 text-sm">Keyboards, Mice & Headsets</p>
                        </div>
                    </div>
                </a>
            </div>
        </div>
    </section>

    <!-- Products Grid -->
    <section class="py-12">
        <div class="container mx-auto px-4">
            <div class="flex flex-col md:flex-row justify-between items-start md:items-center mb-8">
                <h2 class="text-3xl md:text-4xl font-display tracking-wide mb-4 md:mb-0">Featured Products</h2>
                <div class="flex flex-col md:flex-row space-y-4 md:space-y-0 md:space-x-4 w-full md:w-auto">
                    <select class="bg-gray-900 border border-gray-800 rounded px-4 py-2 focus:outline-none focus:ring-2 focus:ring-primary">
                        <option>All Categories</option>
                        <option>Consoles</option>
                        <option>PCs</option>
                        <option>Peripherals</option>
                        <option>Accessories</option>
                    </select>
                    <select class="bg-gray-900 border border-gray-800 rounded px-4 py-2 focus:outline-none focus:ring-2 focus:ring-primary">
                        <option>All Platforms</option>
                        <option>Xbox</option>
                        <option>PlayStation</option>
                        <option>PC</option>
                        <option>Nintendo</option>
                    </select>
                    <select class="bg-gray-900 border border-gray-800 rounded px-4 py-2 focus:outline-none focus:ring-2 focus:ring-primary">
                        <option>Sort By</option>
                        <option>Price: Low to High</option>
                        <option>Price: High to Low</option>
                        <option>Rating</option>
                        <option>Newest</option>
                    </select>
                </div>
            </div>
            <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 gap-6">
                <!-- Product Card 1 -->
                <div class="product-card bg-gray-900 rounded-lg overflow-hidden border border-gray-800 transition-all duration-300 hover:border-primary">
                    <div class="relative">
                        <img src="http://static.photos/technology/640x360/20" alt="Xbox Series X" class="w-full h-48 object-cover">
                        <div class="absolute top-2 right-2">
                            <span class="badge-new text-xs font-bold px-2 py-1 rounded-full">NEW</span>
                        </div>
                    </div>
                    <div class="p-4">
                        <div class="flex justify-between items-start">
                            <h3 class="font-bold text-lg mb-1">Xbox Series X</h3>
                            <span class="text-primary font-bold">$499.99</span>
                        </div>
                        <div class="flex items-center mb-3">
                            <div class="flex text-yellow-400">
                                <i data-feather="star" class="w-4 h-4 fill-current"></i>
                                <i data-feather="star" class="w-4 h-4 fill-current"></i>
                                <i data-feather="star" class="w-4 h-4 fill-current"></i>
                                <i data-feather="star" class="w-4 h-4 fill-current"></i>
                                <i data-feather="star" class="w-4 h-4 fill-current"></i>
                            </div>
                            <span class="text-gray-400 text-sm ml-1">(128)</span>
                        </div>
                        <button class="w-full bg-primary hover:bg-blue-700 text-white py-2 rounded font-bold transition">
                            Add to Cart
                        </button>
                    </div>
                </div>
                
                <!-- Product Card 2 -->
                <div class="product-card bg-gray-900 rounded-lg overflow-hidden border border-gray-800 transition-all duration-300 hover:border-primary">
                    <div class="relative">
                        <img src="http://static.photos/technology/640x360/21" alt="PlayStation 5" class="w-full h-48 object-cover">
                        <div class="absolute top-2 right-2">
                            <span class="badge-promo text-xs font-bold px-2 py-1 rounded-full">-15%</span>
                        </div>
                    </div>
                    <div class="p-4">
                        <div class="flex justify-between items-start">
                            <h3 class="font-bold text-lg mb-1">PlayStation 5</h3>
                            <div>
                                <span class="text-gray-400 line-through text-sm mr-2">$499.99</span>
                                <span class="text-primary font-bold">$424.99</span>
                            </div>
                        </div>
                        <div class="flex items-center mb-3">
                            <div class="flex text-yellow-400">
                                <i data-feather="star" class="w-4 h-4 fill-current"></i>
                                <i data-feather="star" class="w-4 h-4 fill-current"></i>
                                <i data-feather="star" class="w-4 h-4 fill-current"></i>
                                <i data-feather="star" class="w-4 h-4 fill-current"></i>
                                <i data-feather="star" class="w-4 h-4"></i>
                            </div>
                            <span class="text-gray-400 text-sm ml-1">(94)</span>
                        </div>
                        <button class="w-full bg-primary hover:bg-blue-700 text-white py-2 rounded font-bold transition">
                            Add to Cart
                        </button>
                    </div>
                </div>
                
                <!-- Product Card 3 -->
                <div class="product-card bg-gray-900 rounded-lg overflow-hidden border border-gray-800 transition-all duration-300 hover:border-primary">
                    <div class="relative">
                        <img src="http://static.photos/technology/640x360/22" alt="Alienware Gaming PC" class="w-full h-48 object-cover">
                    </div>
                    <div class="p-4">
                        <div class="flex justify-between items-start">
                            <h3 class="font-bold text-lg mb-1">Alienware Aurora R15</h3>
                            <span class="text-primary font-bold">$2,199.99</span>
                        </div>
                        <div class="flex items-center mb-3">
                            <div class="flex text-yellow-400">
                                <i data-feather="star" class="w-4 h-4 fill-current"></i>
                                <i data-feather="star" class="w-4 h-4 fill-current"></i>
                                <i data-feather="star" class="w-4 h-4 fill-current"></i>
                                <i data-feather="star" class="w-4 h-4 fill-current"></i>
                                <i data-feather="star" class="w-4 h-4"></i>
                            </div>
                            <span class="text-gray-400 text-sm ml-1">(42)</span>
                        </div>
                        <button class="w-full bg-primary hover:bg-blue-700 text-white py-2 rounded font-bold transition">
                            Add to Cart
                        </button>
                    </div>
                </div>
                
                <!-- Product Card 4 -->
                <div class="product-card bg-gray-900 rounded-lg overflow-hidden border border-gray-800 transition-all duration-300 hover:border-primary">
                    <div class="relative">
                        <img src="http://static.photos/technology/640x360/23" alt="Razer BlackWidow Keyboard" class="w-full h-48 object-cover">
                        <div class="absolute top-2 right-2">
                            <span class="badge-new text-xs font-bold px-2 py-1 rounded-full">NEW</span>
                        </div>
                    </div>
                    <div class="p-4">
                        <div class="flex justify-between items-start">
                            <h3 class="font-bold text-lg mb-1">Razer BlackWidow V4</h3>
                            <span class="text-primary font-bold">$169.99</span>
                        </div>
                        <div class="flex items-center mb-3">
                            <div class="flex text-yellow-400">
                                <i data-feather="star" class="w-4 h-4 fill-current"></i>
                                <i data-feather="star" class="w-4 h-4 fill-current"></i>
                                <i data-feather="star" class="w-4 h-4 fill-current"></i>
                                <i data-feather="star" class="w-4 h-4 fill-current"></i>
                                <i data-feather="star" class="w-4 h-4 fill-current"></i>
                            </div>
                            <span class="text-gray-400 text-sm ml-1">(256)</span>
                        </div>
                        <button class="w-full bg-primary hover:bg-blue-700 text-white py-2 rounded font-bold transition">
                            Add to Cart
                        </button>
                    </div>
                </div>
            </div>
            <div class="mt-8 text-center">
                <button class="border border-primary text-primary hover:bg-primary hover:text-white px-6 py-3 rounded font-bold transition">
                    View All Products
                </button>
            </div>
        </div>
    </section>

    <!-- Features Banner -->
    <section class="py-12 bg-gradient-to-r from-primary to-accent">
        <div class="container mx-auto px-4">
            <div class="grid grid-cols-1 md:grid-cols-3 gap-8 text-center text-dark">
                <div class="flex flex-col items-center" data-aos="fade-up" data-aos-delay="100">
                    <i data-feather="truck" class="w-12 h-12 mb-4"></i>
                    <h3 class="text-xl font-bold mb-2">Free Shipping</h3>
                    <p class="text-gray-800">On all orders over $50</p>
                </div>
                <div class="flex flex-col items-center" data-aos="fade-up" data-aos-delay="200">
                    <i data-feather="refresh-cw" class="w-12 h-12 mb-4"></i>
                    <h3 class="text-xl font-bold mb-2">30-Day Returns</h3>
                    <p class="text-gray-800">Hassle-free returns</p>
                </div>
                <div class="flex flex-col items-center" data-aos="fade-up" data-aos-delay="300">
                    <i data-feather="shield" class="w-12 h-12 mb-4"></i>
                    <h3 class="text-xl font-bold mb-2">2-Year Warranty</h3>
                    <p class="text-gray-800">On all products</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Newsletter -->
    <section class="py-12 bg-gray-900">
        <div class="container mx-auto px-4 max-w-4xl text-center">
            <h2 class="text-3xl md:text-4xl font-display tracking-wide mb-4">Get the Latest Deals</h2>
            <p class="text-gray-300 mb-8 max-w-2xl mx-auto">
                Subscribe to our newsletter and get 10% off your first order plus exclusive access to new releases and special offers.
            </p>
            <div class="flex flex-col md:flex-row gap-2 max-w-lg mx-auto">
                <input type="email" placeholder="Your email address" 
                       class="flex-grow bg-gray-800 border border-gray-700 rounded px-4 py-3 focus:outline-none focus:ring-2 focus:ring-primary">
                <button class="bg-primary hover:bg-blue-700 text-white px-6 py-3 rounded font-bold transition">
                    Subscribe
                </button>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-dark border-t border-gray-800 pt-12 pb-6">
        <div class="container mx-auto px-4">
            <div class="grid grid-cols-1 md:grid-cols-4 gap-8 mb-8">
                <div>
                    <h3 class="text-xl font-display tracking-wide mb-4">TECHDROP</h3>
                    <p class="text-gray-400 mb-4">
                        Premium gaming gear for competitive advantage. Shop the latest consoles, PCs, and accessories.
                    </p>
                    <div class="flex space-x-4">
                        <a href="#" class="text-gray-400 hover:text-primary transition"><i data-feather="facebook"></i></a>
                        <a href="#" class="text-gray-400 hover:text-primary transition"><i data-feather="twitter"></i></a>
                        <a href="#" class="text-gray-400 hover:text-primary transition"><i data-feather="instagram"></i></a>
                        <a href="#" class="text-gray-400 hover:text-primary transition"><i data-feather="youtube"></i></a>
                    </div>
                </div>
                <div>
                    <h4 class="font-bold text-lg mb-4">Shop</h4>
                    <ul class="space-y-2">
                        <li><a href="#" class="text-gray-400 hover:text-primary transition">Xbox</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-primary transition">PlayStation</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-primary transition">Gaming PCs</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-primary transition">Peripherals</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-primary transition">Accessories</a></li>
                    </ul>
                </div>
                <div>
                    <h4 class="font-bold text-lg mb-4">Help</h4>
                    <ul class="space-y-2">
                        <li><a href="#" class="text-gray-400 hover:text-primary transition">Contact Us</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-primary transition">FAQs</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-primary transition">Shipping</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-primary transition">Returns</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-primary transition">Warranty</a></li>
                    </ul>
                </div>
                <div>
                    <h4 class="font-bold text-lg mb-4">Company</h4>
                    <ul class="space-y-2">
                        <li><a href="#" class="text-gray-400 hover:text-primary transition">About Us</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-primary transition">Blog</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-primary transition">Careers</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-primary transition">Press</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-primary transition">Affiliates</a></li>
                    </ul>
                </div>
            </div>
            <div class="border-t border-gray-800 pt-6 flex flex-col md:flex-row justify-between items-center">
                <p class="text-gray-500 text-sm mb-4 md:mb-0">
                    © 2023 TechDrop. All rights reserved.
                </p>
                <div class="flex space-x-6">
                    <a href="#" class="text-gray-500 hover:text-primary transition text-sm">Privacy Policy</a>
                    <a href="#" class="text-gray-500 hover:text-primary transition text-sm">Terms of Service</a>
                    <a href="#" class="text-gray-500 hover:text-primary transition text-sm">Cookies</a>
                </div>
            </div>
        </div>
    </footer>

    <!-- Cart Drawer -->
    <div id="cart-drawer" class="cart-drawer fixed inset-y-0 right-0 w-full md:w-96 bg-gray-900 border-l border-gray-800 z-50 overflow-y-auto">
        <div class="p-6">
            <div class="flex justify-between items-center mb-6">
                <h3 class="text-xl font-display tracking-wide">Your Cart (0)</h3>
                <button id="cart-close" class="p-1 rounded-full hover:bg-gray-800">
                    <i data-feather="x"></i>
                </button>
            </div>
            <div class="text-center py-12">
                <i data-feather="shopping-cart" class="w-12 h-12 mx-auto text-gray-600 mb-4"></i>
                <p class="text-gray-400 mb-6">Your cart is empty</p>
                <button class="border border-primary text-primary hover:bg-primary hover:text-white px-6 py-2 rounded font-bold transition">
                    Continue Shopping
                </button>
            </div>
            <div class="border-t border-gray-800 pt-6 hidden">
                <div class="space-y-4 mb-6">
                    <!-- Cart items would be dynamically inserted here -->
                </div>
                <div class="border-t border-gray-800 pt-4 mb-6">
                    <div class="flex justify-between mb-2">
                        <span class="text-gray-400">Subtotal</span>
                        <span class="font-bold">$0.00</span>
                    </div>
                    <div class="flex justify-between mb-2">
                        <span class="text-gray-400">Shipping</span>
                        <span class="font-bold">Free</span>
                    </div>
                    <div class="flex justify-between text-xl font-bold mt-4">
                        <span>Total</span>
                        <span>$0.00</span>
                    </div>
                </div>
                <button class="w-full bg-primary hover:bg-blue-700 text-white py-3 rounded font-bold transition">
                    Checkout
                </button>
            </div>
        </div>
    </div>

    <script>
        // Initialize AOS animations
        AOS.init({
            duration: 800,
            easing: 'ease-in-out',
            once: true
        });

        // Cart functionality
        const cartToggle = document.getElementById('cart-toggle');
        const cartClose = document.getElementById('cart-close');
        const cartDrawer = document.getElementById('cart-drawer');
        const mobileMenuToggle = document.getElementById('mobile-menu-toggle');
        const mobileMenu = document.getElementById('mobile-menu');

        cartToggle.addEventListener('click', () => {
            cartDrawer.classList.add('open');
        });

        cartClose.addEventListener('click', () => {
            cartDrawer.classList.remove('open');
        });

        mobileMenuToggle.addEventListener('click', () => {
            mobileMenu.classList.toggle('hidden');
        });

        // Initialize feather icons
        feather.replace();

        // Simulate adding items to cart
        const addToCartButtons = document.querySelectorAll('.product-card button');
        const cartCount = document.getElementById('cart-count');

        addToCartButtons.forEach(button => {
            button.addEventListener('click', () => {
                let count = parseInt(cartCount.textContent);
                cartCount.textContent = count + 1;
                
                // Simple animation
                cartCount.classList.add('animate-ping');
                setTimeout(() => {
                    cartCount.classList.remove('animate-ping');
                }, 500);
            });
        });
    </script>
</body>
</html>
