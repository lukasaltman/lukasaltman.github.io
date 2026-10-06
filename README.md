<!DOCTYPE html>
<html lang="cs">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Moje Portfólio - Student 3. ročníku</title>
    <!-- Načtení pěkného moderního písma z Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">
    <!-- Propojení s CSS souborem -->
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <!-- Hlavní hlavička s menu -->
    <header id="hlavicka-stranky">
        <a href="https://www.instagram.com/l_.altman/" target="_blank">Lukáš Altman</a>
    </h1>
        <nav id="navigace">
            <ul>
                <li><a href="#o-mne">O mně</a></li>
                <li><a href="#dovednosti">Dovednosti</a></li>
                <li><a href="#projekty">Projekty</a></li>
                <li><a href="#kontakt">Kontakt</a></li>
            </ul>
        </nav>
    </header>
    <!-- Úvodní sekce (Hero banner) -->
    <section id="uvod">
        <h2 id="uvodni-nadpis">Ahoj, jsem student IT & vývojář ✨</h2>
        <p id="uvodni-text">Studuji 3. ročník a baví mě tvořit webové stránky a aplikace.</p>
    </section>
    <!-- Hlavní obal pro sekce -->
    <main id="hlavni-obsah">
        <!-- Sekce O mně -->
        <section id="o-mne">
            <h2 id="nadpis-o-mne">O mně</h2>
            <p id="popis-o-mne">
                Jsem studentem střední školy se zaměřením na informační technologie.
                Aktuálně se učím základy vývoje webu (HTML, CSS, JavaScript) a základy programování v Pythonu.
                Baví mě tvořit čisté a estetické věci s dobrým uživatelským zážitkem.
            </p>
        </section>
        <!-- Sekce Dovednosti -->
        <section id="dovednosti">
            <h2 id="nadpis-dovednosti">Moje Dovednosti</h2>
            <div id="seznam-dovednosti">
                <div id="dovednost-html">
                    <h3>HTML5</h3>
                    <p>Sémantická struktura a tvorba čistého kódu.</p>
                </div>
                <div id="dovednost-css">
                    <h3>CSS3</h3>
                    <p>Moderní design, růžové palety, Flexbox a responzivita.</p>
                </div>
                <div id="dovednost-js">
                    <h3>JavaScript</h3>
                    <p>Základy interaktivity a logika webových aplikací.</p>
                </div>
            </div>
        </section>
        <!-- Sekce Projekty -->
        <section id="projekty">
            <h2 id="nadpis-projekty">Moje Projekty</h2>
                <div id="projekt-1">
                <h3 id="nazev-projektu-1">Osobní Portfólio</h3>
            <div id="projekt-1">
        <h3 id="nazev-projektu-1">
            <a href="https://lukasaltman.github.io/it-webproject" target="_blank">IT Web Project ✨</a>
        </h3>
        <p id="popis-projektu-1">Školní webový projekt vytvořený v rámci studia IT.</p>
    </div>
            </div>
        </section>
        <!-- Sekce Kontakt -->
        <section id="kontakt">
            <h2 id="nadpis-kontakt">Kontaktujte mě</h2>
            <p id="kontakt-email"><strong>E-mail:</strong> d24723@oa-opava.cz</p>
            <p id="kontakt-github"><strong>GitHub:</strong> https://github.com/lukasaltman</p>
        </section>
    </main>
    <!-- Patička stránky -->
    <footer id="paticka-stranky">
        <p id="text-paticky">&copy; 2026 Lukáš Altman | Vytvořeno s ♡</p>
    </footer>

</body>
</html>