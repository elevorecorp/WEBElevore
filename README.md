<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ELEVORE | God Protocol v3.0</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://unpkg.com/lucide@latest"></script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@100;400;900&family=Space+Grotesk:wght@300;700&family=Unbounded:wght@900&display=swap');
        
        :root {
            --neon: #22c55e;
            --obsidian: #050505;
        }

        * { cursor: crosshair; box-sizing: border-box; }

        body { 
            font-family: 'Inter', sans-serif; 
            background-color: #000; 
            color: #fff; 
            overflow-x: hidden;
            letter-spacing: -0.02em;
        }

        .font-huge { font-family: 'Unbounded', sans-serif; }
        .font-tech { font-family: 'Space Grotesk', sans-serif; }

        /* Textura de ruido cinemático */
        body::before {
            content: "";
            position: fixed;
            top: 0; left: 0; width: 100%; height: 100%;
            background-image: url('https://grainy-gradients.vercel.app/noise.svg');
            opacity: 0.15;
            pointer-events: none;
            z-index: 9999;
        }

        .hero-title {
            font-size: clamp(3rem, 15vw, 12rem);
            line-height: 0.75;
            text-transform: uppercase;
            font-weight: 900;
        }

        .glass-dark {
            background: rgba(10, 10, 10, 0.7);
            backdrop-filter: blur(40px) saturate(180%);
            border: 1px solid rgba(255, 255, 255, 0.05);
        }

        .neon-border-glow {
            position: relative;
        }

        .neon-border-glow::after {
            content: "";
            position: absolute;
            inset: -1px;
            background: linear-gradient(45deg, var(--neon), transparent, var(--neon));
            z-index: -1;
            border-radius: inherit;
            opacity: 0.1;
            transition: 0.5s;
        }

        .neon-border-glow:hover::after {
            opacity: 0.5;
        }

        .btn-god {
            background: #fff;
            color: #000;
            font-weight: 900;
            padding: 1.5rem 3rem;
            border-radius: 9999px;
            text-transform: uppercase;
            letter-spacing: 0.1em;
            transition: 0.5s cubic-bezier(0.19, 1, 0.22, 1);
            position: relative;
            overflow: hidden;
        }

        .btn-god:hover {
            background: var(--neon);
            box-shadow: 0 0 60px var(--neon);
            transform: scale(1.05) rotate(-1deg);
        }

        .reveal {
            opacity: 0;
            transform: translateY(50px);
            transition: 1.2s cubic-bezier(0.19, 1, 0.22, 1);
        }

        .reveal.active {
            opacity: 1;
            transform: translateY(0);
        }

        /* Animación de rejilla de radar */
        .bg-radar {
            background-image: 
                radial-gradient(circle at 50% 50%, rgba(34, 197, 94, 0.05) 0%, transparent 50%),
                linear-gradient(rgba(34, 197, 94, 0.02) 1px, transparent 1px),
                linear-gradient(90deg, rgba(34, 197, 94, 0.02) 1px, transparent 1px);
            background-size: 100% 100%, 60px 60px, 60px 60px;
        }

        .clip-text {
            background: linear-gradient(180deg, #fff 0%, rgba(255,255,255,0.2) 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
    </style>
</head>
<body class="bg-radar">

    <!-- OVERLAY DE CARGA DE SISTEMA -->
    <div id="loader" class="fixed inset-0 z-[10000] bg-black flex items-center justify-center transition-opacity duration-1000">
        <div class="text-center space-y-4">
            <div class="w-16 h-1 bg-white/10 rounded-full overflow-hidden">
                <div id="loader-bar" class="h-full bg-green-500 w-0 transition-all duration-1000"></div>
            </div>
            <p class="font-tech text-[8px] uppercase tracking-[0.8em] animate-pulse">Initializing Elevore God Protocol</p>
        </div>
    </div>

    <!-- HUD NAV -->
    <nav class="fixed top-0 w-full z-[100] p-8">
        <div class="max-w-screen-2xl mx-auto flex justify-between items-center">
            <div class="flex items-center gap-4 group">
                <div class="w-14 h-14 bg-white rounded-full flex items-center justify-center font-huge text-black text-3xl italic group-hover:rotate-12 transition-transform duration-500">E</div>
                <div class="leading-none">
                    <h1 class="font-huge text-lg tracking-tighter">ELEVORE</h1>
                    <span class="font-tech text-[7px] text-green-500 uppercase tracking-[0.6em]">System: Operational</span>
                </div>
            </div>
            
            <div class="hidden lg:flex glass-dark px-10 py-4 rounded-full gap-12 border-white/10 items-center">
                <a href="#misiones" class="font-tech text-[9px] font-bold uppercase tracking-[0.4em] hover:text-green-500 transition">Sector 01: Misiones</a>
                <a href="#vision" class="font-tech text-[9px] font-bold uppercase tracking-[0.4em] hover:text-green-500 transition">Sector 02: Vision</a>
                <a href="#contacto" class="font-tech text-[9px] font-bold uppercase tracking-[0.4em] hover:text-green-500 transition">Sector 03: Contact</a>
            </div>

            <button onclick="window.open('https://wa.me/14079524228')" class="glass-dark p-4 rounded-2xl border-green-500/20 group hover:border-green-500 transition-all">
                <i data-lucide="command" class="w-5 h-5 text-green-500 group-hover:rotate-90 transition-transform"></i>
            </button>
        </div>
    </nav>

    <!-- ULTRA HERO -->
    <section class="relative min-h-screen flex flex-col justify-center items-center px-6 overflow-hidden">
        <div class="absolute top-0 w-full h-full bg-[radial-gradient(circle_at_top_right,rgba(34,197,94,0.08),transparent)]"></div>
        
        <div class="relative z-10 text-center space-y-16">
            <div class="reveal">
                <p class="font-tech text-[10px] md:text-xs font-bold text-green-500 uppercase tracking-[1em] mb-4">
                    Architecting the future of Florida Real Estate
                </p>
            </div>

            <h1 class="hero-title font-huge clip-text reveal">
                OMNIPOTENT <br/>
                <span class="text-transparent" style="-webkit-text-stroke: 1px rgba(255,255,255,0.4);">RESTORATION</span> <br/>
                SYSTEM.
            </h1>

            <div class="reveal flex flex-col items-center space-y-10">
                <p class="max-w-3xl text-slate-400 text-lg md:text-2xl font-light leading-relaxed">
                    ELEVORE is the definitive response to chaos. We detail assets <br class="hidden md:block"/> 
                    with <span class="text-white underline decoration-green-500 underline-offset-8">military-grade precision</span> and proprietary neural tech.
                </p>
                
                <div class="flex flex-col sm:flex-row gap-8">
                    <button class="btn-god px-20 py-10 text-sm shadow-2xl">Deploy Mission ⚡</button>
                    <button class="px-16 py-8 rounded-full font-tech text-[10px] font-black uppercase tracking-[0.5em] border border-white/10 hover:border-green-500 transition-all">
                        Encrypted Portal
                    </button>
                </div>
            </div>
        </div>

        <!-- TELEMETRÍA INFERIOR -->
        <div class="absolute bottom-10 w-full px-12 flex justify-between items-end opacity-20 font-tech text-[8px] uppercase tracking-[0.5em]">
            <div class="space-y-2">
                <p>Status: God_Mode_v3.0</p>
                <p>Lat: 28.5383 / Long: -81.3792</p>
            </div>
            <div class="animate-bounce">Protocol: Initiate Scroll ↓</div>
            <div class="text-right space-y-2">
                <p>Security: High_Encryption</p>
                <p>Authorized: Jose_Mario_CEO</p>
            </div>
        </div>
    </section>

    <!-- MISIONES (B-2 STEALTH CARDS) -->
    <section id="misiones" class="py-60 px-6 max-w-screen-2xl mx-auto">
        <div class="grid lg:grid-cols-3 gap-10">
            <div class="lg:col-span-1 space-y-8 reveal">
                <span class="text-green-500 font-black text-xs uppercase tracking-[0.8em]">Operational Sectors</span>
                <h2 class="text-6xl font-huge leading-none">THE <br/> TRIAD.</h2>
                <p class="text-slate-500 text-sm leading-loose uppercase font-bold max-w-xs">
                    Our units are trained to handle environments where failure is not an option. From Windermere to your next skyscraper.
                </p>
            </div>

            <div class="lg:col-span-2 grid md:grid-cols-2 gap-6">
                <!-- CARD 01 -->
                <div class="glass-dark p-12 rounded-[3.5rem] space-y-10 neon-border-glow reveal group">
                    <div class="flex justify-between items-center">
                        <div class="w-16 h-16 bg-white/5 rounded-2xl flex items-center justify-center text-green-500"><i data-lucide="sparkles" class="w-8 h-8"></i></div>
                        <span class="font-tech text-[9px] text-slate-600 tracking-widest">ID-CODE: OMNI_01</span>
                    </div>
                    <div>
                        <h4 class="text-3xl font-huge italic mb-4">LUXURY DETAILING</h4>
                        <p class="text-slate-400 text-sm font-light leading-relaxed">
                            Restoring the DNA of the property. We clean beyond the visible spectrum. For closings that demand a "perfect" status.
                        </p>
                    </div>
                </div>

                <!-- CARD 02 -->
                <div class="glass-dark p-12 rounded-[3.5rem] space-y-10 neon-border-glow reveal border-amber-500/10">
                    <div class="flex justify-between items-center">
                        <div class="w-16 h-16 bg-white/5 rounded-2xl flex items-center justify-center text-amber-500"><i data-lucide="hammer" class="w-8 h-8"></i></div>
                        <span class="font-tech text-[9px] text-slate-600 tracking-widest">ID-CODE: TECH_02</span>
                    </div>
                    <div>
                        <h4 class="text-3xl font-huge italic mb-4">HANDYMAN OPS</h4>
                        <p class="text-slate-400 text-sm font-light leading-relaxed">
                            Structural and aesthetic integrity. We deploy master-level installations for tech-ready environments.
                        </p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- THE SUPREME INTELLIGENCE -->
    <section id="vision" class="py-40 bg-white text-black rounded-[6rem] mx-6 shadow-[0_0_100px_rgba(34,197,94,0.3)]">
        <div class="max-w-7xl mx-auto px-6 grid lg:grid-cols-2 gap-32 items-center">
            <div class="reveal">
                <span class="bg-black text-white px-6 py-2 rounded-full text-[10px] font-black uppercase tracking-[0.5em]">The Elevore Edge</span>
                <h2 class="text-7xl md:text-9xl font-huge leading-[0.8] mt-12 mb-12">DATA <br/> DRIVEN <br/> CARE.</h2>
                <p class="text-2xl font-light leading-relaxed text-slate-700">
                    We've replaced guessing with <span class="font-black text-black italic">Algorithms</span>. 
                    Every project is managed through our proprietary OS, ensuring 100% transparency.
                </p>
            </div>
            
            <div class="grid grid-cols-2 gap-8 reveal">
                <div class="space-y-8">
                    <div class="border-l-4 border-black pl-6">
                        <h5 class="text-5xl font-huge italic">0%</h5>
                        <p class="text-[9px] font-black uppercase tracking-widest text-slate-400 mt-2">Error Margin</p>
                    </div>
                    <div class="border-l-4 border-black pl-6">
                        <h5 class="text-5xl font-huge italic">30S</h5>
                        <p class="text-[9px] font-black uppercase tracking-widest text-slate-400 mt-2">Neural Quote</p>
                    </div>
                </div>
                <div class="space-y-8 pt-20">
                    <div class="border-l-4 border-black pl-6">
                        <h5 class="text-5xl font-huge italic">100%</h5>
                        <p class="text-[9px] font-black uppercase tracking-widest text-slate-400 mt-2">Satisfaction</p>
                    </div>
                    <div class="border-l-4 border-black pl-6">
                        <h5 class="text-5xl font-huge italic">24/7</h5>
                        <p class="text-[9px] font-black uppercase tracking-widest text-slate-400 mt-2">Cloud Access</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- FINAL MISSION CALL -->
    <section id="contacto" class="py-60 text-center relative overflow-hidden">
        <div class="reveal space-y-12">
            <h2 class="text-[20rem] font-huge font-black italic opacity-[0.03] absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2 select-none">ELEVORE</h2>
            <div class="relative z-10">
                <h3 class="text-5xl md:text-8xl font-huge italic tracking-tighter mb-12 leading-none uppercase">Start your <br/> <span class="text-green-500">Empire</span> Detailing.</h3>
                <button class="btn-god px-24 py-12 text-lg shadow-[0_0_100px_rgba(34,197,94,0.4)] active:scale-95">Initiate Deployment Now</button>
            </div>
        </div>
    </section>

    <!-- FOOTER -->
    <footer class="p-20 bg-[#050505] border-t border-white/5">
        <div class="max-w-screen-2xl mx-auto flex flex-col md:flex-row justify-between items-center gap-12">
            <div class="flex items-center gap-6">
                <div class="w-20 h-20 bg-white rounded-[2rem] flex items-center justify-center font-huge text-black text-4xl shadow-2xl italic">E</div>
                <div class="space-y-2">
                    <p class="font-huge text-lg leading-none">ELEVORE</p>
                    <p class="font-tech text-[8px] text-slate-500 uppercase tracking-[0.5em]">The God Protocol 2026</p>
                </div>
            </div>
            
            <div class="text-center md:text-right space-y-4">
                <p class="font-tech text-[10px] text-green-500 uppercase tracking-widest">Connect with Central Command</p>
                <p class="text-4xl font-huge italic tracking-tighter leading-none">+1 (407) 952-4228</p>
                <div class="flex justify-center md:justify-end gap-10 pt-4">
                    <a href="#" class="text-slate-500 hover:text-white transition"><i data-lucide="instagram"></i></a>
                    <a href="#" class="text-slate-500 hover:text-white transition"><i data-lucide="linkedin"></i></a>
                </div>
            </div>
        </div>
        <div class="mt-40 text-center">
            <p class="font-tech text-[8px] text-slate-800 uppercase tracking-[1.5em] font-black">Powered by Aeternum Intelligence • Orlando • FL</p>
        </div>
    </footer>

    <script>
        lucide.createIcons();

        // Simulación de carga
        window.onload = () => {
            const bar = document.getElementById('loader-bar');
            bar.style.width = '100%';
            setTimeout(() => {
                document.getElementById('loader').style.opacity = '0';
                setTimeout(() => document.getElementById('loader').style.display = 'none', 1000);
            }, 1000);
        };

        // Lógica de revelación
        const reveal = () => {
            const reveals = document.querySelectorAll('.reveal');
            reveals.forEach(r => {
                const windowHeight = window.innerHeight;
                const revealTop = r.getBoundingClientRect().top;
                if (revealTop < windowHeight - 100) {
                    r.classList.add('active');
                }
            });
        };
        window.addEventListener('scroll', reveal);
    </script>
</body>
</html>
