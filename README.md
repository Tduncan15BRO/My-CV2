# My-CV
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Teddy Duncan Jr. - Academic CV</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --primary-color: #1a472a;
            --secondary-color: #2d5016;
            --accent-color: #5a9216;
            --text-color: #2c3e50;
            --light-bg: #f8f9fa;
            --white: #ffffff;
            --border-color: #dee2e6;
        }

        body {
            font-family: 'Georgia', 'Times New Roman', serif;
            line-height: 1.8;
            color: var(--text-color);
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
            min-height: 100vh;
        }

        .container {
            max-width: 1000px;
            margin: 0 auto;
            background: var(--white);
            box-shadow: 0 0 40px rgba(0, 0, 0, 0.1);
            animation: fadeIn 0.8s ease-out;
        }

        @keyframes fadeIn {
            from {
                opacity: 0;
                transform: translateY(20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        header {
            background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
            color: var(--white);
            padding: 60px 40px;
            text-align: center;
            position: relative;
            overflow: hidden;
        }

        header::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 320"><path fill="%23ffffff" fill-opacity="0.05" d="M0,96L48,112C96,128,192,160,288,160C384,160,480,128,576,133.3C672,139,768,181,864,181.3C960,181,1056,139,1152,112C1248,85,1344,75,1392,69.3L1440,64L1440,320L1392,320C1344,320,1248,320,1152,320C1056,320,960,320,864,320C768,320,672,320,576,320C480,320,384,320,288,320C192,320,96,320,48,320L0,320Z"></path></svg>') no-repeat bottom;
            background-size: cover;
        }

        h1 {
            font-size: 2.8em;
            margin-bottom: 10px;
            font-weight: 300;
            letter-spacing: 2px;
            position: relative;
            z-index: 1;
        }

        .subtitle {
            font-size: 1.2em;
            margin-bottom: 30px;
            opacity: 0.95;
            font-style: italic;
            position: relative;
            z-index: 1;
        }

        .contact-info {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 25px;
            position: relative;
            z-index: 1;
            font-size: 0.95em;
        }

        .contact-item {
            display: flex;
            align-items: center;
            gap: 8px;
            transition: transform 0.3s ease;
        }

        .contact-item:hover {
            transform: translateY(-2px);
        }

        .contact-item a {
            color: var(--white);
            text-decoration: none;
            border-bottom: 1px solid transparent;
            transition: border-color 0.3s ease;
        }

        .contact-item a:hover {
            border-bottom-color: var(--white);
        }

        nav {
            background: var(--light-bg);
            padding: 20px 40px;
            border-bottom: 1px solid var(--border-color);
            position: sticky;
            top: 0;
            z-index: 100;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }

        nav ul {
            list-style: none;
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 30px;
        }

        nav a {
            color: var(--primary-color);
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s ease;
            font-size: 0.95em;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        nav a:hover {
            color: var(--accent-color);
        }

        main {
            padding: 40px;
        }

        section {
            margin-bottom: 50px;
            opacity: 0;
            animation: slideUp 0.6s ease-out forwards;
        }

        section:nth-child(1) { animation-delay: 0.1s; }
        section:nth-child(2) { animation-delay: 0.2s; }
        section:nth-child(3) { animation-delay: 0.3s; }
        section:nth-child(4) { animation-delay: 0.4s; }
        section:nth-child(5) { animation-delay: 0.5s; }
        section:nth-child(6) { animation-delay: 0.6s; }
        section:nth-child(7) { animation-delay: 0.7s; }
        section:nth-child(8) { animation-delay: 0.8s; }

        @keyframes slideUp {
            to {
                opacity: 1;
                transform: translateY(0);
            }
            from {
                opacity: 0;
                transform: translateY(20px);
            }
        }

        h2 {
            color: var(--primary-color);
            border-bottom: 2px solid var(--accent-color);
            padding-bottom: 10px;
            margin-bottom: 25px;
            font-size: 1.8em;
            font-weight: 400;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .entry {
            margin-bottom: 25px;
            padding: 20px;
            background: var(--light-bg);
            border-left: 4px solid var(--accent-color);
            transition: all 0.3s ease;
            border-radius: 0 8px 8px 0;
        }

        .entry:hover {
            transform: translateX(5px);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }

        .entry-header {
            display: flex;
            justify-content: space-between;
            align-items: baseline;
            margin-bottom: 10px;
            flex-wrap: wrap;
        }

        .entry-title {
            font-weight: bold;
            color: var(--primary-color);
            font-size: 1.1em;
        }

        .entry-institution {
            color: var(--secondary-color);
            font-style: italic;
            margin-top: 5px;
        }

        .entry-date {
            color: #6c757d;
            font-size: 0.95em;
        }

        .publication {
            margin-bottom: 20px;
            padding: 15px;
            background: var(--light-bg);
            border-radius: 8px;
            transition: all 0.3s ease;
        }

        .publication:hover {
            transform: translateX(3px);
            box-shadow: 0 3px 10px rgba(0, 0, 0, 0.1);
        }

        .book-title {
            font-style: italic;
            font-weight: bold;
            color: var(--primary-color);
        }

        .article-title {
            font-weight: normal;
        }

        .journal-name {
            font-style: italic;
        }

        .award {
            margin-bottom: 20px;
            padding: 15px;
            background: linear-gradient(135deg, #ffefc1 0%, #fff8e1 100%);
            border-radius: 8px;
            border-left: 4px solid #ffc107;
        }

        .course-list {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 10px;
            margin-top: 10px;
        }

        .course {
            padding: 8px 12px;
            background: var(--white);
            border-radius: 5px;
            border: 1px solid var(--border-color);
            transition: all 0.3s ease;
        }

        .course:hover {
            border-color: var(--accent-color);
            transform: translateY(-2px);
        }

        ul {
            list-style: none;
            padding-left: 0;
        }

        ul li {
            position: relative;
            padding-left: 25px;
            margin-bottom: 10px;
        }

        ul li::before {
            content: '▸';
            position: absolute;
            left: 0;
            color: var(--accent-color);
            font-weight: bold;
        }

        .print-button {
            position: fixed;
            bottom: 30px;
            right: 30px;
            background: var(--accent-color);
            color: var(--white);
            border: none;
            padding: 15px 25px;
            border-radius: 50px;
            cursor: pointer;
            font-size: 1em;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
            transition: all 0.3s ease;
            z-index: 1000;
        }

        .print-button:hover {
            transform: translateY(-3px);
            box-shadow: 0 6px 20px rgba(0, 0, 0, 0.3);
            background: var(--primary-color);
        }

        @media (max-width: 768px) {
            header {
                padding: 40px 20px;
            }
            
            h1 {
                font-size: 2em;
            }
            
            nav {
                padding: 15px 20px;
            }
            
            nav ul {
                gap: 15px;
            }
            
            main {
                padding: 20px;
            }
            
            .entry-header {
                flex-direction: column;
            }
            
            .entry-date {
                margin-top: 5px;
            }
        }

        @media print {
            body {
                background: white;
            }
            
            .container {
                box-shadow: none;
            }
            
            nav, .print-button {
                display: none;
            }
            
            header {
                background: var(--primary-color) !important;
                print-color-adjust: exact;
                -webkit-print-color-adjust: exact;
            }
            
            section {
                page-break-inside: avoid;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>TEDDY DUNCAN JR.</h1>
            <div class="subtitle">Assistant Professor of English</div>
            <div class="contact-info">
                <div class="contact-item">
                    <span>📧</span>
                    <a href="mailto:teddyduncanjr407@gmail.com">teddyduncanjr407@gmail.com</a>
                </div>
                <div class="contact-item">
                    <span>📱</span>
                    <span>407-541-7139</span>
                </div>
                <div class="contact-item">
                    <span>📍</span>
                    <span>206 Mc Quigg Avenue, Orlando, FL 32805</span>
                </div>
            </div>
        </header>

        <nav>
            <ul>
                <li><a href="#education">Education</a></li>
                <li><a href="#positions">Positions</a></li>
                <li><a href="#books">Books</a></li>
                <li><a href="#publications">Publications</a></li>
                <li><a href="#teaching">Teaching</a></li>
                <li><a href="#honors">Honors</a></li>
                <li><a href="#service">Service</a></li>
            </ul>
        </nav>

        <main>
            <section id="education">
                <h2>Education</h2>
                <div class="entry">
                    <div class="entry-header">
                        <div>
                            <div class="entry-title">Master of Arts in English</div>
                            <div class="entry-institution">University of South Florida</div>
                        </div>
                        <div class="entry-date">Spring 2022</div>
                    </div>
                </div>
                <div class="entry">
                    <div class="entry-header">
                        <div>
                            <div class="entry-title">Bachelor of Arts in English</div>
                            <div class="entry-institution">University of Central Florida</div>
                        </div>
                        <div class="entry-date">Spring 2020</div>
                    </div>
                </div>
                <div class="entry">
                    <div class="entry-header">
                        <div>
                            <div class="entry-title">Associate of Arts in General Education</div>
                            <div class="entry-institution">Valencia College</div>
                        </div>
                        <div class="entry-date">Fall 2017</div>
                    </div>
                </div>
            </section>

            <section id="positions">
                <h2>Positions Held</h2>
                <div class="entry">
                    <div class="entry-header">
                        <div>
                            <div class="entry-title">Assistant Professor</div>
                            <div class="entry-institution">Valencia College</div>
                        </div>
                        <div class="entry-date">2024 - Current</div>
                    </div>
                </div>
                <div class="entry">
                    <div class="entry-header">
                        <div>
                            <div class="entry-title">Full-Time Professor</div>
                            <div class="entry-institution">Keiser University</div>
                        </div>
                        <div class="entry-date">2022 - 2024</div>
                    </div>
                </div>
                <div class="entry">
                    <div class="entry-header">
                        <div>
                            <div class="entry-title">Graduate Teaching Assistant</div>
                            <div class="entry-institution">University of South Florida</div>
                        </div>
                        <div class="entry-date">2020 - 2022</div>
                    </div>
                </div>
            </section>

            <section id="books">
                <h2>Book Projects</h2>
                <div class="publication">
                    <span class="book-title">Zoological Lacan: A Lacanian Framework for Animality and Humanness</span><br>
                    Routledge, Lines of the Symbolic Series, Under Contract
                </div>
                <div class="publication">
                    <span class="book-title">Interpreting Meat: Theorizing the Commodification and Consumption of Animals</span><br>
                    McFarland & Company, December 2024
                </div>
            </section>

            <section id="publications">
                <h2>Scholarly Publications (Peer-Reviewed)</h2>
                <div class="publication">
                    <span class="article-title">"The Limits of Understanding: Lacanian Pedagogy in the Composition Classroom,"</span>
                    <span class="journal-name">Journal on Excellence in College Teaching</span>, May 2025
                </div>
                <div class="publication">
                    <span class="article-title">"Recognizing Exploitation and Rejecting Analogy: An Analysis of the Meat-Commodity,"</span>
                    <span class="journal-name">Between the Species</span>, March 2024
                </div>
                <div class="publication">
                    <span class="article-title">"The Inexplicable Real and Silent (Female) Desire: A Lacanian Approach to the Unsaid in The Awakening,"</span>
                    <span class="journal-name">Midwest Quarterly</span>, January 2023
                </div>
                <div class="publication">
                    <span class="article-title">"Politics of Dismissal and Death: Tentacle, Necropolitics, and the Political Subject,"</span>
                    <span class="journal-name">Latin American Literary Review</span>, November 2022
                </div>
                <div class="publication">
                    <span class="article-title">"Žižekian Ideology and the 'Sympathetic' Slave-Owner: Ostensible Necessity of Slavery in Our Nig and Minnie's Sacrifice,"</span>
                    <span class="journal-name">International Journal of Žižek Studies</span>, July 2021
                </div>
            </section>

            <section id="teaching">
                <h2>Teaching Experience</h2>
                <div class="entry">
                    <div class="entry-header">
                        <div>
                            <div class="entry-title">Professor</div>
                            <div class="entry-institution">Valencia College (Osceola Campus)</div>
                        </div>
                        <div class="entry-date">January 2024 - Present</div>
                    </div>
                    <div class="course-list">
                        <div class="course">Composition I (ENC 1101) - Online & In-Person</div>
                        <div class="course">Composition II (ENC 1102) - Online & In-Person</div>
                    </div>
                </div>
                <div class="entry">
                    <div class="entry-header">
                        <div>
                            <div class="entry-title">Faculty Professor</div>
                            <div class="entry-institution">Keiser University</div>
                        </div>
                        <div class="entry-date">June 2022 - July 2024</div>
                    </div>
                    <div class="course-list">
                        <div class="course">Basic English (ENC 0001)</div>
                        <div class="course">Composition I (ENC 1101)</div>
                        <div class="course">Composition II (ENC 2102)</div>
                        <div class="course">American Literature (AML 1000)</div>
                        <div class="course">Writing For Managers (ENC 3213)</div>
                        <div class="course">Research Writing (ENC 4313)</div>
                    </div>
                </div>
                <div class="entry">
                    <div class="entry-header">
                        <div>
                            <div class="entry-title">Graduate Teaching Assistant (Instructor of Record)</div>
                            <div class="entry-institution">University of South Florida</div>
                        </div>
                        <div class="entry-date">August 2020 - May 2022</div>
                    </div>
                    <div class="course-list">
                        <div class="course">Composition I (ENC 1101) - Online & In-Person</div>
                        <div class="course">Composition II (ENC 1102) - Online & In-Person</div>
                    </div>
                </div>
            </section>

            <section id="honors">
                <h2>Honors and Awards</h2>
                <div class="award">
                    <strong>Summer Mentor Fellowship</strong>, UCF, Summer 2025<br>
                    Awarded to write chapter of contracted book. ($4,500)
                </div>
                <div class="award">
                    <strong>TLC Appreciation Award</strong>, Keiser University, Fall 2023<br>
                    Awarded for service to campus.
                </div>
                <div class="award">
                    <strong>Irving Deer Memorial Scholarship Award</strong>, USF, Spring 2022<br>
                    Awarded based on merit of graduate research writing. ($1,275)
                </div>
                <div class="award">
                    <strong>Distinguished Undergraduate Research Award</strong>, UCF, Spring 2020<br>
                    Awarded to undergraduates based on merit of conducted research. ($250)
                </div>
                <div class="award">
                    <strong>Selected Poetry Award</strong>, Fallero Literary Magazine, Valencia College, Spring 2017. ($75)
                </div>
            </section>

            <section id="service">
                <h2>Service</h2>
                <ul>
                    <li>Valencia Faculty Learning Committee Convener, 2024-Present</li>
                    <li>Keiser University Literacy Committee Chair, 2023-2024</li>
                    <li>Keiser TLC Coordinator (Technology and Learning Center), 2023-2024</li>
                    <li>Editor of Keiser University Tampa Literary Magazine, 2023-202
