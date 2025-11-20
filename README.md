<!DOCTYPE html>
<html lang="ja">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>懸賞ナビ - 日本最大級の無料プレゼント・抽選まとめ</title>
    <meta name="description" content="無料で応募できる懸賞・プレゼントキャンペーンを毎日更新！必ずもらえるキャンペーンも一目でわかる日本最大級のまとめサイト">
    
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
    <!-- Font Awesome -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">
    
    <style>
        :root {
            --primary: #6366f1;
            --primary-dark: #4f46e5;
            --success: #10b981;
            --warning: #f59e0b;
            --danger: #ef4444;
            --bg: #0f0f17;
            --surface: #162033;
            --card: #1a1a2e;
            --text: #e2e8f0;
            --text-light: #94a3b8;
            --border: #334155;
            --shadow: rgba(0, 0, 0, 0.4);
        }

        * { margin: 0; padding: 0; box-sizing: border-box; }
        body {
            font-family: 'Inter', system-ui, sans-serif;
            background: linear-gradient(135deg, #0f0f17 0%, #16213e 100%);
            color: var(--text);
            line-height: 1.6;
            min-height: 100vh;
            background-attachment: fixed;
        }

        header {
            background: rgba(15, 15, 23, 0.95);
            backdrop-filter: blur(16px);
            border-bottom: 1px solid var(--border);
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            padding: 1.2rem 0;
        }

        .header-inner {
            max-width: 1400px;
            margin: 0 auto;
            padding: 0 2rem;
            display: flex;
            align-items: center;
            justify-content: space-between;
            flex-wrap: wrap;
            gap: 1rem;
        }

        .logo {
            font-size: 2rem;
            font-weight: 800;
            background: linear-gradient(90deg, #a78bfa, #6366f1);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        .search-box {
            position: relative;
            flex: 1;
            max-width: 560px;
            min-width: 280px;
        }

        #search-input {
            width: 100%;
            padding: 0.95rem 1.3rem 0.95rem 3.2rem;
            border-radius: 50px;
            border: 1px solid var(--border);
            background: var(--card);
            color: white;
            font-size: 1rem;
            outline: none;
            transition: all 0.3s ease;
        }

        #search-input:focus {
            border-color: var(--primary);
            box-shadow: 0 0 0 4px rgba(99, 102, 241, 0.25);
        }

        .search-box i {
            position: absolute;
            left: 1.1rem;
            top: 50%;
            transform: translateY(-50%);
            color: #64748b;
            font-size: 1.1rem;
        }

        main { margin-top: 100px; padding: 3rem 0; }

        .container {
            max-width: 1400px;
            margin: 0 auto;
            padding: 0 2rem;
        }

        .hero {
            text-align: center;
            margin-bottom: 4rem;
        }

        .page-title {
            font-size: 3.2rem;
            font-weight: 800;
            background: linear-gradient(90deg, #c084fc, #6366f1, #3b82f6);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            margin-bottom: 0.8rem;
        }

        .subtitle {
            font-size: 1.3rem;
            color: var(--text-light);
            max-width: 700px;
            margin: 0 auto;
        }

        .filters {
            display: flex;
            flex-wrap: wrap;
            gap: 1rem;
            justify-content: center;
            margin-bottom: 3.5rem;
        }

        .filter-btn {
            padding: 0.8rem 1.8rem;
            border-radius: 50px;
            background: var(--surface);
            border: 1px solid var(--border);
            color: var(--text-light);
            cursor: pointer;
            transition: all 0.3s ease;
            font-weight: 500;
        }

        .filter-btn.active,
        .filter-btn:hover {
            background: var(--primary);
            border-color: var(--primary);
            color: white;
            transform: translateY(-2px);
        }

        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(360px, 1fr));
            gap: 2rem;
        }

        .card {
            background: var(--card);
            border-radius: 20px;
            overflow: hidden;
            transition: all 0.4s cubic-bezier(0.25, 0.8, 0.25, 1);
            border: 1px solid var(--border);
            position: relative;
            opacity: 0;
            transform: translateY(20px);
            animation: fadeInUp 0.6s forwards;
        }

        @keyframes fadeInUp {
            to { opacity: 1; transform: translateY(0); }
        }

        .card:hover {
            transform: translateY(-16px);
            box-shadow: 0 25px 50px var(--shadow);
            border-color: var(--primary);
        }

        .tag {
            position: absolute;
            top: 14px;
            right: 14px;
            padding: 0.45rem 0.9rem;
            border-radius: 50px;
            font-size: 0.78rem;
            font-weight: 700;
            z-index: 10;
            text-transform: uppercase;
            letter-spacing: 0.5px;
        }

        .tag.popular { background: var(--warning); }
        .tag.allget { background: var(--success); }
        .tag.new { background: var(--danger); }

        .card-img {
            height: 200px;
            background: linear-gradient(135deg, var(--primary), #8b5cf6);
            position: relative;
            overflow: hidden;
        }

        .card-img::before {
            content: '';
            position: absolute;
            inset: 0;
            background: linear-gradient(45deg, transparent 30%, rgba(255,255,255,0.1) 50%, transparent 70%);
            transform: translateX(-100%);
            animation: shimmer 3s infinite;
        }

        @keyframes shimmer {
            0% { transform: translateX(-100%); }
            100% { transform: translateX(100%); }
        }

        .card-img i {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            font-size: 5rem;
            opacity: 0.15;
            color: white;
        }

        .card-body {
            padding: 1.8rem;
        }

        .card-title {
            font-size: 1.35rem;
            font-weight: 700;
            margin-bottom: 0.8rem;
            color: white;
        }

        .card-desc {
            color: var(--text-light);
            font-size: 0.98rem;
            margin-bottom: 1.4rem;
            line-height: 1.7;
        }

        .card-footer {
            display: flex;
            align-items: center;
            justify-content: space-between;
            padding-top: 1.4rem;
            border-top: 1px solid var(--border);
        }

        .stats {
            color: var(--text-light);
            font-size: 0.9rem;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        .btn {
            padding: 0.8rem 1.8rem;
            background: var(--primary);
            color: white;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 600;
            font-size: 0.95rem;
            transition: all 0.3s ease;
            box-shadow: 0 4px 15px rgba(99, 102, 241, 0.4);
        }

        .btn:hover {
            background: var(--primary-dark);
            transform: translateY(-3px);
            box-shadow: 0 8px 25px rgba(99, 102, 241, 0.6);
        }

        .no-results {
            grid-column: 1 / -1;
            text-align: center;
            padding: 5rem 2rem;
            font-size: 1.5rem;
            color: var(--text-light);
        }

        footer {
            margin-top: 8rem;
            padding: 4rem 2rem 2rem;
            text-align: center;
            color: #64748b;
            border-top: 1px solid var(--border);
            font-size: 0.95rem;
        }

        @media (max-width: 768px) {
            .header-inner { flex-direction: column; padding: 0 1rem; }
            .page-title { font-size: 2.5rem; }
            .grid { grid-template-columns: 1fr; }
            .card-img { height: 180px; }
        }
    </style>
</head>
<body>

    <header>
        <div class="header-inner">
            <div class="logo"><i class="fas fa-gift"></i> 懸賞ナビ</div>
            <div class="search-box">
                <i class="fas fa-search"></i>
                <input type="text" id="search-input" placeholder="サイト名・賞品・キーワードで検索...">
            </div>
        </div>
    </header>

    <main>
        <div class="container">
            <div class="hero">
                <h1 class="page-title">無料懸賞・プレゼントまとめ</h1>
                <p class="subtitle">日本最大級！毎日更新される無料抽選・必ずもらえるキャンペーンを完全網羅</p>
            </div>

            <div class="filters">
                <button class="filter-btn active" data-filter="all">すべて表示</button>
                <button class="filter-btn" data-filter="popular">人気サイト</button>
                <button class="filter-btn" data-filter="allget">必ずもらえる</button>
                <button class="filter-btn" data-filter="daily">毎日更新</button>
            </div>

            <div class="grid" id="site-grid">
                <!-- ここからカード -->
                <div class="card" data-tags="popular daily">
                    <div class="tag popular">人気No.1</div>
                    <div class="card-img"><i class="fas fa-trophy"></i></div>
                    <div class="card-body">
                        <h3 class="card-title">チャンスイット</h3>
                        <p class="card-desc">日本最大級の懸賞サイト。現金10万円・家電・ギフト券など毎日500件以上のキャンペーン更新！</p>
                        <div class="card-footer">
                            <span class="stats"><i class="fas fa-gift"></i> 毎日500件以上</span>
                            <a href="https://www.chance.com/present/" target="_blank" class="btn">今すぐ応募</a>
                        </div>
                    </div>
                </div>

                <div class="card" data-tags="popular daily">
                    <div class="tag popular">老舗</div>
                    <div class="card-img"><i class="fas fa-crown"></i></div>
                    <div class="card-body">
                        <h3 class="card-title">懸賞生活</h3>
                        <p class="card-desc">20年以上の実績を持つ超有名サイト。ネット懸賞からハガキ懸賞まで完全網羅。</p>
                        <div class="card-footer">
                            <span class="stats"><i class="fas fa-history"></i> 毎日更新</span>
                            <a href="https://www.knshow.com/" target="_blank" class="btn">サイトへ</a>
                        </div>
                    </div>
                </div>

                <div class="card" data-tags="allget">
                    <div class="tag allget">100%もらえる</div>
                    <div class="card-img"><i class="fas fa-check-circle"></i></div>
                    <div class="card-body">
                        <h3 class="card-title">必ずもらえるキャンペーンまとめ</h3>
                        <p class="card-desc">レシート応募・アンケート・先着で絶対にもらえるキャンペーンだけを厳選掲載！</p>
                        <div class="card-footer">
                            <span class="stats"><i class="fas fa-star"></i> 全員プレゼント</span>
                            <a href="https://tokaikensyo.com/sweepstakes/absolutelyget/" target="_blank" class="btn">チェック</a>
                        </div>
                    </div>
                </div>

                <!-- さらに追加したいサイトはここにコピペ -->
                <div class="card" data-tags="daily">
                    <div class="tag new">NEW</div>
                    <div class="card-img"><i class="fas fa-medal"></i></div>
                    <div class="card-body">
                        <h3 class="card-title">キャンなび</h3>
                        <p class="card-desc">最新のWEBキャンペーンを毎日更新。「必ずもらえる」情報が充実！</p>
                        <div class="card-footer">
                            <span class="stats"><i class="fas fa-sync"></i> 毎日更新</span>
                            <a href="https://camnavi.net/" target="_blank" class="btn">サイトへ</a>
                        </div>
                    </div>
                </div>
            </div>

            <div class="no-results" id="no-results" style="display:none;">
                <i class="fas fa-search fa-3x mb-4" style="color:#64748b;"></i>
                <p>該当するサイトが見つかりませんでした…</p>
            </div>
        </div>
    </main>

    <footer>
        <p>&copy; 2025 懸賞ナビ - 日本最大級の無料プレゼントまとめサイト</p>
        <p style="margin-top:0.5rem; font-size:0.85rem;">情報は随時更新中。最新情報は各公式サイトでご確認ください。</p>
    </footer>

    <script>
        const searchInput = document.getElementById('search-input');
        const filterBtns = document.querySelectorAll('.filter-btn');
        const cards = document.querySelectorAll('.card');
        const grid = document.getElementById('site-grid');
        const noResults = document.getElementById('no-results');

        function filterCards() {
            const query = searchInput.value.toLowerCase().trim();
            const activeFilter = document.querySelector('.filter-btn.active').dataset.filter;

            let visibleCount = 0;

            cards.forEach((card, index) => {
                const title = card.querySelector('.card-title').textContent.toLowerCase();
                const desc = card.querySelector('.card-desc').textContent.toLowerCase();
                const tags = card.dataset.tags;

                const matchesSearch = title.includes(query) || desc.includes(query) || query === '';
                const matchesFilter = activeFilter === 'all' || tags.includes(activeFilter);

                if (matchesSearch && matchesFilter) {
                    card.style.display = '';
                    card.style.animationDelay = `${index * 0.05}s`;
                    visibleCount++;
                } else {
                    card.style.display = 'none';
                }
            });

            noResults.style.display = visibleCount === 0 ? 'block' : 'none';
        }

        searchInput.addEventListener('input', filterCards);

        filterBtns.forEach(btn => {
            btn.addEventListener('click', () => {
                filterBtns.forEach(b => b.classList.remove('active'));
                btn.classList.add('active');
                filterCards();
            });
        });

        // 初期表示アニメーション
        cards.forEach((card, index) => {
            card.style.animationDelay = `${index * 0.1}s`;
        });
    </script>
</body>
</html>
