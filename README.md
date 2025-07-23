<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Portfólio Profissional</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: #333;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            padding: 20px;
        }

        .container {
            max-width: 800px;
            margin: 0 auto;
            background: white;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 20px 40px rgba(0,0,0,0.1);
        }

        .header {
            background: linear-gradient(135deg, #2c3e50 0%, #34495e 100%);
            color: white;
            padding: 40px;
            text-align: center;
            position: relative;
        }

        .header::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"><defs><pattern id="grain" patternUnits="userSpaceOnUse" width="100" height="100"><circle cx="25" cy="25" r="1" fill="rgba(255,255,255,0.05)"/><circle cx="75" cy="75" r="1" fill="rgba(255,255,255,0.05)"/><circle cx="50" cy="10" r="0.5" fill="rgba(255,255,255,0.03)"/></pattern></defs><rect width="100" height="100" fill="url(%23grain)"/></svg>');
            opacity: 0.3;
        }

        .profile-img {
            width: 120px;
            height: 120px;
            border-radius: 50%;
            background: linear-gradient(45deg, #667eea, #764ba2);
            margin: 0 auto 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 48px;
            color: white;
            position: relative;
            z-index: 1;
        }

        .name {
            font-size: 2.5em;
            font-weight: 300;
            margin-bottom: 10px;
            position: relative;
            z-index: 1;
        }

        .title {
            font-size: 1.3em;
            opacity: 0.9;
            font-weight: 300;
            position: relative;
            z-index: 1;
        }

        .contact-info {
            display: flex;
            justify-content: center;
            gap: 30px;
            margin-top: 20px;
            flex-wrap: wrap;
            position: relative;
            z-index: 1;
        }

        .contact-item {
            display: flex;
            align-items: center;
            gap: 8px;
            font-size: 0.9em;
        }

        .content {
            padding: 40px;
        }

        .section {
            margin-bottom: 40px;
        }

        .section-title {
            font-size: 1.8em;
            color: #2c3e50;
            margin-bottom: 20px;
            padding-bottom: 10px;
            border-bottom: 3px solid #667eea;
            position: relative;
        }

        .section-title::after {
            content: '';
            position: absolute;
            bottom: -3px;
            left: 0;
            width: 50px;
            height: 3px;
            background: #764ba2;
        }

        .about-text {
            font-size: 1.1em;
            line-height: 1.8;
            color: #555;
            text-align: justify;
        }

        .experience-item {
            margin-bottom: 30px;
            padding: 25px;
            background: linear-gradient(135deg, #f8f9fa 0%, #e9ecef 100%);
            border-radius: 12px;
            border-left: 5px solid #667eea;
            transition: transform 0.3s ease;
        }

        .experience-item:hover {
            transform: translateX(5px);
        }

        .job-title {
            font-size: 1.3em;
            font-weight: 600;
            color: #2c3e50;
            margin-bottom: 5px;
        }

        .company {
            font-size: 1.1em;
            color: #667eea;
            font-weight: 500;
            margin-bottom: 5px;
        }

        .period {
            font-size: 0.9em;
            color: #6c757d;
            margin-bottom: 15px;
        }

        .description {
            color: #555;
            line-height: 1.6;
        }

        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
        }

        .skill-category {
            background: linear-gradient(135deg, #f8f9fa 0%, #e9ecef 100%);
            padding: 20px;
            border-radius: 12px;
            border-top: 4px solid #667eea;
        }

        .skill-category h4 {
            color: #2c3e50;
            margin-bottom: 15px;
            font-size: 1.1em;
        }

        .skill-list {
            list-style: none;
        }

        .skill-list li {
            padding: 5px 0;
            color: #555;
            position: relative;
            padding-left: 20px;
        }

        .skill-list li::before {
            content: '●';
            color: #667eea;
            position: absolute;
            left: 0;
        }

        .education-item {
            background: linear-gradient(135deg, #f8f9fa 0%, #e9ecef 100%);
            padding: 20px;
            border-radius: 12px;
            margin-bottom: 20px;
            border-left: 5px solid #764ba2;
        }

        .degree {
            font-size: 1.2em;
            font-weight: 600;
            color: #2c3e50;
            margin-bottom: 5px;
        }

        .institution {
            color: #764ba2;
            font-weight: 500;
            margin-bottom: 5px;
        }

        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
        }

        .project-card {
            background: linear-gradient(135deg, #f8f9fa 0%, #e9ecef 100%);
            padding: 25px;
            border-radius: 12px;
            border-top: 4px solid #667eea;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .project-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0,0,0,0.1);
        }

        .project-title {
            font-size: 1.2em;
            font-weight: 600;
            color: #2c3e50;
            margin-bottom: 10px;
        }

        .project-description {
            color: #555;
            line-height: 1.6;
            margin-bottom: 15px;
        }

        .project-tech {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
        }

        .tech-tag {
            background: #667eea;
            color: white;
            padding: 4px 12px;
            border-radius: 20px;
            font-size: 0.8em;
            font-weight: 500;
        }

        @media print {
            body {
                background: white;
                padding: 0;
            }
            
            .container {
                box-shadow: none;
                border-radius: 0;
            }
            
            .experience-item:hover,
            .project-card:hover {
                transform: none;
            }
        }

        @media (max-width: 768px) {
            .contact-info {
                flex-direction: column;
                gap: 15px;
            }
            
            .content {
                padding: 20px;
            }
            
            .name {
                font-size: 2em;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header class="header">
            <div class="profile-img">
                👤
            </div>
            <h1 class="name">Seu Nome Aqui</h1>
            <p class="title">Desenvolvedor Full Stack | Designer UX/UI</p>
            <div class="contact-info">
                <div class="contact-item">
                    <span>📧</span>
                    <span>seu.email@exemplo.com</span>
                </div>
                <div class="contact-item">
                    <span>📱</span>
                    <span>(11) 99999-9999</span>
                </div>
                <div class="contact-item">
                    <span>🌐</span>
                    <span>linkedin.com/in/seuperfil</span>
                </div>
                <div class="contact-item">
                    <span>📍</span>
                    <span>São Paulo, SP</span>
                </div>
            </div>
        </header>

        <main class="content">
            <section class="section">
                <h2 class="section-title">Sobre Mim</h2>
                <p class="about-text">
                    Desenvolvedor apaixonado por tecnologia com mais de X anos de experiência em desenvolvimento web e mobile. 
                    Especializado em criar soluções inovadoras e eficientes, sempre buscando as melhores práticas e tecnologias 
                    mais recentes. Tenho experiência sólida em trabalho em equipe, metodologias ágeis e entrega de projetos 
                    de alta qualidade dentro dos prazos estabelecidos.
                </p>
            </section>

            <section class="section">
                <h2 class="section-title">Experiência Profissional</h2>
                
                <div class="experience-item">
                    <h3 class="job-title">Desenvolvedor Full Stack Sênior</h3>
                    <p class="company">Empresa Tecnológica Ltda.</p>
                    <p class="period">Janeiro 2022 - Presente</p>
                    <p class="description">
                        Responsável pelo desenvolvimento e manutenção de aplicações web usando React, Node.js e MongoDB. 
                        Liderança técnica de uma equipe de 5 desenvolvedores, implementação de melhores práticas de código 
                        e arquitetura de software. Aumento de 40% na performance das aplicações desenvolvidas.
                    </p>
                </div>

                <div class="experience-item">
                    <h3 class="job-title">Desenvolvedor Frontend</h3>
                    <p class="company">Startup Inovadora S.A.</p>
                    <p class="period">Março 2020 - Dezembro 2021</p>
                    <p class="description">
                        Desenvolvimento de interfaces modernas e responsivas utilizando React, Vue.js e TypeScript. 
                        Colaboração estreita com equipe de design para implementação pixel-perfect. Implementação 
                        de testes automatizados que reduziram bugs em produção em 60%.
                    </p>
                </div>

                <div class="experience-item">
                    <h3 class="job-title">Desenvolvedor Junior</h3>
                    <p class="company">AgênciaTech Digital</p>
                    <p class="period">Junho 2018 - Fevereiro 2020</p>
                    <p class="description">
                        Desenvolvimento de websites e sistemas web para diversos clientes. Experiência com WordPress, 
                        PHP, MySQL e JavaScript. Participação ativa em projetos de e-commerce e landing pages 
                        de alta conversão.
                    </p>
                </div>
            </section>

            <section class="section">
                <h2 class="section-title">Competências Técnicas</h2>
                <div class="skills-grid">
                    <div class="skill-category">
                        <h4>Frontend</h4>
                        <ul class="skill-list">
                            <li>React / Next.js</li>
                            <li>Vue.js / Nuxt.js</li>
                            <li>TypeScript</li>
                            <li>HTML5 / CSS3</li>
                            <li>Sass / Tailwind CSS</li>
                        </ul>
                    </div>
                    
                    <div class="skill-category">
                        <h4>Backend</h4>
                        <ul class="skill-list">
                            <li>Node.js / Express</li>
                            <li>Python / Django</li>
                            <li>PHP / Laravel</li>
                            <li>API REST / GraphQL</li>
                            <li>Microserviços</li>
                        </ul>
                    </div>
                    
                    <div class="skill-category">
                        <h4>Banco de Dados</h4>
                        <ul class="skill-list">
                            <li>MongoDB</li>
                            <li>PostgreSQL</li>
                            <li>MySQL</li>
                            <li>Redis</li>
                            <li>Elasticsearch</li>
                        </ul>
                    </div>
                    
                    <div class="skill-category">
                        <h4>DevOps & Ferramentas</h4>
                        <ul class="skill-list">
                            <li>Docker / Kubernetes</li>
                            <li>AWS / Azure</li>
                            <li>Git / GitHub</li>
                            <li>CI/CD</li>
                            <li>Monitoramento</li>
                        </ul>
                    </div>
                </div>
            </section>

            <section class="section">
                <h2 class="section-title">Projetos Destacados</h2>
                <div class="projects-grid">
                    <div class="project-card">
                        <h3 class="project-title">E-commerce Moderno</h3>
                        <p class="project-description">
                            Plataforma completa de e-commerce com carrinho, pagamentos, gestão de estoque e painel administrativo.
                        </p>
                        <div class="project-tech">
                            <span class="tech-tag">React</span>
                            <span class="tech-tag">Node.js</span>
                            <span class="tech-tag">MongoDB</span>
                            <span class="tech-tag">Stripe</span>
                        </div>
                    </div>
                    
                    <div class="project-card">
                        <h3 class="project-title">App de Produtividade</h3>
                        <p class="project-description">
                            Aplicação web para gestão de tarefas e projetos com funcionalidades de colaboração em equipe.
                        </p>
                        <div class="project-tech">
                            <span class="tech-tag">Vue.js</span>
                            <span class="tech-tag">Firebase</span>
                            <span class="tech-tag">PWA</span>
                            <span class="tech-tag">WebSockets</span>
                        </div>
                    </div>
                    
                    <div class="project-card">
                        <h3 class="project-title">Dashboard Analytics</h3>
                        <p class="project-description">
                            Sistema de visualização de dados em tempo real com gráficos interativos e relatórios personalizados.
                        </p>
                        <div class="project-tech">
                            <span class="tech-tag">React</span>
                            <span class="tech-tag">D3.js</span>
                            <span class="tech-tag">Python</span>
                            <span class="tech-tag">PostgreSQL</span>
                        </div>
                    </div>
                </div>
            </section>

            <section class="section">
                <h2 class="section-title">Formação</h2>
                
                <div class="education-item">
                    <h3 class="degree">Bacharelado em Ciência da Computação</h3>
                    <p class="institution">Universidade Federal de São Paulo</p>
                    <p class="period">2015 - 2019</p>
                </div>
                
                <div class="education-item">
                    <h3 class="degree">Certificação AWS Solutions Architect</h3>
                    <p class="institution">Amazon Web Services</p>
                    <p class="period">2023</p>
                </div>
                
                <div class="education-item">
                    <h3 class="degree">Especialização em UX/UI Design</h3>
                    <p class="institution">Google UX Design Certificate</p>
                    <p class="period">2022</p>
                </div>
            </section>
        </main>
    </div>
</body>
</html>
