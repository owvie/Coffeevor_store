DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Coffevor | Premium Artisan Roastery</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@200;400;600;800&display=swap" rel="stylesheet">
    <style>
        body { font-family: 'Plus Jakarta Sans', sans-serif; scroll-behavior: smooth; }
        .glass-nav { background: rgba(255, 255, 255, 0.8); backdrop-filter: blur(20px); }
        .hero-gradient { background: radial-gradient(circle at top right, #fffbeb, transparent); }
        .cart-sidebar { transition: transform 0.3s ease-in-out; }
        .hide-scrollbar::-webkit-scrollbar { display: none; }
        input, textarea, select { transition: all 0.2s ease; }
        
        .coffee-card { transition: all 0.3s ease; }
        .coffee-card:hover { transform: translateY(-5px); border-color: #78350f20; }
    </style>
</head>
<body class="bg-[#FDFCFB] text-stone-900 selection:bg-amber-200">

    <!-- Navbar -->
    <nav class="fixed w-full z-50 border-b border-stone-100 glass-nav">
        <div class="max-w-7xl mx-auto px-6 h-20 flex items-center justify-between">
            <div class="flex items-center gap-3">
                <div class="bg-amber-900 p-2 rounded-xl shadow-lg">
                    <svg class="w-5 h-5 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8h1a4 4 0 1 1 0 8h-1M3 8h14v9a4 4 0 0 1-4 4H7a4 4 0 0 1-4-4Z"></path></svg>
                </div>
                <span class="font-black text-2xl tracking-tighter text-amber-900 uppercase">Coffevor</span>
            </div>
            <div class="hidden md:flex items-center gap-8 font-extrabold text-[10px] uppercase tracking-widest text-stone-500">
                <a href="#about" class="hover:text-amber-900 transition">Tentang Kami</a>
                <a href="#catalog" class="hover:text-amber-900 transition">Katalog</a>
                <a href="#order-form" class="hover:text-amber-900 transition">Pesan</a>
                <button onclick="toggleCart()" class="relative flex items-center gap-2 bg-amber-900 text-white px-5 py-3 rounded-full shadow-xl hover:scale-105 transition active:scale-95">
                    <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 3h2l.4 2M7 13h10l4-8H5.4M7 13L5.4 5M7 13l-2.293 2.293c-.63.63-.184 1.707.707 1.707H17m0 0a2 2 0 100 4 2 2 0 000-4zm-8 2a2 2 0 11-4 0 2 2 0 014 0z"></path></svg>
                    <span id="cart-count">0</span>
                </button>
            </div>
        </div>
    </nav>

    <!-- Hero -->
    <section class="relative pt-44 pb-20 px-6 hero-gradient">
        <div class="max-w-5xl mx-auto text-center">
            <h1 class="text-6xl md:text-8xl font-black tracking-tighter leading-none mb-6 uppercase">Freshly <span class="text-amber-900">Roasted</span></h1>
            <p class="text-stone-500 text-lg mb-10 font-medium tracking-tight">Kopi artisan kualitas ekspor, dikirim langsung ke rumah Anda.</p>
            <div class="flex flex-wrap justify-center gap-4">
                <a href="#catalog" class="bg-amber-900 text-white px-10 py-5 rounded-2xl font-black uppercase text-xs tracking-widest shadow-xl">Belanja Sekarang</a>
                <a href="#about" class="bg-white border border-stone-200 text-stone-900 px-10 py-5 rounded-2xl font-black uppercase text-xs tracking-widest">Kisah Kami</a>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="py-24 px-6 bg-stone-50">
        <div class="max-w-4xl mx-auto text-center space-y-10">
            <div class="inline-block px-4 py-1.5 rounded-full bg-amber-100 text-amber-900 font-black uppercase text-[10px] tracking-widest mb-4">
                Sejak 2020
            </div>
            <h2 class="text-4xl md:text-6xl font-black uppercase tracking-tighter leading-tight">
                Membawa Semangat <br><span class="text-amber-900">Petani Lokal</span> ke Cangkir Anda
            </h2>
            <div class="grid md:grid-cols-2 gap-12 text-left pt-10">
                <p class="text-stone-500 leading-relaxed text-lg italic border-l-4 border-amber-900/20 pl-6">
                    Coffevor berawal dari kecintaan kami terhadap kekayaan kopi Nusantara. Kami bekerja sama secara langsung dengan petani lokal untuk memastikan setiap biji kopi dipanen pada kematangan sempurna dan diproses dengan standar tertinggi.
                </p>
                <div class="space-y-6">
                    <p class="text-stone-500 leading-relaxed">
                        Setiap batch disangrai dengan presisi oleh <span class="text-amber-900 font-bold">Master Roaster</span> kami untuk memunculkan profil rasa yang unik dan otentik dari setiap daerah asal.
                    </p>
                    <div class="grid grid-cols-2 gap-8 pt-4">
                        <div>
                            <div class="text-3xl font-black text-amber-900 mb-1">100%</div>
                            <div class="text-[10px] font-black uppercase tracking-widest text-stone-400">Biji Kopi Pilihan</div>
                        </div>
                        <div>
                            <div class="text-3xl font-black text-amber-900 mb-1">24h</div>
                            <div class="text-[10px] font-black uppercase tracking-widest text-stone-400">Freshly Roasted</div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Catalog (Tanpa Gambar & Ikon) -->
    <section id="catalog" class="py-24 px-6 bg-white">
        <div class="max-w-7xl mx-auto">
            <div class="flex flex-col md:flex-row md:items-end justify-between mb-12 gap-6">
                <div>
                    <h2 class="text-4xl font-black uppercase tracking-tighter">Koleksi <span class="text-amber-900">Eksklusif</span></h2>
                    <div id="price-badge" class="inline-block mt-4 px-4 py-1 rounded-full bg-stone-100 text-[10px] font-black uppercase tracking-widest text-stone-500">Mode: Harga Customer</div>
                </div>
                <div class="bg-amber-50 border border-amber-100 p-4 rounded-2xl max-w-xs">
                    <p class="text-amber-900 text-[10px] font-black uppercase tracking-widest mb-1">Promo Khusus</p>
                    <p class="text-stone-600 text-[11px] leading-tight font-medium">Gratis Ongkir otomatis untuk total pesanan kelipatan <span class="font-bold">1 Kg</span> (1kg, 2kg, dst).</p>
                </div>
            </div>

            <div class="grid md:grid-cols-3 gap-10">
                <!-- Arabika -->
                <div class="coffee-card bg-stone-50 p-10 rounded-[3.5rem] border border-stone-100 flex flex-col justify-between group transition-all duration-500">
                    <div>
                        <div class="mb-6">
                            <span class="bg-amber-900 text-white text-[9px] font-black uppercase px-3 py-1 rounded-full">Arabica Beans</span>
                        </div>
                        <h3 class="text-3xl font-black uppercase mb-1">Arabika</h3>
                        <p class="text-stone-400 text-[10px] mb-8 font-bold uppercase tracking-[0.2em]">Specialty Grade</p>
                        
                        <div class="space-y-4 mb-8">
                            <label class="text-[10px] font-black uppercase tracking-widest text-stone-400 ml-1">Pilih Ukuran</label>
                            <select id="size-arabika" class="w-full p-5 rounded-2xl bg-white font-bold outline-none text-sm border border-transparent focus:border-amber-900/10 shadow-sm" onchange="updateDisplayPrices()">
                                <option value="0.1" data-price="20000" data-agent="15000">100 Gram</option>
                                <option value="0.25" data-price="50000" data-agent="40000">250 Gram</option>
                                <option value="1" data-price="175000" data-agent="150000">1 KG</option>
                            </select>
                        </div>
                    </div>

                    <div>
                        <div class="flex justify-between items-center mb-8">
                            <span id="price-arabika" class="text-3xl font-black text-amber-900 tracking-tighter">Rp 20.000</span>
                        </div>
                        <button onclick="addToCart('Arabika', 'size-arabika')" class="w-full bg-stone-900 text-white p-6 rounded-2xl font-black uppercase text-[10px] tracking-widest group-hover:bg-amber-900 transition-colors shadow-lg">Tambah ke Keranjang</button>
                    </div>
                </div>

                <!-- Robusta -->
                <div class="coffee-card bg-stone-50 p-10 rounded-[3.5rem] border border-stone-100 flex flex-col justify-between group transition-all duration-500">
                    <div>
                        <div class="mb-6">
                            <span class="bg-amber-950 text-white text-[9px] font-black uppercase px-3 py-1 rounded-full">Robusta Beans</span>
                        </div>
                        <h3 class="text-3xl font-black uppercase mb-1">Robusta</h3>
                        <p class="text-stone-400 text-[10px] mb-8 font-bold uppercase tracking-[0.2em]">Premium Pick</p>
                        
                        <div class="space-y-4 mb-8">
                            <label class="text-[10px] font-black uppercase tracking-widest text-stone-400 ml-1">Pilih Ukuran</label>
                            <select id="size-robusta" class="w-full p-5 rounded-2xl bg-white font-bold outline-none text-sm border border-transparent focus:border-amber-900/10 shadow-sm" onchange="updateDisplayPrices()">
                                <option value="0.1" data-price="17000" data-agent="12000">100 Gram</option>
                                <option value="0.25" data-price="34000" data-agent="28000">250 Gram</option>
                                <option value="1" data-price="140000" data-agent="115000">1 KG</option>
                            </select>
                        </div>
                    </div>

                    <div>
                        <div class="flex justify-between items-center mb-8">
                            <span id="price-robusta" class="text-3xl font-black text-amber-900 tracking-tighter">Rp 17.000</span>
                        </div>
                        <button onclick="addToCart('Robusta', 'size-robusta')" class="w-full bg-stone-900 text-white p-6 rounded-2xl font-black uppercase text-[10px] tracking-widest group-hover:bg-amber-900 transition-colors shadow-lg">Tambah ke Keranjang</button>
                    </div>
                </div>

                <!-- Blend -->
                <div class="coffee-card bg-stone-50 p-10 rounded-[3.5rem] border border-stone-100 flex flex-col justify-between group transition-all duration-500">
                    <div>
                        <div class="mb-6">
                            <span class="bg-amber-700 text-white text-[9px] font-black uppercase px-3 py-1 rounded-full">House Blend</span>
                        </div>
                        <h3 class="text-3xl font-black uppercase mb-1">House Blend</h3>
                        <p class="text-stone-400 text-[10px] mb-8 font-bold uppercase tracking-[0.2em]">Classic Mix</p>
                        
                        <div class="space-y-4 mb-8">
                            <label class="text-[10px] font-black uppercase tracking-widest text-stone-400 ml-1">Pilih Ukuran</label>
                            <select id="size-blend" class="w-full p-5 rounded-2xl bg-white font-bold outline-none text-sm border border-transparent focus:border-amber-900/10 shadow-sm" onchange="updateDisplayPrices()">
                                <option value="0.1" data-price="22000" data-agent="18000">100 Gram</option>
                                <option value="0.25" data-price="50000" data-agent="42000">250 Gram</option>
                                <option value="1" data-price="180000" data-agent="155000">1 KG</option>
                            </select>
                        </div>
                    </div>

                    <div>
                        <div class="flex justify-between items-center mb-8">
                            <span id="price-blend" class="text-3xl font-black text-amber-900 tracking-tighter">Rp 22.000</span>
                        </div>
                        <button onclick="addToCart('House Blend', 'size-blend')" class="w-full bg-stone-900 text-white p-6 rounded-2xl font-black uppercase text-[10px] tracking-widest group-hover:bg-amber-900 transition-colors shadow-lg">Tambah ke Keranjang</button>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Main Order Form -->
    <section id="order-form" class="py-24 px-6 bg-stone-50">
        <div class="max-w-4xl mx-auto bg-white rounded-[4rem] shadow-2xl p-8 md:p-16 border border-stone-100">
            <h2 class="text-3xl font-black uppercase tracking-tighter text-center mb-4">Informasi Pengiriman</h2>
            <p class="text-center text-stone-400 text-sm mb-12 font-medium tracking-tight">Mohon lengkapi data di bawah untuk proses pengiriman cepat.</p>
            
            <form id="shipping-form" onsubmit="handleOrder(event)" class="space-y-8">
                <!-- Group Identity -->
                <div class="p-8 bg-amber-50 rounded-[2.5rem] border border-amber-100">
                    <label class="text-[10px] font-black uppercase tracking-widest text-amber-900 block mb-3">Punya Kode Voucher?</label>
                    <div class="flex gap-3">
                        <input type="text" id="voucher-input" placeholder="Ketik Kode" class="flex-1 p-5 rounded-2xl border-none outline-none font-bold uppercase shadow-inner text-sm">
                        <button type="button" onclick="applyVoucher()" class="bg-amber-900 text-white px-8 rounded-2xl font-black text-[10px] uppercase tracking-widest hover:brightness-110 active:scale-95 transition">Verifikasi</button>
                    </div>
                    <p id="voucher-info" class="text-[9px] font-bold uppercase mt-3 text-amber-900/40 tracking-widest">Masukkan kode khusus agen/dropshipper.</p>
                </div>

                <div class="grid md:grid-cols-2 gap-6">
                    <div class="space-y-3">
                        <label class="text-[10px] font-black uppercase tracking-widest text-stone-400 ml-4">Nama Penerima</label>
                        <input type="text" name="name" required placeholder="Nama Lengkap" class="w-full p-5 rounded-2xl bg-stone-50 outline-none focus:ring-2 ring-amber-900/10 font-bold text-sm">
                    </div>
                    <div class="space-y-3">
                        <label class="text-[10px] font-black uppercase tracking-widest text-stone-400 ml-4">WhatsApp Penerima</label>
                        <input type="tel" name="phone" required placeholder="08xxxx" class="w-full p-5 rounded-2xl bg-stone-50 outline-none focus:ring-2 ring-amber-900/10 font-bold text-sm">
                    </div>
                </div>

                <!-- Agent Name (Only if Agent Mode) -->
                <div id="agent-input-container" class="hidden space-y-3 animate-pulse">
                    <label class="text-[10px] font-black uppercase tracking-widest text-green-600 ml-4 italic">Nama Pengirim (Identitas Dropship)</label>
                    <input type="text" name="agent_name" placeholder="Nama Toko/Pribadi Anda" class="w-full p-5 rounded-2xl bg-green-50 outline-none border border-green-200 font-bold text-sm text-green-900">
                </div>

                <div class="border-t border-stone-100 pt-10">
                    <span class="text-[10px] font-black uppercase tracking-widest text-stone-400 block mb-8 text-center underline decoration-amber-900/20 underline-offset-8">Detail Lokasi Pengiriman</span>
                    <div class="grid grid-cols-2 md:grid-cols-4 gap-4">
                        <input type="text" name="provinsi" placeholder="Provinsi" required class="p-4 rounded-xl bg-stone-50 text-sm font-bold placeholder:text-stone-300">
                        <input type="text" name="kabupaten" placeholder="Kab/Kota" required class="p-4 rounded-xl bg-stone-50 text-sm font-bold placeholder:text-stone-300">
                        <input type="text" name="kecamatan" placeholder="Kecamatan" required class="p-4 rounded-xl bg-stone-50 text-sm font-bold placeholder:text-stone-300">
                        <input type="text" name="desa" placeholder="Desa/Kel" required class="p-4 rounded-xl bg-stone-50 text-sm font-bold placeholder:text-stone-300">
                        <input type="text" name="dusun" placeholder="Dusun" class="p-4 rounded-xl bg-stone-50 text-sm font-bold placeholder:text-stone-300">
                        <input type="text" name="jalan" placeholder="Jalan" class="p-4 rounded-xl bg-stone-50 text-sm font-bold placeholder:text-stone-300">
                        <input type="text" name="blok" placeholder="Blok" class="p-4 rounded-xl bg-stone-50 text-sm font-bold placeholder:text-stone-300">
                        <input type="text" name="no_rumah" placeholder="No. Rumah" class="p-4 rounded-xl bg-stone-50 text-sm font-bold placeholder:text-stone-300">
                        <input type="text" name="rt" placeholder="RT" class="p-4 rounded-xl bg-stone-50 text-sm font-bold placeholder:text-stone-300">
                        <input type="text" name="rw" placeholder="RW" class="p-4 rounded-xl bg-stone-50 text-sm font-bold placeholder:text-stone-300">
                    </div>
                </div>

                <div class="space-y-3 pt-4">
                    <label class="text-[10px] font-black uppercase tracking-widest text-stone-400 ml-4">Permintaan Khusus (Opsional)</label>
                    <textarea name="notes" rows="3" placeholder="Contoh: Giling halus untuk espresso, giling kasar untuk V60, dll." class="w-full p-5 rounded-2xl bg-stone-50 outline-none resize-none font-medium text-sm"></textarea>
                </div>

                <button type="submit" class="w-full bg-amber-900 text-white p-6 rounded-[2rem] font-black uppercase text-xs tracking-widest shadow-2xl hover:scale-[1.01] transition-all active:scale-95 mt-4">
                    Konfirmasi via WhatsApp
                </button>
            </form>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-stone-900 text-white py-20 px-6">
        <div class="max-w-7xl mx-auto flex flex-col md:flex-row justify-between items-center gap-12">
            <div class="text-center md:text-left">
                <div class="flex items-center gap-3 mb-6 justify-center md:justify-start">
                    <div class="bg-amber-900 p-2 rounded-xl">
                        <svg class="w-5 h-5 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8h1a4 4 0 1 1 0 8h-1M3 8h14v9a4 4 0 0 1-4 4H7a4 4 0 0 1-4-4Z"></path></svg>
                    </div>
                    <span class="font-black text-2xl tracking-tighter uppercase">Coffevor</span>
                </div>
                <p class="text-stone-500 text-sm max-w-sm mb-8 leading-relaxed">Nikmati kemewahan kopi artisan pilihan dari tanah Nusantara. Terkurasi, Terpanggang Sempurna.</p>
                <div class="flex gap-6 justify-center md:justify-start">
                    <!-- TikTok -->
                    <a href="https://www.tiktok.com/@c<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Coffevor | Premium Artisan Roastery</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@200;400;600;800&display=swap" rel="stylesheet">
    <style>
        body { font-family: 'Plus Jakarta Sans', sans-serif; scroll-behavior: smooth; }
        .glass-nav { background: rgba(255, 255, 255, 0.8); backdrop-filter: blur(20px); }
        .hero-gradient { background: radial-gradient(circle at top right, #fffbeb, transparent); }
        .cart-sidebar { transition: transform 0.3s ease-in-out; }
        .hide-scrollbar::-webkit-scrollbar { display: none; }
        input, textarea, select { transition: all 0.2s ease; }
        
        .coffee-card { transition: all 0.3s ease; }
        .coffee-card:hover { transform: translateY(-5px); border-color: #78350f20; }
    </style>
</head>
<body class="bg-[#FDFCFB] text-stone-900 selection:bg-amber-200">

    <!-- Navbar -->
    <nav class="fixed w-full z-50 border-b border-stone-100 glass-nav">
        <div class="max-w-7xl mx-auto px-6 h-20 flex items-center justify-between">
            <div class="flex items-center gap-3">
                <div class="bg-amber-900 p-2 rounded-xl shadow-lg">
                    <svg class="w-5 h-5 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8h1a4 4 0 1 1 0 8h-1M3 8h14v9a4 4 0 0 1-4 4H7a4 4 0 0 1-4-4Z"></path></svg>
                </div>
                <span class="font-black text-2xl tracking-tighter text-amber-900 uppercase">Coffevor</span>
            </div>
            <div class="hidden md:flex items-center gap-8 font-extrabold text-[10px] uppercase tracking-widest text-stone-500">
                <a href="#about" class="hover:text-amber-900 transition">Tentang Kami</a>
                <a href="#catalog" class="hover:text-amber-900 transition">Katalog</a>
                <a href="#order-form" class="hover:text-amber-900 transition">Pesan</a>
                <button onclick="toggleCart()" class="relative flex items-center gap-2 bg-amber-900 text-white px-5 py-3 rounded-full shadow-xl hover:scale-105 transition active:scale-95">
                    <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 3h2l.4 2M7 13h10l4-8H5.4M7 13L5.4 5M7 13l-2.293 2.293c-.63.63-.184 1.707.707 1.707H17m0 0a2 2 0 100 4 2 2 0 000-4zm-8 2a2 2 0 11-4 0 2 2 0 014 0z"></path></svg>
                    <span id="cart-count">0</span>
                </button>
            </div>
        </div>
    </nav>

    <!-- Hero -->
    <section class="relative pt-44 pb-20 px-6 hero-gradient">
        <div class="max-w-5xl mx-auto text-center">
            <h1 class="text-6xl md:text-8xl font-black tracking-tighter leading-none mb-6 uppercase">Freshly <span class="text-amber-900">Roasted</span></h1>
            <p class="text-stone-500 text-lg mb-10 font-medium tracking-tight">Kopi artisan kualitas ekspor, dikirim langsung ke rumah Anda.</p>
            <div class="flex flex-wrap justify-center gap-4">
                <a href="#catalog" class="bg-amber-900 text-white px-10 py-5 rounded-2xl font-black uppercase text-xs tracking-widest shadow-xl">Belanja Sekarang</a>
                <a href="#about" class="bg-white border border-stone-200 text-stone-900 px-10 py-5 rounded-2xl font-black uppercase text-xs tracking-widest">Kisah Kami</a>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="py-24 px-6 bg-stone-50">
        <div class="max-w-4xl mx-auto text-center space-y-10">
            <div class="inline-block px-4 py-1.5 rounded-full bg-amber-100 text-amber-900 font-black uppercase text-[10px] tracking-widest mb-4">
                Sejak 2020
            </div>
            <h2 class="text-4xl md:text-6xl font-black uppercase tracking-tighter leading-tight">
                Membawa Semangat <br><span class="text-amber-900">Petani Lokal</span> ke Cangkir Anda
            </h2>
            <div class="grid md:grid-cols-2 gap-12 text-left pt-10">
                <p class="text-stone-500 leading-relaxed text-lg italic border-l-4 border-amber-900/20 pl-6">
                    Coffevor berawal dari kecintaan kami terhadap kekayaan kopi Nusantara. Kami bekerja sama secara langsung dengan petani lokal untuk memastikan setiap biji kopi dipanen pada kematangan sempurna dan diproses dengan standar tertinggi.
                </p>
                <div class="space-y-6">
                    <p class="text-stone-500 leading-relaxed">
                        Setiap batch disangrai dengan presisi oleh <span class="text-amber-900 font-bold">Master Roaster</span> kami untuk memunculkan profil rasa yang unik dan otentik dari setiap daerah asal.
                    </p>
                    <div class="grid grid-cols-2 gap-8 pt-4">
                        <div>
                            <div class="text-3xl font-black text-amber-900 mb-1">100%</div>
                            <div class="text-[10px] font-black uppercase tracking-widest text-stone-400">Biji Kopi Pilihan</div>
                        </div>
                        <div>
                            <div class="text-3xl font-black text-amber-900 mb-1">24h</div>
                            <div class="text-[10px] font-black uppercase tracking-widest text-stone-400">Freshly Roasted</div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Catalog (Tanpa Gambar & Ikon) -->
    <section id="catalog" class="py-24 px-6 bg-white">
        <div class="max-w-7xl mx-auto">
            <div class="flex flex-col md:flex-row md:items-end justify-between mb-12 gap-6">
                <div>
                    <h2 class="text-4xl font-black uppercase tracking-tighter">Koleksi <span class="text-amber-900">Eksklusif</span></h2>
                    <div id="price-badge" class="inline-block mt-4 px-4 py-1 rounded-full bg-stone-100 text-[10px] font-black uppercase tracking-widest text-stone-500">Mode: Harga Customer</div>
                </div>
                <div class="bg-amber-50 border border-amber-100 p-4 rounded-2xl max-w-xs">
                    <p class="text-amber-900 text-[10px] font-black uppercase tracking-widest mb-1">Promo Khusus</p>
                    <p class="text-stone-600 text-[11px] leading-tight font-medium">Gratis Ongkir otomatis untuk total pesanan kelipatan <span class="font-bold">1 Kg</span> (1kg, 2kg, dst).</p>
                </div>
            </div>

            <div class="grid md:grid-cols-3 gap-10">
                <!-- Arabika -->
                <div class="coffee-card bg-stone-50 p-10 rounded-[3.5rem] border border-stone-100 flex flex-col justify-between group transition-all duration-500">
                    <div>
                        <div class="mb-6">
                            <span class="bg-amber-900 text-white text-[9px] font-black uppercase px-3 py-1 rounded-full">Arabica Beans</span>
                        </div>
                        <h3 class="text-3xl font-black uppercase mb-1">Arabika</h3>
                        <p class="text-stone-400 text-[10px] mb-8 font-bold uppercase tracking-[0.2em]">Specialty Grade</p>
                        
                        <div class="space-y-4 mb-8">
                            <label class="text-[10px] font-black uppercase tracking-widest text-stone-400 ml-1">Pilih Ukuran</label>
                            <select id="size-arabika" class="w-full p-5 rounded-2xl bg-white font-bold outline-none text-sm border border-transparent focus:border-amber-900/10 shadow-sm" onchange="updateDisplayPrices()">
                                <option value="0.1" data-price="20000" data-agent="15000">100 Gram</option>
                                <option value="0.25" data-price="50000" data-agent="40000">250 Gram</option>
                                <option value="1" data-price="175000" data-agent="150000">1 KG</option>
                            </select>
                        </div>
                    </div>

                    <div>
                        <div class="flex justify-between items-center mb-8">
                            <span id="price-arabika" class="text-3xl font-black text-amber-900 tracking-tighter">Rp 20.000</span>
                        </div>
                        <button onclick="addToCart('Arabika', 'size-arabika')" class="w-full bg-stone-900 text-white p-6 rounded-2xl font-black uppercase text-[10px] tracking-widest group-hover:bg-amber-900 transition-colors shadow-lg">Tambah ke Keranjang</button>
                    </div>
                </div>

                <!-- Robusta -->
                <div class="coffee-card bg-stone-50 p-10 rounded-[3.5rem] border border-stone-100 flex flex-col justify-between group transition-all duration-500">
                    <div>
                        <div class="mb-6">
                            <span class="bg-amber-950 text-white text-[9px] font-black uppercase px-3 py-1 rounded-full">Robusta Beans</span>
                        </div>
                        <h3 class="text-3xl font-black uppercase mb-1">Robusta</h3>
                        <p class="text-stone-400 text-[10px] mb-8 font-bold uppercase tracking-[0.2em]">Premium Pick</p>
                        
                        <div class="space-y-4 mb-8">
                            <label class="text-[10px] font-black uppercase tracking-widest text-stone-400 ml-1">Pilih Ukuran</label>
                            <select id="size-robusta" class="w-full p-5 rounded-2xl bg-white font-bold outline-none text-sm border border-transparent focus:border-amber-900/10 shadow-sm" onchange="updateDisplayPrices()">
                                <option value="0.1" data-price="17000" data-agent="12000">100 Gram</option>
                                <option value="0.25" data-price="34000" data-agent="28000">250 Gram</option>
                                <option value="1" data-price="140000" data-agent="115000">1 KG</option>
                            </select>
                        </div>
                    </div>

                    <div>
                        <div class="flex justify-between items-center mb-8">
                            <span id="price-robusta" class="text-3xl font-black text-amber-900 tracking-tighter">Rp 17.000</span>
                        </div>
                        <button onclick="addToCart('Robusta', 'size-robusta')" class="w-full bg-stone-900 text-white p-6 rounded-2xl font-black uppercase text-[10px] tracking-widest group-hover:bg-amber-900 transition-colors shadow-lg">Tambah ke Keranjang</button>
                    </div>
                </div>

                <!-- Blend -->
                <div class="coffee-card bg-stone-50 p-10 rounded-[3.5rem] border border-stone-100 flex flex-col justify-between group transition-all duration-500">
                    <div>
                        <div class="mb-6">
                            <span class="bg-amber-700 text-white text-[9px] font-black uppercase px-3 py-1 rounded-full">House Blend</span>
                        </div>
                        <h3 class="text-3xl font-black uppercase mb-1">House Blend</h3>
                        <p class="text-stone-400 text-[10px] mb-8 font-bold uppercase tracking-[0.2em]">Classic Mix</p>
                        
                        <div class="space-y-4 mb-8">
                            <label class="text-[10px] font-black uppercase tracking-widest text-stone-400 ml-1">Pilih Ukuran</label>
                            <select id="size-blend" class="w-full p-5 rounded-2xl bg-white font-bold outline-none text-sm border border-transparent focus:border-amber-900/10 shadow-sm" onchange="updateDisplayPrices()">
                                <option value="0.1" data-price="22000" data-agent="18000">100 Gram</option>
                                <option value="0.25" data-price="50000" data-agent="42000">250 Gram</option>
                                <option value="1" data-price="180000" data-agent="155000">1 KG</option>
                            </select>
                        </div>
                    </div>

                    <div>
                        <div class="flex justify-between items-center mb-8">
                            <span id="price-blend" class="text-3xl font-black text-amber-900 tracking-tighter">Rp 22.000</span>
                        </div>
                        <button onclick="addToCart('House Blend', 'size-blend')" class="w-full bg-stone-900 text-white p-6 rounded-2xl font-black uppercase text-[10px] tracking-widest group-hover:bg-amber-900 transition-colors shadow-lg">Tambah ke Keranjang</button>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Main Order Form -->
    <section id="order-form" class="py-24 px-6 bg-stone-50">
        <div class="max-w-4xl mx-auto bg-white rounded-[4rem] shadow-2xl p-8 md:p-16 border border-stone-100">
            <h2 class="text-3xl font-black uppercase tracking-tighter text-center mb-4">Informasi Pengiriman</h2>
            <p class="text-center text-stone-400 text-sm mb-12 font-medium tracking-tight">Mohon lengkapi data di bawah untuk proses pengiriman cepat.</p>
            
            <form id="shipping-form" onsubmit="handleOrder(event)" class="space-y-8">
                <!-- Group Identity -->
                <div class="p-8 bg-amber-50 rounded-[2.5rem] border border-amber-100">
                    <label class="text-[10px] font-black uppercase tracking-widest text-amber-900 block mb-3">Punya Kode Voucher?</label>
                    <div class="flex gap-3">
                        <input type="text" id="voucher-input" placeholder="Ketik Kode" class="flex-1 p-5 rounded-2xl border-none outline-none font-bold uppercase shadow-inner text-sm">
                        <button type="button" onclick="applyVoucher()" class="bg-amber-900 text-white px-8 rounded-2xl font-black text-[10px] uppercase tracking-widest hover:brightness-110 active:scale-95 transition">Verifikasi</button>
                    </div>
                    <p id="voucher-info" class="text-[9px] font-bold uppercase mt-3 text-amber-900/40 tracking-widest">Masukkan kode khusus agen/dropshipper.</p>
                </div>

                <div class="grid md:grid-cols-2 gap-6">
                    <div class="space-y-3">
                        <label class="text-[10px] font-black uppercase tracking-widest text-stone-400 ml-4">Nama Penerima</label>
                        <input type="text" name="name" required placeholder="Nama Lengkap" class="w-full p-5 rounded-2xl bg-stone-50 outline-none focus:ring-2 ring-amber-900/10 font-bold text-sm">
                    </div>
                    <div class="space-y-3">
                        <label class="text-[10px] font-black uppercase tracking-widest text-stone-400 ml-4">WhatsApp Penerima</label>
                        <input type="tel" name="phone" required placeholder="08xxxx" class="w-full p-5 rounded-2xl bg-stone-50 outline-none focus:ring-2 ring-amber-900/10 font-bold text-sm">
                    </div>
                </div>

                <!-- Agent Name (Only if Agent Mode) -->
                <div id="agent-input-container" class="hidden space-y-3 animate-pulse">
                    <label class="text-[10px] font-black uppercase tracking-widest text-green-600 ml-4 italic">Nama Pengirim (Identitas Dropship)</label>
                    <input type="text" name="agent_name" placeholder="Nama Toko/Pribadi Anda" class="w-full p-5 rounded-2xl bg-green-50 outline-none border border-green-200 font-bold text-sm text-green-900">
                </div>

                <div class="border-t border-stone-100 pt-10">
                    <span class="text-[10px] font-black uppercase tracking-widest text-stone-400 block mb-8 text-center underline decoration-amber-900/20 underline-offset-8">Detail Lokasi Pengiriman</span>
                    <div class="grid grid-cols-2 md:grid-cols-4 gap-4">
                        <input type="text" name="provinsi" placeholder="Provinsi" required class="p-4 rounded-xl bg-stone-50 text-sm font-bold placeholder:text-stone-300">
                        <input type="text" name="kabupaten" placeholder="Kab/Kota" required class="p-4 rounded-xl bg-stone-50 text-sm font-bold placeholder:text-stone-300">
                        <input type="text" name="kecamatan" placeholder="Kecamatan" required class="p-4 rounded-xl bg-stone-50 text-sm font-bold placeholder:text-stone-300">
                        <input type="text" name="desa" placeholder="Desa/Kel" required class="p-4 rounded-xl bg-stone-50 text-sm font-bold placeholder:text-stone-300">
                        <input type="text" name="dusun" placeholder="Dusun" class="p-4 rounded-xl bg-stone-50 text-sm font-bold placeholder:text-stone-300">
                        <input type="text" name="jalan" placeholder="Jalan" class="p-4 rounded-xl bg-stone-50 text-sm font-bold placeholder:text-stone-300">
                        <input type="text" name="blok" placeholder="Blok" class="p-4 rounded-xl bg-stone-50 text-sm font-bold placeholder:text-stone-300">
                        <input type="text" name="no_rumah" placeholder="No. Rumah" class="p-4 rounded-xl bg-stone-50 text-sm font-bold placeholder:text-stone-300">
                        <input type="text" name="rt" placeholder="RT" class="p-4 rounded-xl bg-stone-50 text-sm font-bold placeholder:text-stone-300">
                        <input type="text" name="rw" placeholder="RW" class="p-4 rounded-xl bg-stone-50 text-sm font-bold placeholder:text-stone-300">
                    </div>
                </div>

                <div class="space-y-3 pt-4">
                    <label class="text-[10px] font-black uppercase tracking-widest text-stone-400 ml-4">Permintaan Khusus (Opsional)</label>
                    <textarea name="notes" rows="3" placeholder="Contoh: Giling halus untuk espresso, giling kasar untuk V60, dll." class="w-full p-5 rounded-2xl bg-stone-50 outline-none resize-none font-medium text-sm"></textarea>
                </div>

                <button type="submit" class="w-full bg-amber-900 text-white p-6 rounded-[2rem] font-black uppercase text-xs tracking-widest shadow-2xl hover:scale-[1.01] transition-all active:scale-95 mt-4">
                    Konfirmasi via WhatsApp
                </button>
            </form>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-stone-900 text-white py-20 px-6">
        <div class="max-w-7xl mx-auto flex flex-col md:flex-row justify-between items-center gap-12">
            <div class="text-center md:text-left">
                <div class="flex items-center gap-3 mb-6 justify-center md:justify-start">
                    <div class="bg-amber-900 p-2 rounded-xl">
                        <svg class="w-5 h-5 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8h1a4 4 0 1 1 0 8h-1M3 8h14v9a4 4 0 0 1-4 4H7a4 4 0 0 1-4-4Z"></path></svg>
                    </div>
                    <span class="font-black text-2xl tracking-tighter uppercase">Coffevor</span>
                </div>
                <p class="text-stone-500 text-sm max-w-sm mb-8 leading-relaxed">Nikmati kemewahan kopi artisan pilihan dari tanah Nusantara. Terkurasi, Terpanggang Sempurna.</p>
                <div class="flex gap-6 justify-center md:justify-start">
                    <!-- TikTok -->
                    <a href="https://www.tiktok.com/@coffeevor.officia?_r=1&_t=ZS-93ZvLShaVBR" target="_blank" class="w-12 h-12 bg-white/5 rounded-2xl flex items-center justify-center hover:bg-white/10 transition group">
                        <svg class="w-5 h-5 text-white group-hover:scale-110 transition" fill="currentColor" viewBox="0 0 24 24">
                            <path d="M12.525.02c1.31-.02 2.61-.01 3.91-.02.08 1.53.63 3.09 1.75 4.17 1.12 1.11 2.7 1.62 4.24 1.79v4.03c-1.44-.05-2.89-.35-4.2-.97-.06 3.42-.3 6.84-1.35 10.12-1.13 3.39-3.52 6.5-7.37 7.55-2.91.81-6.19.46-8.79-1.21-2.98-1.74-4.88-5.23-4.66-8.69.11-4.13 2.92-8.03 6.9-9.15 1.14-.32 2.34-.44 3.53-.41V7.71c-1.42-.03-2.88.22-4.13.92-1.57.85-2.67 2.45-2.86 4.22-.24 2.53 1.13 5.09 3.4 6.2 1.3.65 2.82.78 4.24.4 2.05-.51 3.73-2.22 4.23-4.23.46-1.74.52-3.55.51-5.34-.01-3.41-.01-6.81-.01-10.22Z"/>
                        </svg>
                    </a>
                    <!-- Youtube -->
                    <a href="https://youtube.com/@oviewoou?si=g_D4QNqHsxH7cvjA" target="_blank" class="w-12 h-12 bg-white/5 rounded-2xl flex items-center justify-center hover:bg-white/10 transition group">
                        <svg class="w-6 h-6 text-white group-hover:scale-110 transition" fill="currentColor" viewBox="0 0 24 24">
                            <path d="M23.498 6.186a3.016 3.016 0 0 0-2.122-2.136C19.505 3.545 12 3.545 12 3.545s-7.505 0-9.377.505A3.017 3.017 0 0 0 .502 6.186C0 8.07 0 12 0 12s0 3.93.502 5.814a3.016 3.016 0 0 0 2.122 2.136c1.871.505 9.376.505 9.376.505s7.505 0 9.377-.505a3.015 3.015 0 0 0 2.122-2.136C24 15.93 24 12 24 12s0-3.93-.502-5.814Z"/>
                            <path fill="white" d="M9.545 15.568V8.432L15.818 12l-6.273 3.568Z"/>
                        </svg>
                    </a>
                </div>
            </div>
            <div class="text-[10px] font-black uppercase tracking-[0.4em] text-stone-700">
                &copy; 2026 Coffevor Artisan. All Rights Reserved.
            </div>
        </div>
    </footer>

    <!-- Cart Sidebar -->
    <div id="cart-overlay" class="fixed inset-0 z-[60] bg-black/60 hidden backdrop-blur-md" onclick="toggleCart()"></div>
    <div id="cart-sidebar" class="fixed right-0 top-0 h-full w-full max-w-md bg-white z-[70] shadow-2xl translate-x-full cart-sidebar flex flex-col">
        <div class="p-8 border-b border-stone-100 flex justify-between items-center">
            <div>
                <h3 class="text-2xl font-black uppercase tracking-tighter">Keranjang</h3>
                <p id="cart-items-count-text" class="text-[9px] font-bold text-stone-400 uppercase tracking-widest mt-1">0 Item Terpilih</p>
            </div>
            <button onclick="toggleCart()" class="w-10 h-10 rounded-full bg-stone-50 flex items-center justify-center hover:bg-stone-100 transition">
                <svg class="w-4 h-4 text-stone-400" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"></path></svg>
            </button>
        </div>

        <div id="cart-items" class="flex-1 overflow-y-auto p-8 space-y-4 hide-scrollbar">
            <!-- Items appear here -->
        </div>

        <div class="p-8 bg-stone-50 border-t border-stone-100 space-y-6">
            <div id="free-shipping-promo" class="hidden animate-bounce bg-green-100 p-3 rounded-xl border border-green-200 flex items-center justify-center gap-2">
                <svg class="w-4 h-4 text-green-600" fill="currentColor" viewBox="0 0 24 24"><path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm-2 15l-5-5 1.41-1.41L10 14.17l7.59-7.59L19 8l-9 9z"/></svg>
                <span class="text-[10px] font-black text-green-700 uppercase tracking-widest">Gratis Ongkir Aktif!</span>
            </div>
            <div class="flex justify-between items-center">
                <div class="flex flex-col">
                    <span class="text-xs font-black uppercase text-stone-400 tracking-widest">Total Pembayaran</span>
                    <span id="total-weight-text" class="text-[9px] font-bold text-stone-400 uppercase">Berat: 0 Kg</span>
                </div>
                <span id="cart-total" class="text-2xl font-black text-amber-900 tracking-tighter">Rp 0</span>
            </div>
            <button onclick="goToForm()" class="w-full bg-amber-900 text-white p-5 rounded-2xl font-black uppercase text-xs tracking-widest shadow-xl hover:brightness-110 active:scale-95 transition">Selesaikan Pesanan</button>
        </div>
    </div>

    <script>
        let cart = [];
        let isAgent = false;
        const VOUCHER_CODE = "KOPIJUARA";

        function applyVoucher() {
            const val = document.getElementById('voucher-input').value.trim().toUpperCase();
            const info = document.getElementById('voucher-info');
            const agentFields = document.getElementById('agent-input-container');
            const badge = document.getElementById('price-badge');

            if (val === VOUCHER_CODE) {
                isAgent = true;
                info.innerText = "✓ KODE AGEN TERVERIFIKASI";
                info.className = "text-[9px] font-black uppercase mt-3 text-green-600 tracking-widest";
                agentFields.classList.remove('hidden');
                badge.innerText = "Mode: Harga Agen Aktif";
                badge.className = "inline-block mt-4 px-4 py-1 rounded-full bg-green-100 text-[10px] font-black uppercase tracking-widest text-green-700";
            } else {
                isAgent = false;
                info.innerText = val === "" ? "Masukkan kode khusus agen/dropshipper." : "❌ KODE TIDAK DAPAT DITEMUKAN";
                info.className = val === "" ? "text-[9px] font-bold uppercase mt-3 text-amber-900/40 tracking-widest" : "text-[9px] font-black uppercase mt-3 text-red-500 tracking-widest";
                agentFields.classList.add('hidden');
                badge.innerText = "Mode: Harga Customer";
                badge.className = "inline-block mt-4 px-4 py-1 rounded-full bg-stone-100 text-[10px] font-black uppercase tracking-widest text-stone-500";
            }
            syncCartPrices();
            updateDisplayPrices();
            updateCartUI();
        }

        function updateDisplayPrices() {
            const prods = [
                { s: 'size-arabika', p: 'price-arabika' },
                { s: 'size-robusta', p: 'price-robusta' },
                { s: 'size-blend', p: 'price-blend' }
            ];
            prods.forEach(item => {
                const el = document.getElementById(item.s);
                const price = isAgent ? el.options[el.selectedIndex].dataset.agent : el.options[el.selectedIndex].dataset.price;
                document.getElementById(item.p).innerText = `Rp ${parseInt(price).toLocaleString()}`;
            });
        }

        function addToCart(name, selectId) {
            const el = document.getElementById(selectId);
            const opt = el.options[el.selectedIndex];
            const sizeValue = parseFloat(opt.value);
            const sizeLabel = opt.text;
            const price = isAgent ? parseInt(opt.dataset.agent) : parseInt(opt.dataset.price);

            const existing = cart.find(i => i.name === name && i.size === sizeValue);
            if (existing) {
                existing.qty++;
            } else {
                cart.push({ name, size: sizeValue, sizeLabel, price, qty: 1 });
            }
            updateCartUI();
            toggleCart();
        }

        function changeQty(index, delta) {
            cart[index].qty += delta;
            if (cart[index].qty <= 0) cart.splice(index, 1);
            updateCartUI();
        }

        function syncCartPrices() {
            cart = cart.map(item => {
                const slug = item.name.toLowerCase().replace(' ', '-');
                const select = document.getElementById(`size-${slug === 'house-blend' ? 'blend' : slug}`);
                let currentPrice = item.price;
                if(select) {
                    for(let o of select.options) {
                        if(parseFloat(o.value) === item.size) {
                            currentPrice = isAgent ? parseInt(o.dataset.agent) : parseInt(o.dataset.price);
                            break;
                        }
                    }
                }
                return { ...item, price: currentPrice };
            });
        }

        function updateCartUI() {
            const list = document.getElementById('cart-items');
            const count = document.getElementById('cart-count');
            const countText = document.getElementById('cart-items-count-text');
            const total = document.getElementById('cart-total');
            const weightText = document.getElementById('total-weight-text');
            const freeShippingBadge = document.getElementById('free-shipping-promo');
            
            list.innerHTML = '';
            let sum = 0;
            let totalQty = 0;
            let totalWeight = 0;

            if(cart.length === 0) {
                list.innerHTML = '<div class="h-full flex flex-col items-center justify-center text-stone-300 py-20"><svg class="w-12 h-12 mb-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path d="M16 11V7a4 4 0 00-8 0v4M5 9h14l1 12H4L5 9z"></path></svg><p class="text-[10px] font-black uppercase tracking-widest">Keranjang Kosong</p></div>';
            }

            cart.forEach((item, index) => {
                const sub = item.price * item.qty;
                sum += sub;
                totalQty += item.qty;
                totalWeight += (item.size * item.qty);
                list.innerHTML += `
                    <div class="bg-stone-50 p-6 rounded-3xl flex justify-between items-center border border-stone-100">
                        <div class="flex-1">
                            <h4 class="text-[11px] font-black uppercase text-amber-900 leading-none mb-1">${item.name}</h4>
                            <p class="text-[9px] font-bold text-stone-400 uppercase tracking-tight">${item.sizeLabel}</p>
                            <p class="text-sm font-black mt-2 tracking-tight">Rp ${sub.toLocaleString()}</p>
                        </div>
                        <div class="flex items-center gap-4 bg-white px-4 py-2 rounded-2xl shadow-sm border border-stone-100">
                            <button onclick="changeQty(${index}, -1)" class="w-5 h-5 flex items-center justify-center font-bold text-stone-300 hover:text-red-500 transition">-</button>
                            <span class="text-xs font-black w-4 text-center">${item.qty}</span>
                            <button onclick="changeQty(${index}, 1)" class="w-5 h-5 flex items-center justify-center font-bold text-amber-900 hover:scale-125 transition">+</button>
                        </div>
                    </div>
                `;
            });

            const isFreeShipping = totalWeight > 0 && Number.isInteger(totalWeight);
            
            if (isFreeShipping) {
                freeShippingBadge.classList.remove('hidden');
            } else {
                freeShippingBadge.classList.add('hidden');
            }

            count.innerText = totalQty;
            countText.innerText = `${totalQty} Item Terpilih`;
            weightText.innerText = `Total Berat: ${totalWeight.toFixed(2)} Kg`;
            total.innerText = `Rp ${sum.toLocaleString()}`;
        }

        function handleOrder(event) {
            event.preventDefault();
            if (cart.length === 0) return;

            const fd = new FormData(event.target);
            const totalStr = document.getElementById('cart-total').innerText;
            const weightVal = cart.reduce((acc, curr) => acc + (curr.size * curr.qty), 0);
            const freeShipping = Number.isInteger(weightVal) && weightVal > 0;
            
            let itemsText = cart.map(i => `- ${i.name} (${i.sizeLabel}) x${i.qty} = Rp ${(i.price * i.qty).toLocaleString()}`).join('%0A');

            let waMsg = `*PESANAN COFFEVOR (${isAgent ? 'AGEN' : 'CUSTOMER'})*%0A%0A`;
            waMsg += `*PENERIMA:*%0A`;
            waMsg += `- Nama: ${fd.get('name')}%0A`;
            waMsg += `- WA: ${fd.get('phone')}%0A`;

            if(isAgent) {
                waMsg += `%0A*PENGIRIM (DROPSHIP):*%0A`;
                waMsg += `- Agen: ${fd.get('agent_name')}%0A`;
            }

            waMsg += `%0A*ALAMAT:*%0A`;
            waMsg += `${fd.get('jalan') || '-'}, Blok ${fd.get('blok') || '-'} No.${fd.get('no_rumah') || '-'}%0A`;
            waMsg += `RT/RW: ${fd.get('rt') || '-'}/${fd.get('rw') || '-'}%0A`;
            waMsg += `Desa/Dusun: ${fd.get('desa')}/${fd.get('dusun') || '-'}%0A`;
            waMsg += `Kec: ${fd.get('kecamatan')}%0A`;
            waMsg += `${fd.get('kabupaten')}, ${fd.get('provinsi')}%0A`;

            waMsg += `%0A*DETAIL PESANAN:*%0A${itemsText}%0A`;
            waMsg += `%0A*BERAT TOTAL:* ${weightVal.toFixed(2)} Kg%0A`;
            waMsg += `*PROMO:* ${freeShipping ? 'GRATIS ONGKIR AKTIF' : 'Ongkir Normal'}%0A`;
            waMsg += `*TOTAL:* ${totalStr}%0A`;
            if(fd.get('notes')) waMsg += `%0A*CATATAN:* ${fd.get('notes')}`;

            window.open(`https://wa.me/6285881583885?text=${waMsg}`, '_blank');
        }

        function toggleCart() {
            document.getElementById('cart-sidebar').classList.toggle('translate-x-full');
            document.getElementById('cart-overlay').classList.toggle('hidden');
        }

        function goToForm() {
            if(cart.length === 0) return;
            toggleCart();
            document.getElementById('order-form').scrollIntoView();
        }

        window.onload = updateDisplayPrices;
    </script>
</body>
</html>
