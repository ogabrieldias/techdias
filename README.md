HTML:
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, user-scalable=no, initial-scale=1.0">
    <title>Document</title>
    <!-- swiper css -->
    <link
    rel="stylesheet"
    href="https://cdn.jsdelivr.net/npm/swiper@11/swiper-bundle.min.css"/>
    <!-- <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/swiper@9/swiper-bundle.min.css" /> -->
    <!-- box-icons -->
    <link href='https://unpkg.com/boxicons@2.1.4/css/boxicons.min.css' rel='stylesheet'>
    <!-- /box-icons -->
    <link rel="stylesheet" href="../TechDias/css/pages/home.css"> <!-- Link style.css -->
    <link rel="stylesheet" href="../TechDias/css/responsive/responsive.css"> <!-- Link para responsividade -->
    <!-- swiper js -->
    <script src="https://cdn.jsdelivr.net/npm/swiper@11/swiper-bundle.min.js"></script>

    <!-- custom js -->
    <script src="../TechDias/js/pages/home.js" defer></script>
    
    <!-- scroll reveal -->
    <script src="https://unpkg.com/scrollreveal"></script>
    
</head>

<body>

    <header class="header"> <!-- Class Design header -->
    <a href="#" class="logo">TechDias</a> <!-- Class logo | /logo -->
        <nav class="navbar"> <!-- Class navbar -->
            <a href="#home" class="active" >Home</a> <!-- ID home | /home & Class active -->
            <a href="#sobre">Sobre</a> <!-- ID About -->
            <a href="#serviços">Serviços</a> <!-- ID Services -->
            <a href="#planos">Planos</a> <!-- ID portfolio -->
            <a href="#depoimentos">Depoimentos</a> <!-- ID contato -->
            <a href="#agendar">Agendar</a> <!-- ID contato -->
            <a href="#faq">FAQ</a> <!-- ID contato -->
            <a href="#contatos">Contatos</a> <!-- ID contato -->
        </nav> <!-- /navbar-->

        <div class='bx bx-moon' id="darkMode-icon"></div>

        <div class="bx bx-menu" id="menu-icon"></div>
    </header> <!-- Class /Design header -->
    
    

    <section class="home" id="home"> <!--Class home | ID home -->
    </section> <!-- Class /home | ID /home -->

    <section class="sobre" id="sobre" style="background-color: brown; width: 100%; height: 100vh;"> <!-- Class sobre | ID sobre  -->
    </section> <!-- Class /sobre | ID /sobre  -->

    <section class="serviços" id="serviços" style="background-color: aqua; width: 100%; height: 100vh;"> <!-- Class serviços | ID serviços -->
    </section> <!-- Class /serviços | ID /serviços -->

    <section class="planos" id="planos" style="background-color: greenyellow; width: 100%; height: 100vh;"> <!-- Class planos | ID planos -->
    </section> <!-- Class /planos | ID /planos -->n!-- Class depoimentos | ID depoimentos -->
    </section> <!-- Class /depoimentos | ID /depoimentos -->

    <section class="agendar" id="agendar" style="background-color: gold; width: 100%; height: 100vh;">
    </section>

    <section class="faq" id="faq" style="background-color: seagreen; width: 100%; height: 100vh;">
    </section>

    <section class="contatos" id="contatos" style="background-color: fuchsia; width: 100%; height: 100vh;">
    </section>


</body>
</html>

CSS:
home:

@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@100;200;300;400;500;600&display=swap');

*{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    text-decoration: none;
    border: none;
    outline: none;
    scroll-behavior: smooth;
    font-family: 'Poppins', sans-serif;
}

:root {
    --bg-color: #fdfdfd;
    --text-color: #333;
    --main-color: #00FFF5;
    --white-color: #fdfdfd;
    --shadow-color: rgba(0, 0, 0, .2);
    --cor-destaque: #00ADB5;
    --color-title: #00FFF5;
    
}

/* .dark-mode {
    --bg-color: #0D0C0D;
    --text-color: #fdfdfd;
    --shadow-color: rgba(0, 0, 0, .7);
    --main-color: #D92B04;
    --cor-destaque: #D92B04;
} */

.dark-mode { /* (dark-mode2) */
    /*cor excluida: #393E46 */     
    --bg-color: #222831;
    --text-color: #fdfdfd;
    --shadow-color: rgba(0, 0, 0, .7);
    --main-color: #00ADB5;
    --cor-destaque: #00FFF5;
}

html{
    font-size: 62.5%;
    overflow-x: hidden;     
}

body {
    background-color: var(--bg-color);
    color: var(--text-color);
}

.header {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    padding: 2rem 7%;
    background-color: transparent;
    display: flex;
    align-items: center;
    z-index: 1;
    transition: .5s;
}

.header.sticky {
    background: var(--bg-color);
    box-shadow:  0 .1rem 1rem var(--shadow-color);
}

.logo {
    font-size: 2.5rem;
    color: var(--cor-destaque);
    font-weight: 600;
    cursor: default;
    margin-right: auto;
}

.navbar a {
    position: relative;
    font-size: 1.7rem;
    color: var(--text-color);
    font-weight: 500;
    margin-right: 3.5rem;
}

.header.sticky .navbar a {
    color: var(--text-color);
}

.navbar a.active::before {
    content: '';
    position: absolute;
    left: 0;
    width: 100%;
    height: .2rem;
    bottom: -6px;
    background: var(--white-color);
}

.header.sticky .navbar a::before { /* Cor do Sticky(barra em baixo da letra) */
    background: var(--main-color);
    opacity: .7; 
}

.header.sticky .navbar a.active { /* Cor da letra ativa */
    color: var(--main-color);
}

#darkMode-icon {
    font-size: 2.4rem;
    color: var(--color-title);
    cursor: pointer;
}

.header.sticky #darkMode-icon {
    color: var(--text-color);
    opacity: .9;
}

#menu-icon {
    font-size: 3.6rem; 
    color: var(--cor-destaque);
    display: none;
}

section{
    min-height: 100vh;
    padding: 10rem 7% 2rem;
    background-color: var(--bg-color);
}

responsive:

/* BREAKPOINTS */
@media (max-width: 1440px) {
    .header{
        padding: 2rem 7%;
        width: 100%;
    }

    .navbar a {
        font-size: 2.1rem;
    }
    
    .logo {
        font-size: 3.5rem;
    }

    section {
        padding: 10rem 7% 2rem;
        /* max-height: 100vh; */
    }

    html {
        font-size: 51%;
    }
}

@media (max-width: 1200px) {
    .header{
        padding: 2rem 6%;
    }

    section {
        padding: 10rem 7% 2rem;
    }

    html {
        font-size: 51%;
    }
}  

@media (max-width: 991px) {
    html {
        font-size: 48%;
    }
    
    .navbar a.active::before {
        color: var(--main-color);
        opacity: .7;
    }
}  

@media (max-width: 768px) {
    html {
        font-size:47%;
    }

    #darkMode-icon {
        position: absolute;
        right: 12rem;
        font-size: 2.6rem;
        color: var(--cor-destaque);
        margin-bottom: .1rem;
    }

    .navbar {
        position: absolute;
        top: 100%;
        left: 0;
        width: 100%;
        padding: 1rem 3%;
        background: var(--bg-color);
        border-top: .1rem solid var(--cor-destaque);
        box-shadow: 0 .5rem 1rem rgba(0, 0, 0, .1);
        display: none;
    }

    .navbar.active {
        display: block;
    }

    .navbar a {
        display: block;
        font-size: 2rem;
        margin: 3rem 0;
        color: var(--cor-destaque);
    }

    .navbar a:nth-child(1),
    .navbar a:nth-child(2) {
        color: var(--cor-destaque);
    }

    .navbar a:active {
        color: var(--main-color);
    }

    .navbar a::before {
        display: none;
    }
}

@media (max-width: 450px) {
    html {
        font-size: 50%;
    }

    #darkMode-icon {
        right: 10rem;
    }

    .home {
        padding: 0 3% 30rem;
    }
}
