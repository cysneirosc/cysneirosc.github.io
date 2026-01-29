[proposta_ast_engenharia.html](https://github.com/user-attachments/files/24937835/proposta_ast_engenharia.html)
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Proposta Blog + Diagnóstico Digital | AST Engenharia</title>
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@300;400;500;600;700;800;900&display=swap" rel="stylesheet">
    <style>
        :root {
            --coral: #E8674F;
            --coral-dark: #d55a44;
            --purple: #7B2CBF;
            --purple-dark: #6a25a6;
            --dark: #2D3748;
            --light: #F7FAFC;
            --white: #ffffff;
            --gray: #718096;
            --ast-blue: #0a2540;
            --ast-orange: #f7931e;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Montserrat', sans-serif;
            color: var(--dark);
            line-height: 1.7;
            background: var(--light);
        }

        /* ANIMAÇÕES */
        @keyframes fadeInUp {
            from { opacity: 0; transform: translateY(30px); }
            to { opacity: 1; transform: translateY(0); }
        }

        @keyframes fadeInLeft {
            from { opacity: 0; transform: translateX(-30px); }
            to { opacity: 1; transform: translateX(0); }
        }

        @keyframes pulse {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.05); }
        }

        @keyframes shimmer {
            0% { background-position: -200% 0; }
            100% { background-position: 200% 0; }
        }

        @keyframes float {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-10px); }
        }

        /* HERO */
        .hero {
            min-height: 100vh;
            background: linear-gradient(135deg, var(--purple) 0%, var(--coral) 100%);
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            padding: 60px 40px;
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(255,255,255,0.1) 0%, transparent 60%);
            animation: pulse 8s ease-in-out infinite;
        }

        .hero-content {
            position: relative;
            z-index: 1;
            max-width: 900px;
        }

        .partnership {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 30px;
            margin-bottom: 50px;
            animation: fadeInUp 0.8s ease-out;
        }

        .brand-box {
            background: rgba(255,255,255,0.15);
            backdrop-filter: blur(10px);
            padding: 20px 35px;
            border-radius: 12px;
            border: 1px solid rgba(255,255,255,0.2);
        }

        .brand-box h3 {
            font-size: 1.4rem;
            font-weight: 800;
            color: var(--white);
            letter-spacing: 3px;
        }

        .brand-box span {
            font-size: 0.75rem;
            color: rgba(255,255,255,0.7);
            letter-spacing: 1px;
        }

        .plus {
            font-size: 2rem;
            color: rgba(255,255,255,0.5);
            font-weight: 300;
        }

        .hero h1 {
            font-size: 3rem;
            font-weight: 900;
            color: var(--white);
            margin-bottom: 25px;
            line-height: 1.2;
            animation: fadeInUp 0.8s ease-out 0.2s backwards;
        }

        .hero h1 span {
            display: block;
            font-size: 1.8rem;
            font-weight: 400;
            opacity: 0.9;
            margin-top: 10px;
        }

        .hero-subtitle {
            font-size: 1.15rem;
            color: rgba(255,255,255,0.9);
            max-width: 750px;
            margin: 0 auto 40px;
            line-height: 1.8;
            animation: fadeInUp 0.8s ease-out 0.4s backwards;
        }

        .hero-badges {
            display: flex;
            gap: 20px;
            justify-content: center;
            flex-wrap: wrap;
            margin-top: 30px;
            animation: fadeInUp 0.8s ease-out 0.6s backwards;
        }

        .badge {
            background: rgba(255,255,255,0.2);
            padding: 12px 25px;
            border-radius: 50px;
            font-size: 0.9rem;
            font-weight: 600;
            color: var(--white);
            border: 1px solid rgba(255,255,255,0.3);
        }

        .scroll-hint {
            position: absolute;
            bottom: 30px;
            left: 50%;
            transform: translateX(-50%);
            color: rgba(255,255,255,0.6);
            font-size: 0.85rem;
            animation: pulse 2s ease-in-out infinite;
        }

        /* SEÇÕES */
        section {
            padding: 80px 40px;
            max-width: 1100px;
            margin: 0 auto;
        }

        section h2 {
            font-size: 2rem;
            font-weight: 800;
            color: var(--purple);
            margin-bottom: 15px;
            position: relative;
            display: inline-block;
        }

        section h2::after {
            content: '';
            position: absolute;
            bottom: -8px;
            left: 0;
            width: 60px;
            height: 4px;
            background: linear-gradient(90deg, var(--coral), var(--purple));
            border-radius: 2px;
        }

        .section-intro {
            font-size: 1.1rem;
            color: var(--gray);
            margin-bottom: 40px;
            max-width: 800px;
        }

        /* CONTEXTO */
        .context-box {
            background: linear-gradient(135deg, var(--dark) 0%, #1a202c 100%);
            border-radius: 20px;
            padding: 50px;
            color: var(--white);
            margin-top: 40px;
        }

        .context-box h3 {
            font-size: 1.5rem;
            margin-bottom: 25px;
            color: var(--coral);
        }

        .context-list {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 20px;
        }

        .context-item {
            display: flex;
            align-items: flex-start;
            gap: 15px;
        }

        .context-icon {
            width: 40px;
            height: 40px;
            background: linear-gradient(135deg, var(--coral), var(--purple));
            border-radius: 10px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.2rem;
            flex-shrink: 0;
        }

        .context-item p {
            font-size: 0.95rem;
            color: rgba(255,255,255,0.85);
            line-height: 1.6;
        }

        .context-item strong {
            color: var(--coral);
        }

        /* DOIS SERVIÇOS */
        .services-section {
            background: var(--light);
            padding: 80px 40px;
            max-width: none;
        }

        .services-content {
            max-width: 1100px;
            margin: 0 auto;
        }

        .services-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 30px;
            margin-top: 50px;
        }

        .service-card {
            background: var(--white);
            border-radius: 20px;
            overflow: hidden;
            box-shadow: 0 10px 40px rgba(0,0,0,0.1);
            transition: all 0.4s ease;
            position: relative;
        }

        .service-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 60px rgba(123, 44, 191, 0.2);
        }

        .service-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 5px;
            background: linear-gradient(90deg, var(--coral), var(--purple));
        }

        .service-header {
            padding: 35px 35px 0;
        }

        .service-number {
            display: inline-block;
            background: linear-gradient(135deg, var(--coral), var(--purple));
            color: var(--white);
            font-size: 0.8rem;
            font-weight: 700;
            padding: 6px 15px;
            border-radius: 20px;
            margin-bottom: 15px;
        }

        .service-card h3 {
            font-size: 1.5rem;
            color: var(--dark);
            margin-bottom: 10px;
        }

        .service-card .subtitle {
            font-size: 0.95rem;
            color: var(--gray);
            margin-bottom: 25px;
        }

        .service-body {
            padding: 0 35px 35px;
        }

        .service-features {
            list-style: none;
        }

        .service-features li {
            padding: 12px 0;
            padding-left: 30px;
            position: relative;
            font-size: 0.95rem;
            color: var(--dark);
            border-bottom: 1px solid #f0f0f0;
        }

        .service-features li:last-child {
            border-bottom: none;
        }

        .service-features li::before {
            content: '✓';
            position: absolute;
            left: 0;
            color: var(--coral);
            font-weight: 700;
        }

        .service-price {
            background: linear-gradient(135deg, var(--purple) 0%, var(--coral) 100%);
            padding: 25px 35px;
            margin-top: 20px;
        }

        .service-price .value {
            font-size: 2rem;
            font-weight: 800;
            color: var(--white);
        }

        .service-price .installment {
            font-size: 0.95rem;
            color: rgba(255,255,255,0.9);
            margin-top: 5px;
        }

        /* BLOG DETALHES */
        .blog-section {
            background: linear-gradient(135deg, var(--coral) 0%, var(--purple) 100%);
            padding: 80px 40px;
            max-width: none;
        }

        .blog-content {
            max-width: 1100px;
            margin: 0 auto;
        }

        .blog-section h2 {
            color: var(--white);
        }

        .blog-section h2::after {
            background: rgba(255,255,255,0.5);
        }

        .blog-section .section-intro {
            color: rgba(255,255,255,0.9);
        }

        .blog-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 25px;
            margin-top: 40px;
        }

        .blog-card {
            background: rgba(255,255,255,0.95);
            border-radius: 16px;
            padding: 30px;
            text-align: center;
            transition: all 0.3s ease;
        }

        .blog-card:hover {
            transform: translateY(-5px);
        }

        .blog-icon {
            width: 70px;
            height: 70px;
            background: linear-gradient(135deg, var(--coral), var(--purple));
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.8rem;
            margin: 0 auto 20px;
        }

        .blog-card h4 {
            font-size: 1.1rem;
            color: var(--dark);
            margin-bottom: 10px;
        }

        .blog-card p {
            font-size: 0.9rem;
            color: var(--gray);
        }

        /* REFERÊNCIAS */
        .referencias-box {
            background: rgba(255,255,255,0.1);
            border-radius: 16px;
            padding: 30px;
            margin-top: 40px;
            border: 1px solid rgba(255,255,255,0.2);
        }

        .referencias-box h4 {
            color: var(--white);
            margin-bottom: 15px;
            font-size: 1rem;
        }

        .referencias-links {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
        }

        .referencias-links a {
            background: rgba(255,255,255,0.2);
            color: var(--white);
            padding: 10px 20px;
            border-radius: 8px;
            text-decoration: none;
            font-size: 0.85rem;
            transition: all 0.3s ease;
        }

        .referencias-links a:hover {
            background: rgba(255,255,255,0.3);
            transform: translateY(-2px);
        }

        /* DIAGNÓSTICO DETALHES */
        .diag-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 20px;
            margin-top: 40px;
        }

        .diag-item {
            display: flex;
            align-items: flex-start;
            gap: 20px;
            padding: 25px;
            background: var(--white);
            border-radius: 12px;
            box-shadow: 0 2px 12px rgba(0,0,0,0.06);
            transition: all 0.3s ease;
        }

        .diag-item:hover {
            transform: translateX(8px);
            box-shadow: 0 4px 20px rgba(232, 103, 79, 0.15);
        }

        .diag-icon {
            width: 50px;
            height: 50px;
            background: linear-gradient(135deg, var(--purple), var(--coral));
            border-radius: 10px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.4rem;
            flex-shrink: 0;
        }

        .diag-text h4 {
            font-size: 1rem;
            font-weight: 700;
            color: var(--dark);
            margin-bottom: 6px;
        }

        .diag-text p {
            font-size: 0.9rem;
            color: var(--gray);
        }

        /* BENEFÍCIOS CAPTAÇÃO LEADS */
        .leads-section {
            background: var(--dark);
            padding: 80px 40px;
            max-width: none;
        }

        .leads-content {
            max-width: 1100px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 50px;
            align-items: center;
        }

        .leads-text h2 {
            color: var(--white);
            font-size: 1.8rem;
            margin-bottom: 20px;
        }

        .leads-text h2::after {
            background: var(--coral);
        }

        .leads-text p {
            color: rgba(255,255,255,0.8);
            font-size: 1rem;
            line-height: 1.8;
            margin-bottom: 20px;
        }

        .leads-example {
            background: rgba(255,255,255,0.05);
            border-radius: 16px;
            padding: 30px;
            border: 1px solid rgba(255,255,255,0.1);
        }

        .leads-example h4 {
            color: var(--coral);
            margin-bottom: 20px;
            font-size: 1rem;
        }

        .leads-flow {
            display: flex;
            flex-direction: column;
            gap: 15px;
        }

        .flow-step {
            display: flex;
            align-items: center;
            gap: 15px;
            padding: 15px;
            background: rgba(255,255,255,0.05);
            border-radius: 10px;
        }

        .flow-number {
            width: 30px;
            height: 30px;
            background: var(--coral);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 0.85rem;
            font-weight: 700;
            color: var(--white);
            flex-shrink: 0;
        }

        .flow-step p {
            color: rgba(255,255,255,0.9);
            font-size: 0.9rem;
            margin: 0;
        }

        /* CRONOGRAMA */
        .timeline {
            position: relative;
            margin-top: 50px;
        }

        .timeline::before {
            content: '';
            position: absolute;
            left: 30px;
            top: 0;
            bottom: 0;
            width: 3px;
            background: linear-gradient(180deg, var(--coral), var(--purple));
            border-radius: 2px;
        }

        .timeline-item {
            display: flex;
            gap: 30px;
            margin-bottom: 30px;
            position: relative;
        }

        .timeline-marker {
            width: 60px;
            height: 60px;
            background: linear-gradient(135deg, var(--coral), var(--purple));
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 0.9rem;
            font-weight: 800;
            color: var(--white);
            flex-shrink: 0;
            z-index: 1;
            box-shadow: 0 4px 15px rgba(232, 103, 79, 0.4);
        }

        .timeline-content {
            background: var(--white);
            border-radius: 12px;
            padding: 25px;
            box-shadow: 0 4px 20px rgba(0,0,0,0.08);
            flex: 1;
        }

        .timeline-content h4 {
            font-size: 1.1rem;
            font-weight: 700;
            color: var(--purple);
            margin-bottom: 10px;
        }

        .timeline-content p {
            font-size: 0.95rem;
            color: var(--gray);
        }

        /* INVESTIMENTO TOTAL */
        .investment-section {
            background: linear-gradient(135deg, var(--purple) 0%, var(--coral) 100%);
            padding: 80px 40px;
            max-width: none;
        }

        .investment-content {
            max-width: 1000px;
            margin: 0 auto;
            text-align: center;
        }

        .investment-section h2 {
            color: var(--white);
            font-size: 2rem;
            margin-bottom: 40px;
        }

        .investment-section h2::after {
            display: none;
        }

        .investment-cards {
            display: grid;
            grid-template-columns: 1fr 1fr 1fr;
            gap: 25px;
            margin-bottom: 40px;
        }

        .inv-card {
            background: rgba(255,255,255,0.95);
            border-radius: 16px;
            padding: 35px 25px;
            text-align: center;
        }

        .inv-card.highlight {
            background: var(--white);
            transform: scale(1.05);
            box-shadow: 0 20px 50px rgba(0,0,0,0.2);
        }

        .inv-card h4 {
            font-size: 0.9rem;
            color: var(--gray);
            text-transform: uppercase;
            letter-spacing: 2px;
            margin-bottom: 15px;
        }

        .inv-card .price {
            font-size: 2.5rem;
            font-weight: 900;
            color: var(--purple);
            margin-bottom: 5px;
        }

        .inv-card.highlight .price {
            background: linear-gradient(135deg, var(--coral), var(--purple));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .inv-card .desc {
            font-size: 0.9rem;
            color: var(--gray);
        }

        .inv-card.highlight .badge-combo {
            display: inline-block;
            background: linear-gradient(135deg, var(--coral), var(--purple));
            color: var(--white);
            padding: 8px 20px;
            border-radius: 20px;
            font-size: 0.8rem;
            font-weight: 700;
            margin-top: 15px;
        }

        .payment-info {
            background: rgba(255,255,255,0.15);
            border-radius: 12px;
            padding: 30px;
            margin-top: 30px;
        }

        .payment-info h4 {
            color: var(--white);
            margin-bottom: 15px;
        }

        .payment-grid {
            display: flex;
            justify-content: center;
            gap: 40px;
            flex-wrap: wrap;
        }

        .payment-item {
            text-align: center;
        }

        .payment-item span {
            display: block;
            font-size: 1.5rem;
            margin-bottom: 5px;
        }

        .payment-item p {
            color: rgba(255,255,255,0.9);
            font-size: 0.9rem;
            margin: 0;
        }

        .validity-badge {
            display: inline-block;
            background: var(--white);
            color: var(--purple);
            padding: 12px 30px;
            border-radius: 30px;
            font-weight: 700;
            margin-top: 30px;
        }

        /* DIFERENCIAIS */
        .diferenciais-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 20px;
            margin-top: 40px;
        }

        .diferencial-item {
            background: var(--white);
            padding: 30px;
            border-radius: 12px;
            box-shadow: 0 2px 12px rgba(0,0,0,0.06);
            border-left: 4px solid var(--coral);
            transition: all 0.3s ease;
        }

        .diferencial-item:hover {
            transform: translateX(5px);
            box-shadow: 0 6px 25px rgba(232, 103, 79, 0.15);
        }

        .diferencial-item h4 {
            font-size: 1rem;
            font-weight: 700;
            color: var(--coral);
            margin-bottom: 10px;
        }

        .diferencial-item p {
            font-size: 0.9rem;
            color: var(--gray);
        }

        /* CONSULTOR */
        .consultor-section {
            display: grid;
            grid-template-columns: 250px 1fr;
            gap: 50px;
            align-items: center;
            margin-top: 40px;
        }

        .consultor-avatar {
            width: 180px;
            height: 180px;
            background: linear-gradient(135deg, var(--purple), var(--coral));
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 3.5rem;
            color: var(--white);
            font-weight: 800;
            margin: 0 auto;
        }

        .consultor-info h3 {
            font-size: 1.5rem;
            color: var(--dark);
            margin-bottom: 5px;
        }

        .consultor-info .title {
            color: var(--coral);
            font-weight: 600;
            margin-bottom: 20px;
        }

        .consultor-stats {
            display: flex;
            gap: 25px;
            margin: 25px 0;
        }

        .stat {
            text-align: center;
            padding: 15px 20px;
            background: var(--light);
            border-radius: 10px;
        }

        .stat span {
            display: block;
            font-size: 1.6rem;
            font-weight: 800;
            color: var(--purple);
        }

        .stat small {
            font-size: 0.75rem;
            color: var(--gray);
        }

        /* PRÓXIMOS PASSOS */
        .steps-grid {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 20px;
            margin-top: 50px;
        }

        .step-card {
            text-align: center;
            padding: 30px 20px;
            background: var(--white);
            border-radius: 16px;
            box-shadow: 0 4px 20px rgba(0,0,0,0.08);
            transition: all 0.3s ease;
        }

        .step-card:hover {
            transform: translateY(-5px);
        }

        .step-number {
            width: 50px;
            height: 50px;
            background: linear-gradient(135deg, var(--coral), var(--purple));
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.2rem;
            font-weight: 800;
            color: var(--white);
            margin: 0 auto 20px;
        }

        .step-card h4 {
            font-size: 1rem;
            font-weight: 700;
            color: var(--dark);
            margin-bottom: 10px;
        }

        .step-card p {
            font-size: 0.85rem;
            color: var(--gray);
        }

        /* CTA FINAL */
        .cta-section {
            background: var(--dark);
            padding: 80px 40px;
            text-align: center;
            max-width: none;
        }

        .cta-content {
            max-width: 800px;
            margin: 0 auto;
        }

        .cta-section h2 {
            font-size: 2.2rem;
            color: var(--white);
            margin-bottom: 20px;
        }

        .cta-section h2::after {
            display: none;
        }

        .cta-section p {
            font-size: 1.1rem;
            color: rgba(255,255,255,0.8);
            margin-bottom: 40px;
        }

        .cta-buttons {
            display: flex;
            gap: 20px;
            justify-content: center;
            flex-wrap: wrap;
        }

        .btn {
            display: inline-block;
            padding: 18px 40px;
            border-radius: 50px;
            font-weight: 700;
            font-size: 1rem;
            text-decoration: none;
            transition: all 0.3s ease;
        }

        .btn-primary {
            background: #25D366;
            color: var(--white);
            box-shadow: 0 8px 25px rgba(37, 211, 102, 0.4);
        }

        .btn-primary:hover {
            transform: translateY(-3px);
            box-shadow: 0 12px 35px rgba(37, 211, 102, 0.5);
        }

        .btn-secondary {
            background: linear-gradient(135deg, var(--coral), var(--purple));
            color: var(--white);
        }

        .btn-secondary:hover {
            transform: translateY(-3px);
            box-shadow: 0 12px 35px rgba(232, 103, 79, 0.4);
        }

        /* FOOTER */
        footer {
            background: #1a1a2e;
            color: var(--white);
            padding: 50px 40px 30px;
        }

        .footer-content {
            max-width: 1100px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: 2fr 1fr 1fr;
            gap: 50px;
            margin-bottom: 40px;
        }

        .footer-brand h3 {
            font-size: 1.5rem;
            color: var(--coral);
            margin-bottom: 15px;
        }

        .footer-brand p {
            font-size: 0.95rem;
            color: rgba(255,255,255,0.7);
            line-height: 1.7;
        }

        .footer-section h4 {
            font-size: 1rem;
            color: var(--coral);
            margin-bottom: 20px;
            font-weight: 700;
        }

        .footer-section a {
            display: block;
            color: rgba(255,255,255,0.7);
            text-decoration: none;
            margin-bottom: 12px;
            font-size: 0.9rem;
            transition: all 0.3s ease;
        }

        .footer-section a:hover {
            color: var(--coral);
            transform: translateX(5px);
        }

        .footer-bottom {
            text-align: center;
            padding-top: 30px;
            border-top: 1px solid rgba(255,255,255,0.1);
            font-size: 0.85rem;
            color: rgba(255,255,255,0.5);
        }

        .footer-bottom a {
            color: var(--coral);
            text-decoration: none;
        }

        /* RESPONSIVO */
        @media (max-width: 1024px) {
            .services-grid,
            .investment-cards,
            .leads-content,
            .consultor-section {
                grid-template-columns: 1fr;
            }

            .diferenciais-grid,
            .blog-grid {
                grid-template-columns: repeat(2, 1fr);
            }

            .steps-grid {
                grid-template-columns: repeat(2, 1fr);
            }

            .footer-content {
                grid-template-columns: 1fr;
                text-align: center;
            }

            .inv-card.highlight {
                transform: none;
            }

            .context-list,
            .diag-grid {
                grid-template-columns: 1fr;
            }
        }

        @media (max-width: 768px) {
            .hero h1 {
                font-size: 2rem;
            }

            .hero h1 span {
                font-size: 1.3rem;
            }

            .partnership {
                flex-direction: column;
                gap: 15px;
            }

            .plus {
                transform: rotate(90deg);
            }

            .hero-badges {
                flex-direction: column;
                align-items: center;
            }

            .diferenciais-grid,
            .blog-grid,
            .steps-grid {
                grid-template-columns: 1fr;
            }

            section {
                padding: 60px 25px;
            }

            .service-card {
                margin-bottom: 20px;
            }
        }
    </style>
</head>
<body>

    <!-- HERO -->
    <section class="hero">
        <div class="hero-content">
            <div class="partnership">
                <div class="brand-box">
                    <h3>CYSNEIROS</h3>
                    <span>CONSULTORES</span>
                </div>
                <span class="plus">+</span>
                <div class="brand-box">
                    <h3>AST</h3>
                    <span>ENGENHARIA</span>
                </div>
            </div>

            <h1>
                Blog Profissional + Site Otimizado
                <span>Transforme seu site em uma máquina de autoridade e captação de leads</span>
            </h1>

            <p class="hero-subtitle">
                Marlan, a AST já é referência em segurança industrial no Ceará. 
                Agora é hora de transformar essa expertise em conteúdo que atrai clientes, 
                posiciona vocês no Google e gera leads qualificados — de forma simples e autônoma.
            </p>

            <div class="hero-badges">
                <span class="badge">📝 Blog Estruturado</span>
                <span class="badge">🔍 Diagnóstico Completo</span>
                <span class="badge">📈 Captação de Leads</span>
                <span class="badge">⚡ 4 Semanas</span>
            </div>
        </div>
        <p class="scroll-hint">↓ Role para conhecer a proposta</p>
    </section>

    <!-- CONTEXTO -->
    <section id="contexto">
        <h2>Entendemos Sua Necessidade</h2>
        <p class="section-intro">
            Na nossa conversa, você deixou claro o que a AST precisa. Organizamos tudo para entregar exatamente isso:
        </p>

        <div class="context-box">
            <h3>O que vocês pediram:</h3>
            <div class="context-list">
                <div class="context-item">
                    <div class="context-icon">📝</div>
                    <p><strong>Blog funcional</strong> — que qualquer pessoa do time consiga alimentar de forma simples, sem precisar de designer</p>
                </div>
                <div class="context-item">
                    <div class="context-icon">📂</div>
                    <p><strong>Área de materiais</strong> — para disponibilizar PDFs, resumos de NRs e arquivos educacionais</p>
                </div>
                <div class="context-item">
                    <div class="context-icon">📧</div>
                    <p><strong>Captação de leads</strong> — visitante deixa nome/email para baixar material e entra na sua base</p>
                </div>
                <div class="context-item">
                    <div class="context-icon">🔒</div>
                    <p><strong>Segurança e backup</strong> — para não perder tudo novamente como aconteceu no passado</p>
                </div>
            </div>
        </div>
    </section>

    <!-- DOIS SERVIÇOS -->
    <section class="services-section">
        <div class="services-content">
            <h2>Dois Serviços Estratégicos</h2>
            <p class="section-intro">
                Estruturamos a proposta em dois blocos independentes que se complementam. 
                Você pode contratar ambos (recomendado) ou escolher apenas um.
            </p>

            <div class="services-grid">
                <!-- SERVIÇO 1: BLOG -->
                <div class="service-card">
                    <div class="service-header">
                        <span class="service-number">SERVIÇO 1</span>
                        <h3>Estruturação do Blog</h3>
                        <p class="subtitle">Ativação, configuração e treinamento completo</p>
                    </div>
                    <div class="service-body">
                        <ul class="service-features">
                            <li>Ativação e configuração do blog no WordPress</li>
                            <li>Design integrado à identidade visual da AST</li>
                            <li>Página de categorias e arquivos organizados</li>
                            <li>Área de materiais para download (PDFs, NRs)</li>
                            <li>Treinamento do time para alimentar o blog</li>
                            <li>Template padrão de postagem</li>
                            <li>Orientações de boas práticas para produção de conteúdo</li>
                            <li>Documentação de uso para o time</li>
                        </ul>
                    </div>
                </div>

                <!-- SERVIÇO 2: DIAGNÓSTICO -->
                <div class="service-card">
                    <div class="service-header">
                        <span class="service-number">SERVIÇO 2</span>
                        <h3>Diagnóstico Digital do Site</h3>
                        <p class="subtitle">Análise completa + recomendações de otimização</p>
                    </div>
                    <div class="service-body">
                        <ul class="service-features">
                            <li>Auditoria técnica completa do WordPress</li>
                            <li>Análise de plugins (atualização, segurança, conflitos)</li>
                            <li>Teste de velocidade (PageSpeed Insights)</li>
                            <li>Verificação de responsividade mobile</li>
                            <li>Análise de oportunidades de SEO on-page</li>
                            <li>Backup completo e seguro do site</li>
                            <li>Mapeamento de oportunidades de captação de leads</li>
                            <li>Relatório com recomendações e ferramentas indicadas</li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- BLOG DETALHES -->
    <section class="blog-section">
        <div class="blog-content">
            <h2>Por Que Ter um Blog Profissional?</h2>
            <p class="section-intro">
                Empresas como Atlas Safe e Timenow usam blogs para posicionar conteúdo técnico no Google. 
                Quando alguém pesquisa "NR-10 requisitos" ou "segurança trabalho em altura", elas aparecem.
            </p>

            <div class="blog-grid">
                <div class="blog-card">
                    <div class="blog-icon">🎯</div>
                    <h4>Autoridade no Setor</h4>
                    <p>Posicione a AST como referência em segurança industrial com conteúdo técnico de qualidade.</p>
                </div>
                <div class="blog-card">
                    <div class="blog-icon">🔍</div>
                    <h4>Tráfego Orgânico</h4>
                    <p>Apareça no Google quando clientes potenciais pesquisarem sobre NRs e segurança do trabalho.</p>
                </div>
                <div class="blog-card">
                    <div class="blog-icon">📧</div>
                    <h4>Geração de Leads</h4>
                    <p>Capture contatos de interessados que baixam seus materiais educacionais.</p>
                </div>
            </div>

            <div class="referencias-box">
                <h4>📌 Referências que você enviou:</h4>
                <div class="referencias-links">
                    <a href="https://atlassafe.com.br/fatores-que-determinam-a-forca-em-uma-queda/" target="_blank">Atlas Safe — Blog Técnico</a>
                    <a href="https://timenow.com.br/conteudo/noticias/" target="_blank">Timenow — Área de Notícias</a>
                </div>
                <p style="color: rgba(255,255,255,0.7); margin-top: 15px; font-size: 0.9rem;">
                    Vamos criar algo no mesmo nível — adaptado para a realidade e identidade da AST.
                </p>
            </div>
        </div>
    </section>

    <!-- DIAGNÓSTICO DETALHES -->
    <section id="diagnostico">
        <h2>O Que o Diagnóstico Vai Analisar?</h2>
        <p class="section-intro">
            Antes de implementar o blog, é fundamental garantir que o site está saudável. 
            Vamos fazer uma varredura completa para identificar problemas e oportunidades.
        </p>

        <div class="diag-grid">
            <div class="diag-item">
                <div class="diag-icon">⚡</div>
                <div class="diag-text">
                    <h4>Velocidade de Carregamento</h4>
                    <p>Análise via PageSpeed. Sites lentos perdem visitantes e posição no Google.</p>
                </div>
            </div>
            <div class="diag-item">
                <div class="diag-icon">🔌</div>
                <div class="diag-text">
                    <h4>Plugins e Atualizações</h4>
                    <p>Verificação de plugins desatualizados, conflitos e vulnerabilidades de segurança.</p>
                </div>
            </div>
            <div class="diag-item">
                <div class="diag-icon">📱</div>
                <div class="diag-text">
                    <h4>Responsividade Mobile</h4>
                    <p>Teste em diferentes dispositivos. Mais de 60% dos acessos vêm do celular.</p>
                </div>
            </div>
            <div class="diag-item">
                <div class="diag-icon">🔍</div>
                <div class="diag-text">
                    <h4>SEO On-Page</h4>
                    <p>Títulos, descrições, heading tags, imagens. O básico que impacta o ranqueamento.</p>
                </div>
            </div>
            <div class="diag-item">
                <div class="diag-icon">🔒</div>
                <div class="diag-text">
                    <h4>Segurança e Backup</h4>
                    <p>Configuração de backup automático para nunca mais perder o site.</p>
                </div>
            </div>
            <div class="diag-item">
                <div class="diag-icon">📊</div>
                <div class="diag-text">
                    <h4>Relatório de Prioridades</h4>
                    <p>Documento com o que corrigir primeiro e recomendações estratégicas.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- CAPTAÇÃO DE LEADS - POSSIBILIDADES -->
    <section class="leads-section">
        <div class="leads-content">
            <div class="leads-text">
                <h2>Possibilidade: Captação de Leads</h2>
                <p>
                    Você mencionou que já tem e-mail marketing, mas não tem gatilho de captura de leads pelo site. 
                    No diagnóstico, vamos identificar como vocês podem implementar isso.
                </p>
                <p>
                    Cada material que você disponibilizar (resumo de NR, checklist, guia) pode virar uma 
                    <strong>isca digital</strong>. Vamos indicar as ferramentas e o caminho para vocês operacionalizarem.
                </p>
            </div>
            <div class="leads-example">
                <h4>Exemplo de Fluxo que Vocês Podem Criar:</h4>
                <div class="leads-flow">
                    <div class="flow-step">
                        <div class="flow-number">1</div>
                        <p>Visitante encontra artigo sobre NR-10 no Google</p>
                    </div>
                    <div class="flow-step">
                        <div class="flow-number">2</div>
                        <p>No final do artigo: "Baixe o Checklist Completo da NR-10"</p>
                    </div>
                    <div class="flow-step">
                        <div class="flow-number">3</div>
                        <p>Para baixar, preenche: Nome, Email, WhatsApp</p>
                    </div>
                    <div class="flow-step">
                        <div class="flow-number">4</div>
                        <p>Lead entra na sua base → E-mail marketing → Conversão</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- CRONOGRAMA -->
    <section id="cronograma">
        <h2>Cronograma do Projeto</h2>
        <p class="section-intro">
            Prazo máximo de execução: <strong>4 semanas</strong>. Trabalho focado e entregas claras.
        </p>

        <div class="timeline">
            <div class="timeline-item">
                <div class="timeline-marker">S1</div>
                <div class="timeline-content">
                    <h4>Semana 1 — Diagnóstico + Planejamento</h4>
                    <p>Auditoria completa do site, backup, análise de plugins, velocidade e SEO. Entrega do relatório de diagnóstico.</p>
                </div>
            </div>
            <div class="timeline-item">
                <div class="timeline-marker">S2</div>
                <div class="timeline-content">
                    <h4>Semana 2 — Estruturação do Blog</h4>
                    <p>Ativação do blog, configuração de categorias, design integrado à identidade visual da AST.</p>
                </div>
            </div>
            <div class="timeline-item">
                <div class="timeline-marker">S3</div>
                <div class="timeline-content">
                    <h4>Semana 3 — Captação de Leads + Materiais</h4>
                    <p>Implementação dos formulários de captura, área de downloads, integração com e-mail marketing.</p>
                </div>
            </div>
            <div class="timeline-item">
                <div class="timeline-marker">S4</div>
                <div class="timeline-content">
                    <h4>Semana 4 — Treinamento + Entrega Final</h4>
                    <p>Treinamento do time para alimentar o blog, template de postagem, introdução a SEO e IA. Entrega final.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- INVESTIMENTO -->
    <section class="investment-section">
        <div class="investment-content">
            <h2>Investimento</h2>

            <div class="investment-cards">
                <div class="inv-card">
                    <h4>Blog</h4>
                    <p class="price">R$ 1.657</p>
                    <p class="desc">Estruturação + Treinamento</p>
                </div>
                <div class="inv-card highlight">
                    <h4>Pacote Completo</h4>
                    <p class="price">R$ 2.987</p>
                    <p class="desc">Blog + Diagnóstico</p>
                    <span class="badge-combo">🎯 5% de desconto</span>
                </div>
                <div class="inv-card">
                    <h4>Diagnóstico</h4>
                    <p class="price">R$ 1.487</p>
                    <p class="desc">Análise + Relatório</p>
                </div>
            </div>

            <div class="payment-info">
                <h4>Condições de Pagamento</h4>
                <div class="payment-grid">
                    <div class="payment-item">
                        <span>💳</span>
                        <p>PIX ou Transferência</p>
                    </div>
                    <div class="payment-item">
                        <span>📅</span>
                        <p>50% início + 50% entrega</p>
                    </div>
                </div>
            </div>

            <span class="validity-badge">Proposta válida por 15 dias</span>
        </div>
    </section>

    <!-- DIFERENCIAIS -->
    <section id="diferenciais">
        <h2>Por que Contratar a Cysneiros?</h2>
        <p class="section-intro">
            Não somos agência de marketing. Somos consultores que entregam soluções práticas e treináveis.
        </p>

        <div class="diferenciais-grid">
            <div class="diferencial-item">
                <h4>✓ Foco em Autonomia</h4>
                <p>Você e seu time vão aprender a alimentar o blog. Sem dependência eterna.</p>
            </div>
            <div class="diferencial-item">
                <h4>✓ WordPress é Nossa Praia</h4>
                <p>Conhecemos a plataforma profundamente. Configuração limpa e profissional.</p>
            </div>
            <div class="diferencial-item">
                <h4>✓ Treinamento Incluso</h4>
                <p>Não entregamos só o sistema. Ensinamos a usar com inteligência.</p>
            </div>
            <div class="diferencial-item">
                <h4>✓ Visão Estratégica</h4>
                <p>Identificamos oportunidades e indicamos ferramentas para você crescer.</p>
            </div>
            <div class="diferencial-item">
                <h4>✓ Backup e Segurança</h4>
                <p>Nunca mais perder o site. Configuramos backup automático.</p>
            </div>
            <div class="diferencial-item">
                <h4>✓ Prazo Respeitado</h4>
                <p>4 semanas no máximo. Sem enrolação, entregas claras.</p>
            </div>
        </div>
    </section>

    <!-- CTA FINAL -->
    <section class="cta-section">
        <div class="cta-content">
            <h2>Vamos Transformar o Site da AST?</h2>
            <p>
                Marlan, vocês já são referência em segurança industrial. 
                Agora é hora de aparecer para quem pesquisa sobre isso no Google.
            </p>
            <div class="cta-buttons">
                <a href="https://wa.me/5581999141429?text=Oi%20Gabriel!%20Vi%20a%20proposta%20para%20a%20AST%20e%20tenho%20interesse%20em%20conversar." class="btn btn-primary">💬 Falar no WhatsApp</a>
                <a href="mailto:contato@cysneiros.com.br?subject=Proposta%20AST%20Engenharia" class="btn btn-secondary">✉️ Enviar Email</a>
            </div>
        </div>
    </section>

    <!-- FOOTER -->
    <footer>
        <div class="footer-content">
            <div class="footer-brand">
                <h3>CYSNEIROS & CONSULTORES</h3>
                <p>Consultoria estratégica em marketing digital e design de negócios. 
                   Transformamos empresas com inteligência, metodologia e resultados mensuráveis.</p>
                <p style="margin-top: 15px;">
                    <a href="https://www.cysneiros.com.br" target="_blank" style="color: var(--coral); font-weight: 600;">www.cysneiros.com.br</a>
                </p>
            </div>
            <div class="footer-section">
                <h4>Serviços</h4>
                <a href="#">Estruturação de Blog</a>
                <a href="#">Diagnóstico Digital</a>
                <a href="#">Planejamento Estratégico</a>
                <a href="#">Design de Negócios</a>
            </div>
            <div class="footer-section">
                <h4>Contato</h4>
                <a href="https://wa.me/5581999141429">📱 (81) 99914-1429</a>
                <a href="mailto:contato@cysneiros.com.br">✉️ contato@cysneiros.com.br</a>
                <a href="#">📍 Recife, Pernambuco</a>
            </div>
        </div>
        <div class="footer-bottom">
            <p>© 2026 Cysneiros & Consultores | Todos os direitos reservados</p>
            <p style="margin-top: 8px;">Proposta exclusiva para <strong>AST Engenharia de Segurança Industrial</strong> — Janeiro de 2026</p>
        </div>
    </footer>

</body>
</html>
