<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CENDOL DAWET | KSD Chef Squad</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Oswald:wght@400;700&family=Plus+Jakarta+Sans:wght@400;600;800&display=swap');
        
        :root {
            --marvel-red: #ed1d24;
            --iron-gold: #facc15;
            --vibranium-purple: #a855f7;
            --shield-blue: #3b82f6;
        }

        body {
            font-family: 'Plus Jakarta Sans', sans-serif;
            background: #020617;
            color: white;
            scroll-behavior: smooth;
            overflow-x: hidden;
        }

        .font-marvel { font-family: 'Oswald', sans-serif; text-transform: uppercase; }

        /* Scroller Atas Utama */
        .ksd-marquee {
            background: var(--marvel-red);
            overflow: hidden;
            white-space: nowrap;
            padding: 10px 0;
            font-size: 12px;
            font-weight: 900;
            letter-spacing: 0.4em;
            border-bottom: 4px solid rgba(0,0,0,0.3);
            box-shadow: 0 10px 30px rgba(237, 29, 36, 0.3);
        }

        .ksd-marquee-inner {
            display: inline-block;
            animation: marquee 30s linear infinite;
        }

        /* Scroller Nama Punggawa */
        .names-marquee {
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.05), transparent);
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
            overflow: hidden;
            white-space: nowrap;
            padding: 25px 0;
        }

        .names-marquee-inner {
            display: inline-block;
            animation: marquee 20s linear infinite;
        }

        @keyframes marquee {
            0% { transform: translateX(0); }
            100% { transform: translateX(-50%); }
        }

        .glass-panel {
            background: rgba(255, 255, 255, 0.02);
            backdrop-filter: blur(25px);
            border: 1px solid rgba(255, 255, 255, 0.1);
            transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
        }

        /* Tampilan Nama yang diperbarui (Profile Card) */
        .profile-card {
            position: relative;
            padding: 20px;
            border-radius: 15px;
            overflow: hidden;
            min-width: 250px;
            margin: 0 15px;
            display: inline-block;
            vertical-align: top;
            background: rgba(15, 23, 42, 0.8);
            border-left: 4px solid var(--accent);
        }

        .profile-card::before {
            content: "ID-DECODED";
            position: absolute;
            top: 5px;
            right: 10px;
            font-size: 8px;
            opacity: 0.3;
            font-family: monospace;
        }

        .hero-section {
            background: linear-gradient(rgba(2, 6, 23, 0.7), rgba(2, 6, 23, 0.95)), 
                        url('https://images.unsplash.com/photo-1555939594-58d7cb561ad1?auto=format&fit=crop&q=80&w=2000');
            background-size: cover;
            background-position: center;
        }

        /* Modal styling */
        .modal-overlay {
            opacity: 0;
            visibility: hidden;
            transition: all 0.4s ease;
        }
        .modal-overlay.active {
            opacity: 1;
            visibility: visible;
        }

        .contact-input {
            background: rgba(255,255,255,0.05);
            border: 1px solid rgba(255,255,255,0.1);
            color: white;
            padding: 12px 16px;
            border-radius: 10px;
            width: 100%;
            transition: 0.3s;
        }
        .contact-input:focus {
            outline: none;
            border-color: var(--marvel-red);
            background: rgba(255,255,255,0.1);
        }

        /* Instagram Button Special Style */
        .ig-btn {
            background: linear-gradient(45deg, #f09433 0%, #e6683c 25%, #dc2743 50%, #cc2366 75%, #bc1888 100%);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        .ig-btn:hover {
            transform: translateY(-5px) scale(1.05);
            box-shadow: 0 10px 25px rgba(220, 39, 67, 0.4);
        }
    </style>
</head>
<body class="overflow-x-hidden">

    <!-- KSD Chef Squad Top Marquee -->
    <div class="ksd-marquee fixed top-0 w-full z-[60]">
        <div class="ksd-marquee-inner font-marvel text-black font-black">
            ACCESSING ABIT STRATEGIC ARCHIVES • KSD CHEF SQUAD ASSEMBLED • MISSION: GASTRONOMIC SUPREMACY • STATUS: OVER-COOKING THE COMPETITION • ENCRYPTED DATA DETECTED • 
            ACCESSING ABIT STRATEGIC ARCHIVES • KSD CHEF SQUAD ASSEMBLED • MISSION: GASTRONOMIC SUPREMACY •
        </div>
    </div>

    <!-- Universal Modal -->
    <div id="universal-modal" class="modal-overlay fixed inset-0 z-[100] flex items-center justify-center p-4 bg-black/98 backdrop-blur-2xl">
        <div class="glass-panel max-w-5xl w-full rounded-[3rem] overflow-hidden relative flex flex-col md:flex-row border-b-8 border-red-600 shadow-2xl">
            <button onclick="closeModal()" class="absolute top-8 right-8 text-white hover:text-red-500 text-3xl z-20 bg-black/50 rounded-full w-14 h-14 flex items-center justify-center transition">
                <i class="fas fa-times"></i>
            </button>
            <div id="modal-img-box" class="w-full md:w-1/2 h-80 md:h-auto bg-slate-900 relative">
                <!-- Content via JS -->
            </div>
            <div class="w-full md:w-1/2 p-12 md:p-16">
                <div id="modal-tag" class="text-red-500 font-bold uppercase tracking-[0.4em] text-[10px] mb-4"></div>
                <h2 id="modal-title" class="text-6xl font-marvel mb-6 italic leading-none"></h2>
                <div id="modal-desc" class="text-slate-400 leading-relaxed mb-10 text-lg italic"></div>
                <div id="modal-extra" class="space-y-6"></div>
            </div>
        </div>
    </div>

    <!-- Nav -->
    <nav class="fixed w-full z-50 bg-slate-950/90 backdrop-blur-md border-b border-white/5 top-[32px]">
        <div class="max-w-7xl mx-auto px-8 py-5 flex justify-between items-center">
            <div class="flex items-center gap-4">
                <div class="bg-red-600 px-4 py-1.5 font-black text-3xl italic skew-x-[-15deg] shadow-lg shadow-red-600/30">ABIT</div>
                <div class="h-10 w-[1px] bg-white/10 hidden md:block"></div>
                <span class="font-marvel text-xl tracking-tighter text-slate-300 hidden md:block">COMMAND_CENTER</span>
            </div>
            <div class="flex gap-12 font-bold text-[11px] uppercase tracking-[0.3em]">
                <a href="#home" class="hover:text-red-500 transition-all">Intel</a>
                <a href="#tim" class="hover:text-red-500 transition-all">Personnel</a>
                <a href="#menu" class="hover:text-red-500 transition-all">Arsenal</a>
                <a href="#contact" class="hover:text-red-500 transition-all">Comms</a>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section id="home" class="hero-section min-h-screen flex flex-col items-center justify-center text-center px-6 relative overflow-hidden">
        <div class="z-10 mt-20">
            <div class="inline-flex items-center gap-3 bg-red-600/10 border border-red-600/30 px-6 py-2 rounded-full mb-10">
                <span class="w-2 h-2 bg-red-600 rounded-full animate-ping"></span>
                <span class="text-[10px] font-black tracking-[0.4em] uppercase text-red-500">Live Mission: Operation Savory</span>
            </div>
            <h1 class="text-8xl md:text-[200px] font-marvel leading-[0.8] mb-8 italic tracking-tighter">
                CENDOL <br><span class="text-red-600">DAWET</span>
            </h1>
            <p class="max-w-2xl mx-auto text-slate-400 text-lg md:text-xl uppercase tracking-[0.4em] font-light leading-relaxed">
                Unit Taktis Kuliner ABIT Hadir Untuk <br>
                <span class="text-white font-bold">Mendominasi Indra Perasa Anda.</span>
            </p>
            <div class="mt-16 flex flex-wrap justify-center gap-6">
                <a href="#menu" class="px-10 py-4 bg-red-600 hover:bg-red-700 font-black text-xs uppercase tracking-[0.4em] italic skew-x-[-15deg] transition-all">
                    View Arsenal
                </a>
                <a href="https://instagram.com/rafly_aout" target="_blank" class="px-10 py-4 ig-btn font-black text-xs uppercase tracking-[0.4em] italic skew-x-[-15deg] transition-all flex items-center gap-3">
                    <i class="fab fa-instagram text-lg"></i> Follow HQ
                </a>
            </div>
        </div>
        
        <!-- Large BG Watermark -->
        <div class="absolute -bottom-20 -left-20 opacity-[0.05] pointer-events-none select-none">
            <h2 class="text-[40rem] font-marvel italic leading-none">KSD</h2>
        </div>
    </section>

    <!-- Personnel Bar -->
    <div class="names-marquee mt-10">
        <div class="names-marquee-inner" id="scrolling-names">
            <!-- Content via JS -->
        </div>
    </div>

    <!-- Personnel Section -->
    <section id="tim" class="py-32 bg-slate-950 relative">
        <div class="max-w-7xl mx-auto px-8">
            <div class="flex flex-col md:flex-row items-end justify-between mb-24 gap-6">
                <div>
                    <h3 class="text-red-600 font-marvel tracking-[0.8em] text-xs mb-4">Personnel Intelligence</h3>
                    <h2 class="text-6xl md:text-8xl font-marvel italic leading-none uppercase">The Squad</h2>
                </div>
                <p class="max-w-md text-slate-500 text-sm leading-relaxed italic">
                    Setiap anggota tim KSD Chef Squad dipilih melalui seleksi ketat untuk memastikan integritas rasa dan presisi penyajian yang tidak tertandingi.
                </p>
            </div>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-10" id="personnel-grid">
                <!-- Content via JS -->
            </div>
        </div>
    </section>

    <!-- Arsenal Section -->
    <section id="menu" class="py-32 bg-slate-900/40 relative">
        <div class="max-w-7xl mx-auto px-8">
            <div class="text-center mb-24">
                <h3 class="text-red-600 font-marvel tracking-[0.5em] text-xs mb-4">Field Equipment</h3>
                <h2 class="text-7xl font-marvel italic mb-6 leading-none">THE ARSENAL</h2>
                <div class="h-1 w-20 bg-red-600 mx-auto rounded-full"></div>
            </div>

            <div class="grid grid-cols-1 lg:grid-cols-2 gap-12" id="menu-grid">
                <!-- Content via JS -->
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="py-32 bg-black relative overflow-hidden">
        <div class="max-w-7xl mx-auto px-8 relative z-10">
            <div class="grid grid-cols-1 lg:grid-cols-2 gap-20">
                <div>
                    <h3 class="text-red-600 font-marvel tracking-[0.5em] text-xs mb-4">Transmission Channel</h3>
                    <h2 class="text-6xl font-marvel italic mb-8">SECURE COMMS</h2>
                    <p class="text-slate-400 text-lg mb-12 leading-relaxed">
                        Butuh bantuan taktis atau ingin melakukan reservasi markas? Hubungi kanal komunikasi utama kami di bawah ini.
                    </p>
                    
                    <div class="space-y-8">
                        <a href="https://instagram.com/rafly_aout" target="_blank" class="flex items-center gap-6 group">
                            <div class="w-16 h-16 rounded-2xl bg-white/5 flex items-center justify-center text-red-600 text-2xl group-hover:bg-red-600 group-hover:text-white transition-all">
                                <i class="fab fa-instagram"></i>
                            </div>
                            <div>
                                <p class="text-[10px] font-black uppercase tracking-widest text-slate-500">Instagram Command</p>
                                <p class="text-xl font-bold">@rafly_aout</p>
                            </div>
                        </a>
                        <div class="flex items-center gap-6 group">
                            <div class="w-16 h-16 rounded-2xl bg-white/5 flex items-center justify-center text-red-600 text-2xl group-hover:bg-red-600 group-hover:text-white transition-all">
                                <i class="fas fa-phone"></i>
                            </div>
                            <div>
                                <p class="text-[10px] font-black uppercase tracking-widest text-slate-500">Emergency Line</p>
                                <p class="text-xl font-bold">+62 821-2345-6789</p>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="glass-panel p-10 rounded-[2rem] border-t-4 border-red-600">
                    <form onsubmit="event.preventDefault(); alert('Transmission Sent to HQ!');" class="space-y-6">
                        <div class="grid grid-cols-2 gap-6">
                            <div class="space-y-2">
                                <label class="text-[9px] font-black uppercase tracking-widest text-slate-500 ml-1">Codename</label>
                                <input type="text" class="contact-input" placeholder="Sobat Abit">
                            </div>
                            <div class="space-y-2">
                                <label class="text-[9px] font-black uppercase tracking-widest text-slate-500 ml-1">Comms ID</label>
                                <input type="email" class="contact-input" placeholder="agent@abit.com">
                            </div>
                        </div>
                        <div class="space-y-2">
                            <label class="text-[9px] font-black uppercase tracking-widest text-slate-500 ml-1">Message Briefing</label>
                            <textarea rows="4" class="contact-input resize-none" placeholder="Tuliskan misi makan siang Anda..."></textarea>
                        </div>
                        <button type="submit" class="w-full py-5 bg-red-600 hover:bg-red-700 font-black text-sm uppercase tracking-[0.5em] italic rounded-xl transition-all shadow-xl shadow-red-600/20">
                            Send Transmission
                        </button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="py-20 bg-slate-950 border-t border-white/5 text-center">
        <div class="bg-red-600 inline-block px-6 py-2 font-black text-5xl italic mb-8 skew-x-[-15deg]">ABIT</div>
        <div class="flex justify-center gap-8 mb-10 text-slate-500 text-2xl">
            <a href="https://instagram.com/rafly_aout" target="_blank" class="hover:text-red-500 transition-all"><i class="fab fa-instagram"></i></a>
        </div>
        <p class="text-slate-700 text-[10px] uppercase tracking-[0.8em] font-bold">In Cendol We Trust • Since 2026</p>
    </footer>

    <script>
        const personnelData = [
            {
                name: 'RAFLY',
                alias: 'The Iron Chef',
                icon: 'fa-microchip',
                color: '#facc15',
                desc: 'Spesialis termodinamika pangan. Mampu menghitung titik didih minyak paling presisi untuk menciptakan keajaiban tekstur.',
                skill: 'Searing Level: 99'
            },
            {
                name: 'USHINCHA',
                alias: 'Sugar Sorceress',
                icon: 'fa-wand-sparkles',
                color: '#ef4444',
                desc: 'Menguasai alkimia gula aren dan santan murni. Setiap racikan cendolnya adalah karya seni cair yang mematikan dahaga.',
                skill: 'Alchemy Level: MAX'
            },
            {
                name: 'VANNY',
                alias: 'Cosmic Liaison',
                icon: 'fa-bolt',
                color: '#3b82f6',
                desc: 'Koordinator dimensi logistik. Memastikan setiap hidangan berpindah dari dapur ke meja dalam kecepatan sub-atomik.',
                skill: 'Speed: Hypersonic'
            },
            {
                name: 'DANDI',
                alias: 'Vibranium Supply',
                icon: 'fa-shield-halved',
                color: '#a855f7',
                desc: 'Penanggung jawab rantai pasokan paling murni di Bumi. Tidak ada bahan baku yang lolos jika tidak memenuhi standar KSD.',
                skill: 'Quality Integrity: 100%'
            },
            {
                name: 'RAMLI',
                alias: 'First Sentinel',
                icon: 'fa-user-shield',
                color: '#06b6d4',
                desc: 'Komandan garda depan pelayanan. Menjaga kepuasan pelanggan dengan karisma diplomatik tingkat tinggi.',
                skill: 'Diplomacy: Legend'
            }
        ];

        const menuData = [
            {
                name: 'Bebek Mjolnir',
                price: '48K',
                tag: 'Strike Class',
                img: 'https://images.unsplash.com/photo-1544025162-d76694265947?auto=format&fit=crop&q=80&w=800',
                accent: '#ed1d24',
                desc: 'Bebek pilihan yang ditempa dengan bumbu rahasia 24 jam. Dagingnya lumer seketika seolah dipalu oleh Dewa Guntur.',
                stats: 'Damage: 99 | Stamina: +100'
            },
            {
                name: 'Ikan Lele Vibranium',
                price: '32K',
                tag: 'Tanker Class',
                img: 'https://images.unsplash.com/photo-1598511757337-fe2cd8714b58?auto=format&fit=crop&q=80&w=800',
                accent: '#3b82f6',
                desc: 'Ikan Lele segar (Ikan Asli!) yang dibalur zirah tepung garing. Renyahnya awet, gurihnya permanen. Disajikan dengan Sambal Petir.',
                stats: 'Crunchiness: 100% | Resistance: Max'
            },
            {
                name: 'Bola Ubi Infinity',
                price: '20K',
                tag: 'Energy Sphere',
                img: 'https://images.unsplash.com/photo-1599487488170-d11ec9c172f0?auto=format&fit=crop&q=80&w=800',
                accent: '#a855f7',
                desc: 'Ubi madu kuning pilihan yang digoreng hingga kopong namun kenyal. Mengandung energi manis yang tak terbatas.',
                stats: 'Energy: +50 | Sweetness: Galaxy'
            },
            {
                name: 'Es Teh S.H.I.E.L.D',
                price: '8K',
                tag: 'Utility Class',
                img: 'https://images.unsplash.com/photo-1556679343-c7306c1976bc?auto=format&fit=crop&q=80&w=800',
                accent: '#06b6d4',
                desc: 'Pendingin sistem internal tubuh. Menggunakan daun teh pegunungan tinggi untuk menurunkan suhu tubuh pasca tempur.',
                stats: 'Cooling: 100% | Refreshment: Infinite'
            }
        ];

        // Init Marquee Names
        const scrollNames = document.getElementById('scrolling-names');
        const repeatedNames = [...personnelData, ...personnelData]; // Loop
        repeatedNames.forEach(p => {
            const el = document.createElement('div');
            el.className = 'profile-card';
            el.style.setProperty('--accent', p.color);
            el.innerHTML = `
                <div class="flex items-center gap-4">
                    <div class="w-12 h-12 rounded-lg bg-white/5 flex items-center justify-center" style="color: ${p.color}">
                        <i class="fas ${p.icon} text-2xl"></i>
                    </div>
                    <div>
                        <h4 class="text-xl font-marvel italic text-white">${p.name}</h4>
                        <p class="text-[8px] font-black uppercase tracking-widest" style="color: ${p.color}">${p.alias}</p>
                    </div>
                </div>
            `;
            scrollNames.appendChild(el);
        });

        // Init Grid Personnel
        const pGrid = document.getElementById('personnel-grid');
        personnelData.forEach(p => {
            const el = document.createElement('div');
            el.className = 'glass-panel p-10 rounded-[2.5rem] border-t-2 hover:-translate-y-4 group cursor-pointer';
            el.style.borderColor = p.color;
            el.onclick = () => showHero(p);
            el.innerHTML = `
                <div class="h-48 mb-8 flex items-center justify-center bg-slate-900 rounded-3xl group-hover:bg-slate-800 transition-all">
                    <i class="fas ${p.icon} text-[6rem] opacity-20 group-hover:opacity-100 transition-all" style="color: ${p.color}"></i>
                </div>
                <h4 class="text-3xl font-marvel italic mb-2 tracking-tighter">${p.name}</h4>
                <p class="text-[10px] font-black uppercase tracking-[0.3em] mb-4" style="color: ${p.color}">${p.alias}</p>
                <div class="h-[1px] w-full bg-white/5 mb-6"></div>
                <p class="text-slate-500 text-sm leading-relaxed italic line-clamp-2">"${p.desc}"</p>
            `;
            pGrid.appendChild(el);
        });

        // Init Menu Grid
        const mGrid = document.getElementById('menu-grid');
        menuData.forEach(item => {
            const el = document.createElement('div');
            el.className = 'glass-panel p-8 rounded-[3rem] group cursor-pointer hover:border-red-600/50 flex flex-col md:flex-row gap-8 items-center border-l-4';
            el.style.borderLeftColor = item.accent;
            el.onclick = () => showMenu(item);
            el.innerHTML = `
                <div class="w-full md:w-56 h-56 flex-shrink-0 overflow-hidden rounded-[2rem] bg-slate-800 border border-white/5">
                    <img src="${item.img}" class="w-full h-full object-cover group-hover:scale-110 transition duration-700">
                </div>
                <div class="flex-grow text-center md:text-left">
                    <div class="flex flex-col md:flex-row justify-between items-center mb-4 gap-2">
                        <h4 class="text-4xl font-marvel italic">${item.name}</h4>
                        <span class="text-2xl font-black text-red-600 font-marvel">${item.price}</span>
                    </div>
                    <p class="text-[10px] text-slate-500 font-bold uppercase tracking-widest mb-6">${item.tag}</p>
                    <div class="h-1 bg-white/5 rounded-full overflow-hidden group-hover:bg-red-600/10">
                        <div class="h-full bg-red-600 w-3/4 animate-pulse"></div>
                    </div>
                </div>
            `;
            mGrid.appendChild(el);
        });

        const modal = document.getElementById('universal-modal');
        const imgBox = document.getElementById('modal-img-box');
        const mTitle = document.getElementById('modal-title');
        const mTag = document.getElementById('modal-tag');
        const mDesc = document.getElementById('modal-desc');
        const mExtra = document.getElementById('modal-extra');

        function showHero(p) {
            imgBox.innerHTML = `
                <div class="absolute inset-0 flex items-center justify-center text-[18rem] opacity-20" style="color: ${p.color}">
                    <i class="fas ${p.icon}"></i>
                </div>
                <div class="absolute inset-0 flex flex-col items-center justify-center p-10">
                    <div class="w-64 h-64 rounded-full bg-gradient-to-tr from-slate-900 via-slate-800 to-slate-900 flex items-center justify-center shadow-2xl border-4" style="border-color: ${p.color}">
                        <i class="fas ${p.icon} text-[8rem]" style="color: ${p.color}"></i>
                    </div>
                </div>
            `;
            mTitle.innerText = p.name;
            mTag.innerText = p.alias;
            mDesc.innerText = p.desc;
            mExtra.innerHTML = `
                <div class="bg-white/5 p-8 rounded-[2rem] border-l-8" style="border-color: ${p.color}">
                    <p class="text-[10px] font-black uppercase tracking-widest text-slate-500 mb-3">Ability Signature</p>
                    <p class="text-2xl font-marvel italic text-white tracking-[0.2em] animate-pulse">${p.skill}</p>
                </div>
            `;
            modal.style.borderBottomColor = p.color;
            modal.classList.add('active');
            document.body.style.overflow = 'hidden';
        }

        function showMenu(item) {
            imgBox.innerHTML = `<img src="${item.img}" class="w-full h-full object-cover group-hover:scale-110">`;
            mTitle.innerText = item.name;
            mTag.innerText = item.tag;
            mDesc.innerText = item.desc;
            mExtra.innerHTML = `
                <div class="bg-red-600/10 p-8 rounded-[2rem] border-l-8 border-red-600">
                    <p class="text-[10px] font-black uppercase tracking-widest text-red-500 mb-3">Tactical Specs</p>
                    <p class="text-2xl font-marvel italic text-white tracking-[0.2em]">${item.stats}</p>
                </div>
                <button class="w-full py-6 bg-red-600 hover:bg-red-700 font-black text-sm uppercase tracking-[0.5em] italic rounded-2xl transition-all shadow-xl shadow-red-600/40">
                    Initiate Deployment
                </button>
            `;
            modal.style.borderBottomColor = '#ed1d24';
            modal.classList.add('active');
            document.body.style.overflow = 'hidden';
        }

        function closeModal() {
            modal.classList.remove('active');
            document.body.style.overflow = 'auto';
        }

        window.onclick = (e) => { if(e.target == modal) closeModal(); }
    </script>
</body>
</html>
