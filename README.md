<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sushan Mendaka | SM Studios</title>
    
    <!-- Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&family=JetBrains+Mono:wght@400;700&display=swap" rel="stylesheet">
    
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    
    <!-- FontAwesome for Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

    <script>
        tailwind.config = {
            theme: {
                extend: {
                    fontFamily: {
                        sans: ['Inter', 'sans-serif'],
                        mono: ['JetBrains Mono', 'monospace'],
                    },
                    colors: {
                        dark: '#030712', // Very deep gray/black
                        brand: {
                            400: '#60a5fa',
                            500: '#3b82f6',
                            600: '#2563eb',
                        }
                    },
                    animation: {
                        'float': 'float 6s ease-in-out infinite',
                        'glow': 'glow 2s ease-in-out infinite alternate',
                    },
                    keyframes: {
                        float: {
                            '0%, 100%': { transform: 'translateY(0)' },
                            '50%': { transform: 'translateY(-10px)' },
                        },
                        glow: {
                            '0%': { boxShadow: '0 0 5px rgba(59, 130, 246, 0.2)' },
                            '100%': { boxShadow: '0 0 20px rgba(59, 130, 246, 0.6), 0 0 40px rgba(59, 130, 246, 0.2)' }
                        }
                    }
                }
            }
        }
    </script>

    <style>
        body {
            background-color: #030712;
            color: #f8fafc;
            overflow-x: hidden;
        }

        /* Scrollbar styling */
        ::-webkit-scrollbar {
            width: 8px;
        }
        ::-webkit-scrollbar-track {
            background: #030712; 
        }
        ::-webkit-scrollbar-thumb {
            background: #1e3a8a; 
            border-radius: 4px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: #3b82f6; 
        }

        /* Typing Effect Cursor */
        .cursor::after {
            content: '|';
            animation: blink 1s step-start infinite;
            color: #3b82f6;
        }
        @keyframes blink {
            50% { opacity: 0; }
        }

        /* Scroll Reveal Classes */
        .reveal {
            opacity: 0;
            transform: translateY(30px);
            transition: all 0.8s ease-out;
        }
        .reveal.active {
            opacity: 1;
            transform: translateY(0);
        }

        /* Background grid effect */
        .bg-grid {
            background-size: 40px 40px;
            background-image: linear-gradient(to right, rgba(59, 130, 246, 0.05) 1px, transparent 1px),
                              linear-gradient(to bottom, rgba(59, 130, 246, 0.05) 1px, transparent 1px);
        }
        
        .glowing-border:hover {
            box-shadow: 0 0 15px rgba(59, 130, 246, 0.5);
            border-color: rgba(59, 130, 246, 0.8);
        }
    </style>
</head>
<body class="bg-grid antialiased selection:bg-brand-500 selection:text-white">

    <!-- Background glow elements -->
    <div class="fixed top-0 left-0 w-full h-full overflow-hidden -z-10 pointer-events-none">
        <div class="absolute top-[-10%] left-[-10%] w-[40%] h-[40%] rounded-full bg-brand-600/10 blur-[120px]"></div>
        <div class="absolute bottom-[-10%] right-[-10%] w-[40%] h-[40%] rounded-full bg-brand-600/10 blur-[120px]"></div>
    </div>

    <nav class="fixed w-full z-50 top-0 border-b border-white/5 bg-dark/80 backdrop-blur-md">
        <div class="max-w-6xl mx-auto px-6 py-4 flex justify-between items-center">
            <a href="#" class="text-xl font-bold tracking-tighter">
                SM<span class="text-brand-500">.</span>STUDIOS
            </a>
            <div class="hidden md:flex space-x-8 text-sm font-medium text-gray-400">
                <a href="#about" class="hover:text-brand-400 transition-colors">About</a>
                <a href="#skills" class="hover:text-brand-400 transition-colors">Tech Stack</a>
                <a href="#stats" class="hover:text-brand-400 transition-colors">Stats</a>
                <a href="#contact" class="hover:text-brand-400 transition-colors">Connect</a>
            </div>
            <!-- Mobile Menu Icon (Placeholder for interaction) -->
            <button class="md:hidden text-gray-400 hover:text-brand-400">
                <i class="fa-solid fa-bars text-xl"></i>
            </button>
        </div>
    </nav>

    <main class="pt-28 pb-16 px-6 max-w-6xl mx-auto flex flex-col gap-24">
        
        <section id="about" class="min-h-[70vh] flex flex-col justify-center reveal">
            <div class="max-w-3xl">
                <div class="inline-block px-3 py-1 mb-6 border border-brand-500/30 rounded-full bg-brand-500/10 text-brand-400 text-sm font-mono animate-float">
                    <i class="fa-solid fa-sparkles mr-2"></i> Welcome to my creative space
                </div>
                
                <h1 class="text-5xl md:text-7xl font-bold leading-tight mb-4">
                    👋 Hi, I'm <br/>
                    <span class="text-transparent bg-clip-text bg-gradient-to-r from-brand-400 to-blue-700">Sushan Mendaka</span>
                </h1>
                
                <h2 class="text-2xl md:text-4xl font-light text-gray-400 mb-8 h-12">
                    <span id="typewriter" class="cursor"></span>
                </h2>

                <p class="text-lg text-gray-400 mb-8 max-w-2xl leading-relaxed">
                    I build modern web applications and create creative digital experiences. From pixel-perfect UI designs to robust backend architectures and dynamic motion graphics.
                </p>

                <ul class="space-y-3 mb-10 text-gray-300">
                    <li class="flex items-center gap-3">
                        <i class="fa-solid fa-rocket text-brand-500"></i> Founder of <strong class="text-white ml-1">SM Studios</strong>
                    </li>
                    <li class="flex items-center gap-3">
                        <i class="fa-solid fa-laptop-code text-brand-500"></i> Developing modern and responsive websites
                    </li>
                    <li class="flex items-center gap-3">
                        <i class="fa-solid fa-pen-nib text-brand-500"></i> UI/UX Design & Branding
                    </li>
                    <li class="flex items-center gap-3">
                        <i class="fa-solid fa-film text-brand-500"></i> Video Editing & Motion Graphics
                    </li>
                    <li class="flex items-center gap-3">
                        <i class="fa-solid fa-seedling text-brand-500"></i> Always learning new technologies
                    </li>
                    <li class="flex items-center gap-3">
                        <i class="fa-solid fa-location-dot text-brand-500"></i> Colombo, Sri Lanka
                    </li>
                </ul>

                <blockquote class="border-l-4 border-brand-500 pl-4 italic text-gray-400 text-xl font-light">
                    "Design creates the experience. Code brings it to life."
                </blockquote>
            </div>
        </section>

        <section id="skills" class="py-10 scroll-mt-24 reveal">
            <div class="flex items-center gap-4 mb-12">
                <h2 class="text-3xl md:text-4xl font-bold">Tech Stack</h2>
                <div class="h-[1px] flex-1 bg-gradient-to-r from-brand-500/50 to-transparent"></div>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
                <!-- Frontend -->
                <div class="bg-white/[0.02] border border-white/10 rounded-2xl p-6 transition-all duration-300 glowing-border group">
                    <div class="flex items-center gap-3 mb-6">
                        <div class="w-10 h-10 rounded-lg bg-brand-500/20 flex items-center justify-center text-brand-400 group-hover:scale-110 transition-transform">
                            <i class="fa-brands fa-html5 text-xl"></i>
                        </div>
                        <h3 class="text-xl font-semibold">Frontend</h3>
                    </div>
                    <div class="flex flex-wrap gap-2">
                        <span class="px-3 py-1 bg-white/5 border border-white/10 rounded-md text-sm hover:bg-brand-500/20 hover:border-brand-500/50 hover:text-brand-300 cursor-default transition-colors">HTML</span>
                        <span class="px-3 py-1 bg-white/5 border border-white/10 rounded-md text-sm hover:bg-brand-500/20 hover:border-brand-500/50 hover:text-brand-300 cursor-default transition-colors">CSS</span>
                        <span class="px-3 py-1 bg-white/5 border border-white/10 rounded-md text-sm hover:bg-brand-500/20 hover:border-brand-500/50 hover:text-brand-300 cursor-default transition-colors">JS/TS</span>
                        <span class="px-3 py-1 bg-white/5 border border-white/10 rounded-md text-sm hover:bg-brand-500/20 hover:border-brand-500/50 hover:text-brand-300 cursor-default transition-colors">React</span>
                        <span class="px-3 py-1 bg-white/5 border border-white/10 rounded-md text-sm hover:bg-brand-500/20 hover:border-brand-500/50 hover:text-brand-300 cursor-default transition-colors">Next.js</span>
                        <span class="px-3 py-1 bg-white/5 border border-white/10 rounded-md text-sm hover:bg-brand-500/20 hover:border-brand-500/50 hover:text-brand-300 cursor-default transition-colors">Vue</span>
                        <span class="px-3 py-1 bg-white/5 border border-white/10 rounded-md text-sm hover:bg-brand-500/20 hover:border-brand-500/50 hover:text-brand-300 cursor-default transition-colors">Tailwind</span>
                        <span class="px-3 py-1 bg-white/5 border border-white/10 rounded-md text-sm hover:bg-brand-500/20 hover:border-brand-500/50 hover:text-brand-300 cursor-default transition-colors">Bootstrap</span>
                        <span class="px-3 py-1 bg-white/5 border border-white/10 rounded-md text-sm hover:bg-brand-500/20 hover:border-brand-500/50 hover:text-brand-300 cursor-default transition-colors">Sass</span>
                        <span class="px-3 py-1 bg-white/5 border border-white/10 rounded-md text-sm hover:bg-brand-500/20 hover:border-brand-500/50 hover:text-brand-300 cursor-default transition-colors">Vite</span>
                    </div>
                </div>

                <!-- Backend -->
                <div class="bg-white/[0.02] border border-white/10 rounded-2xl p-6 transition-all duration-300 glowing-border group">
                    <div class="flex items-center gap-3 mb-6">
                        <div class="w-10 h-10 rounded-lg bg-brand-500/20 flex items-center justify-center text-brand-400 group-hover:scale-110 transition-transform">
                            <i class="fa-solid fa-server text-xl"></i>
                        </div>
                        <h3 class="text-xl font-semibold">Backend</h3>
                    </div>
                    <div class="flex flex-wrap gap-2">
                        <span class="px-3 py-1 bg-white/5 border border-white/10 rounded-md text-sm hover:bg-brand-500/20 hover:border-brand-500/50 hover:text-brand-300 cursor-default transition-colors">Node.js</span>
                        <span class="px-3 py-1 bg-white/5 border border-white/10 rounded-md text-sm hover:bg-brand-500/20 hover:border-brand-500/50 hover:text-brand-300 cursor-default transition-colors">Express</span>
                        <span class="px-3 py-1 bg-white/5 border border-white/10 rounded-md text-sm hover:bg-brand-500/20 hover:border-brand-500/50 hover:text-brand-300 cursor-default transition-colors">PHP</span>
                        <span class="px-3 py-1 bg-white/5 border border-white/10 rounded-md text-sm hover:bg-brand-500/20 hover:border-brand-500/50 hover:text-brand-300 cursor-default transition-colors">Laravel</span>
                        <span class="px-3 py-1 bg-white/5 border border-white/10 rounded-md text-sm hover:bg-brand-500/20 hover:border-brand-500/50 hover:text-brand-300 cursor-default transition-colors">Python</span>
                        <span class="px-3 py-1 bg-white/5 border border-white/10 rounded-md text-sm hover:bg-brand-500/20 hover:border-brand-500/50 hover:text-brand-300 cursor-default transition-colors">Java</span>
                    </div>
                </div>

                <!-- Databases -->
                <div class="bg-white/[0.02] border border-white/10 rounded-2xl p-6 transition-all duration-300 glowing-border group">
                    <div class="flex items-center gap-3 mb-6">
                        <div class="w-10 h-10 rounded-lg bg-brand-500/20 flex items-center justify-center text-brand-400 group-hover:scale-110 transition-transform">
                            <i class="fa-solid fa-database text-xl"></i>
                        </div>
                        <h3 class="text-xl font-semibold">Databases & Services</h3>
                    </div>
                    <div class="flex flex-wrap gap-2">
                        <span class="px-3 py-1 bg-white/5 border border-white/10 rounded-md text-sm hover:bg-brand-500/20 hover:border-brand-500/50 hover:text-brand-300 cursor-default transition-colors">MySQL</span>
                        <span class="px-3 py-1 bg-white/5 border border-white/10 rounded-md text-sm hover:bg-brand-500/20 hover:border-brand-500/50 hover:text-brand-300 cursor-default transition-colors">PostgreSQL</span>
                        <span class="px-3 py-1 bg-white/5 border border-white/10 rounded-md text-sm hover:bg-brand-500/20 hover:border-brand-500/50 hover:text-brand-300 cursor-default transition-colors">MongoDB</span>
                        <span class="px-3 py-1 bg-white/5 border border-white/10 rounded-md text-sm hover:bg-brand-500/20 hover:border-brand-500/50 hover:text-brand-300 cursor-default transition-colors">Firebase</span>
                        <span class="px-3 py-1 bg-white/5 border border-white/10 rounded-md text-sm hover:bg-brand-500/20 hover:border-brand-500/50 hover:text-brand-300 cursor-default transition-colors">Supabase</span>
                        <span class="px-3 py-1 bg-white/5 border border-white/10 rounded-md text-sm hover:bg-brand-500/20 hover:border-brand-500/50 hover:text-brand-300 cursor-default transition-colors">Redis</span>
                    </div>
                </div>

                <!-- Tools & DevOps -->
                <div class="bg-white/[0.02] border border-white/10 rounded-2xl p-6 transition-all duration-300 glowing-border group md:col-span-2 lg:col-span-1">
                    <div class="flex items-center gap-3 mb-6">
                        <div class="w-10 h-10 rounded-lg bg-brand-500/20 flex items-center justify-center text-brand-400 group-hover:scale-110 transition-transform">
                            <i class="fa-solid fa-toolbox text-xl"></i>
                        </div>
                        <h3 class="text-xl font-semibold">Tools & DevOps</h3>
                    </div>
                    <div class="flex flex-wrap gap-2">
                        <span class="px-3 py-1 bg-white/5 border border-white/10 rounded-md text-sm hover:bg-brand-500/20 hover:border-brand-500/50 hover:text-brand-300 cursor-default transition-colors">Git</span>
                        <span class="px-3 py-1 bg-white/5 border border-white/10 rounded-md text-sm hover:bg-brand-500/20 hover:border-brand-500/50 hover:text-brand-300 cursor-default transition-colors">GitHub</span>
                        <span class="px-3 py-1 bg-white/5 border border-white/10 rounded-md text-sm hover:bg-brand-500/20 hover:border-brand-500/50 hover:text-brand-300 cursor-default transition-colors">VS Code</span>
                        <span class="px-3 py-1 bg-white/5 border border-white/10 rounded-md text-sm hover:bg-brand-500/20 hover:border-brand-500/50 hover:text-brand-300 cursor-default transition-colors">Linux</span>
                        <span class="px-3 py-1 bg-white/5 border border-white/10 rounded-md text-sm hover:bg-brand-500/20 hover:border-brand-500/50 hover:text-brand-300 cursor-default transition-colors">Docker</span>
                        <span class="px-3 py-1 bg-white/5 border border-white/10 rounded-md text-sm hover:bg-brand-500/20 hover:border-brand-500/50 hover:text-brand-300 cursor-default transition-colors">Postman</span>
                        <span class="px-3 py-1 bg-white/5 border border-white/10 rounded-md text-sm hover:bg-brand-500/20 hover:border-brand-500/50 hover:text-brand-300 cursor-default transition-colors">NPM</span>
                        <span class="px-3 py-1 bg-white/5 border border-white/10 rounded-md text-sm hover:bg-brand-500/20 hover:border-brand-500/50 hover:text-brand-300 cursor-default transition-colors">Actions</span>
                        <span class="px-3 py-1 bg-white/5 border border-white/10 rounded-md text-sm hover:bg-brand-500/20 hover:border-brand-500/50 hover:text-brand-300 cursor-default transition-colors">Bash</span>
                    </div>
                </div>

                <!-- Design & Video -->
                <div class="bg-white/[0.02] border border-white/10 rounded-2xl p-6 transition-all duration-300 glowing-border group md:col-span-2 lg:col-span-2">
                    <div class="flex items-center gap-3 mb-6">
                        <div class="w-10 h-10 rounded-lg bg-brand-500/20 flex items-center justify-center text-brand-400 group-hover:scale-110 transition-transform">
                            <i class="fa-solid fa-palette text-xl"></i>
                        </div>
                        <h3 class="text-xl font-semibold">Design & Video Editing</h3>
                    </div>
                    <div class="flex flex-wrap gap-2">
                        <span class="px-3 py-1 bg-white/5 border border-white/10 rounded-md text-sm hover:bg-brand-500/20 hover:border-brand-500/50 hover:text-brand-300 cursor-default transition-colors">Figma</span>
                        <span class="px-3 py-1 bg-white/5 border border-white/10 rounded-md text-sm hover:bg-brand-500/20 hover:border-brand-500/50 hover:text-brand-300 cursor-default transition-colors">Photoshop</span>
                        <span class="px-3 py-1 bg-white/5 border border-white/10 rounded-md text-sm hover:bg-brand-500/20 hover:border-brand-500/50 hover:text-brand-300 cursor-default transition-colors">Illustrator</span>
                        <span class="px-3 py-1 bg-white/5 border border-white/10 rounded-md text-sm hover:bg-brand-500/20 hover:border-brand-500/50 hover:text-brand-300 cursor-default transition-colors">After Effects</span>
                        <span class="px-3 py-1 bg-white/5 border border-white/10 rounded-md text-sm hover:bg-brand-500/20 hover:border-brand-500/50 hover:text-brand-300 cursor-default transition-colors">Premiere Pro</span>
                        <span class="px-3 py-1 bg-white/5 border border-white/10 rounded-md text-sm hover:bg-brand-500/20 hover:border-brand-500/50 hover:text-brand-300 cursor-default transition-colors">Blender</span>
                    </div>
                </div>
            </div>
        </section>

        <section id="stats" class="py-10 scroll-mt-24 reveal">
            <div class="flex items-center gap-4 mb-12">
                <h2 class="text-3xl md:text-4xl font-bold">GitHub Statistics</h2>
                <div class="h-[1px] flex-1 bg-gradient-to-r from-brand-500/50 to-transparent"></div>
            </div>

            <div class="flex flex-wrap justify-center gap-6">
                <!-- Stat Cards -->
                <div class="rounded-xl overflow-hidden shadow-lg border border-white/10 hover:border-brand-500/50 hover:shadow-[0_0_20px_rgba(59,130,246,0.3)] transition-all bg-[#1a1b26]">
                    <img height="165" class="h-[165px] object-cover" src="https://github-readme-stats.vercel.app/api?username=smstudios-ui&show_icons=true&theme=tokyonight&hide_border=true" alt="GitHub Stats" />
                </div>
                
                <div class="rounded-xl overflow-hidden shadow-lg border border-white/10 hover:border-brand-500/50 hover:shadow-[0_0_20px_rgba(59,130,246,0.3)] transition-all bg-[#1a1b26]">
                    <img height="165" class="h-[165px] object-cover" src="https://github-readme-stats.vercel.app/api/top-langs/?username=smstudios-ui&layout=compact&theme=tokyonight&hide_border=true" alt="Top Languages" />
                </div>
            </div>
            
            <div class="flex justify-center mt-6">
                <div class="rounded-xl overflow-hidden shadow-lg border border-white/10 hover:border-brand-500/50 hover:shadow-[0_0_20px_rgba(59,130,246,0.3)] transition-all bg-[#1a1b26] w-full max-w-[800px] flex justify-center">
                    <img class="max-w-full h-auto" src="https://streak-stats.demolab.com?user=smstudios-ui&theme=tokyonight&hide_border=true" alt="GitHub Streak" />
                </div>
            </div>
        </section>

        <section id="contact" class="py-16 text-center reveal">
            <h2 class="text-3xl font-bold mb-8">Connect With Me</h2>
            
            <div class="flex flex-wrap justify-center gap-6">
                <!-- GitHub -->
                <a href="https://github.com/smstudios-ui" target="_blank" class="group relative px-6 py-3 bg-white/5 border border-white/10 rounded-full flex items-center gap-3 hover:bg-white/10 hover:border-brand-500/50 transition-all">
                    <div class="absolute inset-0 rounded-full bg-brand-500/20 blur-md opacity-0 group-hover:opacity-100 transition-opacity"></div>
                    <i class="fa-brands fa-github text-xl relative z-10"></i>
                    <span class="font-medium relative z-10">smstudios-ui</span>
                </a>
                
                <!-- LinkedIn -->
                <a href="https://www.linkedin.com/in/sushan-mendaka/" target="_blank" class="group relative px-6 py-3 bg-white/5 border border-white/10 rounded-full flex items-center gap-3 hover:bg-[#0A66C2]/20 hover:border-[#0A66C2]/50 transition-all">
                    <div class="absolute inset-0 rounded-full bg-[#0A66C2]/20 blur-md opacity-0 group-hover:opacity-100 transition-opacity"></div>
                    <i class="fa-brands fa-linkedin text-xl text-[#0A66C2] relative z-10"></i>
                    <span class="font-medium relative z-10">sushan-mendaka</span>
                </a>

                <!-- Portfolio -->
                <a href="https://smstudios.online" target="_blank" class="group relative px-6 py-3 bg-white/5 border border-white/10 rounded-full flex items-center gap-3 hover:bg-brand-500/20 hover:border-brand-500/50 transition-all">
                    <div class="absolute inset-0 rounded-full bg-brand-500/20 blur-md opacity-0 group-hover:opacity-100 transition-opacity"></div>
                    <i class="fa-solid fa-globe text-xl text-brand-400 relative z-10"></i>
                    <span class="font-medium relative z-10">smstudios.online</span>
                </a>
            </div>
        </section>

    </main>

    <footer class="border-t border-white/10 bg-dark py-8 text-center text-sm text-gray-500">
        <p>© 2026 Sushan Mendaka | SM Studios. Built with <i class="fa-solid fa-heart text-brand-500"></i></p>
    </footer>

    <script>
        // Typing Animation Logic
        const words = ["💻 Web Developer", "🎨 Graphic Designer", "🎬 Video Editor"];
        let i = 0;
        let timer;
        const targetElement = document.getElementById('typewriter');

        function typeWriter() {
            let word = words[i].split('');
            let loopTyping = function() {
                if (word.length > 0) {
                    targetElement.innerHTML += word.shift();
                } else {
                    setTimeout(deleting, 2000); // Wait 2 seconds before deleting
                    return false;
                };
                timer = setTimeout(loopTyping, 100); // Typing speed
            };
            loopTyping();
        }

        function deleting() {
            let word = words[i].split('');
            let loopDeleting = function() {
                if (word.length > 0) {
                    word.pop();
                    targetElement.innerHTML = word.join('');
                } else {
                    // Move to next word
                    if (words.length > (i + 1)) {
                        i++;
                    } else {
                        i = 0; // Loop back to start
                    };
                    setTimeout(typeWriter, 500); // Wait 0.5s before typing next
                    return false;
                };
                timer = setTimeout(loopDeleting, 50); // Deleting speed
            };
            loopDeleting();
        }
        
        // Start typing animation
        setTimeout(typeWriter, 500);

        // Scroll Reveal Animation (Intersection Observer)
        document.addEventListener("DOMContentLoaded", function() {
            const reveals = document.querySelectorAll(".reveal");

            const revealOptions = {
                threshold: 0.15, // Trigger when 15% of the element is visible
                rootMargin: "0px 0px -50px 0px"
            };

            const revealOnScroll = new IntersectionObserver(function(
                entries,
                revealOnScroll
            ) {
                entries.forEach(entry => {
                    if (!entry.isIntersecting) {
                        return;
                    } else {
                        entry.target.classList.add("active");
                        revealOnScroll.unobserve(entry.target); // Optional: Stop observing once revealed
                    }
                });
            }, revealOptions);

            reveals.forEach(reveal => {
                revealOnScroll.observe(reveal);
            });
        });
    </script>
</body>
</html>
