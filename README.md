# bio_kitty
Підготовка до НМТ з біології від Ані❤️ 
<!DOCTYPE html>
<html lang="uk">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Підготовка до НМТ з біології | Цифровий котик</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        beige: {
                            light: '#F5F0E6',
                            DEFAULT: '#E8DCCA',
                            dark: '#D4C5B1',
                        },
                        brown: {
                            light: '#B8A99A',
                            DEFAULT: '#9A8A78',
                            dark: '#7D6E5D',
                        }
                    },
                    fontFamily: {
                        'sans': ['Montserrat', 'sans-serif'],
                        'serif': ['Merriweather', 'serif'],
                    }
                }
            }
        }
    </script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@300;400;500;600;700&family=Merriweather:wght@300;400;700&display=swap');
        
        body {
            background-color: #F5F0E6;
            font-family: 'Montserrat', sans-serif;
        }
        
        .cat-paw {
            position: relative;
            display: inline-block;
        }
        
        .cat-paw::after {
            content: '🐾';
            position: absolute;
            font-size: 1.2rem;
            opacity: 0;
            transition: all 0.3s ease;
        }
        
        .cat-paw:hover::after {
            opacity: 1;
            transform: translateY(5px);
        }
        
        .page-container {
            display: none;
        }
        
        .page-container.active {
            display: block;
        }
        
        .cat-ears {
            position: relative;
        }
        
        .cat-ears::before,
        .cat-ears::after {
            content: '';
            position: absolute;
            top: -15px;
            width: 15px;
            height: 15px;
            background-color: #D4C5B1;
            border-radius: 50% 50% 0 0;
        }
        
        .cat-ears::before {
            left: -5px;
            transform: rotate(-30deg);
        }
        
        .cat-ears::after {
            right: -5px;
            transform: rotate(30deg);
        }
    </style>
</head>
<body class="min-h-screen flex flex-col">
    <!-- Логотип і навігація -->
    <header class="bg-beige-dark shadow-md">
        <div class="container mx-auto px-4 py-3">
            <div class="flex flex-col md:flex-row justify-between items-center">
                <div class="flex items-center mb-4 md:mb-0">
                    <div class="relative mr-3">
                        <svg class="w-12 h-12" viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg">
                            <circle cx="50" cy="50" r="45" fill="#9A8A78" />
                            <circle cx="35" cy="40" r="5" fill="#F5F0E6" />
                            <circle cx="65" cy="40" r="5" fill="#F5F0E6" />
                            <path d="M40 60 Q50 70 60 60" stroke="#F5F0E6" stroke-width="3" fill="none" />
                            <path d="M30 30 Q20 15 10 25" stroke="#9A8A78" stroke-width="3" fill="none" />
                            <path d="M70 30 Q80 15 90 25" stroke="#9A8A78" stroke-width="3" fill="none" />
                            <ellipse cx="30" cy="70" rx="5" ry="3" fill="#F5F0E6" transform="rotate(-20 30 70)" />
                            <ellipse cx="70" cy="70" rx="5" ry="3" fill="#F5F0E6" transform="rotate(20 70 70)" />
                        </svg>
                    </div>
                    <h1 class="text-xl md:text-2xl font-bold text-brown-dark">Цифровий котик</h1>
                </div>
                <nav class="w-full md:w-auto"> <ul class="flex flex-wrap justify-center md:justify-end space-x-1 md:space-x-4">
                        <li><button onclick="showPage('home')" class="cat-paw px-3 py-2 rounded-lg hover:bg-beige transition-colors nav-link active" data-page="home">Головна</button></li>
                        <li><button onclick="showPage('notes')" class="cat-paw px-3 py-2 rounded-lg hover:bg-beige transition-colors nav-link" data-page="notes">Конспекти</button></li>
                        <li><button onclick="showPage('tests')" class="cat-paw px-3 py-2 rounded-lg hover:bg-beige transition-colors nav-link" data-page="tests">Тести</button></li>
                        <li><button onclick="showPage('contacts')" class="cat-paw px-3 py-2 rounded-lg hover:bg-beige transition-colors nav-link" data-page="contacts">Контакти</button></li>
                        <li><button onclick="showPage('card')" class="cat-paw px-3 py-2 rounded-lg hover:bg-beige transition-colors nav-link" data-page="card">Візитівка</button></li>
                    </ul>
                </nav>
            </div>
        </div>
    </header>

    <!-- Основний контент -->
    <main class="flex-grow container mx-auto px-4 py-8">
        <!-- Головна сторінка -->
        <div id="home" class="page-container active">
            <div class="flex flex-col md:flex-row items-center md:items-start gap-8">
                <div class="w-full md:w-1/3 flex justify-center">
                    <div class="relative rounded-full overflow-hidden w-64 h-64 border-4 border-beige-dark shadow-lg">
                        <svg class="w-full h-full" viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg">
                            <circle cx="50" cy="50" r="50" fill="#D4C5B1" />
                            <circle cx="35" cy="40" r="5" fill="#7D6E5D" />
                            <circle cx="65" cy="40" r="5" fill="#7D6E5D" />
                            <path d="M40 60 Q50 70 60 60" stroke="#7D6E5D" stroke-width="3" fill="none" />
                            <ellipse cx="50" cy="45" rx="10" ry="5" fill="#F5F0E6" opacity="0.5" />
                            <path d="M25 25 Q15 15 20 5" stroke="#D4C5B1" stroke-width="3" fill="none" />
                            <path d="M75 25 Q85 15 80 5" stroke="#D4C5B1" stroke-width="3" fill="none" />
                        </svg>
                        <div class="absolute bottom-0 left-0 right-0 bg-beige-dark bg-opacity-70 py-2 text-center text-white">
                            Фото викладача
                        </div>
                    </div>
                </div>
                <div class="w-full md:w-2/3">
                    <h2 class="text-3xl font-serif font-bold mb-4 text-brown-dark cat-ears relative inline-block">Про мене</h2>
                    <p class="mb-4 text-brown">Вітаю! Я ваш викладач біології та автор курсу підготовки до НМТ. Маю багаторічний досвід викладання та підготовки учнів до іспитів. Моя методика поєднує структуровані конспекти, інтерактивні тести та індивідуальний підхід до кожного учня.</p>
                    <p class="mb-6 text-brown">На цьому сайті ви знайдете всі необхідні матеріали для успішної підготовки до НМТ з біології. Конспекти розділені за темами відповідно до програми, а тести допоможуть перевірити ваші знання.</p>
                    
                    <div class="bg-beige rounded-lg p-6 shadow-md">
                        <h3 class="text-xl font-semibold mb-3 text-brown-dark">Чому варто обрати мій курс:</h3>
                        <ul class="list-disc list-inside space-y-2 text-brown">
                            <li>Структуровані матеріали, що відповідають програмі НМТ</li>
                            <li>Інтерактивні тести для закріплення знань</li>
                            <li>Індивідуальний підхід та консультації</li>
                            <li>Доступ до матеріалів 24/7</li>
                            <li>Регулярні оновлення та додаткові матеріали</li>
                        </ul>
                    </div> <div class="mt-6 flex flex-wrap gap-3">
                        <a href="#" onclick="showPage('notes')" class="inline-block bg-brown text-white px-5 py-2 rounded-lg hover:bg-brown-dark transition-colors">Переглянути конспекти</a>
                        <a href="#" onclick="showPage('tests')" class="inline-block bg-brown-light text-white px-5 py-2 rounded-lg hover:bg-brown transition-colors">Спробувати тести</a>
                    </div>
                </div>
            </div>
        </div>

        <!-- Сторінка з конспектами -->
        <div id="notes" class="page-container">
            <h2 class="text-3xl font-serif font-bold mb-6 text-brown-dark cat-ears relative inline-block">Конспекти</h2>
            <p class="mb-6 text-brown">Тут ви знайдете структуровані конспекти з усіх тем, необхідних для успішного складання НМТ з біології.</p>
            
            <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                <!-- Розділ 1 -->
                <div class="bg-beige rounded-lg p-6 shadow-md">
                    <h3 class="text-xl font-semibold mb-3 text-brown-dark flex items-center">
                        <span class="mr-2">🧬</span> Розділ 1: Молекулярний рівень організації життя
                    </h3>
                    <ul class="space-y-3">
                        <li class="flex items-center">
                            <svg class="w-5 h-5 mr-2 text-brown" fill="currentColor" viewBox="0 0 20 20">
                                <path d="M9 2a1 1 0 000 2h2a1 1 0 100-2H9z"></path>
                                <path fill-rule="evenodd" d="M4 5a2 2 0 012-2 3 3 0 003 3h2a3 3 0 003-3 2 2 0 012 2v11a2 2 0 01-2 2H6a2 2 0 01-2-2V5zm3 4a1 1 0 000 2h.01a1 1 0 100-2H7zm3 0a1 1 0 000 2h3a1 1 0 100-2h-3zm-3 4a1 1 0 100 2h.01a1 1 0 100-2H7zm3 0a1 1 0 100 2h3a1 1 0 100-2h-3z" clip-rule="evenodd"></path>
                            </svg>
                            <a href="#" class="text-brown-dark hover:underline">Хімічні елементи живих організмів</a>
                        </li>
                        <li class="flex items-center">
                            <svg class="w-5 h-5 mr-2 text-brown" fill="currentColor" viewBox="0 0 20 20">
                                <path d="M9 2a1 1 0 000 2h2a1 1 0 100-2H9z"></path>
                                <path fill-rule="evenodd" d="M4 5a2 2 0 012-2 3 3 0 003 3h2a3 3 0 003-3 2 2 0 012 2v11a2 2 0 01-2 2H6a2 2 0 01-2-2V5zm3 4a1 1 0 000 2h.01a1 1 0 100-2H7zm3 0a1 1 0 000 2h3a1 1 0 100-2h-3zm-3 4a1 1 0 100 2h.01a1 1 0 100-2H7zm3 0a1 1 0 100 2h3a1 1 0 100-2h-3z" clip-rule="evenodd"></path>
                            </svg>
                            <a href="#" class="text-brown-dark hover:underline">Білки, їхня структура та функції</a>
                        </li>
                        <li class="flex items-center">
                            <svg class="w-5 h-5 mr-2 text-brown" fill="currentColor" viewBox="0 0 20 20">
                                <path d="M9 2a1 1 0 000 2h2a1 1 0 100-2H9z"></path>
                                <path fill-rule="evenodd" d="M4 5a2 2 0 012-2 3 3 0 003 3h2a3 3 0 003-3 2 2 0 012 2v11a2 2 0 01-2 2H6a2 2 0 01-2-2V5zm3 4a1 1 0 000 2h.01a1 1 0 100-2H7zm3 0a1 1 0 000 2h3a1 1 0 100-2h-3zm-3 4a1 1 0 100 2h.01a1 1 0 100-2H7zm3 0a1 1 0 100 2h3a1 1 0 100-2h-3z" clip-rule="evenodd"></path>
                            </svg>
                            <a href="#" class="text-brown-dark hover:underline">Нуклеїнові кислоти</a>
                        </li>
                    </ul>
                </div>
                
                <!-- Розділ 2 -->
                <div class="bg-beige rounded-lg p-6 shadow-md">
                    <h3 class="text-xl font-semibold mb-3 text-brown-dark flex items-center">
                        <span class="mr-2">🦠</span> Розділ 2: Клітинний рівень організації життя
                    </h3>
                    <ul class="space-y-3">
                        <li class="flex items-center"> <svg class="w-5 h-5 mr-2 text-brown" fill="currentColor" viewBox="0 0 20 20">
                                <path d="M9 2a1 1 0 000 2h2a1 1 0 100-2H9z"></path>
                                <path fill-rule="evenodd" d="M4 5a2 2 0 012-2 3 3 0 003 3h2a3 3 0 003-3 2 2 0 012 2v11a2 2 0 01-2 2H6a2 2 0 01-2-2V5zm3 4a1 1 0 000 2h.01a1 1 0 100-2H7zm3 0a1 1 0 000 2h3a1 1 0 100-2h-3zm-3 4a1 1 0 100 2h.01a1 1 0 100-2H7zm3 0a1 1 0 100 2h3a1 1 0 100-2h-3z" clip-rule="evenodd"></path>
                            </svg>
                            <a href="#" class="text-brown-dark hover:underline">Структура клітини</a>
                        </li>
                        <li class="flex items-center">
                            <svg class="w-5 h-5 mr-2 text-brown" fill="currentColor" viewBox="0 0 20 20">
                                <path d="M9 2a1 1 0 000 2h2a1 1 0 100-2H9z"></path>
                                <path fill-rule="evenodd" d="M4 5a2 2 0 012-2 3 3 0 003 3h2a3 3 0 003-3 2 2 0 012 2v11a2 2 0 01-2 2H6a2 2 0 01-2-2V5zm3 4a1 1 0 000 2h.01a1 1 0 100-2H7zm3 0a1 1 0 000 2h3a1 1 0 100-2h-3zm-3 4a1 1 0 100 2h.01a1 1 0 100-2H7zm3 0a1 1 0 100 2h3a1 1 0 100-2h-3z" clip-rule="evenodd"></path>
                            </svg>
                            <a href="#" class="text-brown-dark hover:underline">Клітинний цикл</a>
                        </li>
                        <li class="flex items-center">
                            <svg class="w-5 h-5 mr-2 text-brown" fill="currentColor" viewBox="0 0 20 20">
                                <path d="M9 2a1 1 0 000 2h2a1 1 0 100-2H9z"></path>
                                <path fill-rule="evenodd" d="M4 5a2 2 0 012-2 3 3 0 003 3h2a3 3 0 003-3 2 2 0 012 2v11a2 2 0 01-2 2H6a2 2 0 01-2-2V5zm3 4a1 1 0 000 2h.01a1 1 0 100-2H7zm3 0a1 1 0 000 2h3a1 1 0 100-2h-3zm-3 4a1 1 0 100 2h.01a1 1 0 100-2H7zm3 0a1 1 0 100 2h3a1 1 0 100-2h-3z" clip-rule="evenodd"></path>
                            </svg>
                            <a href="#" class="text-brown-dark hover:underline">Мітоз і мейоз</a>
                        </li>
                    </ul>
                </div>
                
                <!-- Розділ 3 -->
                <div class="bg-beige rounded-lg p-6 shadow-md">
                    <h3 class="text-xl font-semibold mb-3 text-brown-dark flex items-center">
                        <span class="mr-2">🌱</span> Розділ 3: Організмовий рівень життя
                    </h3>
                    <ul class="space-y-3">
                        <li class="flex items-center">
                            <svg class="w-5 h-5 mr-2 text-brown" fill="currentColor" viewBox="0 0 20 20">
                                <path d="M9 2a1 1 0 000 2h2a1 1 0 100-2H9z"></path>
                                <path fill-rule="evenodd" d="M4 5a2 2 0 012-2 3 3 0 003 3h2a3 3 0 003-3 2 2 0 012 2v11a2 2 0 01-2 2H6a2 2 0 01-2-2V5zm3 4a1 1 0 000 2h.01a1 1 0 100-2H7zm3 0a1 1 0 000 2h3a1 1 0 100-2h-3zm-3 4a1 1 0 100 2h.01a1 1 0 100-2H7zm3 0a1 1 0 100 2h3a1 1 0 100-2h-3z" clip-rule="evenodd"></path>
                            </svg>
                            <a href="#" class="text-brown-dark hover:underline">Бактерії та віруси</a>
                        </li>
                        <li class="flex items-center">
                            <svg class="w-5 h-5 mr-2 text-brown" fill="currentColor" viewBox="0 0 20 20">
                                <path d="M9 2a1 1 0 000 2h2a1 1 0 100-2H9z"></path>
                                <path fill-rule="evenodd" d="M4 5a2 2 0 012-2 3 3 0 003 3h2a3 3 0 003-3 2 2 0 012 2v11a2 2 0 01-2 2H6a2 2 0 01-2-2V5zm3 4a1 1 0 000 2h.01a1 1 0 100-2H7zm3 0a1 1 0 000 2h3a1 1 0 100-2h-3zm-3 4a1 1 0 100 2h.01a1 1 0 100-2H7zm3 0a1 1 0 100 2h3a1 1 0 100-2h-3z" clip-rule="evenodd"></path>
                            </svg>
                            <a href="#" class="text-brown-dark hover:underline">Рослини</a>
                        </li>
                        <li class="flex items-center"> <svg class="w-5 h-5 mr-2 text-brown" fill="currentColor" viewBox="0 0 20 20">
                                <path d="M9 2a1 1 0 000 2h2a1 1 0 100-2H9z"></path>
                                <path fill-rule="evenodd" d="M4 5a2 2 0 012-2 3 3 0 003 3h2a3 3 0 003-3 2 2 0 012 2v11a2 2 0 01-2 2H6a2 2 0 01-2-2V5zm3 4a1 1 0 000 2h.01a1 1 0 100-2H7zm3 0a1 1 0 000 2h3a1 1 0 100-2h-3zm-3 4a1 1 0 100 2h.01a1 1 0 100-2H7zm3 0a1 1 0 100 2h3a1 1 0 100-2h-3z" clip-rule="evenodd"></path>
                            </svg>
                            <a href="#" class="text-brown-dark hover:underline">Тварини</a>
                        </li>
                    </ul>
                </div>
                
                <!-- Розділ 4 -->
                <div class="bg-beige rounded-lg p-6 shadow-md">
                    <h3 class="text-xl font-semibold mb-3 text-brown-dark flex items-center">
                        <span class="mr-2">👤</span> Розділ 4: Людина
                    </h3>
                    <ul class="space-y-3">
                        <li class="flex items-center">
                            <svg class="w-5 h-5 mr-2 text-brown" fill="currentColor" viewBox="0 0 20 20">
                                <path d="M9 2a1 1 0 000 2h2a1 1 0 100-2H9z"></path>
                                <path fill-rule="evenodd" d="M4 5a2 2 0 012-2 3 3 0 003 3h2a3 3 0 003-3 2 2 0 012 2v11a2 2 0 01-2 2H6a2 2 0 01-2-2V5zm3 4a1 1 0 000 2h.01a1 1 0 100-2H7zm3 0a1 1 0 000 2h3a1 1 0 100-2h-3zm-3 4a1 1 0 100 2h.01a1 1 0 100-2H7zm3 0a1 1 0 100 2h3a1 1 0 100-2h-3z" clip-rule="evenodd"></path>
                            </svg>
                            <a href="#" class="text-brown-dark hover:underline">Тканини та органи</a>
                        </li>
                        <li class="flex items-center">
                            <svg class="w-5 h-5 mr-2 text-brown" fill="currentColor" viewBox="0 0 20 20">
                                <path d="M9 2a1 1 0 000 2h2a1 1 0 100-2H9z"></path>
                                <path fill-rule="evenodd" d="M4 5a2 2 0 012-2 3 3 0 003 3h2a3 3 0 003-3 2 2 0 012 2v11a2 2 0 01-2 2H6a2 2 0 01-2-2V5zm3 4a1 1 0 000 2h.01a1 1 0 100-2H7zm3 0a1 1 0 000 2h3a1 1 0 100-2h-3zm-3 4a1 1 0 100 2h.01a1 1 0 100-2H7zm3 0a1 1 0 100 2h3a1 1 0 100-2h-3z" clip-rule="evenodd"></path>
                            </svg>
                            <a href="#" class="text-brown-dark hover:underline">Системи органів</a>
                        </li>
                        <li class="flex items-center">
                            <svg class="w-5 h-5 mr-2 text-brown" fill="currentColor" viewBox="0 0 20 20">
                                <path d="M9 2a1 1 0 000 2h2a1 1 0 100-2H9z"></path>
                                <path fill-rule="evenodd" d="M4 5a2 2 0 012-2 3 3 0 003 3h2a3 3 0 003-3 2 2 0 012 2v11a2 2 0 01-2 2H6a2 2 0 01-2-2V5zm3 4a1 1 0 000 2h.01a1 1 0 100-2H7zm3 0a1 1 0 000 2h3a1 1 0 100-2h-3zm-3 4a1 1 0 100 2h.01a1 1 0 100-2H7zm3 0a1 1 0 100 2h3a1 1 0 100-2h-3z" clip-rule="evenodd"></path>
                            </svg>
                            <a href="#" class="text-brown-dark hover:underline">Фізіологія людини</a>
                        </li>
                    </ul>
                </div>
            </div>
        </div>

        <!-- Сторінка з тестами -->
        <div id="tests" class="page-container">
            <h2 class="text-3xl font-serif font-bold mb-6 text-brown-dark cat-ears relative inline-block">Тести</h2>
            <p class="mb-6 text-brown">Перевірте свої знання за допомогою інтерактивних тестів. Виберіть розділ та почніть тестування.</p>
            
            <div class="mb-8">
                <h3 class="text-xl font-semibold mb-4 text-brown-dark">Оберіть розділ:</h3>
                <div class="flex flex-wrap gap-3">
                    <button onclick="selectTestSection(1)" class="test-section-btn px-4 py-2 rounded-lg bg-beige hover:bg-beige-dark transition-colors">Молекулярний рівень</button> <button onclick="selectTestSection(2)" class="test-section-btn px-4 py-2 rounded-lg bg-beige hover:bg-beige-dark transition-colors">Клітинний рівень</button>
                    <button onclick="selectTestSection(3)" class="test-section-btn px-4 py-2 rounded-lg bg-beige hover:bg-beige-dark transition-colors">Організмовий рівень</button>
                    <button onclick="selectTestSection(4)" class="test-section-btn px-4 py-2 rounded-lg bg-beige hover:bg-beige-dark transition-colors">Людина</button>
                </div>
            </div>
            
            <!-- Інтерактивний тест -->
            <div id="test-container" class="bg-beige rounded-lg p-6 shadow-md hidden">
                <h3 id="test-title" class="text-xl font-semibold mb-4 text-brown-dark">Тест: Молекулярний рівень</h3>
                
                <div id="question-container" class="mb-6">
                    <p id="question-text" class="text-lg mb-3 text-brown-dark">Яка з наведених молекул є мономером білків?</p>
                    <div class="space-y-2">
                        <div class="flex items-center">
                            <input type="radio" id="answer1" name="answer" class="mr-2">
                            <label for="answer1" class="text-brown">Глюкоза</label>
                        </div>
                        <div class="flex items-center">
                            <input type="radio" id="answer2" name="answer" class="mr-2">
                            <label for="answer2" class="text-brown">Амінокислота</label>
                        </div>
                        <div class="flex items-center">
                            <input type="radio" id="answer3" name="answer" class="mr-2">
                            <label for="answer3" class="text-brown">Нуклеотид</label>
                        </div>
                        <div class="flex items-center">
                            <input type="radio" id="answer4" name="answer" class="mr-2">
                            <label for="answer4" class="text-brown">Жирна кислота</label>
                        </div>
                    </div>
                </div>
                
                <div class="flex justify-between">
                    <button id="prev-question" class="px-4 py-2 rounded-lg bg-brown-light text-white hover:bg-brown transition-colors">Попереднє питання</button>
                    <button id="next-question" class="px-4 py-2 rounded-lg bg-brown text-white hover:bg-brown-dark transition-colors">Наступне питання</button>
                </div>
                
                <div id="test-progress" class="mt-4 bg-beige-light rounded-full h-2.5">
                    <div class="bg-brown-dark h-2.5 rounded-full" style="width: 25%"></div>
                </div>
                <p class="text-right text-sm mt-1 text-brown">Питання 1 з 4</p>
            </div>
            
            <!-- Посилання на зовнішні тести -->
            <div class="mt-8">
                <h3 class="text-xl font-semibold mb-4 text-brown-dark">Додаткові тести:</h3>
                <ul class="space-y-3">
                    <li class="flex items-center">
                        <svg class="w-5 h-5 mr-2 text-brown" fill="currentColor" viewBox="0 0 20 20">
                            <path fill-rule="evenodd" d="M12.293 5.293a1 1 0 011.414 0l4 4a1 1 0 010 1.414l-4 4a1 1 0 01-1.414-1.414L14.586 11H3a1 1 0 110-2h11.586l-2.293-2.293a1 1 0 010-1.414z" clip-rule="evenodd"></path>
                        </svg>
                        <a href="#" class="text-brown-dark hover:underline">Тести ЗНО минулих років</a>
                    </li>
                    <li class="flex items-center">
                        <svg class="w-5 h-5 mr-2 text-brown" fill="currentColor" viewBox="0 0 20 20">
                            <path fill-rule="evenodd" d="M12.293 5.293a1 1 0 011.414 0l4 4a1 1 0 010 1.414l-4 4a1 1 0 01-1.414-1.414L14.586 11H3a1 1 0 110-2h11.586l-2.293-2.293a1 1 0 010-1.414z" clip-rule="evenodd"></path>
                        </svg> <a href="#" class="text-brown-dark hover:underline">Тренувальні тести НМТ</a>
                    </li>
                    <li class="flex items-center">
                        <svg class="w-5 h-5 mr-2 text-brown" fill="currentColor" viewBox="0 0 20 20">
                            <path fill-rule="evenodd" d="M12.293 5.293a1 1 0 011.414 0l4 4a1 1 0 010 1.414l-4 4a1 1 0 01-1.414-1.414L14.586 11H3a1 1 0 110-2h11.586l-2.293-2.293a1 1 0 010-1.414z" clip-rule="evenodd"></path>
                        </svg>
                        <a href="#" class="text-brown-dark hover:underline">Тематичні тести з біології</a>
                    </li>
                </ul>
            </div>
        </div>

        <!-- Сторінка з контактами -->
        <div id="contacts" class="page-container">
            <h2 class="text-3xl font-serif font-bold mb-6 text-brown-dark cat-ears relative inline-block">Контакти</h2>
            <p class="mb-6 text-brown">Зв'яжіться зі мною, якщо у вас виникли питання або ви хочете записатися на консультацію.</p>
            
            <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                <div class="bg-beige rounded-lg p-6 shadow-md">
                    <h3 class="text-xl font-semibold mb-4 text-brown-dark">Соціальні мережі</h3>
                    <div class="flex flex-col space-y-4">
                        <a href="#" class="flex items-center text-brown-dark hover:text-brown transition-colors">
                            <div class="w-12 h-12 bg-brown-light rounded-full flex items-center justify-center mr-4">
                                <i class="fab fa-telegram-plane text-white text-2xl"></i>
                            </div>
                            <span>Telegram</span>
                        </a>
                        <a href="#" class="flex items-center text-brown-dark hover:text-brown transition-colors">
                            <div class="w-12 h-12 bg-brown-light rounded-full flex items-center justify-center mr-4">
                                <i class="fab fa-instagram text-white text-2xl"></i>
                            </div>
                            <span>Instagram</span>
                        </a>
                        <a href="#" class="flex items-center text-brown-dark hover:text-brown transition-colors">
                            <div class="w-12 h-12 bg-brown-light rounded-full flex items-center justify-center mr-4">
                                <i class="fab fa-viber text-white text-2xl"></i>
                            </div>
                            <span>Viber</span>
                        </a>
                    </div>
                </div>
                
                <div class="bg-beige rounded-lg p-6 shadow-md">
                    <h3 class="text-xl font-semibold mb-4 text-brown-dark">Зворотній зв'язок</h3>
                    <form class="space-y-4">
                        <div>
                            <label for="name" class="block text-brown mb-1">Ім'я</label>
                            <input type="text" id="name" class="w-full px-3 py-2 border border-beige-dark rounded-lg focus:outline-none focus:ring-2 focus:ring-brown-light">
                        </div>
                        <div>
                            <label for="email" class="block text-brown mb-1">Email</label>
                            <input type="email" id="email" class="w-full px-3 py-2 border border-beige-dark rounded-lg focus:outline-none focus:ring-2 focus:ring-brown-light">
                        </div>
                        <div>
                            <label for="message" class="block text-brown mb-1">Повідомлення</label>
                            <textarea id="message" rows="4" class="w-full px-3 py-2 border border-beige-dark rounded-lg focus:outline-none focus:ring-2 focus:ring-brown-light"></textarea>
                        </div>
                        <button type="button" class="px-4 py-2 bg-brown text-white rounded-lg hover:bg-brown-dark transition-colors">Надіслати</button> </form>
                    <p class="mt-4 text-sm text-brown">Це демо-форма. Для справжнього зв'язку використовуйте соціальні мережі.</p>
                </div>
            </div>
        </div>

        <!-- Сторінка з візитівкою -->
        <div id="card" class="page-container">
            <h2 class="text-3xl font-serif font-bold mb-6 text-brown-dark cat-ears relative inline-block">Моя візитівка</h2>
            
            <div class="bg-beige rounded-lg overflow-hidden shadow-lg">
                <div class="md:flex">
                    <div class="md:w-1/3 bg-beige-dark p-6 flex items-center justify-center">
                        <div class="relative w-48 h-48 rounded-full overflow-hidden border-4 border-beige shadow-lg">
                            <svg class="w-full h-full" viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg">
                                <circle cx="50" cy="50" r="50" fill="#D4C5B1" />
                                <circle cx="35" cy="40" r="5" fill="#7D6E5D" />
                                <circle cx="65" cy="40" r="5" fill="#7D6E5D" />
                                <path d="M40 60 Q50 70 60 60" stroke="#7D6E5D" stroke-width="3" fill="none" />
                                <ellipse cx="50" cy="45" rx="10" ry="5" fill="#F5F0E6" opacity="0.5" />
                                <path d="M25 25 Q15 15 20 5" stroke="#D4C5B1" stroke-width="3" fill="none" />
                                <path d="M75 25 Q85 15 80 5" stroke="#D4C5B1" stroke-width="3" fill="none" />
                            </svg>
                        </div>
                    </div>
                    <div class="md:w-2/3 p-6">
                        <h3 class="text-2xl font-bold text-brown-dark mb-2">Підготовка до НМТ з біології</h3>
                        <p class="text-brown mb-4">Індивідуальні та групові заняття для успішного складання НМТ</p>
                        
                        <div class="mb-6">
                            <h4 class="text-lg font-semibold text-brown-dark mb-2">Переваги моїх занять:</h4>
                            <ul class="space-y-2">
                                <li class="flex items-start">
                                    <svg class="w-5 h-5 mr-2 text-brown-dark mt-0.5" fill="currentColor" viewBox="0 0 20 20">
                                        <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd"></path>
                                    </svg>
                                    <span class="text-brown">Індивідуальний підхід до кожного учня</span>
                                </li>
                                <li class="flex items-start">
                                    <svg class="w-5 h-5 mr-2 text-brown-dark mt-0.5" fill="currentColor" viewBox="0 0 20 20">
                                        <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd"></path>
                                    </svg>
                                    <span class="text-brown">Структуровані матеріали та конспекти</span>
                                </li>
                                <li class="flex items-start">
                                    <svg class="w-5 h-5 mr-2 text-brown-dark mt-0.5" fill="currentColor" viewBox="0 0 20 20">
                                        <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd"></path>
                                    </svg>
                                    <span class="text-brown">Регулярні тести та відстеження прогресу</span>
                                </li>
                                <li class="flex items-start"> <svg class="w-5 h-5 mr-2 text-brown-dark mt-0.5" fill="currentColor" viewBox="0 0 20 20">
                                        <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd"></path>
                                    </svg>
                                    <span class="text-brown">Доступ до онлайн-матеріалів 24/7</span>
                                </li>
                            </ul>
                        </div>
                        
                        <div class="mb-6">
                            <h4 class="text-lg font-semibold text-brown-dark mb-2">Формат занять:</h4>
                            <div class="flex flex-wrap gap-2">
                                <span class="px-3 py-1 bg-beige-dark rounded-full text-brown text-sm">Індивідуальні</span>
                                <span class="px-3 py-1 bg-beige-dark rounded-full text-brown text-sm">Групові (до 5 осіб)</span>
                                <span class="px-3 py-1 bg-beige-dark rounded-full text-brown text-sm">Онлайн</span>
                                <span class="px-3 py-1 bg-beige-dark rounded-full text-brown text-sm">Офлайн</span>
                            </div>
                        </div>
                        
                        <div class="flex items-center justify-between">
                            <div>
                                <h4 class="text-lg font-semibold text-brown-dark">Ціна:</h4>
                                <p class="text-2xl font-bold text-brown">від 300 грн / заняття</p>
                            </div>
                            <a href="#" onclick="showPage('contacts')" class="px-6 py-3 bg-brown text-white rounded-lg hover:bg-brown-dark transition-colors">Записатися</a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </main>

    <!-- Підвал -->
    <footer class="bg-beige-dark py-6 mt-8">
        <div class="container mx-auto px-4">
            <div class="flex flex-col md:flex-row justify-between items-center">
                <div class="mb-4 md:mb-0">
                    <div class="flex items-center">
                        <div class="relative mr-3">
                            <svg class="w-10 h-10" viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg">
                                <circle cx="50" cy="50" r="45" fill="#9A8A78" />
                                <circle cx="35" cy="40" r="5" fill="#F5F0E6" />
                                <circle cx="65" cy="40" r="5" fill="#F5F0E6" />
                                <path d="M40 60 Q50 70 60 60" stroke="#F5F0E6" stroke-width="3" fill="none" />
                            </svg>
                        </div>
                        <h2 class="text-lg font-bold text-brown-dark">Цифровий котик</h2>
                    </div>
                    <p class="text-sm text-brown mt-1">Підготовка до НМТ з біології</p>
                </div>
                <div class="flex space-x-4">
                    <a href="#" class="text-brown-dark hover:text-brown transition-colors">
                        <i class="fab fa-telegram-plane text-xl"></i>
                    </a>
                    <a href="#" class="text-brown-dark hover:text-brown transition-colors">
                        <i class="fab fa-instagram text-xl"></i>
                    </a>
                    <a href="#" class="text-brown-dark hover:text-brown transition-colors">
                        <i class="fab fa-viber text-xl"></i>
                    </a>
                </div>
            </div>
            <div class="mt-4 text-center text-sm text-brown">
                <p>&copy; 2023 Цифровий котик. Всі права захищені.</p>
            </div>
        </div>
    </footer>

    <script>
        // Функція для переключення між сторінками
        function showPage(pageId) {
            // Приховуємо всі сторінки document.querySelectorAll('.page-container').forEach(page => {
                page.classList.remove('active');
            });
            
            // Показуємо обрану сторінку
            document.getElementById(pageId).classList.add('active');
            
            // Оновлюємо активне посилання в навігації
            document.querySelectorAll('.nav-link').forEach(link => {
                link.classList.remove('active', 'bg-beige');
                if (link.getAttribute('data-page') === pageId) {
                    link.classList.add('active', 'bg-beige');
                }
            });
            
            // Прокручуємо сторінку вгору
            window.scrollTo(0, 0);
        }
        
        // Функція для вибору розділу тестів
        function selectTestSection(sectionId) {
            // Показуємо контейнер з тестом
            document.getElementById('test-container').classList.remove('hidden');
            
            // Оновлюємо заголовок тесту відповідно до обраного розділу
            const titles = [
                "Тест: Молекулярний рівень",
                "Тест: Клітинний рівень",
                "Тест: Організмовий рівень",
                "Тест: Людина"
            ];
            document.getElementById('test-title').textContent = titles[sectionId - 1];
            
            // Виділяємо активну кнопку розділу
            document.querySelectorAll('.test-section-btn').forEach((btn, index) => {
                if (index === sectionId - 1) {
                    btn.classList.add('bg-beige-dark');
                    btn.classList.remove('bg-beige');
                } else {
                    btn.classList.remove('bg-beige-dark');
                    btn.classList.add('bg-beige');
                }
            });
            
            // Прокручуємо до тесту
            document.getElementById('test-container').scrollIntoView({ behavior: 'smooth' });
        }
        
        // Ініціалізація сторінки
        document.addEventListener('DOMContentLoaded', function() {
            // Показуємо головну сторінку за замовчуванням
            showPage('home');
            
            // Обробники подій для кнопок тесту
            document.getElementById('next-question').addEventListener('click', function() {
                // Тут можна додати логіку для переходу до наступного питання
                alert('Перехід до наступного питання');
            });
            
            document.getElementById('prev-question').addEventListener('click', function() {
                // Тут можна додати логіку для переходу до попереднього питання
                alert('Перехід до попереднього питання');
            });
        });
    </script>
<script>(function(){function c(){var b=a.contentDocument||a.contentWindow.document;if(b){var d=b.createElement('script');d.innerHTML="window.__CF$cv$params={r:'965be60d8226247c',t:'MTc1MzYxNjgxMS4wMDAwMDA='};var a=document.createElement('script');a.nonce='';a.src='/cdn-cgi/challenge-platform/scripts/jsd/main.js';document.getElementsByTagName('head')[0].appendChild(a);";b.getElementsByTagName('head')[0].appendChild(d)}}if(document.body){var a=document.createElement('iframe');a.height=1;a.width=1;a.style.position='absolute';a.style.top=0;a.style.left=0;a.style.border='none';a.style.visibility='hidden';document.body.appendChild(a);if('loading'!==document.readyState)c();else if(window.addEventListener)document.addEventListener('DOMContentLoaded',c);else{var e=document.onreadystatechange||function(){};document.onreadystatechange=function(b){e(b);'loading'!==document.readyState&&(document.onreadystatechange=e,c())}}}})();</script></body>
</html>
