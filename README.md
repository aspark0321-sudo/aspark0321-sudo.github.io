# aspark0321-sudo.github.io

<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>박소현 | R&D Planning Portfolio</title>

    <meta name="description"
          content="박소현의 LIG D&A 연구기획 직무 포트폴리오">

    <style>

        /* =====================================================
           01. GLOBAL
        ===================================================== */

        :root {
            --navy: #0B1F3A;
            --deep-navy: #071426;
            --blue: #174A7E;
            --light-blue: #EAF0F7;
            --lighter-blue: #F5F8FC;

            --white: #FFFFFF;
            --black: #111827;
            --text: #1F2937;
            --sub-text: #64748B;
            --line: #DCE3EC;

            --max-width: 1180px;

            --shadow:
                0 10px 30px rgba(11, 31, 58, 0.08);

            --radius: 16px;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family:
                -apple-system,
                BlinkMacSystemFont,
                "Segoe UI",
                "Noto Sans KR",
                sans-serif;

            color: var(--text);
            background: var(--white);
            line-height: 1.7;
        }

        a {
            text-decoration: none;
            color: inherit;
        }

        button {
            font-family: inherit;
        }

        img {
            max-width: 100%;
            display: block;
        }

        .container {
            width: min(92%, var(--max-width));
            margin: 0 auto;
        }


        /* =====================================================
           02. HEADER
        ===================================================== */

        header {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            z-index: 1000;

            background: rgba(255,255,255,0.94);
            backdrop-filter: blur(12px);

            border-bottom: 1px solid rgba(220,227,236,0.8);
        }

        .nav {
            height: 72px;

            display: flex;
            align-items: center;
            justify-content: space-between;
        }

        .logo {
            font-weight: 800;
            font-size: 18px;
            color: var(--navy);
            letter-spacing: -0.5px;
        }

        .logo span {
            display: block;
            font-size: 10px;
            font-weight: 500;
            color: var(--sub-text);
            letter-spacing: 1.5px;
            margin-top: -3px;
        }

        .nav-links {
            display: flex;
            gap: 30px;
            align-items: center;
        }

        .nav-links a {
            font-size: 13px;
            font-weight: 600;
            color: var(--sub-text);
            transition: 0.25s;
        }

        .nav-links a:hover {
            color: var(--navy);
        }

        .nav-cta {
            padding: 9px 16px;
            background: var(--navy);
            color: white !important;
            border-radius: 8px;
        }


        /* =====================================================
           03. HERO
        ===================================================== */

        .hero {
            min-height: 100vh;

            display: flex;
            align-items: center;

            background:
                linear-gradient(
                    135deg,
                    #ffffff 0%,
                    #ffffff 58%,
                    #F1F5FA 100%
                );

            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: "";
            position: absolute;

            width: 500px;
            height: 500px;

            right: -180px;
            top: 80px;

            border-radius: 50%;

            background: rgba(23,74,126,0.05);
        }

        .hero-content {
            position: relative;
            z-index: 1;

            max-width: 900px;
            padding-top: 60px;
        }

        .hero-label {
            display: inline-flex;
            align-items: center;
            gap: 8px;

            padding: 7px 13px;

            border-radius: 30px;

            background: var(--light-blue);
            color: var(--blue);

            font-size: 12px;
            font-weight: 700;

            margin-bottom: 28px;
        }

        .hero-label::before {
            content: "";
            width: 6px;
            height: 6px;
            background: var(--blue);
            border-radius: 50%;
        }

        .hero h1 {
            font-size: clamp(42px, 6vw, 76px);
            line-height: 1.12;
            letter-spacing: -3px;

            color: var(--navy);

            margin-bottom: 25px;
        }

        .hero h1 span {
            color: var(--blue);
        }

        .hero-description {
            font-size: 19px;
            line-height: 1.7;
            color: var(--sub-text);

            max-width: 700px;
            margin-bottom: 38px;
        }

        .hero-description strong {
            color: var(--navy);
        }

        .hero-buttons {
            display: flex;
            gap: 12px;
            flex-wrap: wrap;
        }

        .btn {
            display: inline-flex;
            align-items: center;
            justify-content: center;

            padding: 13px 22px;

            border-radius: 9px;

            font-size: 13px;
            font-weight: 700;

            transition: 0.25s;
        }

        .btn-primary {
            background: var(--navy);
            color: white;
        }

        .btn-primary:hover {
            background: var(--blue);
            transform: translateY(-2px);
        }

        .btn-outline {
            border: 1px solid var(--line);
            color: var(--navy);
            background: white;
        }

        .btn-outline:hover {
            border-color: var(--navy);
            transform: translateY(-2px);
        }

        .hero-keywords {
            margin-top: 70px;

            display: flex;
            gap: 10px;
            flex-wrap: wrap;
        }

        .keyword {
            padding: 8px 14px;

            border: 1px solid var(--line);
            border-radius: 30px;

            color: var(--sub-text);
            font-size: 12px;
            font-weight: 600;

            background: rgba(255,255,255,0.7);
        }


        /* =====================================================
           04. SECTION COMMON
        ===================================================== */

        section {
            padding: 110px 0;
        }

        .section-header {
            margin-bottom: 55px;
        }

        .section-number {
            color: var(--blue);
            font-size: 12px;
            font-weight: 800;
            letter-spacing: 2px;
            margin-bottom: 10px;
        }

        .section-title {
            color: var(--navy);
            font-size: clamp(30px, 4vw, 44px);
            line-height: 1.2;
            letter-spacing: -1.5px;
            margin-bottom: 14px;
        }

        .section-description {
            max-width: 650px;
            color: var(--sub-text);
            font-size: 15px;
        }


        /* =====================================================
           05. ABOUT
        ===================================================== */

        #about {
            background: var(--lighter-blue);
        }

        .profile-intro {
            display: grid;
            grid-template-columns: 1fr 2fr;
            gap: 70px;
            margin-bottom: 70px;
        }

        .profile-title {
            font-size: 27px;
            color: var(--navy);
            line-height: 1.45;
            letter-spacing: -1px;
        }

        .profile-title span {
            color: var(--blue);
        }

        .profile-text {
            color: var(--sub-text);
            font-size: 15px;
        }

        .profile-text strong {
            color: var(--navy);
        }


        /* Timeline */

        .timeline {
            position: relative;
            padding-left: 30px;
        }

        .timeline::before {
            content: "";
            position: absolute;

            left: 6px;
            top: 10px;
            bottom: 10px;

            width: 1px;

            background: #C8D4E2;
        }

        .timeline-item {
            position: relative;
            padding: 0 0 42px 35px;
        }

        .timeline-item:last-child {
            padding-bottom: 0;
        }

        .timeline-dot {
            position: absolute;

            left: -1px;
            top: 5px;

            width: 14px;
            height: 14px;

            border-radius: 50%;

            background: white;
            border: 3px solid var(--blue);
        }

        .timeline-date {
            font-size: 12px;
            font-weight: 700;
            color: var(--blue);

            margin-bottom: 5px;
        }

        .timeline-title {
            font-size: 20px;
            font-weight: 800;
            color: var(--navy);

            margin-bottom: 5px;
        }

        .timeline-subtitle {
            font-size: 13px;
            color: var(--sub-text);
            margin-bottom: 10px;
        }

        .timeline-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 7px;
        }

        .timeline-tag {
            padding: 5px 10px;

            background: white;
            border: 1px solid var(--line);
            border-radius: 20px;

            color: var(--sub-text);
            font-size: 11px;
            font-weight: 600;
        }


        /* =====================================================
           06. EXPERIENCE
        ===================================================== */

        .experience-tabs {
            display: flex;
            gap: 8px;
            flex-wrap: wrap;

            margin-bottom: 35px;
        }

        .experience-tab {
            border: 1px solid var(--line);
            background: white;

            color: var(--sub-text);

            padding: 11px 18px;

            border-radius: 8px;

            cursor: pointer;

            font-size: 13px;
            font-weight: 700;

            transition: 0.25s;
        }

        .experience-tab.active,
        .experience-tab:hover {
            background: var(--navy);
            border-color: var(--navy);
            color: white;
        }

        .experience-content {
            display: none;

            animation: fadeUp 0.4s ease;
        }

        .experience-content.active {
            display: block;
        }

        @keyframes fadeUp {
            from {
                opacity: 0;
                transform: translateY(10px);
            }

            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .experience-grid {
            display: grid;
            grid-template-columns: 1.2fr 0.8fr;
            gap: 25px;
        }

        .experience-main,
        .experience-side {
            background: white;
            border: 1px solid var(--line);
            border-radius: var(--radius);

            padding: 35px;

            box-shadow: var(--shadow);
        }

        .experience-heading {
            display: flex;
            justify-content: space-between;
            gap: 20px;

            margin-bottom: 30px;
        }

        .experience-company {
            color: var(--navy);
            font-size: 27px;
            line-height: 1.3;
            margin-bottom: 5px;
        }

        .experience-position {
            color: var(--blue);
            font-size: 13px;
            font-weight: 700;
        }

        .experience-period {
            color: var(--sub-text);
            font-size: 12px;
            white-space: nowrap;
        }

        .content-label {
            font-size: 11px;
            letter-spacing: 1.5px;
            font-weight: 800;
            color: var(--blue);

            margin-bottom: 12px;
        }

        .experience-list {
            list-style: none;
            margin-bottom: 32px;
        }

        .experience-list li {
            position: relative;

            padding-left: 18px;
            margin-bottom: 9px;

            color: var(--text);
            font-size: 14px;
        }

        .experience-list li::before {
            content: "•";

            position: absolute;
            left: 0;

            color: var(--blue);
            font-weight: 800;
        }

        .achievement-box {
            background: var(--lighter-blue);

            padding: 23px;

            border-radius: 12px;
        }

        .achievement-box li {
            font-weight: 600;
        }

        .takeaway {
            margin-top: 20px;

            padding: 22px;

            border-left: 3px solid var(--blue);

            background: #F8FAFD;
        }

        .takeaway p {
            color: var(--text);
            font-size: 14px;
        }


        /* Side */

        .metric {
            padding: 20px 0;
            border-bottom: 1px solid var(--line);
        }

        .metric:last-child {
            border-bottom: 0;
        }

        .metric-number {
            color: var(--navy);
            font-size: 38px;
            font-weight: 800;
            line-height: 1;
        }

        .metric-label {
            color: var(--sub-text);
            font-size: 12px;
            margin-top: 5px;
        }

        .image-placeholder {
            width: 100%;
            height: 220px;

            display: flex;
            align-items: center;
            justify-content: center;

            background: var(--light-blue);

            border-radius: 12px;

            color: var(--blue);
            font-size: 12px;
            font-weight: 700;

            text-align: center;

            margin-top: 25px;
        }

        .image-placeholder img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            border-radius: 12px;
        }


        /* =====================================================
           07. R&D LIFE CYCLE
        ===================================================== */

        .lifecycle {
            margin-top: 60px;

            display: grid;
            grid-template-columns: repeat(6, 1fr);
        }

        .life-step {
            position: relative;

            text-align: center;

            padding: 25px 10px;
        }

        .life-step:not(:last-child)::after {
            content: "→";

            position: absolute;

            right: -8px;
            top: 37px;

            color: #A8B6C7;
            font-weight: 700;
        }

        .life-number {
            width: 50px;
            height: 50px;

            margin: 0 auto 12px;

            border-radius: 50%;

            display: flex;
            align-items: center;
            justify-content: center;

            background: var(--navy);
            color: white;

            font-size: 13px;
            font-weight: 800;
        }

        .life-title {
            color: var(--navy);
            font-size: 13px;
            font-weight: 800;
        }

        .life-desc {
            color: var(--sub-text);
            font-size: 11px;
            margin-top: 4px;
        }


        /* =====================================================
           08. COMPETENCIES
        ===================================================== */

        #competencies {
            background: var(--navy);
            color: white;
        }

        #competencies .section-number {
            color: #8FB4D8;
        }

        #competencies .section-title {
            color: white;
        }

        #competencies .section-description {
            color: #AEBFD1;
        }

        .competency-grid {
            display: grid;
            grid-template-columns: repeat(5, 1fr);
            gap: 14px;
        }

        .competency-card {
            padding: 28px 22px;

            border: 1px solid rgba(255,255,255,0.12);
            background: rgba(255,255,255,0.04);

            border-radius: 14px;

            transition: 0.3s;
        }

        .competency-card:hover {
            transform: translateY(-6px);
            background: rgba(255,255,255,0.08);
        }

        .competency-icon {
            width: 44px;
            height: 44px;

            border-radius: 10px;

            background: rgba(255,255,255,0.1);

            display: flex;
            align-items: center;
            justify-content: center;

            margin-bottom: 22px;

            font-size: 18px;
        }

        .competency-card h3 {
            font-size: 16px;
            margin-bottom: 9px;
        }

        .competency-card p {
            color: #AEBFD1;
            font-size: 12px;
            line-height: 1.65;
        }

        .competency-evidence {
            margin-top: 18px;

            padding-top: 15px;

            border-top: 1px solid rgba(255,255,255,0.1);

            color: #D6E2ED;

            font-size: 11px;
            font-weight: 600;
        }


        /* =====================================================
           09. HOW I WORK
        ===================================================== */

        .work-process {
            display: grid;
            grid-template-columns: repeat(5, 1fr);
            gap: 15px;
        }

        .work-card {
            padding: 28px;

            border: 1px solid var(--line);
            border-radius: var(--radius);

            background: white;

            position: relative;
        }

        .work-card-number {
            color: var(--blue);
            font-size: 11px;
            font-weight: 800;
            letter-spacing: 1px;

            margin-bottom: 20px;
        }

        .work-card h3 {
            color: var(--navy);
            font-size: 18px;
            margin-bottom: 8px;
        }

        .work-card p {
            color: var(--sub-text);
            font-size: 12px;
        }


        /* =====================================================
           10. PROJECT
        ===================================================== */

        #project {
            background: var(--lighter-blue);
        }

        .project-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 20px;
        }

        .project-card {
            background: white;

            border: 1px solid var(--line);
            border-radius: var(--radius);

            overflow: hidden;

            transition: 0.3s;
        }

        .project-card:hover {
            transform: translateY(-5px);
            box-shadow: var(--shadow);
        }

        .project-image {
            height: 230px;

            display: flex;
            align-items: center;
            justify-content: center;

            background:
                linear-gradient(
                    135deg,
                    var(--navy),
                    var(--blue)
                );

            color: white;

            font-size: 13px;
            font-weight: 700;
        }

        .project-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .project-body {
            padding: 27px;
        }

        .project-category {
            color: var(--blue);

            font-size: 10px;
            font-weight: 800;
            letter-spacing: 1.3px;

            margin-bottom: 8px;
        }

        .project-title {
            color: var(--navy);
            font-size: 21px;
            margin-bottom: 9px;
        }

        .project-desc {
            color: var(--sub-text);
            font-size: 13px;

            margin-bottom: 18px;
        }

        .project-result {
            padding: 14px;

            background: var(--lighter-blue);

            border-radius: 9px;

            color: var(--navy);

            font-size: 12px;
            font-weight: 700;
        }


        /* =====================================================
           11. PROJECT DETAIL
        ===================================================== */

        .case-study {
            margin-top: 60px;

            background: white;

            border: 1px solid var(--line);
            border-radius: var(--radius);

            padding: 40px;

            box-shadow: var(--shadow);
        }

        .case-header {
            display: flex;
            justify-content: space-between;
            gap: 30px;

            margin-bottom: 35px;
        }

        .case-title {
            color: var(--navy);
            font-size: 28px;
        }

        .case-role {
            color: var(--blue);
            font-size: 12px;
            font-weight: 700;
        }

        .case-columns {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 20px;
        }

        .case-box {
            padding: 23px;

            border: 1px solid var(--line);
            border-radius: 12px;
        }

        .case-box h4 {
            color: var(--navy);
            font-size: 14px;
            margin-bottom: 9px;
        }

        .case-box p {
            color: var(--sub-text);
            font-size: 12px;
        }


        /* =====================================================
           12. ACTIVITIES
        ===================================================== */

        .activity-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 15px;
        }

        .activity-card {
            padding: 25px;

            border: 1px solid var(--line);
            border-radius: 12px;

            background: white;
        }

        .activity-card h3 {
            color: var(--navy);
            font-size: 17px;
            margin-bottom: 5px;
        }

        .activity-period {
            color: var(--blue);
            font-size: 11px;
            font-weight: 700;
            margin-bottom: 12px;
        }

        .activity-card p {
            color: var(--sub-text);
            font-size: 12px;
        }


        /* =====================================================
           13. SITEMAP
        ===================================================== */

        .sitemap {
            background: var(--deep-navy);
            color: white;

            padding: 65px 0;
        }

        .sitemap-title {
            font-size: 12px;
            letter-spacing: 2px;

            color: #8FB4D8;

            margin-bottom: 25px;
        }

        .sitemap-grid {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 35px;
        }

        .sitemap-column h3 {
            font-size: 13px;
            margin-bottom: 12px;
        }

        .sitemap-column a {
            display: block;

            color: #91A5BA;

            font-size: 11px;

            margin-bottom: 5px;

            transition: 0.2s;
        }

        .sitemap-column a:hover {
            color: white;
        }

        footer {
            background: var(--deep-navy);

            border-top: 1px solid rgba(255,255,255,0.08);

            padding: 25px 0;

            color: #71859A;

            font-size: 10px;
        }

        .footer-inner {
            display: flex;
            justify-content: space-between;
        }


        /* =====================================================
           14. RESPONSIVE
        ===================================================== */

        @media (max-width: 900px) {

            .nav-links {
                display: none;
            }

            .profile-intro {
                grid-template-columns: 1fr;
                gap: 20px;
            }

            .experience-grid {
                grid-template-columns: 1fr;
            }

            .competency-grid {
                grid-template-columns: repeat(2, 1fr);
            }

            .work-process {
                grid-template-columns: repeat(2, 1fr);
            }

            .lifecycle {
                grid-template-columns: repeat(3, 1fr);
            }

            .life-step:nth-child(3)::after {
                display: none;
            }

            .case-columns {
                grid-template-columns: 1fr;
            }

            .sitemap-grid {
                grid-template-columns: repeat(2, 1fr);
            }
        }


        @media (max-width: 600px) {

            section {
                padding: 75px 0;
            }

            .hero h1 {
                letter-spacing: -2px;
            }

            .hero-description {
                font-size: 16px;
            }

            .experience-main,
            .experience-side,
            .case-study {
                padding: 24px;
            }

            .experience-heading {
                flex-direction: column;
            }

            .project-grid,
            .activity-grid {
                grid-template-columns: 1fr;
            }

            .competency-grid {
                grid-template-columns: 1fr;
            }

            .work-process {
                grid-template-columns: 1fr;
            }

            .lifecycle {
                grid-template-columns: repeat(2, 1fr);
            }

            .life-step::after {
                display: none !important;
            }

            .sitemap-grid {
                grid-template-columns: 1fr 1fr;
            }

            .footer-inner {
                flex-direction: column;
                gap: 5px;
            }
        }

    </style>
</head>


<body>


<!-- =========================================================
     HEADER
========================================================= -->

<header>

    <div class="container nav">

        <a href="#home" class="logo">
            SOHYUN PARK
            <span>R&D PLANNING PORTFOLIO</span>
        </a>

        <nav class="nav-links">

            <a href="#about">ABOUT</a>

            <a href="#experience">EXPERIENCE</a>

            <a href="#competencies">COMPETENCIES</a>

            <a href="#project">PROJECT</a>

            <a href="#sitemap" class="nav-cta">SITEMAP</a>

        </nav>

    </div>

</header>



<!-- =========================================================
     HERO
========================================================= -->

<section class="hero" id="home">

    <div class="container">

        <div class="hero-content">

            <div class="hero-label">
                LIG D&A · R&D PLANNING
            </div>

            <h1>
                기술과 사업을 연결하고<br>
                <span>R&D 과제를 구조화하는</span><br>
                연구기획 인재, 박소현입니다.
            </h1>

            <p class="hero-description">

                한국연구재단에서 <strong>R&D 과제관리와 기술기획</strong>을,
                CS Energy에서 <strong>신재생에너지 사업성 검토와 글로벌 시장분석</strong>을
                경험했습니다.

                <br><br>

                복잡한 정보를 구조화하고,
                기준을 세워 우선순위를 정하며,
                과제의 시작부터 후속조치까지 연결하는 방식으로 일합니다.

            </p>

            <div class="hero-buttons">

                <a href="#project" class="btn btn-primary">
                    VIEW PROJECTS →
                </a>

                <a href="#competencies" class="btn btn-outline">
                    CORE COMPETENCIES
                </a>

            </div>


            <div class="hero-keywords">

                <div class="keyword">
                    PROJECT MANAGEMENT
                </div>

                <div class="keyword">
                    TECHNOLOGY PLANNING
                </div>

                <div class="keyword">
                    BUSINESS ANALYSIS
                </div>

                <div class="keyword">
                    GLOBAL RESEARCH
                </div>

                <div class="keyword">
                    COMMUNICATION
                </div>

            </div>

        </div>

    </div>

</section>



<!-- =========================================================
     ABOUT
========================================================= -->

<section id="about">

    <div class="container">

        <div class="section-header">

            <div class="section-number">
                01 · ABOUT ME
            </div>

            <h2 class="section-title">
                경험의 흐름
            </h2>

            <p class="section-description">
                소재 연구에서 시작해 신재생에너지 사업개발,
                국가 R&D 과제관리까지 경험의 범위를 넓혀왔습니다.
            </p>

        </div>


        <div class="profile-intro">

            <div>

                <h3 class="profile-title">

                    기술을 이해하고,<br>
                    데이터를 구조화하고,<br>
                    <span>과제를 끝까지 관리합니다.</span>

                </h3>

            </div>


            <div>

                <p class="profile-text">

                    재료공학을 전공하며 소재의 구조와 물성에 대한
                    기술적 기반을 쌓았습니다.

                    <br><br>

                    이후 CS Energy에서 미국 신재생에너지 사업개발을 경험하며
                    기술·시장·규제 정보를 바탕으로 사업성을 검토했습니다.

                    <br><br>

                    현재는 한국연구재단에서 국가 R&D 사업의
                    선정·평가·협약·성과관리와 기술기획 업무를 경험하며
                    <strong>연구개발의 전체 흐름을 관리하는 역량</strong>을
                    쌓고 있습니다.

                </p>

            </div>

        </div>


        <!-- Timeline -->

        <div class="timeline">


            <div class="timeline-item">

                <div class="timeline-dot"></div>

                <div class="timeline-date">
                    2026.04 — 2026.08
                </div>

                <div class="timeline-title">
                    한국연구재단
                </div>

                <div class="timeline-subtitle">
                    국가전략본부 거대인프라방사선단 · 인턴
                </div>

                <div class="timeline-tags">

                    <span class="timeline-tag">
                        R&D Project Management
                    </span>

                    <span class="timeline-tag">
                        Technology Planning
                    </span>

                    <span class="timeline-tag">
                        Evaluation
                    </span>

                </div>

            </div>


            <div class="timeline-item">

                <div class="timeline-dot"></div>

                <div class="timeline-date">
                    2026.01 — 2026.03
                </div>

                <div class="timeline-title">
                    CS Energy
                </div>

                <div class="timeline-subtitle">
                    미주지역 태양광 사업개발부 · 인턴
                </div>

                <div class="timeline-tags">

                    <span class="timeline-tag">
                        Renewable Energy
                    </span>

                    <span class="timeline-tag">
                        Business Development
                    </span>

                    <span class="timeline-tag">
                        Market Analysis
                    </span>

                </div>

            </div>


            <div class="timeline-item">

                <div class="timeline-dot"></div>

                <div class="timeline-date">
                    2024.07 — 2024.08
                </div>

                <div class="timeline-title">
                    충남대학교 김병관 교수 연구실
                </div>

                <div class="timeline-subtitle">
                    학부연구생 · 열전소재 연구
                </div>

                <div class="timeline-tags">

                    <span class="timeline-tag">
                        Materials Research
                    </span>

                    <span class="timeline-tag">
                        Data Analysis
                    </span>

                    <span class="timeline-tag">
                        Experiment Design
                    </span>

                </div>

            </div>


            <div class="timeline-item">

                <div class="timeline-dot"></div>

                <div class="timeline-date">
                    2023.01 — 2023.12
                </div>

                <div class="timeline-title">
                    충남대학교 공과대학 학생회 '이온'
                </div>

                <div class="timeline-subtitle">
                    홍보국 차장
                </div>

                <div class="timeline-tags">

                    <span class="timeline-tag">
                        Communication
                    </span>

                    <span class="timeline-tag">
                        Event Planning
                    </span>

                </div>

            </div>


            <div class="timeline-item">

                <div class="timeline-dot"></div>

                <div class="timeline-date">
                    2023.05 — 2023.07
                </div>

                <div class="timeline-title">
                    Tetra Pak Eco Supporters
                </div>

                <div class="timeline-subtitle">
                    에코 서포터즈
                </div>

                <div class="timeline-tags">

                    <span class="timeline-tag">
                        Content Planning
                    </span>

                    <span class="timeline-tag">
                        ESG
                    </span>

                </div>

            </div>


            <div class="timeline-item">

                <div class="timeline-dot"></div>

                <div class="timeline-date">
                    2022.06 — 2022.11
                </div>

                <div class="timeline-title">
                    한국원자력연구원
                </div>

                <div class="timeline-subtitle">
                    안전문화 서포터즈
                </div>

                <div class="timeline-tags">

                    <span class="timeline-tag">
                        Technical Communication
                    </span>

                    <span class="timeline-tag">
                        Nuclear Safety
                    </span>

                </div>

            </div>


        </div>

    </div>

</section>



<!-- =========================================================
     EXPERIENCE
========================================================= -->

<section id="experience">

    <div class="container">

        <div class="section-header">

            <div class="section-number">
                02 · EXPERIENCE
            </div>

            <h2 class="section-title">
                주요 경험
            </h2>

            <p class="section-description">
                업무의 역할뿐 아니라 실제 결과와 그 경험에서 얻은
                직무적 인사이트를 함께 정리했습니다.
            </p>

        </div>


        <!-- Tabs -->

        <div class="experience-tabs">

            <button
                class="experience-tab active"
                onclick="showExperience('nrf', this)">
                한국연구재단
            </button>

            <button
                class="experience-tab"
                onclick="showExperience('cs', this)">
                CS Energy
            </button>

            <button
                class="experience-tab"
                onclick="showExperience('lab', this)">
                연구실
            </button>

            <button
                class="experience-tab"
                onclick="showExperience('student', this)">
                학생회
            </button>

            <button
                class="experience-tab"
                onclick="showExperience('external', this)">
                대외활동
            </button>

        </div>



        <!-- NRF -->

        <div id="nrf" class="experience-content active">

            <div class="experience-grid">

                <div class="experience-main">

                    <div class="experience-heading">

                        <div>

                            <h3 class="experience-company">
                                한국연구재단
                            </h3>

                            <div class="experience-position">
                                국가전략본부 거대인프라방사선단 · 인턴
                            </div>

                        </div>

                        <div class="experience-period">
                            2026.04 — 2026.08
                        </div>

                    </div>


                    <div class="content-label">
                        KEY RESPONSIBILITIES
                    </div>

                    <ul class="experience-list">

                        <li>
                            연구과제 진행 현황 및 업무 히스토리 리스트업,
                            향후 과제 추진계획 수립
                        </li>

                        <li>
                            원자력정책연구사업 사업관리
                        </li>

                        <li>
                            과학기술분야 연구기획과제 사업관리
                        </li>

                        <li>
                            국가비즈니스벨트거점 인프라구축 사업업무
                        </li>

                        <li>
                            방사선 이종접합소재(접착제) RFP 기획 및 검토
                        </li>

                        <li>
                            국가연구개발혁신법 및 사업관리 규정 검토
                        </li>

                        <li>
                            연구책임자 및 과학기술정보통신부 민원·문의사항 대응
                        </li>

                    </ul>


                    <div class="content-label">
                        ADDITIONAL WORK
                    </div>

                    <ul class="experience-list">

                        <li>협약변경 검토 및 검토결과 알림 공문 작성</li>

                        <li>과제 정리 및 인수인계 업무</li>

                        <li>요건검토 및 RFP 기획</li>

                        <li>공개용 최종보고서 제출 및 IRIS 일괄 접수</li>

                        <li>방사선진흥종합계획 수립 회의 준비</li>

                        <li>직접비·간접비 검토</li>

                        <li>후보자 및 평가위원 섭외</li>

                        <li>자문료·출장여비·업추비 등 행정업무</li>

                        <li>선정 및 최종평가 예산 계상</li>

                        <li>PO 역량강화 관련 자료 조사</li>

                    </ul>


                    <div class="achievement-box">

                        <div class="content-label">
                            KEY ACHIEVEMENTS
                        </div>

                        <ul class="experience-list">

                            <li>
                                방사선 이종접합소재 RFP 기획안 최종 수정 및 사업공고
                            </li>

                            <li>
                                원자력정책연구사업 총 8건 선정·최종평가 및 결과안 도출
                            </li>

                            <li>
                                인프라구축 사업 최종평가 결과 정리 및 과기부 보고
                            </li>

                            <li>
                                과학기술분야 연구기획과제 1건 선정·기획 및 결과안 보고
                            </li>

                        </ul>

                    </div>


                    <div class="takeaway">

                        <div class="content-label">
                            KEY TAKEAWAY
                        </div>

                        <p>
                            R&D 과제관리는 단순한 일정 관리가 아니라
                            규정·평가·예산·성과를 연결하여 과제의 전체 흐름을
                            관리하는 업무임을 경험했습니다.
                        </p>

                    </div>

                </div>


                <div class="experience-side">

                    <div class="content-label">
                        EXPERIENCE METRICS
                    </div>

                    <div class="metric">

                        <div class="metric-number">
                            8
                        </div>

                        <div class="metric-label">
                            원자력정책연구사업 선정·최종평가 과제
                        </div>

                    </div>

                    <div class="metric">

                        <div class="metric-number">
                            1
                        </div>

                        <div class="metric-label">
                            방사선 이종접합소재 RFP 기획
                        </div>

                    </div>

                    <div class="metric">

                        <div class="metric-number">
                            1
                        </div>

                        <div class="metric-label">
                            연구기획과제 선정·기획
                        </div>

                    </div>


                    <!-- 이미지 삽입 위치 -->

                    <div class="image-placeholder">

                        NRF 업무 / 회의 / 결과물 이미지<br>
                        <small>
                            images/nrf.jpg
                        </small>

                    </div>

                </div>

            </div>


            <!-- R&D Lifecycle -->

            <div class="lifecycle">

                <div class="life-step">

                    <div class="life-number">01</div>

                    <div class="life-title">
                        기획
                    </div>

                    <div class="life-desc">
                        기술·사업목표
                    </div>

                </div>

                <div class="life-step">

                    <div class="life-number">02</div>

                    <div class="life-title">
                        선정
                    </div>

                    <div class="life-desc">
                        평가위원·평가
                    </div>

                </div>

                <div class="life-step">

                    <div class="life-number">03</div>

                    <div class="life-title">
                        협약
                    </div>

                    <div class="life-desc">
                        협약·예산
                    </div>

                </div>

                <div class="life-step">

                    <div class="life-number">04</div>

                    <div class="life-title">
                        수행
                    </div>

                    <div class="life-desc">
                        진행상황 관리
                    </div>

                </div>

                <div class="life-step">

                    <div class="life-number">05</div>

                    <div class="life-title">
                        평가
                    </div>

                    <div class="life-desc">
                        결과·보완
                    </div>

                </div>

                <div class="life-step">

                    <div class="life-number">06</div>

                    <div class="life-title">
                        후속관리
                    </div>

                    <div class="life-desc">
                        결과보고·성과
                    </div>

                </div>

            </div>

        </div>



        <!-- CS ENERGY -->

        <div id="cs" class="experience-content">

            <div class="experience-grid">

                <div class="experience-main">

                    <div class="experience-heading">

                        <div>

                            <h3 class="experience-company">
                                CS Energy
                            </h3>

                            <div class="experience-position">
                                미주지역 태양광 사업개발부 · 인턴
                            </div>

                        </div>

                        <div class="experience-period">
                            2026.01 — 2026.03
                        </div>

                    </div>


                    <div class="content-label">
                        KEY RESPONSIBILITIES
                    </div>

                    <ul class="experience-list">

                        <li>
                            미국 신재생에너지 프로젝트 개발 프로세스 지원
                        </li>

                        <li>
                            PVcase를 활용한 주요 State 개발 안건 부지 스크리닝
                        </li>

                        <li>
                            미국 신재생에너지 법안 동향 모니터링 및 DB 구축
                        </li>

                        <li>
                            계통여유·지가 등 기준에 따른 태양광 부지 스크리닝
                        </li>

                        <li>
                            BESS 전력 트레이딩 및 세제혜택 검토
                        </li>

                    </ul>


                    <div class="achievement-box">

                        <div class="content-label">
                            KEY ACHIEVEMENTS
                        </div>

                        <ul class="experience-list">

                            <li>
                                미국 태양광 부지 후보지 트래커 2건 구축
                            </li>

                            <li>
                                트래커별 10개 후보지 발굴
                            </li>

                            <li>
                                미국 전력시장 구조 및 전력수익·계약구조 보고서 작성·발표
                            </li>

                            <li>
                                MISO 계통 스터디 프로세스 분석 및 도식화
                            </li>

                            <li>
                                Illinois State 법안동향 DB 구축 및 사업성 검토
                            </li>

                        </ul>

                    </div>


                    <div class="takeaway">

                        <div class="content-label">
                            KEY TAKEAWAY
                        </div>

                        <p>
                            사업성 검토에서는 모든 조건을 동일하게 보는 것보다
                            핵심 기준을 먼저 정의하고 정보를 구조화하여
                            의사결정에 필요한 정보를 빠르게 만드는 것이 중요하다는 점을 배웠습니다.
                        </p>

                    </div>

                </div>


                <div class="experience-side">

                    <div class="content-label">
                        EXPERIENCE METRICS
                    </div>

                    <div class="metric">

                        <div class="metric-number">
                            20+
                        </div>

                        <div class="metric-label">
                            태양광 후보지 검토
                        </div>

                    </div>

                    <div class="metric">

                        <div class="metric-number">
                            2
                        </div>

                        <div class="metric-label">
                            Site Screening Tracker
                        </div>

                    </div>

                    <div class="metric">

                        <div class="metric-number">
                            1
                        </div>

                        <div class="metric-label">
                            미국 State Policy Database
                        </div>

                    </div>


                    <div class="image-placeholder">

                        CS Energy / Tracker / 미국 지도 이미지<br>

                        <small>
                            images/cs-energy.jpg
                        </small>

                    </div>

                </div>

            </div>

        </div>



        <!-- LAB -->

        <div id="lab" class="experience-content">

            <div class="experience-grid">

                <div class="experience-main">

                    <div class="experience-heading">

                        <div>

                            <h3 class="experience-company">
                                충남대학교 연구실
                            </h3>

                            <div class="experience-position">
                                김병관 교수 연구실 · 학부연구생
                            </div>

                        </div>

                        <div class="experience-period">
                            2024.07 — 2024.08
                        </div>

                    </div>


                    <div class="content-label">
                        KEY RESPONSIBILITIES
                    </div>

                    <ul class="experience-list">

                        <li>
                            바이오 폴리머 기반 열전소재의 합성조건·조성비·열전특성 데이터 표 구축
                        </li>

                        <li>
                            우수 소재의 물성 분석 및 무기 열전소재와 비교
                        </li>

                        <li>
                            TOBC 및 [EMIM][DCA] 소재 선정 및 실험 설계
                        </li>

                        <li>
                            연구 세미나를 통한 실험설계안 공유 및 연구방향성 수립
                        </li>

                    </ul>


                    <div class="achievement-box">

                        <div class="content-label">
                            KEY ACHIEVEMENT
                        </div>

                        <ul class="experience-list">

                            <li>
                                Bacterial Cellulose 기반 TOBC 및 [EMIM][DCA]
                                복합체 합성을 통한 열전연구 진행
                            </li>

                            <li>
                                문헌 데이터를 기준에 따라 정리하여 소재별 특성 비교
                            </li>

                        </ul>

                    </div>


                    <div class="takeaway">

                        <div class="content-label">
                            KEY TAKEAWAY
                        </div>

                        <p>
                            기술을 이해하기 위해서는 개별적인 수치보다
                            소재 조성·공정조건·구조·물성 간의 관계를
                            체계적으로 비교하는 것이 중요하다는 것을 경험했습니다.
                        </p>

                    </div>

                </div>


                <div class="experience-side">

                    <div class="content-label">
                        RESEARCH
                    </div>

                    <div class="metric">

                        <div class="metric-number">
                            50+
                        </div>

                        <div class="metric-label">
                            문헌 데이터 분석
                        </div>

                    </div>

                    <div class="metric">

                        <div class="metric-number">
                            2
                        </div>

                        <div class="metric-label">
                            주요 소재 시스템
                        </div>

                    </div>


                    <div class="image-placeholder">

                        실험 / 연구 포스터 / 데이터 이미지<br>

                        <small>
                            images/lab.jpg
                        </small>

                    </div>

                </div>

            </div>

        </div>



        <!-- STUDENT -->

        <div id="student" class="experience-content">

            <div class="experience-grid">

                <div class="experience-main">

                    <div class="experience-heading">

                        <div>

                            <h3 class="experience-company">
                                충남대학교 공과대학 학생회 '이온'
                            </h3>

                            <div class="experience-position">
                                홍보국 차장
                            </div>

                        </div>

                        <div class="experience-period">
                            2023.01 — 2023.12
                        </div>

                    </div>


                    <ul class="experience-list">

                        <li>
                            공과대학 축제·벼룩시장 등 주요 행사 홍보물 제작
                        </li>

                        <li>
                            SNS 채널 운영 및 콘텐츠 관리
                        </li>

                        <li>
                            정기 회의록 작성 및 감사자료 정리
                        </li>

                        <li>
                            성년의 날 영화제 및 공과대학 축제 기획·운영 지원
                        </li>

                    </ul>


                    <div class="takeaway">

                        <div class="content-label">
                            KEY TAKEAWAY
                        </div>

                        <p>
                            다양한 구성원이 참여하는 조직에서
                            정보를 명확하게 전달하고 공동의 목표를 위해
                            역할을 조율하는 경험을 쌓았습니다.
                        </p>

                    </div>

                </div>


                <div class="experience-side">

                    <div class="content-label">
                        CORE SKILLS
                    </div>

                    <div class="metric">

                        <div class="metric-number">
                            1
                        </div>

                        <div class="metric-label">
                            홍보국 차장
                        </div>

                    </div>

                    <div class="metric">

                        <div class="metric-number">
                            2+
                        </div>

                        <div class="metric-label">
                            주요 대규모 행사
                        </div>

                    </div>

                    <div class="image-placeholder">

                        학생회 행사 이미지<br>

                        <small>
                            images/student-council.jpg
                        </small>

                    </div>

                </div>

            </div>

        </div>



        <!-- EXTERNAL -->

        <div id="external" class="experience-content">

            <div class="activity-grid">

                <div class="activity-card">

                    <h3>
                        Tetra Pak Eco Supporters
                    </h3>

                    <div class="activity-period">
                        2023.05 — 2023.07
                    </div>

                    <p>
                        환경보호 테마 UCC 영상 기획 및 편집 총괄.
                        팀 미션 우수상 수상.
                        인포그래픽·카드뉴스 기반 콘텐츠 8개 제작.
                    </p>

                </div>


                <div class="activity-card">

                    <h3>
                        KAERI 안전문화 서포터즈
                    </h3>

                    <div class="activity-period">
                        2022.06 — 2022.11
                    </div>

                    <p>
                        방사성 요오드 흡착제 연구논문 및 보도자료를 기반으로
                        카드뉴스 6건 제작.
                        원자력 안전·방사선 방호 관련 블로그 운영.
                        최종 활동 평가 최우수상 수상.
                    </p>

                </div>

            </div>

        </div>

    </div>

</section>



<!-- =========================================================
     COMPETENCIES
========================================================= -->

<section id="competencies">

    <div class="container">

        <div class="section-header">

            <div class="section-number">
                03 · CORE COMPETENCIES
            </div>

            <h2 class="section-title">
                제가 일하는 방식과 역량
            </h2>

            <p class="section-description">
                추상적인 역량보다 실제 경험과 결과물을 기반으로
                제가 수행할 수 있는 업무를 보여드립니다.
            </p>

        </div>


        <div class="competency-grid">


            <div class="competency-card">

                <div class="competency-icon">
                    01
                </div>

                <h3>
                    과제관리
                </h3>

                <p>
                    R&D 과제의 진행상황,
                    평가·협약·결과보고 등
                    업무 흐름을 구조화합니다.
                </p>

                <div class="competency-evidence">
                    NRF · 8개 과제 선정/최종평가
                </div>

            </div>


            <div class="competency-card">

                <div class="competency-icon">
                    02
                </div>

                <h3>
                    기술기획
                </h3>

                <p>
                    기술을 사전 학습하고
                    연구목표·내용·성과기준을 검토하여
                    기획에 반영합니다.
                </p>

                <div class="competency-evidence">
                    NRF · 방사선 이종접합소재 RFP
                </div>

            </div>


            <div class="competency-card">

                <div class="competency-icon">
                    03
                </div>

                <h3>
                    사업성 검토
                </h3>

                <p>
                    기술·시장·계통·규제 정보를
                    기준에 따라 비교하고
                    사업 후보지를 선별합니다.
                </p>

                <div class="competency-evidence">
                    CS Energy · Solar Site Screening
                </div>

            </div>


            <div class="competency-card">

                <div class="competency-icon">
                    04
                </div>

                <h3>
                    글로벌 리서치
                </h3>

                <p>
                    해외 정책·법안·시장자료를
                    조사하고 업무에 활용할 수 있도록
                    데이터화합니다.
                </p>

                <div class="competency-evidence">
                    CS Energy · U.S. Policy DB
                </div>

            </div>


            <div class="competency-card">

                <div class="competency-icon">
                    05
                </div>

                <h3>
                    협업·커뮤니케이션
                </h3>

                <p>
                    관계자의 요구사항을 파악하고
                    필요한 정보를 명확하게 정리하여
                    공동의 목표를 달성합니다.
                </p>

                <div class="competency-evidence">
                    NRF · 학생회 · 대외활동
                </div>

            </div>


        </div>

    </div>

</section>



<!-- =========================================================
     HOW I WORK
========================================================= -->

<section>

    <div class="container">

        <div class="section-header">

            <div class="section-number">
                04 · HOW I WORK
            </div>

            <h2 class="section-title">
                문제를 해결하는 5단계
            </h2>

            <p class="section-description">
                새로운 업무를 맡았을 때 제가 가장 중요하게 생각하는
                업무 접근 방식입니다.
            </p>

        </div>


        <div class="work-process">


            <div class="work-card">

                <div class="work-card-number">
                    STEP 01
                </div>

                <h3>
                    Understand
                </h3>

                <p>
                    업무의 목적과
                    판단 기준부터 파악합니다.
                </p>

            </div>


            <div class="work-card">

                <div class="work-card-number">
                    STEP 02
                </div>

                <h3>
                    Structure
                </h3>

                <p>
                    복잡한 정보를
                    목적에 맞게 구조화합니다.
                </p>

            </div>


            <div class="work-card">

                <div class="work-card-number">
                    STEP 03
                </div>

                <h3>
                    Prioritize
                </h3>

                <p>
                    중요도에 따라
                    검토순서와 자원을 배분합니다.
                </p>

            </div>


            <div class="work-card">

                <div class="work-card-number">
                    STEP 04
                </div>

                <h3>
                    Coordinate
                </h3>

                <p>
                    관계자와 기준을 공유하고
                    의견을 조율합니다.
                </p>

            </div>


            <div class="work-card">

                <div class="work-card-number">
                    STEP 05
                </div>

                <h3>
                    Follow-up
                </h3>

                <p>
                    결과에서 끝내지 않고
                    후속조치까지 관리합니다.
                </p>

            </div>


        </div>

    </div>

</section>



<!-- =========================================================
     PROJECT
========================================================= -->

<section id="project">

    <div class="container">

        <div class="section-header">

            <div class="section-number">
                05 · PROJECT
            </div>

            <h2 class="section-title">
                Selected Projects
            </h2>

            <p class="section-description">
                경험을 단순히 나열하는 대신,
                연구기획 직무와 직접 연결되는 프로젝트를 중심으로 정리했습니다.
            </p>

        </div>


        <div class="project-grid">


            <!-- Project 01 -->

            <div class="project-card">

                <div class="project-image">

                    <!-- 실제 이미지 사용 시 -->
                    <!--
                    <img src="images/rfp.jpg"
                         alt="방사선 이종접합소재 RFP 기획">
                    -->

                    RFP PLANNING
                </div>

                <div class="project-body">

                    <div class="project-category">
                        TECHNOLOGY PLANNING
                    </div>

                    <h3 class="project-title">
                        방사선 이종접합소재 RFP 기획
                    </h3>

                    <p class="project-desc">
                        기술내용을 사전 학습하고 연구목표,
                        연구내용 및 성과기준을 검토하여
                        전문가 기획회의와 수정과정을 거쳐
                        RFP 완성에 참여했습니다.
                    </p>

                    <div class="project-result">
                        RESULT · RFP 최종안 완성 및 사업공고
                    </div>

                </div>

            </div>



            <!-- Project 02 -->

            <div class="project-card">

                <div class="project-image">

                    R&D PROJECT MANAGEMENT

                </div>

                <div class="project-body">

                    <div class="project-category">
                        PROJECT MANAGEMENT
                    </div>

                    <h3 class="project-title">
                        R&D 선정·최종평가 관리
                    </h3>

                    <p class="project-desc">
                        연구과제 진행현황과 업무 히스토리를 관리하고
                        평가계획·위원 섭외·평가결과·후속조치 등
                        과제의 전체 흐름을 관리했습니다.
                    </p>

                    <div class="project-result">
                        RESULT · 원자력정책연구사업 8건 관리
                    </div>

                </div>

            </div>



            <!-- Project 03 -->

            <div class="project-card">

                <div class="project-image">

                    U.S. SOLAR SITE SCREENING

                </div>

                <div class="project-body">

                    <div class="project-category">
                        BUSINESS ANALYSIS
                    </div>

                    <h3 class="project-title">
                        미국 태양광 부지 스크리닝
                    </h3>

                    <p class="project-desc">
                        토지·계통·환경·규제 등 사업성 검토요소를
                        기준화하고 PVcase 및 다양한 자료를 활용해
                        미국 태양광 후보지를 검토했습니다.
                    </p>

                    <div class="project-result">
                        RESULT · Tracker 2건 / 후보지 20건+
                    </div>

                </div>

            </div>



            <!-- Project 04 -->

            <div class="project-card">

                <div class="project-image">

                    THERMOELECTRIC MATERIALS

                </div>

                <div class="project-body">

                    <div class="project-category">
                        TECHNOLOGY ANALYSIS
                    </div>

                    <h3 class="project-title">
                        바이오 폴리머 열전소재 데이터 분석
                    </h3>

                    <p class="project-desc">
                        다양한 문헌에서 소재의 조성·합성조건·
                        열전특성 데이터를 구조화하고
                        소재별 특성을 비교하여 실험 설계에 활용했습니다.
                    </p>

                    <div class="project-result">
                        RESULT · 50+ 문헌 데이터 구조화
                    </div>

                </div>

            </div>


        </div>



        <!-- Case Study -->

        <div class="case-study">

            <div class="case-header">

                <div>

                    <div class="content-label">
                        FEATURED CASE
                    </div>

                    <h3 class="case-title">
                        R&D 과제관리 경험에서 배운 것
                    </h3>

                </div>

                <div class="case-role">
                    PROJECT MANAGEMENT
                </div>

            </div>


            <div class="case-columns">


                <div class="case-box">

                    <h4>
                        CHALLENGE
                    </h4>

                    <p>
                        여러 과제의 진행상황,
                        평가 일정, 결과보고 및
                        후속업무를 동시에 관리해야 했습니다.
                    </p>

                </div>


                <div class="case-box">

                    <h4>
                        ACTION
                    </h4>

                    <p>
                        과제별 업무 히스토리를 정리하고
                        현재 진행단계와 향후 추진업무를
                        구분하여 관리했습니다.
                    </p>

                </div>


                <div class="case-box">

                    <h4>
                        RESULT
                    </h4>

                    <p>
                        원자력정책연구사업 8건의
                        선정·최종평가 및 결과보고 업무를
                        체계적으로 수행했습니다.
                    </p>

                </div>


            </div>

        </div>

    </div>

</section>



<!-- =========================================================
     ADDITIONAL ACTIVITIES
========================================================= -->

<section>

    <div class="container">

        <div class="section-header">

            <div class="section-number">
                06 · ADDITIONAL EXPERIENCE
            </div>

            <h2 class="section-title">
                기술을 전달하는 경험
            </h2>

            <p class="section-description">
                기술적 내용을 이해하는 것에서 나아가,
                상대방에게 쉽게 전달하고 콘텐츠로 구조화하는 경험을 쌓았습니다.
            </p>

        </div>


        <div class="activity-grid">


            <div class="activity-card">

                <h3>
                    Tetra Pak Eco Supporters
                </h3>

                <div class="activity-period">
                    2023.05 — 2023.07
                </div>

                <p>
                    환경보호 테마 UCC 기획·편집 총괄.
                    인포그래픽 및 카드뉴스 8개 제작.
                    팀 미션 우수상 수상.
                </p>

            </div>


            <div class="activity-card">

                <h3>
                    KAERI 안전문화 서포터즈
                </h3>

                <div class="activity-period">
                    2022.06 — 2022.11
                </div>

                <p>
                    연구논문과 보도자료를 기반으로
                    원자력 안전 및 방사선 방호 관련 콘텐츠 제작.
                    최종 활동 평가 최우수상 수상.
                </p>

            </div>


        </div>

    </div>

</section>



<!-- =========================================================
     SITEMAP
========================================================= -->

<section class="sitemap" id="sitemap">

    <div class="container">

        <div class="sitemap-title">
            SITEMAP
        </div>


        <div class="sitemap-grid">


            <div class="sitemap-column">

                <h3>
                    ABOUT
                </h3>

                <a href="#home">
                    Home
                </a>

                <a href="#about">
                    Profile
                </a>

                <a href="#about">
                    Career Timeline
                </a>

            </div>


            <div class="sitemap-column">

                <h3>
                    EXPERIENCE
                </h3>

                <a href="#experience">
                    한국연구재단
                </a>

                <a href="#experience">
                    CS Energy
                </a>

                <a href="#experience">
                    Research Lab
                </a>

                <a href="#experience">
                    Student Council
                </a>

            </div>


            <div class="sitemap-column">

                <h3>
                    COMPETENCIES
                </h3>

                <a href="#competencies">
                    Project Management
                </a>

                <a href="#competencies">
                    Technology Planning
                </a>

                <a href="#competencies">
                    Business Analysis
                </a>

                <a href="#competencies">
                    Global Research
                </a>

                <a href="#competencies">
                    Communication
                </a>

            </div>


            <div class="sitemap-column">

                <h3>
                    PROJECT
                </h3>

                <a href="#project">
                    R&D Project Management
                </a>

                <a href="#project">
                    RFP Planning
                </a>

                <a href="#project">
                    U.S. Solar Site Screening
                </a>

                <a href="#project">
                    Thermoelectric Materials
                </a>

            </div>


        </div>

    </div>

</section>



<!-- =========================================================
     FOOTER
========================================================= -->

<footer>

    <div class="container footer-inner">

        <div>
            © 2026 PARK SOHYUN
        </div>

        <div>
            R&D PLANNING PORTFOLIO
        </div>

    </div>

</footer>



<!-- =========================================================
     JAVASCRIPT
========================================================= -->

<script>

    /*
     * EXPERIENCE TAB
     */

    function showExperience(id, button) {

        const contents =
            document.querySelectorAll(".experience-content");

        const tabs =
            document.querySelectorAll(".experience-tab");


        contents.forEach(content => {

            content.classList.remove("active");

        });


        tabs.forEach(tab => {

            tab.classList.remove("active");

        });


        document.getElementById(id)
            .classList.add("active");

        button.classList.add("active");

    }



    /*
     * HEADER SCROLL EFFECT
     */

    window.addEventListener("scroll", function() {

        const header =
            document.querySelector("header");

        if (window.scrollY > 30) {

            header.style.boxShadow =
                "0 5px 20px rgba(11,31,58,0.06)";

        } else {

            header.style.boxShadow = "none";

        }

    });



    /*
     * INTERSECTION ANIMATION
     */

    const observer =
        new IntersectionObserver(
            (entries) => {

                entries.forEach(entry => {

                    if (entry.isIntersecting) {

                        entry.target.style.opacity = "1";

                        entry.target.style.transform =
                            "translateY(0)";

                    }

                });

            },
            {
                threshold: 0.08
            }
        );


    document
        .querySelectorAll(
            ".project-card, .competency-card, .work-card, .activity-card"
        )
        .forEach(el => {

            el.style.opacity = "0";

            el.style.transform = "translateY(20px)";

            el.style.transition =
                "opacity 0.6s ease, transform 0.6s ease";

            observer.observe(el);

        });

</script>


</body>
</html>
