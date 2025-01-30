<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Football Player Profile</title>
    <!-- Bootstrap CSS -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha3/dist/css/bootstrap.min.css" rel="stylesheet">
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;700&display=swap" rel="stylesheet">
    <!-- Bootstrap Bundle JS -->
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;700&display=swap" rel="stylesheet">
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>


    <style>
        body {
            font-family: 'Roboto', sans-serif;
            line-height: 1.8;
            background: linear-gradient(135deg, #32cd32, #2575fc);
            color: #fff;
        }
        .navbar {
    background: linear-gradient(135deg, #32cd32, #2575fc); /* پس‌زمینه گرادینت */
    padding: 15px 0;
    border-radius: 12px; /* گوشه‌های گرد */
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2); /* سایه */
    backdrop-filter: blur(10px); /* افکت مات */
}

.navbar-brand {
    font-size: 1.8rem;
    font-weight: bold;
    color: #fff !important;
    letter-spacing: 1px;
    transition: 0.3s;
}

.navbar-brand:hover {
    color: #f8f9fa !important;
    transform: scale(1.1);
}

.navbar-nav .nav-link {
    font-size: 1.1rem;
    color: white !important;
    margin: 0 10px;
    transition: 0.3s;
    padding: 8px 12px;
    border-radius: 8px;
}

.navbar-nav .nav-link:hover {
    background: rgba(255, 255, 255, 0.2);
    transform: translateY(-2px);
}
        header {
            background: linear-gradient(to bottom, rgba(0, 0, 0, 0.7), rgba(0, 0, 0, 0.5)), url('player-header.jpg') no-repeat center center/cover;
            height: 500px;
            color: white;
            text-align: center;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            position: relative;
        }
        header h1 {
            font-size: 4rem;
            font-weight: 700;
            text-transform: uppercase;
            background: linear-gradient(90deg, #ff8c00, #ff3e3e);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            text-shadow: 2px 2px 15px rgba(0, 0, 0, 0.8);
        }
        header p {
            font-size: 1.3rem;
            margin-top: 20px;
            color: #f1f1f1;
            text-shadow: 1px 1px 10px rgba(0, 0, 0, 0.7);
        }

        .welcome-section img {
            max-width: 100%;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
        }

        .achievements ul {
            list-style: none;
            padding: 0;
        }
        .achievements ul li {
            background: rgba(255, 255, 255, 0.1);
            margin: 10px 0;
            padding: 10px 15px;
            border-radius: 5px;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
        }

        .carousel-inner img {
            border-radius: 10px;
        }

        .testimonials blockquote {
            font-style: italic;
            border-left: 4px solid #ff8c00;
            padding-left: 10px;
            margin-bottom: 20px;
        }

        .footer {
            background-color: rgba(0, 0, 0, 0.7);
            color: white;
            padding: 20px 0;
            text-align: center;
        }
        .footer .social-icons a {
            color: white;
            margin: 0 10px;
            font-size: 1.5rem;
            text-decoration: none;
            transition: color 0.3s;
        }
        .footer .social-icons a:hover {
            color: #ff8c00;
        }
        .fixed-size {
    max-width: 100%;
    height: 660px; /* تنظیم ارتفاع به‌طور خودکار */
    object-fit: cover; /* برش صحیح تصویر */
    border-radius: 10px;
    }
    .gallery-title {
    font-size: 2.5rem; /* اندازه بزرگ‌تر */
    font-weight: bold; /* متن ضخیم */
    text-align: center; /* تراز وسط */
    color: #E3F2FD; /* رنگ اصلی */
    text-transform: uppercase; /* متن به حروف بزرگ */
    letter-spacing: 2px; /* فاصله بین حروف */
    margin-bottom: 20px; /* فاصله از محتوای پایین */
    position: relative; /* برای افزودن افکت زیر خط */
    display: inline-block; /* برای خط زیر */
}

   .gallery-title::after {
    content: "";
    display: block;
    width: 100px; /* عرض خط زیر متن */
    height: 4px; /* ضخامت خط */
    background-color: #ECECEC; /* رنگ خط */
    margin: 10px auto 0; /* فاصله خط از متن */
    border-radius: 2px; /* گردی لبه‌های خط */
}


.hero-section::after {
    content: "";
    position: absolute;
    bottom: -1px;
    left: 0;
    width: 100%;
    height: 100px;
    background: #00A86B;
    clip-path: polygon(0 100%, 50% 80%, 100% 100%);
    animation: waveMove 5s infinite alternate ease-in-out;
}

@keyframes waveMove {
    0% { clip-path: polygon(0 100%, 50% 85%, 100% 100%); }
    100% { clip-path: polygon(0 100%, 50% 75%, 100% 100%); }
}
.hero-section {
    background: linear-gradient(135deg, #00A86B, #2575fc); /* پس‌زمینه گرادینت */
    color: white; /* متن سفید */
    text-align: center; /* تراز وسط */
    padding: 60px 20px; /* فاصله داخلی */
    border-radius: 20px; /* گوشه‌های گرد */
    box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2); /* سایه برای عمق */
    max-width: 800px; /* حداکثر عرض */
    margin: 50px auto; /* وسط‌چینی */
}

.hero-section h1 {
    font-size: 3rem; /* اندازه بزرگ‌تر عنوان */
    font-weight: bold; /* ضخامت بیشتر */
    text-transform: uppercase; /* تبدیل به حروف بزرگ */
    letter-spacing: 2px; /* فاصله بین حروف */
    text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.3); /* سایه متن */
}

.hero-section p {
    font-size: 1.2rem; /* اندازه متن */
    margin-top: 10px; /* فاصله از عنوان */
    opacity: 0.9; /* کمی شفافیت */
}

    </style>
</head>
<body>   
    <!-- Navbar -->
    <nav class="navbar navbar-expand-lg navbar-dark">
        <div class="container">
            <a class="navbar-brand" href="#">Toni Kroos</a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav ms-auto">
                    <li class="nav-item"><a class="nav-link" href="#home">Home</a></li>
                    <li class="nav-item"><a class="nav-link" href="#biography">Biography</a></li>
                    <li class="nav-item"><a class="nav-link" href="#achievements">Achievements</a></li>
                    <li class="nav-item"><a class="nav-link" href="#gallery">Gallery</a></li>
                    <li class="nav-item"><a class="nav-link" href="#testimonials">comments</a></li>
                </ul>
            </div>
        </div>
    </nav>
    

    <script>
        function toggleMenu() {
            document.querySelector('.nav-links').classList.toggle('active');
        }
    </script>

    

    <!-- Header -->
    <header>
        <section class="hero-section">
            <h1>MY NAME IS Toni Kroos</h1>
            <p>The Official Profile of a Football Legend</p>
        </section>
        
    </header>

    <!-- Main Content -->
    <div class="container mt-5">
        <!-- Welcome Section -->
        <section id="home" class="welcome-section text-center">
            
            <img src="https://cdn.yjc.ir/files/fa/news/1395/10/7/5621091_962.jpg" alt="Player in Action" class="img-fluid mb-4" style="width:400px; height: 400px;;">
            <img src="https://asrturkiye.com/wp-content/uploads/2024/10/%D8%AA%D9%88%D9%86%DB%8C-%DA%A9%D8%B1%D9%88%D8%B3.webp" alt="Player in Action" class="img-fluid mb-4" style="width:400px; height: 400px;;">
            <img src="https://news-cdn.varzesh3.com/pictures/2024/02/20/B/og300ubp6.jpg?w=800" alt="Player in Action" class="img-fluid mb-4" style="width:400px; height: 400px;;">
            <h2>Welcome to Toni Kroos World</h2>
            <p>I am Toni Kroos a professional footballer playing as a Midfielde for Real Madrid</p>
        </section>

        <!-- Biography Section -->
        <section id="biography" class="mt-5">
            <h2>About Toni Kroos</h2>
            <p><strong>Height:</strong> 180cm</p>
            <p><strong>Position:</strong>Midfielder</p>
            <p><strong>Team:</strong> Real Madrid</p>
            <h2>Toni Kroos:</h2>
            <p>Toni Kroos (born 4 January 1990) is a German former footballer who plays for Real Madrid and the Germany national football team. 
                He is considered one of the best midfielders in football history, known for his accurate passes, useful crosses, long-range shots and attacking skills in playmaking and also for organizing a team among players and football fans. He is one of the best playmakers in history. He provides the most accurate responses and crosses possible. Due to the great accuracy of Toni Kroos' responses, he has been nicknamed the engineer. He is always considered to be in the best layer and the most complete midfielders in football history. Kroos is known as the most honored football player in German history, having won 34 trophies during his 17-year career. He finally said goodbye to club competitions after the 2023–24 UEFA Champions League and to national and world football competitions at the 2024 UEFA Euro.</p>
            <h2>Personal life:</h2>
            <p>Toni Kroos was born on 4 January 1990 in Greifswald. He has a younger brother, Felix Kroos, who is also a professional footballer. His father Roland worked as a youth coach for Hansa Rostock. In his youth, Toni was an average student and spent a lot of time practicing football, however, he was well-behaved in class and was well-liked by his peers at school.
                Toni married his long-term girlfriend Jessica Farber on 13 June 2015. They have two sons and a daughter. He also owns a house on the island of Mallorca.</p>
            <h2>Career performance:</h2>
            <h3>Club career:</h3>
            <h3>Early years:</h3>
                He started his football career at his hometown club Greifswalder SC, but soon joined the more famous Hansa-Rostok club and the club's youth team.
                <h3>Bayern Munich:</h3>
                He was noticed by Bayern Munich in 2006 and joined the club. Kroos made 205 appearances for the club, scoring 25 goals.
                <h3>Bayer Leverkusen:</h3>
                In 2009, Kroos joined Bayer Leverkusen on loan. On 18 April 2009, he scored his first Bundesliga goal in a 2–1 defeat to Wolfsburg.
                <h3>Real Madrid:</h3>
                On 17 July 2014, Real Madrid announced that they had reached a final agreement for the transfer of Kroos. Kroos' contract was announced to be for 6 years. The fee was estimated to be around €25 million.
                He made his last appearance for Real Madrid in the 2024–23 Champions League final against Borussia Dortmund, winning his last trophy with Real Madrid during his club career. During his 10 seasons at Real Madrid, he won four La Liga titles and five Champions League trophies, as well as the Club World Cup five times.
                <h3>International career:</h3>
                Toni Kroos has been a regular in all German national football teams since 2014. He made his debut for the German national team in 2010 and was part of the German national team at the 2010 World Cup and Euro 2012. In 2014, he became the second player born in East Germany to win the World Cup after Matthias Sommer (1990).
        </section>

        <!-- Achievements Section -->
        <section id="achievements" class="mt-5 achievements">
            <h2>Achievements</h2>
            <ul>
                <li>Championship in the 2014 World Cup with the German national team</li>
                <li>Winning all the honors in Spain and Germany with Real Madrid and Bayern Munich</li>
                <li>Winning all the honors in Europe along with Real Madrid and Bayern Munich</li>
            </ul>
        </section>

        <!-- Gallery Section -->
        <section id="gallery" class="mt-5">
            <Center>
            <h2 class="gallery-title">Gallery</h2>
            </Center>
            <div id="carouselExampleIndicators" class="carousel slide" data-bs-ride="carousel">
                <div class="carousel-inner">
                    <div class="carousel-item active">
                        <img src="https://cdn.eghtesadnews.com/thumbnail/UQZM3M3V42kb/mW4TY_vzMeEG1fqb61-mcCKrGYGcOSm4SW9Yyhl5b2N1qvFeEPKLcFkzrdrrAcG9cg9gAf9kJWJmze2Es8GZhDlkJqwVKQrtbc4eiJrCiYs,/Untitled.jpg" class="d-block w-100 fixed-size" alt="...">
                    </div>
                    <div class="carousel-item">
                        <img src="https://ts18.tarafdari.com/contents/user763239/news/photo_2024-03-24_11-27-54.jpg" class="d-block w-100 fixed-size" alt="...">
                    </div>
                    <div class="carousel-item">
                        <img src="https://cdn.etemadonline.com/thumbnail/4anchR0aM39X/ehElMRVuo0EFHFrusS9hOc_4F_1qGBmyn5Ym7JNXdnhXoExBHxP6d-y_2m57V24kODV0c2JzZ9Y,/%D8%AA%D9%88%D9%86%DB%8C+%DA%A9%D8%B1%D9%88%D8%B3.jpg" class="d-block w-100 fixed-size" alt="...">
                    </div>
                </div>
                <button class="carousel-control-prev" type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide="prev">
                    <span class="carousel-control-prev-icon" aria-hidden="true"></span>
                    <span class="visually-hidden">Previous</span>
                </button>
                <button class="carousel-control-next" type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide="next">
                    <span class="carousel-control-next-icon" aria-hidden="true"></span>
                    <span class="visually-hidden">Next</span>
                </button>
            </div>
        </section>
        
        
        <!-- Testimonials Section -->
        <section id="testimonials" class="mt-5 testimonials">
            <h3>Coach and player comments</h3>
            <blockquote>
                <p>Zidan:I like watching him play. I like attending his training sessions. The training sessions are special. I'm not saying this to make a statement. He works very simply. He never gives the ball away. Maybe he does it once. He always plays with opportunism and intelligence. He never has a bad day. He loves football and always shows up motivated. This unites us. He loves football. For me, playing is more important than anything. Winning is important, but playing is the most important thing.</p>
            </blockquote>
            <blockquote>
                <p>Modric:At Real Madrid you can't afford not to be at a good level and Kroos is a unique player. He can make everything look like slow motion.</p>
            </blockquote>
            <blockquote>
                <p>Casemiro:Kroos always sets the rhythm of Real Madrid's games. He is one of the most important players in the team because he manages the ball. If Toni wants us to pause, we do. If he wants us to speed up the game, we do. We play based on Kroos' performance.</p>
            </blockquote>
            <blockquote>
                <p>Perez:Santiago Bernabeu said that the best should play in this game. That's why we bought Zidane, Ronaldo Nazario, Beckham, Ronaldo and Zidane. Buying the best gives the feeling that the best are playing in every position. Kroos has a style that makes everyone come to the pitch to see him. For me, he is one of the players who was born to play for Real Madrid.</p>
            </blockquote>
            <blockquote>
                <p>Matthias Sammer:Kroos is the conductor of the orchestra. He is the man who creates balance. Kroos provides what you want in a game: keeping calm and giving the team time to manage everything.</p>
            </blockquote>
            <blockquote>
                <p>Klose:If this boy doesn't become a star, it means I don't see anything in football. That's what I said as soon as I saw him at the Bayern academy."</p>
            </blockquote>
            <blockquote>
                <p>Robbie Williams (singer):Kroos has won everything at Real Madrid and that's why he should go to United! The English Premier League is the best league in the world for me. Real Madrid make me feel short. Football is my religion and I don't like there to be any gods bigger than mine.</p>
            </blockquote>
        </section>
    </div>

   
