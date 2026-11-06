<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>동해시 관광안내 - 푸른 바다와 자연을 품은 도시</title>
    <style>
        /* 기본 스타일 초기화 */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Pretendard', -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
        }

        body {
            color: #333;
            line-height: 1.6;
            background-color: #f8f9fa;
        }

        a {
            text-decoration: none;
            color: inherit;
        }

        /* 네비게이션 바 */
        header {
            position: fixed;
            top: 0;
            width: 100%;
            background-color: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(5px);
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            z-index: 1000;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1rem 5%;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: bold;
            color: #0066cc;
        }

        nav ul {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        nav a {
            font-weight: 600;
            color: #444;
            transition: color 0.3s;
        }

        nav a:hover {
            color: #0066cc;
        }

        /* 메인 히어로 섹션 */
        .hero {
            height: 80vh;
            background: linear-gradient(rgba(0, 0, 0, 0.4), rgba(0, 0, 0, 0.4)), 
                        url('https://images.unsplash.com/photo-1507525428034-b723cf961d3e?auto=format&fit=crop&w=1600&q=80') center/cover no-repeat;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            color: #fff;
            padding: 0 1rem;
            margin-top: 60px;
        }

        .hero h1 {
            font-size: 3rem;
            margin-bottom: 1rem;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.5);
        }

        .hero p {
            font-size: 1.25rem;
            margin-bottom: 2rem;
            max-width: 600px;
        }

        .btn-primary {
            background-color: #0066cc;
            color: #fff;
            padding: 0.8rem 2rem;
            border-radius: 30px;
            font-weight: bold;
            transition: background-color 0.3s;
        }

        .btn-primary:hover {
            background-color: #004b99;
        }

        /* 테마별 관광지 섹션 */
        .container {
            max-width: 1200px;
            margin: 4rem auto;
            padding: 0 1.5rem;
        }

        .section-title {
            text-align: center;
            margin-bottom: 3rem;
        }

        .section-title h2 {
            font-size: 2rem;
            color: #111;
            margin-bottom: 0.5rem;
        }

        .section-title p {
            color: #666;
        }

        .card-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .card {
            background: #fff;
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 4px 15px rgba(0,0,0,0.05);
            transition: transform 0.3s, box-shadow 0.3s;
        }

        .card:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 25px rgba(0,0,0,0.1);
        }

        .card-img {
            height: 200px;
            background-size: cover;
            background-position: center;
        }

        .card-content {
            padding: 1.5rem;
        }

        .card-tag {
            display: inline-block;
            background-color: #e6f0fa;
            color: #0066cc;
            padding: 0.2rem 0.6rem;
            border-radius: 4px;
            font-size: 0.85rem;
            font-weight: bold;
            margin-bottom: 0.5rem;
        }

        .card-title {
            font-size: 1.25rem;
            margin-bottom: 0.5rem;
        }

        .card-desc {
            font-size: 0.95rem;
            color: #666;
            line-height: 1.5;
        }

        /* 추천 여행 코스 탭 */
        .course-section {
            background-color: #fff;
            padding: 4rem 1.5rem;
        }

        .course-box {
            background: #f8f9fa;
            border-left: 4px solid #0066cc;
            padding: 1.5rem;
            margin-top: 1rem;
            border-radius: 0 8px 8px 0;
        }

        .course-box h4 {
            font-size: 1.1rem;
            color: #0066cc;
            margin-bottom: 0.5rem;
        }

        /* 푸터 */
        footer {
            background-color: #222;
            color: #aaa;
            padding: 3rem 5% 1.5rem;
            text-align: center;
            font-size: 0.9rem;
        }

        footer p {
            margin-bottom: 0.5rem;
        }

        /* 반응형 디자인 */
        @media (max-width: 768px) {
            nav ul {
                display: none; /* 모바일 메뉴는 단순화를 위해 생략 */
            }
            .hero h1 {
                font-size: 2rem;
            }
        }
    </style>
</head>
<body>

    <!-- Header -->
    <header>
        <div class="logo">🌊 동해, 어디까지 가봤니?</div>
        <nav>
            <ul>
                <li><a href="#ocean">바다&해변</a></li>
                <li><a href="#nature">자연&계곡</a></li>
                <li><a href="#history">감성&역사</a></li>
                <li><a href="#course">추천코스</a></li>
            </ul>
        </nav>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <h1>낭만과 힐링이 있는 곳, 동해시</h1>
        <p>에메랄드빛 해변부터 무릉계곡의 웅장함까지, 당신만을 위한 특별한 여행을 시작하세요.</p>
        <a href="#theme" class="btn-primary">주제별 여행지 보기</a>
    </section>

    <!-- Theme Section -->
    <section class="container" id="theme">
        <div class="section-title">
            <h2>관광 테마별 명소</h2>
            <p>취향에 맞는 동해시의 다채로운 매력을 발견해 보세요.</p>
        </div>

        <div class="card-grid">
            <!-- Card 1 -->
            <div class="card" id="ocean">
                <div class="card-img" style="background-image: url('https://images.unsplash.com/photo-1507525428034-b723cf961d3e?auto=format&fit=crop&w=600&q=80');"></div>
                <div class="card-content">
                    <span class="card-tag">OCEAN & BEACH</span>
                    <h3 class="card-title">망상해수욕장 & 도째비골</h3>
                    <p class="card-desc">넓은 울창한 송림과 깨끗한 백사장이 펼쳐진 망상해변, 그리고 액티비티와 일출을 동시에 즐기는 도째비골 스카이밸리입니다.</p>
                </div>
            </div>

            <!-- Card 2 -->
            <div class="card" id="nature">
                <div class="card-img" style="background-image: url('https://images.unsplash.com/photo-1448375240586-882707db888b?auto=format&fit=crop&w=600&q=80');"></div>
                <div class="card-content">
                    <span class="card-tag">NATURE & TREKKING</span>
                    <h3 class="card-title">무릉계곡 & 베틀바위</h3>
                    <p class="card-desc">신선이 놀다 간 듯한 명승지. 웅장한 기암괴석과 맑은 계곡물이 어우러져 사계절 내내 뛰어난 경관을 자랑합니다.</p>
                </div>
            </div>

            <!-- Card 3 -->
            <div class="card" id="history">
                <div class="card-img" style="background-image: url('https://images.unsplash.com/photo-1519046904884-53103b34b206?auto=format&fit=crop&w=600&q=80');"></div>
                <div class="card-content">
                    <span class="card-tag">EMOTION & VILLAGE</span>
                    <h3 class="card-title">논골담길 & 묵호등대</h3>
                    <p class="card-desc">어촌 마을의 삶과 아기자기한 벽화가 숨쉬는 길. 언덕길을 따라 올라가면 묵호 바다가 한눈에 내려다보입니다.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Course Section -->
    <section class="course-section" id="course">
        <div class="container" style="margin: 0 auto;">
            <div class="section-title">
                <h2>추천 여행 코스</h2>
                <p>알차게 즐기는 동해시 당일 / 1박 2일 코스</p>
            </div>

            <div class="course-box">
                <h4>[당일 코스] 감성 & 힐링 투어</h4>
                <p>묵호역 → 논골담길 스탬프 투어 → 묵호등대 & 도째비골 스카이밸리 → 추암촛대바위 일몰</p>
            </div>

            <div class="course-box">
                <h4>[1박 2일 코스] 액티비티 & 자연 탐방</h4>
                <p><strong>1일차:</strong> 무릉계곡 트레킹 → 무릉별유천지 스카이글라이더 → 천곡황금박쥐동굴</p>
                <p style="margin-top: 0.5rem;"><strong>2일차:</strong> 망상해변 산책 → 묵호항 수산시장 먹거리 체험 → 도째비골 자이언트 슬라이드</p>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <p><strong>동해시 문화관광 안내</strong></p>
        <p>강원특별자치도 동해시 천곡로 77 (동해시청)</p>
        <p>관광안내 다산콜센터: 120 / 관광안내소: 033-530-2800</p>
        <p style="margin-top: 1rem; color: #666;">© Donghae City Tourism. All rights reserved.</p>
    </footer>

</body>
</html>
