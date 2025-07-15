<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CookEase - Smart Cooking System</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://cdn.jsdelivr.net/npm/font-awesome@4.7.0/css/font-awesome.min.css" rel="stylesheet">
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        primary: '#FF8C00', // Orange
                        secondary: '#FFD700', // Yellow
                        accent: '#FF4500', // Red
                        neutral: '#F5F5DC', // Beige
                        dark: '#333333', // Dark gray
                        herb: '#228B22', // Green
                        sweet: '#8A2BE2', // Purple
                        clean: '#FFFFFF', // White
                        rich: '#A52A2A', // Brown
                    },
                    fontFamily: {
                        sans: ['Inter', 'sans-serif'],
                        display: ['Montserrat', 'sans-serif'],
                    },
                }
            }
        }
    </script>
    <style type="text/tailwindcss">
        @layer utilities {
            .content-auto {
                content-visibility: auto;
            }
            .text-shadow {
                text-shadow: 0 2px 4px rgba(0,0,0,0.1);
            }
            .bg-gradient-appetite {
                background: linear-gradient(135deg, #FF8C00 0%, #FF4500 100%);
            }
            .card-hover {
                transition: transform 0.3s ease, box-shadow 0.3s ease;
            }
            .card-hover:hover {
                transform: translateY(-5px);
                box-shadow: 0 10px 25px -5px rgba(0, 0, 0, 0.1);
            }
        }
    </style>
</head>
<body class="bg-neutral text-dark font-sans">
    <!-- Navigation -->
    <nav class="fixed w-full bg-white/90 backdrop-blur-sm z-50 transition-all duration-300 shadow-md" id="navbar">
        <div class="container mx-auto px-4 py-3 flex justify-between items-center">
            <div class="flex items-center">
                <span class="text-primary text-2xl font-bold">CookEase</span>
                <span class="ml-2 text-xs bg-herb text-white px-2 py-1 rounded-full">CA</span>
            </div>
            <div class="hidden md:flex space-x-8">
                <a href="#problems" class="font-medium hover:text-primary transition-colors">Problems</a>
                <a href="#targets" class="font-medium hover:text-primary transition-colors">Targets</a>
                <a href="#design" class="font-medium hover:text-primary transition-colors">Design</a>
                <a href="#functions" class="font-medium hover:text-primary transition-colors">Functions</a>
            </div>
            <button class="md:hidden text-dark text-xl">
                <i class="fa fa-bars"></i>
            </button>
        </div>
    </nav>

    <!-- Hero Section -->
    <header class="pt-24 pb-16 md:pt-32 md:pb-24 bg-gradient-appetite text-white">
        <div class="container mx-auto px-4">
            <div class="max-w-4xl mx-auto text-center">
                <h1 class="text-[clamp(2.5rem,5vw,4rem)] font-bold leading-tight text-shadow mb-6">
                    CookEase!
                </h1>
                <p class="text-[clamp(1.2rem,2vw,1.5rem)] mb-8">
                    "Less mess. Less stress. More ease in every meal."
                </p>
                <div class="flex flex-col sm:flex-row justify-center gap-4 mb-10">
                    <a href="#design" class="bg-white text-primary px-8 py-3 rounded-full font-semibold hover:bg-neutral transition-colors shadow-lg">
                        Explore Design
                    </a>
                    <a href="#functions" class="bg-transparent border-2 border-white text-white px-8 py-3 rounded-full font-semibold hover:bg-white/10 transition-colors">
                        Discover Features
                    </a>
                </div>
                <div class="flex flex-wrap justify-center gap-8">
                    <div class="flex items-center">
                        <i class="fa fa-microphone text-2xl mr-2"></i>
                        <span>Voice Guidance</span>
                    </div>
                    <div class="flex items-center">
                        <i class="fa fa-cutlery text-2xl mr-2"></i>
                        <span>Smart Spices</span>
                    </div>
                    <div class="flex items-center">
                        <i class="fa fa-calendar text-2xl mr-2"></i>
                        <span>Meal Planning</span>
                    </div>
                    <div class="flex items-center">
                        <i class="fa fa-shopping-cart text-2xl mr-2"></i>
                        <span>Smart Shopping</span>
                    </div>
                </div>
            </div>
        </div>
    </header>

    <!-- Problems Section -->
    <section id="problems" class="py-16 bg-white">
        <div class="container mx-auto px-4">
            <div class="max-w-4xl mx-auto">
                <h2 class="text-[clamp(1.8rem,3vw,2.5rem)] font-bold text-dark mb-10 text-center">
                    The Cooking Challenges We Solve
                </h2>
                <div class="grid md:grid-cols-2 gap-8">
                    <div class="bg-neutral/50 p-6 rounded-xl shadow-sm card-hover">
                        <div class="text-primary text-3xl mb-4">
                            <i class="fa fa-clock-o"></i>
                        </div>
                        <h3 class="text-xl font-bold mb-3">Time Constraints</h3>
                        <p class="text-gray-700">
                            Busy schedules make it challenging to plan, shop, and prepare meals. Our system streamlines the entire process, from recipe discovery to cleanup.
                        </p>
                    </div>
                    <div class="bg-neutral/50 p-6 rounded-xl shadow-sm card-hover">
                        <div class="text-primary text-3xl mb-4">
                            <i class="fa fa-question-circle"></i>
                        </div>
                        <h3 class="text-xl font-bold mb-3">Cooking Skills</h3>
                        <p class="text-gray-700">
                            Many lack confidence in the kitchen. Our voice-guided system provides step-by-step instructions, making complex recipes accessible to everyone.
                        </p>
                    </div>
                    <div class="bg-neutral/50 p-6 rounded-xl shadow-sm card-hover">
                        <div class="text-primary text-3xl mb-4">
                            <i class="fa fa-shopping-basket"></i>
                        </div>
                        <h3 class="text-xl font-bold mb-3">Shopping Hassles</h3>
                        <p class="text-gray-700">
                            Forgetting ingredients or buying duplicates is common. Our smart shopping list and integration with local stores eliminate these issues.
                        </p>
                    </div>
                    <div class="bg-neutral/50 p-6 rounded-xl shadow-sm card-hover">
                        <div class="text-primary text-3xl mb-4">
                            <i class="fa fa-leaf"></i>
                        </div>
                        <h3 class="text-xl font-bold mb-3">Food Waste</h3>
                        <p class="text-gray-700">
                            Ingredients often go to waste due to poor planning. Our expiration tracking and recipe suggestions help use everything you buy.
                        </p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Target Audience Section -->
    <section id="targets" class="py-16 bg-neutral/30">
        <div class="container mx-auto px-4">
            <div class="max-w-4xl mx-auto">
                <h2 class="text-[clamp(1.8rem,3vw,2.5rem)] font-bold text-dark mb-10 text-center">
                    Designed For You
                </h2>
                <div class="grid md:grid-cols-3 gap-6">
                    <div class="bg-white rounded-xl overflow-hidden shadow-md card-hover">
                        <div class="h-48 bg-primary/20 flex items-center justify-center">
                            <i class="fa fa-graduation-cap text-6xl text-primary"></i>
                        </div>
                        <div class="p-6">
                            <h3 class="text-xl font-bold mb-2">College Students</h3>
                            <p class="text-gray-700">
                                Living away from home for the first time? Learn to cook simple, delicious meals without the stress.
                            </p>
                        </div>
                    </div>
                    <div class="bg-white rounded-xl overflow-hidden shadow-md card-hover">
                        <div class="h-48 bg-secondary/20 flex items-center justify-center">
                            <i class="fa fa-briefcase text-6xl text-secondary"></i>
                        </div>
                        <div class="p-6">
                            <h3 class="text-xl font-bold mb-2">Busy Professionals</h3>
                            <p class="text-gray-700">
                                Short on time but want home-cooked meals? Our system helps you cook efficiently, even on weeknights.
                            </p>
                        </div>
                    </div>
                    <div class="bg-white rounded-xl overflow-hidden shadow-md card-hover">
                        <div class="h-48 bg-herb/20 flex items-center justify-center">
                            <i class="fa fa-home text-6xl text-herb"></i>
                        </div>
                        <div class="p-6">
                            <h3 class="text-xl font-bold mb-2">Young Adults Living Alone</h3>
                            <p class="text-gray-700">
                                Discover the joy of cooking for one with recipes that minimize waste and maximize flavor.
                            </p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Design Section -->
    <section id="design" class="py-16 bg-white">
        <div class="container mx-auto px-4">
            <div class="max-w-6xl mx-auto">
                <h2 class="text-[clamp(1.8rem,3vw,2.5rem)] font-bold text-dark mb-10 text-center">
                    Modern Design for Your Kitchen
                </h2>
                
                <!-- Main Components -->
                <div class="mb-16">
                    <h3 class="text-2xl font-bold mb-8 text-center">Main Components</h3>
                    <div class="grid md:grid-cols-3 gap-8">
                        <div class="bg-neutral/50 rounded-xl overflow-hidden shadow-md card-hover">
                            <div class="h-48 bg-primary/30 flex items-center justify-center p-4">
                                <i class="fa fa-microphone text-6xl text-primary"></i>
                            </div>
                            <div class="p-6">
                                <h4 class="text-xl font-bold mb-2 text-primary">Voice-Guided Cooking Hub</h4>
                                <p class="text-gray-700">
                                    Touch-free, recipe-by-step guidance with a compact screen for visuals and timers. Syncs with your calendar and entertainment apps.
                                </p>
                                <ul class="mt-4 space-y-2">
                                    <li class="flex items-start">
                                        <i class="fa fa-check text-herb mt-1 mr-2"></i>
                                        <span>Voice commands: "Next step," "Repeat that," "How much garlic?"</span>
                                    </li>
                                    <li class="flex items-start">
                                        <i class="fa fa-check text-herb mt-1 mr-2"></i>
                                        <span>Syncs with Spotify/YouTube for entertainment while cooking</span>
                                    </li>
                                </ul>
                            </div>
                        </div>
                        
                        <div class="bg-neutral/50 rounded-xl overflow-hidden shadow-md card-hover">
                            <div class="h-48 bg-rich/30 flex items-center justify-center p-4">
                                <i class="fa fa-flask text-6xl text-rich"></i>
                            </div>
                            <div class="p-6">
                                <h4 class="text-xl font-bold mb-2 text-rich">Magnetic Spice Pod Carousel</h4>
                                <p class="text-gray-700">
                                    Holds 6-8 refillable spice pods with click-to-dispense system. Pre-labeled and pre-mixed for convenience.
                                </p>
                                <ul class="mt-4 space-y-2">
                                    <li class="flex items-start">
                                        <i class="fa fa-check text-herb mt-1 mr-2"></i>
                                        <span>One click = ¼ tsp of your favorite spice blend</span>
                                    </li>
                                    <li class="flex items-start">
                                        <i class="fa fa-check text-herb mt-1 mr-2"></i>
                                        <span>Curated refill packs for different cuisines available</span>
                                    </li>
                                </ul>
                            </div>
                        </div>
                        
                        <div class="bg-neutral/50 rounded-xl overflow-hidden shadow-md card-hover">
                            <div class="h-48 bg-herb/30 flex items-center justify-center p-4">
                                <i class="fa fa-cutlery text-6xl text-herb"></i>
                            </div>
                            <div class="p-6">
                                <h4 class="text-xl font-bold mb-2 text-herb">Stand-to-Cook Tray</h4>
                                <p class="text-gray-700">
                                    Lightweight, non-slip cutting board and ingredient tray designed for comfort and easy storage.
                                </p>
                                <ul class="mt-4 space-y-2">
                                    <li class="flex items-start">
                                        <i class="fa fa-check text-herb mt-1 mr-2"></i>
                                        <span>Encourages upright posture for comfortable cooking</span>
                                    </li>
                                    <li class="flex items-start">
                                        <i class="fa fa-check text-herb mt-1 mr-2"></i>
                                        <span>Foldable design for vertical storage</span>
                                    </li>
                                </ul>
                            </div>
                        </div>
                    </div>
                </div>
                
                <!-- App Design Mockup -->
                <div class="bg-gradient-to-r from-primary/10 to-herb/10 rounded-2xl p-8 md:p-12">
                    <h3 class="text-2xl font-bold mb-6 text-center">App Interface</h3>
                    <div class="flex flex-col md:flex-row items-center gap-8">
                        <div class="w-full md:w-1/2">
                            <div class="relative">
                                <div class="bg-white rounded-3xl shadow-2xl overflow-hidden border-8 border-dark max-w-xs mx-auto">
                                    <div class="bg-gradient-appetite h-24 flex items-center justify-center">
                                        <h4 class="text-white font-bold text-xl">CookEase</h4>
                                    </div>
                                    <div class="p-4 h-[400px] overflow-y-auto">
                                        <!-- App content mockup -->
                                        <div class="mb-4">
                                            <div class="bg-neutral rounded-lg p-3 mb-3">
                                                <div class="flex justify-between items-center mb-2">
                                                    <h5 class="font-bold">Tonight's Dinner</h5>
                                                    <span class="text-xs bg-herb text-white px-2 py-1 rounded-full">30 min</span>
                                                </div>
                                                <p class="text-sm">Teriyaki Chicken with Stir Fry Veggies</p>
                                                <div class="flex justify-between mt-2 text-xs text-gray-500">
                                                    <span>Ready in: 6:00 PM</span>
                                                    <span><i class="fa fa-bell"></i> Reminder set</span>
                                                </div>
                                            </div>
                                            
                                            <div class="bg-neutral rounded-lg p-3 mb-3">
                                                <h5 class="font-bold mb-2">Your Spice Collection</h5>
                                                <div class="grid grid-cols-3 gap-2">
                                                    <div class="bg-white rounded p-2 text-center text-xs">
                                                        <div class="w-8 h-8 bg-primary/20 rounded-full mx-auto mb-1"></div>
                                                        <span>Teriyaki</span>
                                                    </div>
                                                    <div class="bg-white rounded p-2 text-center text-xs">
                                                        <div class="w-8 h-8 bg-rich/20 rounded-full mx-auto mb-1"></div>
                                                        <span>Italian Herbs</span>
                                                    </div>
                                                    <div class="bg-white rounded p-2 text-center text-xs">
                                                        <div class="w-8 h-8 bg-accent/20 rounded-full mx-auto mb-1"></div>
                                                        <span>Spicy Chili</span>
                                                    </div>
                                                </div>
                                            </div>
                                            
                                            <div class="bg-neutral rounded-lg p-3 mb-3">
                                                <h5 class="font-bold mb-2">Shopping List</h5>
                                                <ul class="space-y-1 text-sm">
                                                    <li class="flex items-center">
                                                        <input type="checkbox" class="mr-2">
                                                        <span>Chicken breast (1 lb)</span>
                                                    </li>
                                                    <li class="flex items-center">
                                                        <input type="checkbox" class="mr-2">
                                                        <span>Broccoli (1 head)</span>
                                                    </li>
                                                    <li class="flex items-center">
                                                        <input type="checkbox" class="mr-2" checked>
                                                        <span>Soy sauce (1 cup)</span>
                                                    </li>
                                                </ul>
                                            </div>
                                            
                                            <div class="bg-neutral rounded-lg p-3">
                                                <h5 class="font-bold mb-2">Quick Recipes</h5>
                                                <div class="space-y-2">
                                                    <div class="flex items-center bg-white rounded p-2">
                                                        <div class="w-10 h-10 bg-herb/20 rounded-full flex items-center justify-center mr-3">
                                                            <i class="fa fa-leaf text-herb"></i>
                                                        </div>
                                                        <div>
                                                            <p class="font-medium text-sm">Avocado Toast</p>
                                                            <p class="text-xs text-gray-500">3 ingredients • 5 min</p>
                                                        </div>
                                                    </div>
                                                    <div class="flex items-center bg-white rounded p-2">
                                                        <div class="w-10 h-10 bg-rich/20 rounded-full flex items-center justify-center mr-3">
                                                            <i class="fa fa-coffee text-rich"></i>
                                                        </div>
                                                        <div>
                                                            <p class="font-medium text-sm">Instant Noodles</p>
                                                            <p class="text-xs text-gray-500">2 ingredients • 3 min</p>
                                                        </div>
                                                    </div>
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                    <div class="border-t border-gray-200 p-2 flex justify-around">
                                        <i class="fa fa-home text-primary text-xl"></i>
                                        <i class="fa fa-book text-gray-400 text-xl"></i>
                                        <i class="fa fa-shopping-basket text-gray-400 text-xl"></i>
                                        <i class="fa fa-user text-gray-400 text-xl"></i>
                                    </div>
                                </div>
                                <div class="absolute -bottom-4 -right-4 bg-white rounded-full p-2 shadow-lg">
                                    <i class="fa fa-microphone text-primary text-xl"></i>
                                </div>
                            </div>
                        </div>
                        
                        <div class="w-full md:w-1/2">
                            <h4 class="text-xl font-bold mb-4">Intuitive Mobile Experience</h4>
                            <p class="text-gray-700 mb-6">
                                Our app is designed with a clean, intuitive interface that makes meal planning, recipe discovery, and shopping a breeze.
                            </p>
                            <ul class="space-y-4">
                                <li class="flex items-start">
                                    <div class="bg-primary/20 rounded-full p-2 mr-4">
                                        <i class="fa fa-calendar text-primary"></i>
                                    </div>
                                    <div>
                                        <h5 class="font-bold mb-1">Smart Meal Scheduling</h5>
                                        <p class="text-gray-700 text-sm">
                                            Plan your meals for the week and set reminders to start cooking.
                                        </p>
                                    </div>
                                </li>
                                <li class="flex items-start">
                                    <div class="bg-herb/20 rounded-full p-2 mr-4">
                                        <i class="fa fa-search text-herb"></i>
                                    </div>
                                    <div>
                                        <h5 class="font-bold mb-1">Personalized Recipe Recommendations</h5>
                                        <p class="text-gray-700 text-sm">
                                            Discover recipes based on your spice collection and dietary preferences.
                                        </p>
                                    </div>
                                </li>
                                <li class="flex items-start">
                                    <div class="bg-rich/20 rounded-full p-2 mr-4">
                                        <i class="fa fa-shopping-cart text-rich"></i>
                                    </div>
                                    <div>
                                        <h5 class="font-bold mb-1">Integrated Shopping List</h5>
                                        <p class="text-gray-700 text-sm">
                                            Automatically generate shopping lists and compare prices at local stores.
                                        </p>
                                    </div>
                                </li>
                            </ul>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Functions Section -->
    <section id="functions" class="py-16 bg-gradient-to-b from-white to-neutral/30">
        <div class="container mx-auto px-4">
            <div class="max-w-6xl mx-auto">
                <h2 class="text-[clamp(1.8rem,3vw,2.5rem)] font-bold text-dark mb-10 text-center">
                    Powerful Features
                </h2>
                
                <!-- Feature Grid -->
                <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-6">
                    <div class="bg-white rounded-xl p-6 shadow-sm card-hover">
                        <div class="text-primary text-3xl mb-4">
                            <i class="fa fa-microphone"></i>
                        </div>
                        <h3 class="text-xl font-bold mb-3">Voice-Activated Recipes</h3>
                        <p class="text-gray-700">
                            Cook hands-free with voice commands. Ask for the next step, ingredient measurements, or cooking times.
                        </p>
                    </div>
                    
                    <div class="bg-white rounded-xl p-6 shadow-sm card-hover">
                        <div class="text-secondary text-3xl mb-4">
                            <i class="fa fa-map-marker"></i>
                        </div>
                        <h3 class="text-xl font-bold mb-3">Smart Shopping</h3>
                        <p class="text-gray-700">
                            Find the best prices at nearby supermarkets and Amazon Fresh. See real-time availability and compare options.
                        </p>
                    </div>
                    
                    <div class="bg-white rounded-xl p-6 shadow-sm card-hover">
                        <div class="text-herb text-3xl mb-4">
                            <i class="fa fa-refresh"></i>
                        </div>
                        <h3 class="text-xl font-bold mb-3">Spice Substitution</h3>
                        <p class="text-gray-700">
                            Don't have a specific spice? Our system suggests substitutes based on what you already have.
                        </p>
                    </div>
                    
                    <div class="bg-white rounded-xl p-6 shadow-sm card-hover">
                        <div class="text-rich text-3xl mb-4">
                            <i class="fa fa-clock-o"></i>
                        </div>
                        <h3 class="text-xl font-bold mb-3">Expiration Tracking</h3>
                        <p class="text-gray-700">
                            Keep track of ingredient expiration dates and get recipe suggestions for items about to expire.
                        </p>
                    </div>
                    
                    <div class="bg-white rounded-xl p-6 shadow-sm card-hover">
                        <div class="text-accent text-3xl mb-4">
                            <i class="fa fa-users"></i>
                        </div>
                        <h3 class="text-xl font-bold mb-3">Cooking Community</h3>
                        <p class="text-gray-700">
                            Share recipes, cooking tips, and photos with friends. Rate dishes and get inspired by others.
                        </p>
                    </div>
                    
                    <div class="bg-white rounded-xl p-6 shadow-sm card-hover">
                        <div class="text-sweet text-3xl mb-4">
                            <i class="fa fa-money"></i>
                        </div>
                        <h3 class="text-xl font-bold mb-3">Wallet & Accounting</h3>
                        <p class="text-gray-700">
                            Track your spending on groceries and meals. Set budgets and see monthly breakdowns.
                        </p>
                    </div>
                </div>
                
                <!-- California-Specific Features -->
                <div class="mt-16 bg-gradient-to-r from-primary/10 to-secondary/10 rounded-2xl p-8 md:p-12">
                    <h3 class="text-2xl font-bold mb-6 text-center">California-Specific Features</h3>
                    <div class="grid md:grid-cols-2 gap-8">
                        <div class="bg-white/80 backdrop-blur-sm rounded-xl p-6 shadow-sm">
                            <div class="text-primary text-3xl mb-4">
                                <i class="fa fa-leaf"></i>
                            </div>
                            <h4 class="text-xl font-bold mb-3">Farm-to-Table Integration</h4>
                            <p class="text-gray-700">
                                Connect with local California farmers markets and get fresh, seasonal produce recommendations.
                            </p>
                        </div>
                        
                        <div class="bg-white/80 backdrop-blur-sm rounded-xl p-6 shadow-sm">
                            <div class="text-herb text-3xl mb-4">
                                <i class="fa fa-sun-o"></i>
                            </div>
                            <h4 class="text-xl font-bold mb-3">Seasonal Recipe Suggestions</h4>
                            <p class="text-gray-700">
                                Get recipes tailored to California's abundant seasonal produce, from avocados to citrus fruits.
                            </p>
                        </div>
                        
                        <div class="bg-white/80 backdrop-blur-sm rounded-xl p-6 shadow-sm">
                            <div class="text-rich text-3xl mb-4">
                                <i class="fa fa-map"></i>
                            </div>
                            <h4 class="text-xl font-bold mb-3">Local Grocery Partnerships</h4>
                            <p class="text-gray-700">
                                Exclusive deals and discounts at California grocery chains like Whole Foods, Trader Joe's, and Ralphs.
                            </p>
                        </div>
                        
                        <div class="bg-white/80 backdrop-blur-sm rounded-xl p-6 shadow-sm">
                            <div class="text-sweet text-3xl mb-4">
                                <i class="fa fa-tint"></i>
                            </div>
                            <h4 class="text-xl font-bold mb-3">Water Conservation Tips</h4>
                            <p class="text-gray-700">
                                Eco-friendly cooking suggestions that help conserve water, an important resource in California.
                            </p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- CTA Section -->
    <section class="py-16 bg-gradient-appetite text-white">
        <div class="container mx-auto px-4">
            <div class="max-w-4xl mx-auto text-center">
                <h2 class="text-[clamp(1.8rem,3vw,2.5rem)] font-bold mb-6">
                    Ready to Transform Your Cooking Experience?
                </h2>
                <p class="text-[clamp(1rem,1.5vw,1.2rem)] mb-8">
                    Join thousands of Californians who are simplifying their cooking routine with CookEase.
                </p>
                <div class="flex flex-col sm:flex-row justify-center gap-4">
                    <a href="#" class="bg-white text-primary px-8 py-3 rounded-full font-semibold hover:bg-neutral transition-colors shadow-lg">
                        Pre-Order Now
                    </a>
                    <a href="#" class="bg-transparent border-2 border-white text-white px-8 py-3 rounded-full font-semibold hover:bg-white/10 transition-colors">
                        Learn More
                    </a>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-dark text-white py-12">
        <div class="container mx-auto px-4">
            <div class="grid md:grid-cols-4 gap-8">
                <div>
                    <h3 class="text-xl font-bold mb-4">CookEase</h3>
                    <p class="text-gray-400 mb-4">
                        Making cooking simple, accessible, and enjoyable for everyone.
                    </p>
                    <div class="flex space-x-4">
                        <a href="#" class="text-gray-400 hover:text-white transition-colors">
                            <i class="fa fa-facebook"></i>
                        </a>
                        <a href="#" class="text-gray-400 hover:text-white transition-colors">
                            <i class="fa fa-twitter"></i>
                        </a>
                        <a href="#" class="text-gray-400 hover:text-white transition-colors">
                            <i class="fa fa-instagram"></i>
                        </a>
                    </div>
                </div>
                
                <div>
                    <h3 class="text-lg font-bold mb-4">Quick Links</h3>
                    <ul class="space-y-2">
                        <li><a href="#problems" class="text-gray-400 hover:text-white transition-colors">Problems</a></li>
                        <li><a href="#targets" class="text-gray-400 hover:text-white transition-colors">Targets</a></li>
                        <li><a href="#design" class="text-gray-400 hover:text-white transition-colors">Design</a></li>
                        <li><a href="#functions" class="text-gray-400 hover:text-white transition-colors">Functions</a></li>
                    </ul>
                </div>
                
                <div>
                    <h3 class="text-lg font-bold mb-4">Support</h3>
                    <ul class="space-y-2">
                        <li><a href="#" class="text-gray-400 hover:text-white transition-colors">FAQs</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white transition-colors">Contact Us</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white transition-colors">Privacy Policy</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white transition-colors">Terms of Service</a></li>
                    </ul>
                </div>
                
                <div>
                    <h3 class="text-lg font-bold mb-4">Subscribe</h3>
                    <p class="text-gray-400 mb-4">
                        Get updates on new features and California-specific recipes.
                    </p>
                    <form class="mb-4">
                        <div class="flex">
                            <input type="email" placeholder="Your email" class="px-4 py-2 rounded-l-full w-full focus:outline-none text-dark">
                            <button type="submit" class="bg-primary text-white px-4 py-2 rounded-r-full hover:bg-primary/80 transition-colors">
                                <i class="fa fa-paper-plane"></i>
                            </button>
                        </div>
                    </form>
                    <p class="text-xs text-gray-500">
                        By subscribing, you agree to our Privacy Policy and consent to receive updates.
                    </p>
                </div>
            </div>
            
            <div class="border-t border-gray-800 mt-8 pt-8 text-center text-gray-500 text-sm">
                <p>&copy; 2025 CookEase. All rights reserved.</p>
            </div>
        </div>
    </footer>

    <script>
        // Navbar scroll effect
        const navbar = document.getElementById('navbar');
        window.addEventListener('scroll', () => {
            if (window.scrollY > 100) {
                navbar.classList.add('py-2');
                navbar.classList.remove('py-3');
                navbar.classList.add('shadow-md');
            } else {
                navbar.classList.add('py-3');
                navbar.classList.remove('py-2');
                navbar.classList.remove('shadow-md');
            }
        });

        // Smooth scrolling for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                
                const targetId = this.getAttribute('href');
                if (targetId === '#') return;
                
                const targetElement = document.querySelector(targetId);
                if (targetElement) {
                    window.scrollTo({
                        top: targetElement.offsetTop - 80,
                        behavior: 'smooth'
                    });
                }
            });
        });
    </script>
</body>
</html>
    
