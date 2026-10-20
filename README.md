
<!DOCTYPE html>
<html lang="cs">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Moje portfolio - Student 3. ročníku</title>

    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">

    <link rel="stylesheet" href="style.css">
</head>
<body>

    <header id="hlavicka-stranky">
        <a href="https://www.instagram.com/l_.altman/"
           target="_blank" rel="noopener noreferrer">Lukáš Altman</a>

        <nav id="navigace">
            <ul>
                <li><a href="#o-mne">O mně</a></li>
                <li><a href="#dovednosti">Dovednosti</a></li>
                <li><a href="#projekty">Projekty</a></li>
                <li><a href="#kontakt">Kontakt</a></li>
            </ul>
        </nav>
    </header>

    <section id="uvod">
        <h1 id="uvodni-nadpis">Ahoj, jsem student IT &amp; vývojář ✨</h1>
        <p id="uvodni-text">
            Studuji 3. ročník a baví mě tvořit webové stránky a aplikace.
        </p>
    </section>

    <main id="hlavni-obsah">

        <section id="o-mne">
            <h2 id="nadpis-o-mne">O mně</h2>
            <p id="popis-o-mne">
                Jsem studentem střední školy se zaměřením na informační technologie.
                Aktuálně se učím základy vývoje webu (HTML, CSS, JavaScript)
                a základy programování v Pythonu.
                Baví mě tvořit čisté a estetické věci s dobrým uživatelským zážitkem.
            </p>
        </section>

        <section id="dovednosti">
            <h2 id="nadpis-dovednosti">Moje dovednosti</h2>

            <div id="seznam-dovednosti">
                <div class="dovednost-karta" id="dovednost-html">
                    <h3>HTML5</h3>
                    <p>Sémantická struktura a tvorba čistého kódu.</p>
                </div>

                <div class="dovednost-karta" id="dovednost-css">
                    <h3>CSS3</h3>
                    <p>Moderní design, růžové palety, Flexbox a responzivita.</p>
                </div>

                <div class="dovednost-karta" id="dovednost-js">
                    <h3>JavaScript</h3>
                    <p>Základy interaktivity a logika webových aplikací.</p>
                </div>
            </div>
        </section>

        <section id="projekty">
            <h2 id="nadpis-projekty">Moje projekty</h2>

            <div id="projekt-1">
                <h3 id="nazev-projektu-1">
                    <a href="https://lukasaltman.github.io/it-webproject"
                       target="_blank" rel="noopener noreferrer">
                        IT Web Project ✨
                    </a>
                </h3>

                <p id="popis-projektu-1">
                    Školní webový projekt vytvořený v rámci studia IT.
                </p>
            </div>
        </section>

        <section id="kontakt">
            <h2 id="nadpis-kontakt">Kontaktujte mě</h2>

            <p id="kontakt-email">
                <strong>E-mail:</strong>
                <a href="mailto:d24723@oa-opava.cz">d24723@oa-opava.cz</a>
            </p>

            <p id="kontakt-github">
                <strong>GitHub:</strong>
                <a href="https://github.com/lukasaltman"
                   target="_blank" rel="noopener noreferrer">
                    github.com/lukasaltman
                </a>
            </p>

            <form id="kontaktni-formular" action="#" method="post" novalidate>
                <h3>Napište mi zprávu</h3>

                <div class="form-skupina">
                    <label for="jmeno">Jméno a příjmení *</label>
                    <input type="text" id="jmeno" name="jmeno"
                           required minlength="2" placeholder="Vaše jméno"
                           autocomplete="name">
                    <span class="chyba-zprava" id="chyba-jmeno"></span>
                </div>

                <div class="form-skupina">
                    <label for="email">E-mailová adresa *</label>
                    <input type="email" id="email" name="email"
                           required placeholder="vas@email.cz"
                           autocomplete="email">
                    <span class="chyba-zprava" id="chyba-email"></span>
                </div>

                <div class="form-skupina">
                    <label for="zprava">Zpráva *</label>
                    <textarea id="zprava" name="zprava" rows="4"
                              required minlength="10"
                              placeholder="Co mi chcete sdělit..."></textarea>
                    <span class="chyba-zprava" id="chyba-zprava"></span>
                </div>

                <button type="submit" id="tlacitko-odeslat">
                    Odeslat zprávu
                </button>

                <div id="form-status" role="status" aria-live="polite"></div>
            </form>
        </section>

    </main>

    <footer id="paticka-stranky">
        <p id="text-paticky">
            &copy; 2026 Lukáš Altman | Vytvořeno s ♡
        </p>

        <p id="zdroj-kod">
            <small>
                Design &amp; kód navržen s pomocí
                <a href="https://gemini.google.com"
                   target="_blank" rel="noopener noreferrer">Gemini AI</a>
            </small>
        </p>
    </footer>

    <script>
        document.addEventListener('DOMContentLoaded', () => {
            const form = document.getElementById('kontaktni-formular');
            const status = document.getElementById('form-status');

            const jmeno = document.getElementById('jmeno');
            const email = document.getElementById('email');
            const zprava = document.getElementById('zprava');

            form.addEventListener('submit', (e) => {
                e.preventDefault();

                let jePlatny = true;

                document.querySelectorAll('.chyba-zprava').forEach((el) => {
                    el.textContent = '';
                });

                status.textContent = '';

                if (jmeno.value.trim().length < 2) {
                    document.getElementById('chyba-jmeno').textContent =
                        'Zadejte jméno alespoň se 2 znaky.';
                    jePlatny = false;
                }

                const emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;

                if (!emailRegex.test(email.value.trim())) {
                    document.getElementById('chyba-email').textContent =
                        'Zadejte platnou e-mailovou adresu.';
                    jePlatny = false;
                }

                if (zprava.value.trim().length < 10) {
                    document.getElementById('chyba-zprava').textContent =
                        'Zpráva musí mít alespoň 10 znaků.';
                    jePlatny = false;
                }

                if (jePlatny) {
                    status.style.color = 'green';
                    status.textContent =
                        'Formulář je vyplněn správně. Zpráva zatím nebyla odeslána.';
                    form.reset();
                } else {
                    status.style.color = 'red';
                    status.textContent =
                        'Prosím, opravte chyby ve formuláři.';
                }
            });
        });
    </script>

</body>
</html>
