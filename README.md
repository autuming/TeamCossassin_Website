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
        </nav>
      </div>
    </header>

<div class="team-title">
  <span class="typing">Team Cossassin</span>
</div>



  <section class="main-image-slider">
    <div class="slider">
      <img src="img/1234.jpg" alt="대표 이미지1" class="slide active">
      <img src="img/2222.png" alt="대표 이미지2" class="slide">
      <img src="img/3333.jpeg" alt="대표 이미지3" class="slide">
    </div>
  </section>



    <section class="intro" id="about">
      <div class="section-title">About Us</div>
      <p class="intro-text">
        TEAM COSSASSIN은 날카로운 기획력과 정밀한 코드로, 장르의 틈새를 파고드는 게임 개발팀입니다.<br/>
        우리는 색다른 게임 아이디어를 현실로 만드는 데 집중하며,<br/>
        재미와 감동, 쾌감을 게임을 통해 동시에 전달합니다.
      </p>
    </section>

    <section class="team-cards" id="team">
  <div class="section-title">Our Team</div>
  <div class="card-container">
    <div class="card">
      <h3>이가을</h3>
      <p>대표<br><span class="role">Team Leader</span></p>
    </div>
    <div class="card">
      <h3>장기성</h3>
      <p>메인 개발자<br><span class="role">Lead Developer</span></p>
    </div>
    <div class="card">
      <h3>신창호</h3>
      <p>서브 개발자<br><span class="role">Assistant Developer</span></p>
    </div>
    <div class="card">
      <h3>조화영</h3>
      <p>웹 제작, SNS 담당자<br><span class="role">Web Developer, Social Media Manager</span></p>
    </div>
    <div class="card">
      <h3>김재준</h3>
      <p>게임 아트 담당자<br><span class="role">Game Artist</span></p>
    </div>
    <div class="card">
      <h3>이재학</h3>
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
  const slides = document.querySelectorAll('.slide');
  let current = 0;

  function showNextSlide() {
    slides[current].classList.remove('active');
    current = (current + 1) % slides.length;
    slides[current].classList.add('active');
  }

  setInterval(showNextSlide, 5000); // 5초마다 천천히 전환
</script>


</body>
</html>
