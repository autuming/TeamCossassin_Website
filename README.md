<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
    <title>Team Cossassin - Game Dev Team</title>
    <link href="https://fonts.googleapis.com/css2?family=Anton&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="styles/style.css" />
</head>
<body>
    <div class="container">
        
        <header class="site-header">
            <div class="nav-container">
                <a href="#" class="logo-left">
                    <img src="img/logo.png" alt="Team Cossassin 로고" class="logo-img" />
                </a>
                
                <nav class="nav-right">
                    <a href="#about">About</a>
                    <a href="#team">Contact</a>
                    <a href="#aboutgame">Our Games</a>
                    <a href="gallery.html">Gallery</a>
                </nav>
            </div>
        </header>

        <div class="team-title">
            <span class="typing">Team Cossassin</span>
        </div>

        <section class="main-image-slider">
            <div class="slider">
                <img src="img/meet2.jpg" alt="대표 이미지1" class="slide active">
                <img src="img/meet3.jpg" alt="대표 이미지2" class="slide">
                <img src="img/2222.png" alt="대표 이미지3" class="slide">
            </div>
        </section>

        <section class="intro" id="about">
            <div class="section-title">About Us</div>
            <p class="intro-text">
                TEAM COSSASSIN은 날카로운 기획력과 정밀한 코드로, 장르의 틈새를 파고드는 게임 개발팀입니다.<br/>
                우리는 색다른 게임 아이디어를 현실로 만드는 데 집중하며,<br/>
                재미와 감동, 쾌감을 게임을 통해 동시에 전달합니다.<br><br>
                <a href="gallery.html" class="gallery-link">→ 팀 갤러리 보러가기</a>
            </p>
        </section>

        <section class="game-section" id="aboutgame">
            <div class="section-title">About Our Games</div>
            <p class="subtitle">향수를 자극하는 감성 액션</p>
            <h2 class="gradient-title">NOSTALGIA</h2>
            
            <div class="game-slider">
                <div class="game-slides">
                    <div class="game-slide active">
                        <video src="videos/short/11.mp4" autoplay muted loop playsinline></video>
                    </div>
                    <div class="game-slide">
                        <video src="videos/short/22.mp4" autoplay muted loop playsinline></video>
                    </div>
                    <div class="game-slide">
                        <video src="videos/short/33.mp4" autoplay muted loop playsinline></video>
                    </div>
                </div>

                <div class="bar-pagination">
                    <span class="bar active" onclick="currentSlide(0)"></span>
                    <span class="bar" onclick="currentSlide(1)"></span>
                    <span class="bar" onclick="currentSlide(2)"></span>
                </div>
            </div>

            <p class="game-description">
                Team Cossassin이 만든 게임들을 만나보세요. <br>
                다양한 장르와 감각적인 연출이 어우러진 작품들을 소개합니다. <br>
                --<br><br>
            </p>
        </section>

        <section class="team-cards" id="team">
            <div class="section-title">Our Team</div>
            <div class="card-container">
                <div class="card">
                    <h3>Gaeul Lee</h3>
                    <p>대표<br><span class="role">Team Leader</span></p>
                </div>
                <div class="card">
                    <h3>테라 | Terrrrrrra</h3>
                    <p>메인 개발자<br><span class="role">Lead Developer</span></p>
                </div>
                <div class="card">
                    <h3>Changho Shin</h3>
                    <p>서브 개발자<br><span class="role">Assistant Developer</span></p>
                </div>
                <div class="card">
                    <h3>Hwayoung Cho</h3>
                    <p>웹 제작, SNS 담당자<br><span class="role">Web Developer, Social Media Manager</span></p>
                </div>
                <div class="card">
                    <h3>Jaejun Kim</h3>
                    <p>게임 아트 담당자<br><span class="role">Game Artist</span></p>
                </div>
                <div class="card">
                    <h3>Jaehak Lee</h3>
                    <p>기획<br><span class="role">Game Design</span></p>
                </div>
            </div>
        </section>

        <section class="social-icons">
            <div class="section-title">Follow Us</div>
            <a href="https://www.instagram.com/team_cossassin/?igsh=ZDI4c3lkZWxrODVp" target="_blank">
                <img src="img/instagram.png" alt="Instagram 로고" class="icon-img" />
                Instagram
            </a>
            <a href="https://youtube.com/@teamcossassin" target="_blank">
                <img src="img/youtube.png" alt="YouTube 로고" class="icon-img" />
                YouTube
            </a>
        </section>

        <footer>
            &copy; 2025 Team Cossassin. All rights reserved.
        </footer>
    </div>

    <script>
        const slidesMain = document.querySelectorAll('.slide');
        let currentMain = 0;

        function showNextSlide() {
            slidesMain[currentMain].classList.remove('active');
            currentMain = (currentMain + 1) % slidesMain.length;
            slidesMain[currentMain].classList.add('active');
        }

        setInterval(showNextSlide, 5000); // 5초마다 자동 전환
    </script>

    <script>
        let currentIndex = 0;
        const gameSlideItems = document.querySelectorAll('.game-slide');
        const bars = document.querySelectorAll('.bar');
        const totalGameSlides = bars.length;

        function showGameSlide(index) {
            gameSlideItems.forEach(slide => slide.classList.remove('active'));
            bars.forEach(bar => bar.classList.remove('active'));
            gameSlideItems[index].classList.add('active');
            bars[index].classList.add('active');
            currentIndex = index;
        }

        function currentSlide(index) {
            showGameSlide(index);
        }
    </script>
</body>
</html>
