<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">

    <meta
        name="viewport"
        content="width=device-width, initial-scale=1.0"
    >

    <meta
        name="description"
        content="SP Artistry offers premium bridal makeup, HD makeup, airbrush makeup, hairstyling and saree draping services in Chennai."
    >

    <title>SP Artistry | Premium Bridal Makeup Artist in Chennai</title>

    <!-- Google Fonts -->
    <link
        rel="preconnect"
        href="https://fonts.googleapis.com"
    >

    <link
        rel="preconnect"
        href="https://fonts.gstatic.com"
        crossorigin
    >

    <link
        href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:wght@500;600;700&family=Montserrat:wght@300;400;500;600;700&display=swap"
        rel="stylesheet"
    >

    <!-- Font Awesome -->
    <link
        rel="stylesheet"
        href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.7.2/css/all.min.css"
    >

    <style>
        :root {
            --primary: #7a294d;
            --primary-dark: #4b1530;
            --secondary: #b76e79;
            --gold: #caa45d;
            --gold-light: #ead5a4;
            --cream: #fffaf5;
            --soft-pink: #f9eef1;
            --white: #ffffff;
            --dark: #25171e;
            --text: #5c4b53;
            --border: rgba(183, 110, 121, 0.18);
            --shadow: 0 20px 55px rgba(73, 29, 49, 0.12);
            --transition: 0.4s ease;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
            scroll-padding-top: 90px;
        }

        body {
            font-family: "Montserrat", sans-serif;
            background: var(--cream);
            color: var(--text);
            line-height: 1.75;
            overflow-x: hidden;
        }

        body.menu-open {
            overflow: hidden;
        }

        img {
            width: 100%;
            display: block;
        }

        a {
            text-decoration: none;
            color: inherit;
        }

        ul {
            list-style: none;
        }

        button,
        input,
        textarea,
        select {
            font: inherit;
        }

        .container {
            width: min(1180px, 90%);
            margin: auto;
        }

        .section {
            position: relative;
            padding: 110px 0;
            overflow: hidden;
        }

        .section-light {
            background: var(--white);
        }

        .section-soft {
            background:
                radial-gradient(
                    circle at top left,
                    rgba(202, 164, 93, 0.12),
                    transparent 30%
                ),
                var(--soft-pink);
        }

        .section-heading {
            max-width: 720px;
            margin: 0 auto 60px;
            text-align: center;
        }

        .section-tag {
            display: inline-flex;
            align-items: center;
            gap: 10px;
            margin-bottom: 14px;
            color: var(--gold);
            font-size: 13px;
            font-weight: 700;
            letter-spacing: 3px;
            text-transform: uppercase;
        }

        .section-tag::before,
        .section-tag::after {
            content: "";
            width: 35px;
            height: 1px;
            background: var(--gold);
        }

        h1,
        h2,
        h3,
        h4 {
            font-family: "Cormorant Garamond", serif;
            color: var(--dark);
            line-height: 1.15;
        }

        .section-heading h2 {
            margin-bottom: 18px;
            font-size: clamp(42px, 5vw, 64px);
            font-weight: 700;
        }

        .section-heading p {
            max-width: 620px;
            margin: auto;
            color: #75646d;
            font-size: 16px;
        }

        .gold-text {
            color: var(--gold);
        }

        .btn {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            gap: 11px;
            min-height: 56px;
            padding: 14px 30px;
            border: 1px solid transparent;
            border-radius: 50px;
            font-size: 14px;
            font-weight: 700;
            letter-spacing: 0.4px;
            cursor: pointer;
            transition: var(--transition);
        }

        .btn-primary {
            color: var(--white);
            background: linear-gradient(
                135deg,
                var(--primary),
                var(--secondary)
            );
            box-shadow: 0 14px 30px rgba(122, 41, 77, 0.25);
        }

        .btn-primary:hover {
            transform: translateY(-4px);
            box-shadow: 0 20px 38px rgba(122, 41, 77, 0.34);
        }

        .btn-outline {
            color: var(--white);
            border-color: rgba(255, 255, 255, 0.55);
            background: rgba(255, 255, 255, 0.08);
            backdrop-filter: blur(10px);
        }

        .btn-outline:hover {
            color: var(--primary-dark);
            background: var(--white);
            border-color: var(--white);
            transform: translateY(-4px);
        }

        /* Scroll Progress */

        .scroll-progress {
            position: fixed;
            top: 0;
            left: 0;
            z-index: 2000;
            width: 0%;
            height: 3px;
            background: linear-gradient(
                90deg,
                var(--gold),
                var(--secondary)
            );
        }

        /* Navigation */

        .navbar {
            position: fixed;
            top: 0;
            left: 0;
            z-index: 1000;
            width: 100%;
            padding: 20px 0;
            transition: var(--transition);
        }

        .navbar.scrolled {
            padding: 12px 0;
            background: rgba(255, 250, 245, 0.96);
            box-shadow: 0 10px 35px rgba(54, 26, 40, 0.09);
            backdrop-filter: blur(14px);
        }

        .nav-wrapper {
            display: flex;
            align-items: center;
            justify-content: space-between;
        }

        .logo {
            display: flex;
            flex-direction: column;
            color: var(--white);
            line-height: 1;
            transition: var(--transition);
        }

        .navbar.scrolled .logo {
            color: var(--primary-dark);
        }

        .logo-main {
            font-family: "Cormorant Garamond", serif;
            font-size: 31px;
            font-weight: 700;
            letter-spacing: 1px;
        }

        .logo-small {
            margin-top: 5px;
            color: var(--gold-light);
            font-size: 8px;
            font-weight: 700;
            letter-spacing: 4px;
            text-transform: uppercase;
        }

        .navbar.scrolled .logo-small {
            color: var(--gold);
        }

        .nav-links {
            display: flex;
            align-items: center;
            gap: 30px;
        }

        .nav-links a {
            position: relative;
            color: rgba(255, 255, 255, 0.9);
            font-size: 13px;
            font-weight: 600;
            transition: var(--transition);
        }

        .navbar.scrolled .nav-links a {
            color: var(--dark);
        }

        .nav-links a:not(.nav-booking)::after {
            content: "";
            position: absolute;
            left: 0;
            bottom: -7px;
            width: 0;
            height: 2px;
            background: var(--gold);
            transition: var(--transition);
        }

        .nav-links a:hover::after,
        .nav-links a.active::after {
            width: 100%;
        }

        .nav-booking {
            padding: 11px 20px;
            border: 1px solid rgba(255, 255, 255, 0.55);
            border-radius: 30px;
        }

        .navbar.scrolled .nav-booking {
            color: var(--white);
            border-color: var(--primary);
            background: var(--primary);
        }

        .nav-booking:hover {
            color: var(--primary-dark) !important;
            background: var(--white);
        }

        .navbar.scrolled .nav-booking:hover {
            color: var(--white) !important;
            background: var(--secondary);
            border-color: var(--secondary);
        }

        .menu-toggle {
            display: none;
            width: 46px;
            height: 46px;
            border: 1px solid rgba(255, 255, 255, 0.4);
            border-radius: 50%;
            color: var(--white);
            background: rgba(255, 255, 255, 0.08);
            cursor: pointer;
        }

        .navbar.scrolled .menu-toggle {
            color: var(--primary);
            border-color: var(--border);
            background: var(--white);
        }

        /* Hero */

        .hero {
            position: relative;
            min-height: 100vh;
            display: flex;
            align-items: center;
            color: var(--white);
            background:
                linear-gradient(
                    90deg,
                    rgba(49, 17, 35, 0.9) 0%,
                    rgba(73, 25, 48, 0.72) 45%,
                    rgba(49, 17, 35, 0.3) 100%
                ),
                url("images/hero.jpg") center/cover no-repeat;
            overflow: hidden;
        }

        .hero::before {
            content: "";
            position: absolute;
            inset: 0;
            background:
                radial-gradient(
                    circle at 78% 25%,
                    rgba(234, 213, 164, 0.24),
                    transparent 28%
                ),
                linear-gradient(
                    to top,
                    rgba(27, 10, 19, 0.52),
                    transparent 45%
                );
        }

        .hero::after {
            content: "";
            position: absolute;
            right: -140px;
            bottom: -180px;
            width: 480px;
            height: 480px;
            border: 1px solid rgba(234, 213, 164, 0.3);
            border-radius: 50%;
            box-shadow:
                0 0 0 55px rgba(234, 213, 164, 0.06),
                0 0 0 110px rgba(234, 213, 164, 0.04);
        }

        .hero-content {
            position: relative;
            z-index: 2;
            max-width: 760px;
            padding-top: 90px;
        }

        .hero-subtitle {
            display: flex;
            align-items: center;
            gap: 13px;
            margin-bottom: 20px;
            color: var(--gold-light);
            font-size: 12px;
            font-weight: 700;
            letter-spacing: 4px;
            text-transform: uppercase;
        }

        .hero-subtitle::before {
            content: "";
            width: 48px;
            height: 1px;
            background: var(--gold-light);
        }

        .hero h1 {
            margin-bottom: 22px;
            color: var(--white);
            font-size: clamp(62px, 8vw, 108px);
            font-weight: 700;
            letter-spacing: -2px;
        }

        .hero h1 span {
            display: block;
            color: var(--gold-light);
            font-size: 0.72em;
            font-style: italic;
        }

        .hero-description {
            max-width: 620px;
            margin-bottom: 34px;
            color: rgba(255, 255, 255, 0.82);
            font-size: clamp(16px, 2vw, 19px);
            font-weight: 300;
        }

        .hero-buttons {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
        }

        .hero-features {
            display: flex;
            flex-wrap: wrap;
            gap: 28px;
            margin-top: 44px;
        }

        .hero-feature {
            display: flex;
            align-items: center;
            gap: 10px;
            color: rgba(255, 255, 255, 0.86);
            font-size: 13px;
        }

        .hero-feature i {
            color: var(--gold-light);
        }

        .scroll-down {
            position: absolute;
            left: 50%;
            bottom: 28px;
            z-index: 3;
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 8px;
            color: rgba(255, 255, 255, 0.7);
            font-size: 9px;
            letter-spacing: 3px;
            text-transform: uppercase;
            transform: translateX(-50%);
        }

        .scroll-down i {
            font-size: 17px;
            animation: bounce 1.8s infinite;
        }

        @keyframes bounce {
            0%,
            100% {
                transform: translateY(0);
            }

            50% {
                transform: translateY(8px);
            }
        }

        /* About */

        .about-grid {
            display: grid;
            grid-template-columns: 0.95fr 1.05fr;
            gap: 80px;
            align-items: center;
        }

        .about-image-wrap {
            position: relative;
            padding: 0 35px 35px 0;
        }

        .about-main-image {
            position: relative;
            z-index: 2;
            height: 640px;
            border-radius: 220px 220px 25px 25px;
            object-fit: cover;
            box-shadow: var(--shadow);
        }

        .about-image-wrap::before {
            content: "";
            position: absolute;
            right: 0;
            bottom: 0;
            width: 80%;
            height: 80%;
            border: 2px solid var(--gold);
            border-radius: 190px 190px 25px 25px;
        }

        .experience-badge {
            position: absolute;
            right: -15px;
            top: 70px;
            z-index: 3;
            display: flex;
            width: 135px;
            height: 135px;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            border: 8px solid var(--cream);
            border-radius: 50%;
            color: var(--white);
            text-align: center;
            background: linear-gradient(
                135deg,
                var(--primary),
                var(--secondary)
            );
            box-shadow: var(--shadow);
        }

        .experience-badge strong {
            font-family: "Cormorant Garamond", serif;
            font-size: 37px;
            line-height: 1;
        }

        .experience-badge span {
            margin-top: 5px;
            font-size: 9px;
            font-weight: 700;
            letter-spacing: 1.5px;
            text-transform: uppercase;
        }

        .about-content .section-tag {
            justify-content: flex-start;
        }

        .about-content .section-tag::before {
            display: none;
        }

        .about-content h2 {
            margin-bottom: 22px;
            font-size: clamp(44px, 5vw, 68px);
        }

        .about-content h3 {
            margin-bottom: 20px;
            color: var(--secondary);
            font-size: 27px;
            font-weight: 600;
        }

        .about-content > p {
            margin-bottom: 18px;
        }

        .service-checklist {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 14px 20px;
            margin: 30px 0 35px;
        }

        .service-checklist li {
            display: flex;
            align-items: center;
            gap: 11px;
            color: var(--dark);
            font-size: 14px;
            font-weight: 600;
        }

        .service-checklist i {
            display: flex;
            width: 25px;
            height: 25px;
            align-items: center;
            justify-content: center;
            border-radius: 50%;
            color: var(--primary);
            background: rgba(202, 164, 93, 0.18);
            font-size: 11px;
        }

        /* Services */

        .service-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 25px;
        }

        .service-card {
            position: relative;
            min-height: 310px;
            padding: 38px 30px;
            border: 1px solid var(--border);
            border-radius: 20px;
            background: rgba(255, 255, 255, 0.84);
            box-shadow: 0 15px 40px rgba(64, 31, 47, 0.07);
            transition: var(--transition);
            overflow: hidden;
        }

        .service-card::before {
            content: "";
            position: absolute;
            top: -85px;
            right: -85px;
            width: 170px;
            height: 170px;
            border-radius: 50%;
            background: linear-gradient(
                135deg,
                rgba(202, 164, 93, 0.24),
                rgba(183, 110, 121, 0.1)
            );
            transition: var(--transition);
        }

        .service-card:hover {
            border-color: rgba(202, 164, 93, 0.45);
            transform: translateY(-10px);
            box-shadow: var(--shadow);
        }

        .service-card:hover::before {
            transform: scale(1.35);
        }

        .service-icon {
            position: relative;
            z-index: 1;
            display: flex;
            width: 68px;
            height: 68px;
            margin-bottom: 28px;
            align-items: center;
            justify-content: center;
            border-radius: 18px;
            color: var(--white);
            background: linear-gradient(
                135deg,
                var(--primary),
                var(--secondary)
            );
            box-shadow: 0 14px 25px rgba(122, 41, 77, 0.2);
            font-size: 25px;
        }

        .service-card h3 {
            margin-bottom: 13px;
            font-size: 27px;
        }

        .service-card p {
            font-size: 14px;
        }

        .service-number {
            position: absolute;
            right: 25px;
            bottom: 18px;
            color: rgba(122, 41, 77, 0.07);
            font-family: "Cormorant Garamond", serif;
            font-size: 70px;
            font-weight: 700;
        }

        /* Why Choose Us */

        .features-strip {
            background:
                linear-gradient(
                    135deg,
                    rgba(75, 21, 48, 0.97),
                    rgba(122, 41, 77, 0.93)
                ),
                url("images/texture.jpg") center/cover;
        }

        .feature-grid {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 35px;
        }

        .feature-item {
            color: var(--white);
            text-align: center;
        }

        .feature-icon {
            display: flex;
            width: 75px;
            height: 75px;
            margin: 0 auto 20px;
            align-items: center;
            justify-content: center;
            border: 1px solid rgba(234, 213, 164, 0.45);
            border-radius: 50%;
            color: var(--gold-light);
            background: rgba(255, 255, 255, 0.06);
            font-size: 27px;
        }

        .feature-item h3 {
            margin-bottom: 10px;
            color: var(--white);
            font-size: 24px;
        }

        .feature-item p {
            color: rgba(255, 255, 255, 0.68);
            font-size: 13px;
        }

        /* Gallery */

        .gallery-grid {
            display: grid;
            grid-template-columns: repeat(12, 1fr);
            grid-auto-rows: 250px;
            gap: 18px;
        }

        .gallery-item {
            position: relative;
            border-radius: 18px;
            cursor: pointer;
            overflow: hidden;
        }

        .gallery-item:nth-child(1) {
            grid-column: span 5;
            grid-row: span 2;
        }

        .gallery-item:nth-child(2) {
            grid-column: span 4;
        }

        .gallery-item:nth-child(3) {
            grid-column: span 3;
        }

        .gallery-item:nth-child(4) {
            grid-column: span 3;
        }

        .gallery-item:nth-child(5) {
            grid-column: span 4;
        }

        .gallery-item:nth-child(6) {
            grid-column: span 7;
        }

        .gallery-item:nth-child(7) {
            grid-column: span 5;
        }

        .gallery-item img {
            height: 100%;
            object-fit: cover;
            transition: transform 0.8s ease;
        }

        .gallery-item::after {
            content: "";
            position: absolute;
            inset: 0;
            background: linear-gradient(
                to top,
                rgba(47, 16, 33, 0.7),
                transparent 60%
            );
            opacity: 0.5;
            transition: var(--transition);
        }

        .gallery-item:hover img {
            transform: scale(1.08);
        }

        .gallery-item:hover::after {
            opacity: 0.85;
        }

        .gallery-caption {
            position: absolute;
            left: 24px;
            bottom: 20px;
            z-index: 2;
            color: var(--white);
            transform: translateY(15px);
            opacity: 0;
            transition: var(--transition);
        }

        .gallery-item:hover .gallery-caption {
            transform: translateY(0);
            opacity: 1;
        }

        .gallery-caption h3 {
            color: var(--white);
            font-size: 24px;
        }

        .gallery-caption span {
            color: var(--gold-light);
            font-size: 11px;
            letter-spacing: 2px;
            text-transform: uppercase;
        }

        /* Pricing */

        .pricing-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 28px;
            align-items: stretch;
        }

        .price-card {
            position: relative;
            display: flex;
            min-height: 510px;
            padding: 42px 32px;
            flex-direction: column;
            border: 1px solid var(--border);
            border-radius: 22px;
            background: var(--white);
            box-shadow: 0 18px 45px rgba(64, 31, 47, 0.08);
            transition: var(--transition);
            overflow: hidden;
        }

        .price-card:hover {
            transform: translateY(-10px);
            box-shadow: var(--shadow);
        }

        .price-card.featured {
            border: 1px solid var(--gold);
            background:
                radial-gradient(
                    circle at top right,
                    rgba(202, 164, 93, 0.19),
                    transparent 32%
                ),
                var(--white);
            transform: translateY(-15px);
        }

        .price-card.featured:hover {
            transform: translateY(-24px);
        }

        .popular-label {
            position: absolute;
            top: 23px;
            right: -38px;
            width: 150px;
            padding: 7px;
            color: var(--white);
            text-align: center;
            background: var(--gold);
            font-size: 9px;
            font-weight: 700;
            letter-spacing: 1px;
            text-transform: uppercase;
            transform: rotate(40deg);
        }

        .package-icon {
            display: flex;
            width: 58px;
            height: 58px;
            margin-bottom: 24px;
            align-items: center;
            justify-content: center;
            border-radius: 50%;
            color: var(--primary);
            background: var(--soft-pink);
            font-size: 22px;
        }

        .price-card h3 {
            margin-bottom: 8px;
            font-size: 31px;
        }

        .package-subtitle {
            min-height: 45px;
            margin-bottom: 25px;
            font-size: 13px;
        }

        .price {
            margin-bottom: 26px;
            color: var(--primary);
            font-family: "Cormorant Garamond", serif;
            font-size: 48px;
            font-weight: 700;
            line-height: 1;
        }

        .price span {
            display: block;
            margin-top: 7px;
            color: #8a7780;
            font-family: "Montserrat", sans-serif;
            font-size: 11px;
            font-weight: 500;
            letter-spacing: 1px;
            text-transform: uppercase;
        }

        .package-list {
            display: grid;
            gap: 13px;
            margin-bottom: 30px;
        }

        .package-list li {
            display: flex;
            align-items: center;
            gap: 10px;
            color: var(--dark);
            font-size: 14px;
        }

        .package-list i {
            color: var(--gold);
            font-size: 12px;
        }

        .price-card .btn {
            width: 100%;
            margin-top: auto;
        }

        .price-note {
            margin-top: 35px;
            text-align: center;
            font-size: 13px;
        }

        /* Testimonials */

        .testimonial-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 25px;
        }

        .testimonial-card {
            position: relative;
            padding: 35px 30px;
            border: 1px solid var(--border);
            border-radius: 20px;
            background: var(--white);
            box-shadow: 0 15px 40px rgba(64, 31, 47, 0.07);
            transition: var(--transition);
        }

        .testimonial-card:hover {
            transform: translateY(-8px);
            box-shadow: var(--shadow);
        }

        .quote-icon {
            position: absolute;
            top: 22px;
            right: 25px;
            color: rgba(202, 164, 93, 0.18);
            font-size: 50px;
        }

        .stars {
            margin-bottom: 19px;
            color: var(--gold);
            font-size: 13px;
            letter-spacing: 3px;
        }

        .testimonial-card > p {
            position: relative;
            z-index: 2;
            min-height: 125px;
            color: #65545d;
            font-family: "Cormorant Garamond", serif;
            font-size: 21px;
            font-style: italic;
            line-height: 1.6;
        }

        .reviewer {
            display: flex;
            margin-top: 26px;
            padding-top: 21px;
            align-items: center;
            gap: 13px;
            border-top: 1px solid var(--border);
        }

        .reviewer-avatar {
            display: flex;
            width: 48px;
            height: 48px;
            flex-shrink: 0;
            align-items: center;
            justify-content: center;
            border-radius: 50%;
            color: var(--white);
            background: linear-gradient(
                135deg,
                var(--primary),
                var(--secondary)
            );
            font-family: "Cormorant Garamond", serif;
            font-size: 22px;
            font-weight: 700;
        }

        .reviewer h4 {
            font-size: 19px;
        }

        .reviewer span {
            color: #967f89;
            font-size: 11px;
        }

        /* Contact */

        .contact-section {
            background:
                linear-gradient(
                    135deg,
                    rgba(55, 17, 36, 0.95),
                    rgba(111, 37, 71, 0.92)
                ),
                url("images/contact-bg.jpg") center/cover fixed;
        }

        .contact-wrapper {
            display: grid;
            grid-template-columns: 0.9fr 1.1fr;
            gap: 60px;
            align-items: center;
        }

        .contact-content {
            color: rgba(255, 255, 255, 0.75);
        }

        .contact-content .section-tag {
            justify-content: flex-start;
            color: var(--gold-light);
        }

        .contact-content .section-tag::before {
            display: none;
        }

        .contact-content .section-tag::after {
            background: var(--gold-light);
        }

        .contact-content h2 {
            margin-bottom: 22px;
            color: var(--white);
            font-size: clamp(46px, 6vw, 73px);
        }

        .contact-content > p {
            margin-bottom: 30px;
        }

        .contact-list {
            display: grid;
            gap: 18px;
        }

        .contact-item {
            display: flex;
            align-items: center;
            gap: 16px;
        }

        .contact-item-icon {
            display: flex;
            width: 48px;
            height: 48px;
            flex-shrink: 0;
            align-items: center;
            justify-content: center;
            border: 1px solid rgba(234, 213, 164, 0.35);
            border-radius: 50%;
            color: var(--gold-light);
            background: rgba(255, 255, 255, 0.07);
        }

        .contact-item span {
            display: block;
            color: var(--gold-light);
            font-size: 10px;
            font-weight: 700;
            letter-spacing: 1.5px;
            text-transform: uppercase;
        }

        .contact-item a,
        .contact-item p {
            color: var(--white);
            font-size: 14px;
        }

        .booking-card {
            padding: 42px;
            border: 1px solid rgba(255, 255, 255, 0.2);
            border-radius: 24px;
            background: rgba(255, 255, 255, 0.96);
            box-shadow: 0 30px 70px rgba(20, 5, 13, 0.3);
        }

        .booking-card h3 {
            margin-bottom: 10px;
            font-size: 35px;
        }

        .booking-card > p {
            margin-bottom: 28px;
            font-size: 13px;
        }

        .form-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 18px;
        }

        .form-group {
            position: relative;
        }

        .form-group.full-width {
            grid-column: span 2;
        }

        .form-group label {
            display: block;
            margin-bottom: 7px;
            color: var(--dark);
            font-size: 12px;
            font-weight: 600;
        }

        .form-group input,
        .form-group select,
        .form-group textarea {
            width: 100%;
            border: 1px solid #eadde3;
            border-radius: 11px;
            outline: none;
            color: var(--dark);
            background: #fffafa;
            transition: var(--transition);
        }

        .form-group input,
        .form-group select {
            height: 51px;
            padding: 0 16px;
        }

        .form-group textarea {
            min-height: 110px;
            padding: 14px 16px;
            resize: vertical;
        }

        .form-group input:focus,
        .form-group select:focus,
        .form-group textarea:focus {
            border-color: var(--secondary);
            background: var(--white);
            box-shadow: 0 0 0 4px rgba(183, 110, 121, 0.1);
        }

        .booking-card .btn {
            width: 100%;
            margin-top: 20px;
        }

        /* Footer */

        footer {
            padding: 35px 0;
            color: rgba(255, 255, 255, 0.62);
            background: #1d1017;
            font-size: 12px;
        }

        .footer-wrapper {
            display: flex;
            align-items: center;
            justify-content: space-between;
            gap: 20px;
        }

        .footer-logo {
            color: var(--white);
            font-family: "Cormorant Garamond", serif;
            font-size: 25px;
            font-weight: 700;
        }

        .footer-socials {
            display: flex;
            gap: 12px;
        }

        .footer-socials a {
            display: flex;
            width: 38px;
            height: 38px;
            align-items: center;
            justify-content: center;
            border: 1px solid rgba(255, 255, 255, 0.14);
            border-radius: 50%;
            color: var(--gold-light);
            transition: var(--transition);
        }

        .footer-socials a:hover {
            color: var(--primary-dark);
            background: var(--gold-light);
            transform: translateY(-3px);
        }

        /* WhatsApp Button */

        .whatsapp-float {
            position: fixed;
            right: 23px;
            bottom: 23px;
            z-index: 900;
            display: flex;
            height: 58px;
            padding: 0 20px;
            align-items: center;
            gap: 10px;
            border-radius: 50px;
            color: var(--white);
            background: #25d366;
            box-shadow: 0 12px 35px rgba(37, 211, 102, 0.35);
            font-size: 13px;
            font-weight: 700;
            transition: var(--transition);
        }

        .whatsapp-float i {
            font-size: 24px;
        }

        .whatsapp-float:hover {
            background: #1fba59;
            transform: translateY(-5px) scale(1.03);
        }

        .whatsapp-float::before {
            content: "";
            position: absolute;
            inset: -7px;
            z-index: -1;
            border: 1px solid rgba(37, 211, 102, 0.45);
            border-radius: 50px;
            animation: pulse 2s infinite;
        }

        @keyframes pulse {
            0% {
                transform: scale(0.94);
                opacity: 1;
            }

            100% {
                transform: scale(1.15);
                opacity: 0;
            }
        }

        /* Image Lightbox */

        .lightbox {
            position: fixed;
            inset: 0;
            z-index: 3000;
            display: flex;
            padding: 30px;
            align-items: center;
            justify-content: center;
            background: rgba(18, 7, 13, 0.94);
            visibility: hidden;
            opacity: 0;
            transition: var(--transition);
        }

        .lightbox.active {
            visibility: visible;
            opacity: 1;
        }

        .lightbox img {
            max-width: 1000px;
            max-height: 88vh;
            border-radius: 14px;
            object-fit: contain;
            box-shadow: 0 25px 80px rgba(0, 0, 0, 0.5);
            transform: scale(0.9);
            transition: var(--transition);
        }

        .lightbox.active img {
            transform: scale(1);
        }

        .lightbox-close {
            position: absolute;
            top: 25px;
            right: 30px;
            width: 48px;
            height: 48px;
            border: 1px solid rgba(255, 255, 255, 0.3);
            border-radius: 50%;
            color: var(--white);
            background: rgba(255, 255, 255, 0.08);
            cursor: pointer;
            font-size: 21px;
        }

        /* Scroll Reveal */

        .reveal {
            transform: translateY(55px);
            opacity: 0;
            transition:
                opacity 0.9s ease,
                transform 0.9s ease;
        }

        .reveal-left {
            transform: translateX(-60px);
            opacity: 0;
            transition:
                opacity 0.9s ease,
                transform 0.9s ease;
        }

        .reveal-right {
            transform: translateX(60px);
            opacity: 0;
            transition:
                opacity 0.9s ease,
                transform 0.9s ease;
        }

        .reveal.active,
        .reveal-left.active,
        .reveal-right.active {
            transform: translate(0);
            opacity: 1;
        }

        .delay-1 {
            transition-delay: 0.1s;
        }

        .delay-2 {
            transition-delay: 0.2s;
        }

        .delay-3 {
            transition-delay: 0.3s;
        }

        .delay-4 {
            transition-delay: 0.4s;
        }

        /* Responsive */

        @media (max-width: 1024px) {
            .nav-links {
                gap: 18px;
            }

            .about-grid {
                gap: 50px;
            }

            .service-grid,
            .pricing-grid,
            .testimonial-grid {
                grid-template-columns: repeat(2, 1fr);
            }

            .price-card.featured {
                transform: none;
            }

            .price-card.featured:hover {
                transform: translateY(-10px);
            }

            .feature-grid {
                grid-template-columns: repeat(2, 1fr);
            }

            .contact-wrapper {
                grid-template-columns: 1fr;
            }
        }

        @media (max-width: 850px) {
            .menu-toggle {
                display: inline-flex;
                align-items: center;
                justify-content: center;
            }

            .nav-links {
                position: fixed;
                top: 0;
                right: -100%;
                width: min(340px, 88%);
                height: 100vh;
                padding: 110px 40px 40px;
                flex-direction: column;
                align-items: flex-start;
                gap: 25px;
                background: var(--cream);
                box-shadow: -20px 0 60px rgba(40, 15, 28, 0.18);
                transition: 0.5s ease;
            }

            .nav-links.active {
                right: 0;
            }

            .nav-links a,
            .navbar.scrolled .nav-links a {
                color: var(--dark);
                font-size: 16px;
            }

            .nav-booking {
                color: var(--white) !important;
                border-color: var(--primary);
                background: var(--primary);
            }

            .about-grid {
                grid-template-columns: 1fr;
            }

            .about-image-wrap {
                max-width: 600px;
                margin: auto;
            }

            .about-main-image {
                height: 580px;
            }

            .gallery-grid {
                grid-template-columns: repeat(2, 1fr);
                grid-auto-rows: 320px;
            }

            .gallery-item,
            .gallery-item:nth-child(1),
            .gallery-item:nth-child(2),
            .gallery-item:nth-child(3),
            .gallery-item:nth-child(4),
            .gallery-item:nth-child(5),
            .gallery-item:nth-child(6),
            .gallery-item:nth-child(7) {
                grid-column: auto;
                grid-row: auto;
            }
        }

        @media (max-width: 650px) {
            .section {
                padding: 85px 0;
            }

            .hero {
                min-height: 800px;
                text-align: center;
                background-position: 62% center;
            }

            .hero::before {
                background: rgba(48, 15, 33, 0.78);
            }

            .hero-content {
                padding-top: 95px;
            }

            .hero-subtitle,
            .hero-buttons,
            .hero-features {
                justify-content: center;
            }

            .hero-subtitle::before {
                display: none;
            }

            .hero h1 {
                font-size: 61px;
                letter-spacing: -1px;
            }

            .hero-description {
                font-size: 15px;
            }

            .hero-features {
                gap: 15px;
            }

            .about-main-image {
                height: 480px;
            }

            .experience-badge {
                right: -5px;
                width: 115px;
                height: 115px;
            }

            .service-grid,
            .pricing-grid,
            .testimonial-grid,
            .feature-grid,
            .gallery-grid {
                grid-template-columns: 1fr;
            }

            .gallery-grid {
                grid-auto-rows: 390px;
            }

            .service-checklist {
                grid-template-columns: 1fr;
            }

            .form-grid {
                grid-template-columns: 1fr;
            }

            .form-group.full-width {
                grid-column: auto;
            }

            .booking-card {
                padding: 30px 22px;
            }

            .footer-wrapper {
                flex-direction: column;
                text-align: center;
            }

            .whatsapp-float {
                right: 15px;
                bottom: 15px;
                width: 58px;
                padding: 0;
                justify-content: center;
                border-radius: 50%;
            }

            .whatsapp-float span {
                display: none;
            }
        }

        @media (max-width: 420px) {
            .hero h1 {
                font-size: 52px;
            }

            .hero-buttons {
                flex-direction: column;
            }

            .hero-buttons .btn {
                width: 100%;
            }

            .gallery-grid {
                grid-auto-rows: 330px;
            }

            .about-main-image {
                height: 420px;
            }

            .experience-badge {
                top: 35px;
                right: -5px;
            }
        }

        @media (prefers-reduced-motion: reduce) {
            html {
                scroll-behavior: auto;
            }

            *,
            *::before,
            *::after {
                animation-duration: 0.01ms !important;
                animation-iteration-count: 1 !important;
                transition-duration: 0.01ms !important;
            }

            .reveal,
            .reveal-left,
            .reveal-right {
                transform: none;
                opacity: 1;
            }
        }
    </style>
</head>

<body>

    <!-- Scroll Progress -->
    <div class="scroll-progress" id="scrollProgress"></div>

    <!-- Navigation -->
    <nav class="navbar" id="navbar">
        <div class="container nav-wrapper">

            <a href="#home" class="logo" aria-label="SP Artistry home">
                <span class="logo-main">SP Artistry</span>
                <span class="logo-small">Bridal Makeup Artist</span>
            </a>

            <button
                class="menu-toggle"
                id="menuToggle"
                type="button"
                aria-label="Open navigation menu"
                aria-expanded="false"
            >
                <i class="fa-solid fa-bars"></i>
            </button>

            <ul class="nav-links" id="navLinks">
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#services">Services</a></li>
                <li><a href="#gallery">Gallery</a></li>
                <li><a href="#pricing">Packages</a></li>
                <li><a href="#reviews">Reviews</a></li>

                <li>
                    <a href="#contact" class="nav-booking">
                        Book Now
                    </a>
                </li>
            </ul>

        </div>
    </nav>

    <!-- Hero Section -->
    <header class="hero" id="home">
        <div class="container">

            <div class="hero-content">

                <p class="hero-subtitle">
                    Premium Bridal Makeup Artist in Chennai
                </p>

                <h1>
                    SP Artistry
                    <span>Where Beauty Becomes Art</span>
                </h1>

                <p class="hero-description">
                    Elegant, timeless and personalised bridal transformations
                    created to make you feel confident, radiant and unforgettable
                    on your special day.
                </p>

                <div class="hero-buttons">

                    <a
                        class="btn btn-primary"
                        href="https://wa.me/919790751968?text=Hello%20SP%20Artistry%2C%20I%20would%20like%20to%20book%20a%20makeup%20appointment."
                        target="_blank"
                        rel="noopener noreferrer"
                    >
                        <i class="fa-brands fa-whatsapp"></i>
                        Book Your Appointment
                    </a>

                    <a class="btn btn-outline" href="#gallery">
                        View Bridal Gallery
                        <i class="fa-solid fa-arrow-right"></i>
                    </a>

                </div>

                <div class="hero-features">

                    <div class="hero-feature">
                        <i class="fa-solid fa-gem"></i>
                        Premium Products
                    </div>

                    <div class="hero-feature">
                        <i class="fa-solid fa-wand-magic-sparkles"></i>
                        Personalised Looks
                    </div>

                    <div class="hero-feature">
                        <i class="fa-solid fa-camera-retro"></i>
                        Camera-Ready Finish
                    </div>

                </div>

            </div>
        </div>

        <a href="#about" class="scroll-down" aria-label="Scroll to about section">
            Scroll
            <i class="fa-solid fa-chevron-down"></i>
        </a>
    </header>

    <!-- About Section -->
    <section class="section section-light" id="about">
        <div class="container">

            <div class="about-grid">

                <div class="about-image-wrap reveal-left">

                    <img
                        class="about-main-image"
                        src="images/about.jpg"
                        alt="SP Artistry bridal makeup"
                        loading="lazy"
                    >

                    <div class="experience-badge">
                        <strong>100%</strong>
                        <span>Personalised Beauty</span>
                    </div>

                </div>

                <div class="about-content reveal-right">

                    <p class="section-tag">About SP Artistry</p>

                    <h2>
                        Beauty Designed Around
                        <span class="gold-text">You</span>
                    </h2>

                    <h3>Every bride deserves her own signature look.</h3>

                    <p>
                        SP Artistry specialises in premium bridal makeup for
                        weddings, engagements, receptions and special occasions.
                        Every look is carefully designed to complement your skin
                        tone, facial features, outfit, jewellery and personality.
                    </p>

                    <p>
                        We use high-quality professional products and refined
                        techniques to create comfortable, long-lasting and
                        camera-ready makeup without hiding your natural beauty.
                    </p>

                    <ul class="service-checklist">

                        <li>
                            <i class="fa-solid fa-check"></i>
                            Bridal Makeup
                        </li>

                        <li>
                            <i class="fa-solid fa-check"></i>
                            HD Makeup
                        </li>

                        <li>
                            <i class="fa-solid fa-check"></i>
                            Airbrush Makeup
                        </li>

                        <li>
                            <i class="fa-solid fa-check"></i>
                            Reception Makeup
                        </li>

                        <li>
                            <i class="fa-solid fa-check"></i>
                            Party Makeup
                        </li>

                        <li>
                            <i class="fa-solid fa-check"></i>
                            Hairstyling
                        </li>

                        <li>
                            <i class="fa-solid fa-check"></i>
                            Saree Draping
                        </li>

                        <li>
                            <i class="fa-solid fa-check"></i>
                            Makeup Consultation
                        </li>

                    </ul>

                    <a
                        class="btn btn-primary"
                        href="https://wa.me/919790751968?text=Hello%20SP%20Artistry%2C%20I%20would%20like%20to%20know%20more%20about%20your%20bridal%20makeup%20services."
                        target="_blank"
                        rel="noopener noreferrer"
                    >
                        Talk to Our Makeup Artist
                        <i class="fa-brands fa-whatsapp"></i>
                    </a>

                </div>

            </div>
        </div>
    </section>

    <!-- Services Section -->
    <section class="section section-soft" id="services">
        <div class="container">

            <div class="section-heading reveal">
                <p class="section-tag">Our Expertise</p>

                <h2>
                    Makeup Services for
                    <span class="gold-text">Every Celebration</span>
                </h2>

                <p>
                    From subtle elegance to regal glamour, every service is
                    personalised to suit your event, outfit and individual style.
                </p>
            </div>

            <div class="service-grid">

                <article class="service-card reveal delay-1">
                    <div class="service-icon">
                        <i class="fa-solid fa-crown"></i>
                    </div>

                    <h3>Bridal Makeup</h3>

                    <p>
                        A complete luxury bridal transformation designed around
                        your wedding outfit, jewellery, skin tone and wedding theme.
                    </p>

                    <span class="service-number">01</span>
                </article>

                <article class="service-card reveal delay-2">
                    <div class="service-icon">
                        <i class="fa-solid fa-ring"></i>
                    </div>

                    <h3>Engagement Makeup</h3>

                    <p>
                        Soft, elegant and polished makeup that enhances your
                        natural features for your engagement celebration.
                    </p>

                    <span class="service-number">02</span>
                </article>

                <article class="service-card reveal delay-3">
                    <div class="service-icon">
                        <i class="fa-solid fa-star"></i>
                    </div>

                    <h3>Reception Makeup</h3>

                    <p>
                        Glamorous, radiant and camera-ready makeup created to
                        complement your reception attire and evening lighting.
                    </p>

                    <span class="service-number">03</span>
                </article>

                <article class="service-card reveal delay-1">
                    <div class="service-icon">
                        <i class="fa-solid fa-champagne-glasses"></i>
                    </div>

                    <h3>Party Makeup</h3>

                    <p>
                        Sophisticated makeup for birthdays, family functions,
                        corporate events, photoshoots and special occasions.
                    </p>

                    <span class="service-number">04</span>
                </article>

                <article class="service-card reveal delay-2">
                    <div class="service-icon">
                        <i class="fa-solid fa-spray-can-sparkles"></i>
                    </div>

                    <h3>Airbrush Makeup</h3>

                    <p>
                        Lightweight, flawless and long-lasting airbrush makeup
                        with a smooth finish suitable for long wedding events.
                    </p>

                    <span class="service-number">05</span>
                </article>

                <article class="service-card reveal delay-3">
                    <div class="service-icon">
                        <i class="fa-solid fa-scissors"></i>
                    </div>

                    <h3>Hairstyling</h3>

                    <p>
                        Elegant bridal buns, braids, curls and contemporary
                        hairstyles personalised for your outfit and accessories.
                    </p>

                    <span class="service-number">06</span>
                </article>

            </div>
        </div>
    </section>

    <!-- Why Choose Us -->
    <section class="section features-strip">
        <div class="container">

            <div class="feature-grid">

                <div class="feature-item reveal delay-1">
                    <div class="feature-icon">
                        <i class="fa-solid fa-palette"></i>
                    </div>

                    <h3>Customised Looks</h3>

                    <p>
                        Makeup designed for your face, outfit, skin tone and style.
                    </p>
                </div>

                <div class="feature-item reveal delay-2">
                    <div class="feature-icon">
                        <i class="fa-solid fa-shield-heart"></i>
                    </div>

                    <h3>Hygienic Practice</h3>

                    <p>
                        Clean tools, sanitised products and careful application.
                    </p>
                </div>

                <div class="feature-item reveal delay-3">
                    <div class="feature-icon">
                        <i class="fa-solid fa-clock"></i>
                    </div>

                    <h3>Long-Lasting Finish</h3>

                    <p>
                        Comfortable makeup created to stay fresh throughout the event.
                    </p>
                </div>

                <div class="feature-item reveal delay-4">
                    <div class="feature-icon">
                        <i class="fa-solid fa-camera"></i>
                    </div>

                    <h3>Photo-Ready Beauty</h3>

                    <p>
                        Balanced makeup that looks beautiful in person and on camera.
                    </p>
                </div>

            </div>
        </div>
    </section>

    <!-- Gallery Section -->
    <section class="section section-light" id="gallery">
        <div class="container">

            <div class="section-heading reveal">
                <p class="section-tag">Bridal Portfolio</p>

                <h2>
                    Our Beautiful
                    <span class="gold-text">Bridal Gallery</span>
                </h2>

                <p>
                    A glimpse into elegant bridal transformations created with
                    precision, artistry and attention to every detail.
                </p>
            </div>

            <div class="gallery-grid">

                <div class="gallery-item reveal">
                    <img
                        src="images/1.jpg"
                        alt="Traditional bridal makeup by SP Artistry"
                        loading="lazy"
                    >

                    <div class="gallery-caption">
                        <span>SP Artistry</span>
                        <h3>Traditional Bridal Look</h3>
                    </div>
                </div>

                <div class="gallery-item reveal delay-1">
                    <img
                        src="images/2.jpg"
                        alt="Elegant engagement makeup"
                        loading="lazy"
                    >

                    <div class="gallery-caption">
                        <span>SP Artistry</span>
                        <h3>Engagement Elegance</h3>
                    </div>
                </div>

                <div class="gallery-item reveal delay-2">
                    <img
                        src="images/3.jpg"
                        alt="Premium reception makeup"
                        loading="lazy"
                    >

                    <div class="gallery-caption">
                        <span>SP Artistry</span>
                        <h3>Reception Glamour</h3>
                    </div>
                </div>

                <div class="gallery-item reveal delay-1">
                    <img
                        src="images/4.jpg"
                        alt="Natural bridal makeup"
                        loading="lazy"
                    >

                    <div class="gallery-caption">
                        <span>SP Artistry</span>
                        <h3>Soft Bridal Beauty</h3>
                    </div>
                </div>

                <div class="gallery-item reveal delay-2">
                    <img
                        src="images/5.jpg"
                        alt="Luxury bridal hairstyle"
                        loading="lazy"
                    >

                    <div class="gallery-caption">
                        <span>SP Artistry</span>
                        <h3>Luxury Hairstyling</h3>
                    </div>
                </div>

                <div class="gallery-item reveal delay-1">
                    <img
                        src="images/6.jpg"
                        alt="HD bridal makeup"
                        loading="lazy"
                    >

                    <div class="gallery-caption">
                        <span>SP Artistry</span>
                        <h3>HD Bridal Finish</h3>
                    </div>
                </div>

                <div class="gallery-item reveal delay-2">
                    <img
                        src="images/7.jpg"
                        alt="Modern bridal makeover"
                        loading="lazy"
                    >

                    <div class="gallery-caption">
                        <span>SP Artistry</span>
                        <h3>Modern Bridal Look</h3>
                    </div>
                </div>

            </div>
        </div>
    </section>

    <!-- Pricing Section -->
    <section class="section section-soft" id="pricing">
        <div class="container">

            <div class="section-heading reveal">
                <p class="section-tag">Makeup Packages</p>

                <h2>
                    Choose Your
                    <span class="gold-text">Perfect Package</span>
                </h2>

                <p>
                    Contact us for final pricing based on your event, location,
                    selected makeup style and additional services.
                </p>
            </div>

            <div class="pricing-grid">

                <article class="price-card reveal delay-1">

                    <div class="package-icon">
                        <i class="fa-solid fa-champagne-glasses"></i>
                    </div>

                    <h3>Party Package</h3>

                    <p class="package-subtitle">
                        Perfect for birthdays, family events and special occasions.
                    </p>

                    <div class="price">
                        Contact Us
                        <span>For customised pricing</span>
                    </div>

                    <ul class="package-list">
                        <li>
                            <i class="fa-solid fa-check"></i>
                            Party Makeup
                        </li>

                        <li>
                            <i class="fa-solid fa-check"></i>
                            Basic Hairstyling
                        </li>

                        <li>
                            <i class="fa-solid fa-check"></i>
                            Eyelashes
                        </li>

                        <li>
                            <i class="fa-solid fa-check"></i>
                            Basic Draping Assistance
                        </li>
                    </ul>

                    <a
                        class="btn btn-primary"
                        href="https://wa.me/919790751968?text=Hello%20SP%20Artistry%2C%20I%20would%20like%20to%20know%20the%20price%20of%20your%20Party%20Makeup%20Package."
                        target="_blank"
                        rel="noopener noreferrer"
                    >
                        Get Package Price
                    </a>

                </article>

                <article class="price-card featured reveal delay-2">

                    <span class="popular-label">Most Popular</span>

                    <div class="package-icon">
                        <i class="fa-solid fa-crown"></i>
                    </div>

                    <h3>Bridal Package</h3>

                    <p class="package-subtitle">
                        A complete premium bridal transformation for your wedding day.
                    </p>

                    <div class="price">
                        Contact Us
                        <span>For customised pricing</span>
                    </div>

                    <ul class="package-list">
                        <li>
                            <i class="fa-solid fa-check"></i>
                            Premium Bridal Makeup
                        </li>

                        <li>
                            <i class="fa-solid fa-check"></i>
                            Bridal Hairstyling
                        </li>

                        <li>
                            <i class="fa-solid fa-check"></i>
                            Saree Draping
                        </li>

                        <li>
                            <i class="fa-solid fa-check"></i>
                            Eyelashes
                        </li>

                        <li>
                            <i class="fa-solid fa-check"></i>
                            Jewellery Setting
                        </li>
                    </ul>

                    <a
                        class="btn btn-primary"
                        href="https://wa.me/919790751968?text=Hello%20SP%20Artistry%2C%20I%20would%20like%20to%20know%20the%20price%20of%20your%20Bridal%20Makeup%20Package."
                        target="_blank"
                        rel="noopener noreferrer"
                    >
                        Get Bridal Quote
                    </a>

                </article>

                <article class="price-card reveal delay-3">

                    <div class="package-icon">
                        <i class="fa-solid fa-star"></i>
                    </div>

                    <h3>Reception Package</h3>

                    <p class="package-subtitle">
                        A glamorous and refined makeover for your reception event.
                    </p>

                    <div class="price">
                        Contact Us
                        <span>For customised pricing</span>
                    </div>

                    <ul class="package-list">
                        <li>
                            <i class="fa-solid fa-check"></i>
                            Reception Makeup
                        </li>

                        <li>
                            <i class="fa-solid fa-check"></i>
                            Premium Hairstyling
                        </li>

                        <li>
                            <i class="fa-solid fa-check"></i>
                            Eyelashes
                        </li>

                        <li>
                            <i class="fa-solid fa-check"></i>
                            Saree or Dupatta Draping
                        </li>
                    </ul>

                    <a
                        class="btn btn-primary"
                        href="https://wa.me/919790751968?text=Hello%20SP%20Artistry%2C%20I%20would%20like%20to%20know%20the%20price%20of%20your%20Reception%20Makeup%20Package."
                        target="_blank"
                        rel="noopener noreferrer"
                    >
                        Get Package Price
                    </a>

                </article>

            </div>

            <p class="price-note reveal">
                Travel charges and early-morning service charges may apply
                depending on the venue and booking time.
            </p>

        </div>
    </section>

    <!-- Testimonials -->
    <section class="section section-light" id="reviews">
        <div class="container">

            <div class="section-heading reveal">
                <p class="section-tag">Client Experiences</p>

                <h2>
                    Words From Our
                    <span class="gold-text">Happy Brides</span>
                </h2>

                <p>
                    Beautiful makeup matters, but comfort, punctuality and confidence
                    matter just as much.
                </p>
            </div>

            <div class="testimonial-grid">

                <article class="testimonial-card reveal delay-1">

                    <i class="fa-solid fa-quote-right quote-icon"></i>

                    <div class="stars">
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                    </div>

                    <p>
                        “My bridal makeup stayed flawless throughout the wedding.
                        It felt comfortable, looked elegant and photographed
                        beautifully.”
                    </p>

                    <div class="reviewer">
                        <div class="reviewer-avatar">A</div>

                        <div>
                            <h4>Ananya</h4>
                            <span>Bridal Makeup Client</span>
                        </div>
                    </div>

                </article>

                <article class="testimonial-card reveal delay-2">

                    <i class="fa-solid fa-quote-right quote-icon"></i>

                    <div class="stars">
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                    </div>

                    <p>
                        “Professional, punctual and extremely talented. The entire
                        look matched my outfit perfectly without feeling too heavy.”
                    </p>

                    <div class="reviewer">
                        <div class="reviewer-avatar">S</div>

                        <div>
                            <h4>Swetha</h4>
                            <span>Reception Makeup Client</span>
                        </div>
                    </div>

                </article>

                <article class="testimonial-card reveal delay-3">

                    <i class="fa-solid fa-quote-right quote-icon"></i>

                    <div class="stars">
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                    </div>

                    <p>
                        “The makeup looked stunning in every photograph. I received
                        so many compliments, and the hairstyle stayed perfect all day.”
                    </p>

                    <div class="reviewer">
                        <div class="reviewer-avatar">P</div>

                        <div>
                            <h4>Priya</h4>
                            <span>Engagement Makeup Client</span>
                        </div>
                    </div>

                </article>

            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section class="section contact-section" id="contact">
        <div class="container">

            <div class="contact-wrapper">

                <div class="contact-content reveal-left">

                    <p class="section-tag">Reserve Your Date</p>

                    <h2>
                        Let’s Create Your
                        <span class="gold-text">Dream Look</span>
                    </h2>

                    <p>
                        Bridal dates can fill quickly. Share your event date,
                        location and preferred service to check availability
                        and receive a customised quotation.
                    </p>

                    <div class="contact-list">

                        <div class="contact-item">

                            <div class="contact-item-icon">
                                <i class="fa-solid fa-location-dot"></i>
                            </div>

                            <div>
                                <span>Location</span>
                                <p>Chennai, Tamil Nadu</p>
                            </div>

                        </div>

                        <div class="contact-item">

                            <div class="contact-item-icon">
                                <i class="fa-solid fa-phone"></i>
                            </div>

                            <div>
                                <span>Call or WhatsApp</span>

                                <a href="tel:+919790751968">
                                    +91 97907 51968
                                </a>
                            </div>

                        </div>

                        <div class="contact-item">

                            <div class="contact-item-icon">
                                <i class="fa-solid fa-envelope"></i>
                            </div>

                            <div>
                                <span>Email</span>

                                <a href="mailto:sanmugapriya123@gmail.com">
                                    sanmugapriya123@gmail.com
                                </a>
                            </div>

                        </div>

                        <div class="contact-item">

                            <div class="contact-item-icon">
                                <i class="fa-brands fa-instagram"></i>
                            </div>

                            <div>
                                <span>Instagram</span>

                                <a
                                    href="https://www.instagram.com/spartistry"
                                    target="_blank"
                                    rel="noopener noreferrer"
                                >
                                    @spartistry
                                </a>
                            </div>

                        </div>

                    </div>
                </div>

                <div class="booking-card reveal-right">

                    <h3>Request an Appointment</h3>

                    <p>
                        Fill in your details and continue your booking through WhatsApp.
                    </p>

                    <form id="bookingForm">

                        <div class="form-grid">

                            <div class="form-group">
                                <label for="clientName">Your Name</label>

                                <input
                                    id="clientName"
                                    name="clientName"
                                    type="text"
                                    placeholder="Enter your name"
                                    required
                                >
                            </div>

                            <div class="form-group">
                                <label for="clientPhone">Phone Number</label>

                                <input
                                    id="clientPhone"
                                    name="clientPhone"
                                    type="tel"
                                    placeholder="Enter your phone number"
                                    required
                                >
                            </div>

                            <div class="form-group">
                                <label for="eventType">Event Type</label>

                                <select
                                    id="eventType"
                                    name="eventType"
                                    required
                                >
                                    <option value="">Select an event</option>
                                    <option value="Bridal Makeup">Bridal Makeup</option>
                                    <option value="Engagement Makeup">
                                        Engagement Makeup
                                    </option>
                                    <option value="Reception Makeup">
                                        Reception Makeup
                                    </option>
                                    <option value="Party Makeup">Party Makeup</option>
                                    <option value="Airbrush Makeup">
                                        Airbrush Makeup
                                    </option>
                                    <option value="Hairstyling">Hairstyling</option>
                                    <option value="Other Service">Other Service</option>
                                </select>
                            </div>

                            <div class="form-group">
                                <label for="eventDate">Event Date</label>

                                <input
                                    id="eventDate"
                                    name="eventDate"
                                    type="date"
                                    required
                                >
                            </div>

                            <div class="form-group full-width">
                                <label for="eventLocation">Event Location</label>

                                <input
                                    id="eventLocation"
                                    name="eventLocation"
                                    type="text"
                                    placeholder="Enter the event location"
                                >
                            </div>

                            <div class="form-group full-width">
                                <label for="clientMessage">Additional Details</label>

                                <textarea
                                    id="clientMessage"
                                    name="clientMessage"
                                    placeholder="Tell us about your preferred makeup style, event timing or any additional requirements"
                                ></textarea>
                            </div>

                        </div>

                        <button class="btn btn-primary" type="submit">
                            <i class="fa-brands fa-whatsapp"></i>
                            Send Booking Request
                        </button>

                    </form>

                </div>

            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container footer-wrapper">

            <div class="footer-logo">
                SP Artistry
            </div>

            <p>
                © <span id="currentYear"></span> SP Artistry.
                All Rights Reserved.
            </p>

            <div class="footer-socials">

                <a
                    href="https://www.instagram.com/spartistry"
                    target="_blank"
                    rel="noopener noreferrer"
                    aria-label="Instagram"
                >
                    <i class="fa-brands fa-instagram"></i>
                </a>

                <a
                    href="https://wa.me/919790751968"
                    target="_blank"
                    rel="noopener noreferrer"
                    aria-label="WhatsApp"
                >
                    <i class="fa-brands fa-whatsapp"></i>
                </a>

                <a
                    href="mailto:sanmugapriya123@gmail.com"
                    aria-label="Email"
                >
                    <i class="fa-solid fa-envelope"></i>
                </a>

            </div>

        </div>
    </footer>

    <!-- Floating WhatsApp Button -->
    <a
        class="whatsapp-float"
        href="https://wa.me/919790751968?text=Hello%20SP%20Artistry%2C%20I%20would%20like%20to%20enquire%20about%20your%20makeup%20services."
        target="_blank"
        rel="noopener noreferrer"
        aria-label="Chat with SP Artistry on WhatsApp"
    >
        <i class="fa-brands fa-whatsapp"></i>
        <span>Chat on WhatsApp</span>
    </a>

    <!-- Gallery Lightbox -->
    <div class="lightbox" id="lightbox">

        <button
            class="lightbox-close"
            id="lightboxClose"
            type="button"
            aria-label="Close image"
        >
            <i class="fa-solid fa-xmark"></i>
        </button>

        <img
            id="lightboxImage"
            src=""
            alt="SP Artistry bridal gallery preview"
        >

    </div>

    <script>
        const navbar = document.getElementById("navbar");
        const scrollProgress = document.getElementById("scrollProgress");
        const menuToggle = document.getElementById("menuToggle");
        const navLinks = document.getElementById("navLinks");
        const navItems = document.querySelectorAll(".nav-links a");
        const revealElements = document.querySelectorAll(
            ".reveal, .reveal-left, .reveal-right"
        );

        /*
         * Sticky navbar and scroll progress
         */
        function handleScroll() {
            if (window.scrollY > 40) {
                navbar.classList.add("scrolled");
            } else {
                navbar.classList.remove("scrolled");
            }

            const documentHeight =
                document.documentElement.scrollHeight - window.innerHeight;

            const scrollPercentage =
                documentHeight > 0
                    ? (window.scrollY / documentHeight) * 100
                    : 0;

            scrollProgress.style.width = scrollPercentage + "%";
        }

        window.addEventListener("scroll", handleScroll);
        handleScroll();

        /*
         * Mobile navigation
         */
        menuToggle.addEventListener("click", function () {
            const isOpen = navLinks.classList.toggle("active");

            document.body.classList.toggle("menu-open", isOpen);
            menuToggle.setAttribute("aria-expanded", String(isOpen));

            menuToggle.innerHTML = isOpen
                ? '<i class="fa-solid fa-xmark"></i>'
                : '<i class="fa-solid fa-bars"></i>';
        });

        navItems.forEach(function (link) {
            link.addEventListener("click", function () {
                navLinks.classList.remove("active");
                document.body.classList.remove("menu-open");
                menuToggle.setAttribute("aria-expanded", "false");
                menuToggle.innerHTML =
                    '<i class="fa-solid fa-bars"></i>';
            });
        });

        /*
         * Scroll reveal animation
         */
        const revealObserver = new IntersectionObserver(
            function (entries, observer) {
                entries.forEach(function (entry) {
                    if (entry.isIntersecting) {
                        entry.target.classList.add("active");
                        observer.unobserve(entry.target);
                    }
                });
            },
            {
                threshold: 0.12,
                rootMargin: "0px 0px -40px 0px"
            }
        );

        revealElements.forEach(function (element) {
            revealObserver.observe(element);
        });

        /*
         * Active navigation link
         */
        const sections = document.querySelectorAll("section[id], header[id]");

        const sectionObserver = new IntersectionObserver(
            function (entries) {
                entries.forEach(function (entry) {
                    if (!entry.isIntersecting) {
                        return;
                    }

                    navItems.forEach(function (link) {
                        link.classList.remove("active");

                        if (
                            link.getAttribute("href") ===
                            "#" + entry.target.id
                        ) {
                            link.classList.add("active");
                        }
                    });
                });
            },
            {
                threshold: 0.35
            }
        );

        sections.forEach(function (section) {
            sectionObserver.observe(section);
        });

        /*
         * Gallery lightbox
         */
        const galleryImages =
            document.querySelectorAll(".gallery-item img");

        const lightbox = document.getElementById("lightbox");
        const lightboxImage =
            document.getElementById("lightboxImage");

        const lightboxClose =
            document.getElementById("lightboxClose");

        galleryImages.forEach(function (image) {
            image.parentElement.addEventListener("click", function () {
                lightboxImage.src = image.src;
                lightboxImage.alt = image.alt;
                lightbox.classList.add("active");
                document.body.style.overflow = "hidden";
            });
        });

        function closeLightbox() {
            lightbox.classList.remove("active");
            document.body.style.overflow = "";
        }

        lightboxClose.addEventListener("click", closeLightbox);

        lightbox.addEventListener("click", function (event) {
            if (event.target === lightbox) {
                closeLightbox();
            }
        });

        document.addEventListener("keydown", function (event) {
            if (event.key === "Escape") {
                closeLightbox();
            }
        });

        /*
         * WhatsApp booking form
         */
        const bookingForm = document.getElementById("bookingForm");
        const eventDateInput = document.getElementById("eventDate");

        const today = new Date();
        const localToday = new Date(
            today.getTime() - today.getTimezoneOffset() * 60000
        )
            .toISOString()
            .split("T")[0];

        eventDateInput.min = localToday;

        bookingForm.addEventListener("submit", function (event) {
            event.preventDefault();

            const name =
                document.getElementById("clientName").value.trim();

            const phone =
                document.getElementById("clientPhone").value.trim();

            const eventType =
                document.getElementById("eventType").value;

            const eventDate =
                document.getElementById("eventDate").value;

            const eventLocation =
                document.getElementById("eventLocation").value.trim();

            const message =
                document.getElementById("clientMessage").value.trim();

            const bookingMessage =
`Hello SP Artistry,

I would like to enquire about a makeup appointment.

Name: ${name}
Phone Number: ${phone}
Event Type: ${eventType}
Event Date: ${eventDate}
Event Location: ${eventLocation || "Not specified"}
Additional Details: ${message || "No additional details"}

Please confirm availability and package pricing.`;

            const whatsappURL =
                "https://wa.me/919790751968?text=" +
                encodeURIComponent(bookingMessage);

            window.open(
                whatsappURL,
                "_blank",
                "noopener,noreferrer"
            );
        });

        /*
         * Dynamic footer year
         */
        document.getElementById("currentYear").textContent =
            new Date().getFullYear();
    </script>

</body>
</html>
