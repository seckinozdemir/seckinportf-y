# seckinportf-y
Fotoğrafçılık, web tasarım, video tasarım, sosyal medya çalışmalarımın yer aldığı çalışmalar
<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Seçkin Özdemir - Portfolyo</title>
    <style>
        * {
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            margin: 0;
            background-color: #f8f9fa;
            color: #333;
        }

        header {
            background: linear-gradient(135deg, #1e293b, #0f172a);
            color: #fff;
            padding: 40px 20px;
            text-align: center;
        }

        header h1 {
            margin: 0 0 10px 0;
            font-size: 2.5rem;
        }

        header p {
            margin: 0;
            color: #94a3b8;
            font-size: 1.1rem;
        }

        main {
            max-width: 1200px;
            margin: 30px auto;
            padding: 0 20px;
        }

        .tab-buttons {
            display: flex;
            gap: 10px;
            border-bottom: 2px solid #e2e8f0;
            margin-bottom: 30px;
            flex-wrap: wrap;
        }

        .tab-button {
            padding: 12px 24px;
            background-color: transparent;
            border: none;
            border-bottom: 3px solid transparent;
            font-size: 1rem;
            font-weight: 600;
            color: #64748b;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .tab-button:hover {
            color: #0284c7;
        }

        .tab-button.active {
            color: #0284c7;
            border-bottom-color: #0284c7;
        }

        .tab-content {
            display: none;
            animation: fadeIn 0.4s ease;
        }

        .tab-content.active {
            display: block;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(5px); }
            to { opacity: 1; transform: translateY(0); }
        }

        /* Fotoğraf Galerisi Grid Stili */
        .portfolio-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
            grid-gap: 20px;
        }

        .portfolio-item {
            background: #fff;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 4px 6px -1px rgba(0,0,0,0.1);
            transition: transform 0.2s ease;
        }

        .portfolio-item:hover {
            transform: translateY(-4px);
        }

        .portfolio-item img {
            width: 100%;
            height: 220px;
            object-fit: cover;
            cursor: pointer;
            display: block;
        }

        .portfolio-item-body {
            padding: 15px;
        }

        .portfolio-item h3 {
            margin: 0 0 5px 0;
            font-size: 1.1rem;
        }

        .portfolio-item p {
            margin: 0;
            color: #64748b;
            font-size: 0.9rem;
        }

        /* Web Siteleri Grid Stili */
        .web-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(320px, 1fr));
            grid-gap: 25px;
        }

        .web-card {
            background: #fff;
            border-radius: 12px;
            padding: 24px;
            box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -1px rgba(0, 0, 0, 0.06);
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            border: 1px solid #e2e8f0;
        }

        .web-card h3 {
            margin-top: 0;
            color: #0f172a;
            font-size: 1.25rem;
        }

        .web-card p {
            color: #475569;
            line-height: 1.6;
            font-size: 0.95rem;
            margin-bottom: 20px;
        }

        .web-card a {
            display: inline-block;
            text-align: center;
            background-color: #0284c7;
            color: #fff;
            text-decoration: none;
            padding: 10px 18px;
            border-radius: 6px;
            font-weight: 500;
            transition: background-color 0.2s;
        }

        .web-card a:hover {
            background-color: #0369a1;
        }

        /* Lightbox (Açılır Görsel) Stilleri */
        .lightbox {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(15, 23, 42, 0.9);
            z-index: 1000;
            justify-content: center;
            align-items: center;
        }

        .lightbox img {
            max-width: 90%;
            max-height: 90%;
            border-radius: 6px;
            box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.5);
        }

        .lightbox-close {
            position: absolute;
            top: 20px;
            right: 30px;
            color: #fff;
            font-size: 40px;
            font-weight: bold;
            cursor: pointer;
            user-select: none;
        }
    </style>
</head>
<body>

    <header>
        <h1>Seçkin Özdemir</h1>
        <p>Portfolyo & Çalışmalar</p>
    </header>

    <main>
        <div class="tabs">
            <div class="tab-buttons">
                <button class="tab-button active" onclick="openTab(event, 'cekim-calismalari')">Çekim Çalışmaları</button>
                <button class="tab-button" onclick="openTab(event, 'site-tasarimlari')">Site Tasarımları</button>
            </div>

            <!-- ÇEKİM ÇALIŞMALARI SEKMESİ -->
            <div id="cekim-calismalari" class="tab-content active">
                <div class="portfolio-grid">
                    <div class="portfolio-item">
                        <img src="4457a2210103431.670bac6564c10.webp" alt="Damlayan Çeşme 1" onclick="openLightbox(this)">
                        <div class="portfolio-item-body">
                            <h3>Damlayan Çeşme - Seri 1</h3>
                            <p>Yüksek enstantane ile su damlasının anlık dondurulması (Siyah-Beyaz).</p>
                        </div>
                    </div>
                    <div class="portfolio-item">
                        <img src="5fac99210103431.670bac6564fb6.webp" alt="Damlayan Çeşme 2" onclick="openLightbox(this)">
                        <div class="portfolio-item-body">
                            <h3>Damlayan Çeşme - Seri 2</h3>
                            <p>Makro perspektif ve yer çekimi hareketinin detaylandırılması.</p>
                        </div>
                    </div>
                    <div class="portfolio-item">
                        <img src="4d5d64210103431.670bac6564809.webp" alt="Damlayan Çeşme 3" onclick="openLightbox(this)">
                        <div class="portfolio-item-body">
                            <h3>Damlayan Çeşme - Seri 3</h3>
                            <p>Işık ve gölge dengesiyle odaklanmış su damlası kadrajı.</p>
                        </div>
                    </div>
                    <div class="portfolio-item">
                        <img src="4daa52217131587.678b820954307.webp" alt="Hareketli Taksi" onclick="openLightbox(this)">
                        <div class="portfolio-item-body">
                            <h3>Panning Tekniği - Şehir Akışı</h3>
                            <p>Uzun pozlama ve araç takibi ile dinamik hareket hissi çekimi.</p>
                        </div>
                    </div>
                    <div class="portfolio-item">
                        <img src="Ekran görüntüsü 2026-08-31 221902.jpg" alt="Martı ve Göl" onclick="openLightbox(this)">
                        <div class="portfolio-item-body">
                            <h3>Göl Kenarı ve Özgürlük</h3>
                            <p>Doğa, su yansıması ve uçan martının minimalist siyah-beyaz kompozisyonu.</p>
                        </div>
                    </div>
                    <div class="portfolio-item">
                        <img src="Ekran görüntüsü 2026-08-31 222114.jpg" alt="Oyuncak Kamyonet" onclick="openLightbox(this)">
                        <div class="portfolio-item-body">
                            <h3>Retro Oyuncak Makro Çekim</h3>
                            <p>Sığ derinlik alanı (DoF) ile doğa içinde ürün/obje odaklı konsept çalışması.</p>
                        </div>
                    </div>
                    <div class="portfolio-item">
                        <img src="Ekran görüntüsü 2026-08-31 222159.jpg" alt="Orman Yansıması Panoraması" onclick="openLightbox(this)">
                        <div class="portfolio-item-body">
                            <h3>Sonbahar ve Yansıma Panoraması</h3>
                            <p>Renk paleti dönüşümü ve su yüzeyi simetrisini vurgulayan üçlü kompozisyon.</p>
                        </div>
                    </div>
                </div>
            </div>

            <!-- SİTE TASARIMLARI SEKMESİ -->
            <div id="site-tasarimlari" class="tab-content">
                <div class="web-grid">
                    
                    <div class="web-card">
                        <div>
                            <h3>81 Şehir 81 Müze</h3>
                            <p>Türkiye'nin 81 ilindeki tarihi ve kültürel müzeleri tek bir çatı altında toplayan dijital rehber projesi. Türkiye'nin zengin müze mirasını tanıtan ve ziyaretçilere detaylı bilgi sunan kapsamlı bir içerik platformudur.</p>
                        </div>
                        <a href="https://81sehir81muze.blogspot.com/" target="_blank" rel="noopener noreferrer">Siteyi İncele &rarr;</a>
                    </div>

                    <div class="web-card">
                        <div>
                            <h3>81 Şehir 81 Heykel</h3>
                            <p>Türkiye genelinde şehirlerin simgesi haline gelmiş anıt ve heykelleri derleyen sanatsal ve kültürel arşiv çalışması. İllerin kamusal sanat eserlerini ve tarihsel arka planlarını dijital ortama aktarır.</p>
                        </div>
                        <a href="https://81sehir81heykel.blogspot.com/" target="_blank" rel="noopener noreferrer">Siteyi İncele &rarr;</a>
                    </div>

                    <div class="web-card">
                        <div>
                            <h3>Türkiye Web Müzesi</h3>
                            <p>Türkiye'deki müzelerin dijital ortama aktarılması, çevrimiçi sergilenmesi ve sanal müze deneyiminin geniş kitlelere ulaştırılmasını hedefleyen dijital arşiv projesi.</p>
                        </div>
                        <a href="https://turkiyewebmuzesi.blogspot.com/" target="_blank" rel="noopener noreferrer">Siteyi İncele &rarr;</a>
                    </div>

                    <div class="web-card">
                        <div>
                            <h3>Benim Koçum</h3>
                            <p>Öğrenci koçluğu, eğitim danışmanlığı ve bireysel gelişim alanında hizmet sunan kurumsal web tasarımı. Kullanıcı dostu arayüzü ve sade tasarımıyla danışan odaklı bir platformdur.</p>
                        </div>
                        <a href="https://www.benimkocum.com.tr/" target="_blank" rel="noopener noreferrer">Siteyi İncele &rarr;</a>
                    </div>

                </div>
            </div>

        </div>
    </main>

    <!-- LIGHTBOX MODAL -->
    <div class="lightbox" id="lightbox" onclick="closeLightbox()">
        <span class="lightbox-close" onclick="closeLightbox()">&times;</span>
        <img src="" alt="Büyük Görsel" id="lightbox-img">
    </div>

    <script>
        function openTab(evt, tabName) {
            var i, tabContent, tabButtons;
            
            tabContent = document.getElementsByClassName("tab-content");
            for (i = 0; i < tabContent.length; i++) {
                tabContent[i].classList.remove("active");
            }
            
            tabButtons = document.getElementsByClassName("tab-button");
            for (i = 0; i < tabButtons.length; i++) {
                tabButtons[i].classList.remove("active");
            }
            
            document.getElementById(tabName).classList.add("active");
            evt.currentTarget.classList.add("active");
        }

        function openLightbox(img) {
            var lightbox = document.getElementById("lightbox");
            var lightboxImg = document.getElementById("lightbox-img");
            lightbox.style.display = "flex";
            lightboxImg.src = img.src;
        }

        function closeLightbox() {
            var lightbox = document.getElementById("lightbox");
            lightbox.style.display = "none";
        }
    </script>
</body>
</html>
