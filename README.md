# eugenianui-sclav.
<!DOCTYPE html>
<html lang="ro">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AnimeSoft - Universul Tău Colorat</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Quicksand:wght@300;400;500;600;700&display=swap');
        
        :root {
            --vibrant-pink: #ff4d6d;
            --deep-purple: #7209b7;
            --electric-blue: #4cc9f0;
            --neon-orange: #ff9e00;
        }

        body {
            font-family: 'Quicksand', sans-serif;
            background-color: #fffafa;
            color: #2d3436;
        }

        .glass-nav {
            background: rgba(255, 255, 255, 0.9);
            backdrop-filter: blur(15px);
            -webkit-backdrop-filter: blur(15px);
            border-bottom: 3px solid var(--vibrant-pink);
        }

        .anime-card {
            transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
            background: white;
            border-radius: 2rem;
            overflow: hidden;
            box-shadow: 0 10px 20px rgba(0,0,0,0.05);
        }

        .anime-card:hover {
            transform: translateY(-12px) scale(1.02);
            box-shadow: 0 30px 40px -15px rgba(255, 77, 109, 0.3);
        }

        .floating {
            animation: floating 5s ease-in-out infinite;
        }

        @keyframes floating {
            0%, 100% { transform: translateY(0px) rotate(0deg); }
            50% { transform: translateY(-20px) rotate(2deg); }
        }

        .gradient-text {
            background: linear-gradient(135deg, var(--vibrant-pink), var(--deep-purple), var(--electric-blue));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-size: 200% 200%;
            animation: gradient-shift 8s linear infinite;
        }

        @keyframes gradient-shift {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        .img-container {
            position: relative;
            overflow: hidden;
            height: 380px;
        }

        .img-container img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.6s ease;
        }

        .anime-card:hover .img-container img {
            transform: scale(1.1);
        }

        .bg-pattern {
            background-image: radial-gradient(var(--vibrant-pink) 0.5px, transparent 0.5px), radial-gradient(var(--electric-blue) 0.5px, #fffafa 0.5px);
            background-size: 40px 40px;
            background-position: 0 0, 20px 20px;
            opacity: 0.1;
            position: fixed;
            inset: 0;
            z-index: -1;
        }

        .btn-vibrant {
            background: linear-gradient(90deg, var(--vibrant-pink), var(--neon-orange));
            color: white;
            transition: all 0.3s ease;
            box-shadow: 0 10px 15px -3px rgba(255, 77, 109, 0.4);
        }

        .btn-vibrant:hover {
            filter: brightness(1.1);
            transform: translateY(-2px);
            box-shadow: 0 15px 20px -5px rgba(255, 77, 109, 0.5);
        }
    </style>
</head>
<body class="overflow-x-hidden">

    <div class="bg-pattern"></div>

    <!-- Navigație -->
    <nav class="fixed w-full z-50 glass-nav">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex items-center justify-between h-20">
                <div class="flex items-center gap-2">
                    <div class="bg-gradient-to-tr from-pink-500 to-yellow-500 p-2.5 rounded-2xl shadow-lg shadow-pink-200">
                        <i class="fas fa-bolt text-white text-xl"></i>
                    </div>
                    <span class="text-3xl font-black tracking-tighter text-gray-800">ANIME<span class="text-pink-500">SOFT</span></span>
                </div>
                
                <div class="hidden md:flex items-center space-x-10">
                    <a href="#" class="text-pink-600 font-bold border-b-4 border-pink-500 pb-1">Acasă</a>
                    <a href="#" class="text-gray-500 hover:text-purple-600 font-bold transition">Catalog</a>
                    <a href="#" class="text-gray-500 hover:text-blue-500 font-bold transition">Comunitate</a>
                    <a href="#" class="text-gray-500 hover:text-orange-500 font-bold transition">Magazin</a>
                </div>

                <div class="flex items-center gap-4">
                    <button class="bg-gray-100 text-gray-700 px-6 py-2.5 rounded-2xl font-bold hover:bg-gray-200 transition">Login</button>
                    <button class="btn-vibrant px-8 py-2.5 rounded-2xl font-bold">Premium</button>
                </div>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <header class="relative pt-48 pb-32 px-4 overflow-hidden">
        <div class="max-w-7xl mx-auto flex flex-col lg:flex-row items-center gap-20">
            <div class="flex-1 text-center lg:text-left z-10">
                <div class="inline-block bg-yellow-100 text-orange-600 px-5 py-2 rounded-full text-sm font-black mb-8 animate-bounce">
                    🚀 NOI LANSĂRI DISPONIBILE
                </div>
                <h1 class="text-6xl md:text-8xl font-black mb-8 leading-none text-gray-900">
                    Găsește-ți <br> <span class="gradient-text">Pacea Prin Anime</span>
                </h1>
                <p class="text-gray-600 text-xl mb-12 max-w-xl leading-relaxed font-medium">
                    Explorează o selecție curată de serii anime relaxante, povești magice și aventuri vizuale într-un spațiu creat special pentru tine.
                </p>
                <div class="flex flex-col sm:flex-row gap-6 justify-center lg:justify-start">
                    <button class="btn-vibrant text-xl px-12 py-5 rounded-[2rem] font-black tracking-wide">
                        Începe Vizionarea
                    </button>
                    <button class="bg-white border-4 border-purple-100 text-purple-600 hover:border-purple-200 px-12 py-5 rounded-[2rem] font-black transition-all">
                        Lista Mea
                    </button>
                </div>
            </div>
            
            <div class="flex-1 relative">
                <!-- Ilustrație Principală (folosind imaginea încărcată image_74acfd.jpg pentru context sau Dandadan image_7f8e83.jpg ca erou) -->
                <div class="relative z-10 floating">
                    <img src="image_7f8e83.jpg" 
                         alt="[Imagine Dandadan]" 
                         class="rounded-[4rem] shadow-[0_50px_100px_-20px_rgba(255,77,109,0.5)] border-[15px] border-white w-full max-w-xl mx-auto transform -rotate-2">
                    
                    <!-- Element decorativ suplimentar din imagini -->
                    <div class="absolute -bottom-10 -right-10 w-48 h-48 sm:w-64 sm:h-64 rounded-[3rem] border-[10px] border-white shadow-2xl overflow-hidden rotate-12 hidden md:block">
                        <img src="image_7f91c4.jpg" alt="[Imagine Call of the Night]" class="w-full h-full object-cover">
                    </div>
                </div>
                
                <div class="absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2 w-[140%] h-[140%] bg-gradient-to-tr from-pink-200/40 to-blue-200/40 rounded-full blur-[120px] -z-10"></div>
            </div>
        </div>
    </header>

    <main class="max-w-7xl mx-auto px-4 py-20">
        
        <!-- Secțiune: Populare în acest sezon -->
        <section class="mb-32">
            <div class="flex justify-between items-end mb-16 px-4">
                <div>
                    <h2 class="text-5xl font-black text-gray-900 mb-4">Populare în <span class="text-pink-500">acest sezon</span></h2>
                    <p class="text-gray-500 text-lg font-bold">Cele mai iubite titluri din comunitate</p>
                </div>
                <a href="#" class="text-pink-500 font-black flex items-center gap-2 hover:gap-4 transition-all">
                    Vezi tot catalogul <i class="fas fa-arrow-right"></i>
                </a>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-10">
                <!-- Card 1: Dandadan -->
                <div class="anime-card p-6 border-b-8 border-pink-400">
                    <div class="img-container rounded-[1.5rem] mb-6 shadow-xl">
                        <img src="image_7f8e83.jpg" alt="[Imagine Dandadan]">
                        <div class="absolute top-5 right-5">
                            <span class="bg-pink-600 text-white px-4 py-1.5 rounded-full text-xs font-black">POPULAR</span>
                        </div>
                    </div>
                    <div class="px-2">
                        <span class="text-pink-400 text-xs font-black tracking-widest uppercase">Action / Sci-Fi</span>
                        <h3 class="text-2xl font-black text-gray-900 mt-2">Dandadan</h3>
                        <div class="flex items-center mt-4 text-orange-400">
                            <i class="fas fa-star mr-1"></i> <span class="font-black text-gray-800">4.9</span>
                            <span class="text-gray-300 ml-auto font-bold text-sm">EP 12</span>
                        </div>
                    </div>
                </div>

                <!-- Card 2: Call of the Night -->
                <div class="anime-card p-6 border-b-8 border-purple-400">
                    <div class="img-container rounded-[1.5rem] mb-6 shadow-xl">
                        <img src="image_7f91c4.jpg" alt="[Imagine Call of the Night]">
                        <div class="absolute top-5 right-5">
                            <span class="bg-purple-600 text-white px-4 py-1.5 rounded-full text-xs font-black">TRENDING</span>
                        </div>
                    </div>
                    <div class="px-2">
                        <span class="text-purple-400 text-xs font-black tracking-widest uppercase">Romance / Night</span>
                        <h3 class="text-2xl font-black text-gray-900 mt-2">Call of the Night</h3>
                        <div class="flex items-center mt-4 text-orange-400">
                            <i class="fas fa-star mr-1"></i> <span class="font-black text-gray-800">4.8</span>
                            <span class="text-gray-300 ml-auto font-bold text-sm">S2</span>
                        </div>
                    </div>
                </div>

                <!-- Card 3: Haikyuu -->
                <div class="anime-card p-6 border-b-8 border-orange-400">
                    <div class="img-container rounded-[1.5rem] mb-6 shadow-xl">
                        <img src="image_7f95e1.jpg" alt="[Imagine Haikyuu]">
                        <div class="absolute top-5 right-5">
                            <span class="bg-orange-600 text-white px-4 py-1.5 rounded-full text-xs font-black">SPORTS</span>
                        </div>
                    </div>
                    <div class="px-2">
                        <span class="text-orange-400 text-xs font-black tracking-widest uppercase">Sports / Team</span>
                        <h3 class="text-2xl font-black text-gray-900 mt-2">Haikyuu!!</h3>
                        <div class="flex items-center mt-4 text-orange-400">
                            <i class="fas fa-star mr-1"></i> <span class="font-black text-gray-800">5.0</span>
                            <span class="text-gray-300 ml-auto font-bold text-sm">FINAL</span>
                        </div>
                    </div>
                </div>

                <!-- Card 4: Sakurasou -->
                <div class="anime-card p-6 border-b-8 border-blue-400">
                    <div class="img-container rounded-[1.5rem] mb-6 shadow-xl">
                        <img src="image_7f9220.jpg" alt="[Imagine Sakurasou]">
                        <div class="absolute top-5 right-5">
                            <span class="bg-blue-600 text-white px-4 py-1.5 rounded-full text-xs font-black">SLICE OF LIFE</span>
                        </div>
                    </div>
                    <div class="px-2">
                        <span class="text-blue-400 text-xs font-black tracking-widest uppercase">Drama / Life</span>
                        <h3 class="text-2xl font-black text-gray-900 mt-2">Sakurasou</h3>
                        <div class="flex items-center mt-4 text-orange-400">
                            <i class="fas fa-star mr-1"></i> <span class="font-black text-gray-800">4.7</span>
                            <span class="text-gray-300 ml-auto font-bold text-sm">CLASSIC</span>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Secțiune Specială: Recomandări Dark -->
        <section class="mb-32">
            <div class="bg-gray-900 rounded-[4rem] p-12 md:p-20 relative overflow-hidden shadow-2xl">
                <div class="absolute top-0 right-0 w-1/2 h-full bg-gradient-to-l from-red-600/20 to-transparent"></div>
                
                <div class="flex flex-col lg:flex-row items-center gap-16 relative z-10">
                    <div class="flex-1 order-2 lg:order-1">
                        <h2 class="text-white text-5xl font-black mb-8">Ești gata pentru <span class="text-red-500">Darkness</span>?</h2>
                        <p class="text-gray-400 text-xl mb-12">
                            Unele povești nu sunt doar despre pace. Explorează latura întunecată a anime-ului cu titluri precum Future Diary.
                        </p>
                        <button class="bg-red-600 hover:bg-red-700 text-white px-10 py-4 rounded-2xl font-black transition-all">
                            Explorează Secțiunea Dark
                        </button>
                    </div>
                    <div class="flex-1 order-1 lg:order-2">
                        <img src="image_7f9582.jpg" alt="[Imagine Future Diary]" class="rounded-[3rem] shadow-2xl border-8 border-gray-800 transform rotate-3 hover:rotate-0 transition-all duration-500">
                    </div>
                </div>
            </div>
        </section>

        <!-- Galerie de Comunitate -->
        <section class="mb-20 px-4">
            <h2 class="text-4xl font-black text-center mb-16">Capturi din <span class="text-blue-500">Comunitate</span></h2>
            <div class="columns-1 md:columns-2 lg:columns-3 gap-8 space-y-8">
                <div class="break-inside-avoid rounded-3xl overflow-hidden shadow-lg border-4 border-white">
                    <img src="image_74acbd.jpg" alt="[Imagine Community 1]" class="w-full">
                </div>
                <div class="break-inside-avoid rounded-3xl overflow-hidden shadow-lg border-4 border-white bg-pink-50 p-8 text-center">
                    <i class="fas fa-quote-left text-pink-400 text-4xl mb-6"></i>
                    <p class="text-gray-700 font-bold text-xl italic">"Cea mai bună platformă pentru a găsi titluri noi și a socializa cu alți fani!"</p>
                    <p class="mt-6 font-black text-pink-500">- OtakuMaster99</p>
                </div>
                <div class="break-inside-avoid rounded-3xl overflow-hidden shadow-lg border-4 border-white">
                    <img src="image_74acfd.jpg" alt="[Imagine Community 2]" class="w-full">
                </div>
            </div>
        </section>

    </main>

    <!-- Footer Vibrant -->
    <footer class="bg-white border-t-8 border-pink-500 pt-24 pb-12">
        <div class="max-w-7xl mx-auto px-4">
            <div class="grid grid-cols-1 md:grid-cols-4 gap-16 mb-20">
                <div class="col-span-2">
                    <div class="flex items-center gap-2 mb-8">
                        <div class="bg-pink-500 p-2.5 rounded-2xl">
                            <i class="fas fa-heart text-white"></i>
                        </div>
                        <span class="text-3xl font-black tracking-tighter text-gray-800">ANIME<span class="text-pink-500">SOFT</span></span>
                    </div>
                    <p class="text-gray-500 font-bold text-lg max-w-sm">Universul tău digital pentru tot ce înseamnă cultură anime și manga. Calitate, comunitate și pasiune.</p>
                </div>
                <div>
                    <h4 class="text-xl font-black mb-6">Link-uri Rapide</h4>
                    <ul class="space-y-4 text-gray-500 font-bold">
                        <li><a href="#" class="hover:text-pink-500 transition">Catalog Anime</a></li>
                        <li><a href="#" class="hover:text-pink-500 transition">Manga Online</a></li>
                        <li><a href="#" class="hover:text-pink-500 transition">Știri</a></li>
                    </ul>
                </div>
                <div>
                    <h4 class="text-xl font-black mb-6">Social</h4>
                    <div class="flex gap-4">
                        <a href="#" class="w-12 h-12 bg-pink-100 text-pink-500 rounded-xl flex items-center justify-center text-xl hover:bg-pink-500 hover:text-white transition-all"><i class="fab fa-discord"></i></a>
                        <a href="#" class="w-12 h-12 bg-pink-100 text-pink-500 rounded-xl flex items-center justify-center text-xl hover:bg-pink-500 hover:text-white transition-all"><i class="fab fa-instagram"></i></a>
                        <a href="#" class="w-12 h-12 bg-pink-100 text-pink-500 rounded-xl flex items-center justify-center text-xl hover:bg-pink-500 hover:text-white transition-all"><i class="fab fa-twitter"></i></a>
                    </div>
                </div>
            </div>
            <div class="text-center pt-12 border-t border-gray-100">
                <p class="text-gray-400 font-black tracking-widest uppercase text-sm">&copy; 2026 AnimeSoft Studio. Toate drepturile rezervate ⚡</p>
            </div>
        </div>
    </footer>

</body>
</html>
