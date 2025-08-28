<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Vestibular UEA 2025 - Guia de Estudos</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary-color: #00539B; /* Azul UEA */
            --secondary-color: #007C4F; /* Verde Amazônia */
            --accent-color: #FF9E1B; /* Laranja para destaque */
            --light-color: #F5F5F5;
            --dark-color: #333333;
            --text-color: #444444;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: var(--light-color);
            color: var(--text-color);
            line-height: 1.6;
        }
        
        header {
            background-color: var(--primary-color);
            color: white;
            padding: 1rem;
            position: sticky;
            top: 0;
            z-index: 100;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }
        
        .header-container {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            display: flex;
            align-items: center;
        }
        
        .logo h1 {
            font-size: 1.5rem;
            margin-left: 10px;
        }
        
        nav ul {
            display: flex;
            list-style: none;
        }
        
        nav ul li {
            margin-left: 1.5rem;
        }
        
        nav ul li a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: opacity 0.3s;
        }
        
        nav ul li a:hover {
            opacity: 0.8;
        }
        
        .hero {
            background: linear-gradient(rgba(0, 83, 155, 0.8), rgba(0, 83, 155, 0.9)), url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="100" height="100" viewBox="0 0 100 100"><rect width="100" height="100" fill="%2300539B"/><path d="M0 0L100 100" stroke="%23007C4F" stroke-width="2"/><path d="M100 0L0 100" stroke="%23007C4F" stroke-width="2"/></svg>');
            background-size: cover;
            color: white;
            text-align: center;
            padding: 3rem 1rem;
            position: relative;
        }
        
        .hero-content {
            max-width: 800px;
            margin: 0 auto;
            position: relative;
            z-index: 2;
        }
        
        .hero h2 {
            font-size: 2.5rem;
            margin-bottom: 1rem;
        }
        
        .hero p {
            font-size: 1.2rem;
            margin-bottom: 2rem;
        }
        
        .concept-credit {
            background-color: rgba(255, 255, 255, 0.2);
            padding: 0.5rem 1rem;
            border-radius: 30px;
            display: inline-block;
            margin-top: 1.5rem;
            font-size: 0.9rem;
            backdrop-filter: blur(5px);
        }
        
        .btn {
            display: inline-block;
            background-color: var(--accent-color);
            color: white;
            padding: 0.8rem 1.5rem;
            border-radius: 5px;
            text-decoration: none;
            font-weight: bold;
            transition: all 0.3s;
            border: none;
            cursor: pointer;
        }
        
        .btn:hover {
            background-color: #e58c15;
            transform: translateY(-2px);
            box-shadow: 0 4px 8px rgba(0,0,0,0.2);
        }
        
        .subjects {
            padding: 3rem 1rem;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .subjects h2 {
            text-align: center;
            margin-bottom: 2rem;
            color: var(--primary-color);
            font-size: 2rem;
        }
        
        .subject-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 2rem;
        }
        
        .subject-card {
            background-color: white;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
            transition: all 0.3s;
            display: flex;
            flex-direction: column;
        }
        
        .subject-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 16px rgba(0,0,0,0.15);
        }
        
        .subject-card-header {
            background-color: var(--secondary-color);
            color: white;
            padding: 1rem;
            text-align: center;
        }
        
        .subject-card-body {
            padding: 1.5rem;
            flex-grow: 1;
        }
        
        .subject-card-body ul {
            list-style-type: none;
            margin-bottom: 1.5rem;
        }
        
        .subject-card-body li {
            margin-bottom: 0.5rem;
            padding-left: 1.5rem;
            position: relative;
        }
        
        .subject-card-body li:before {
            content: "✓";
            position: absolute;
            left: 0;
            color: var(--secondary-color);
        }
        
        .subject-card-footer {
            padding: 0 1.5rem 1.5rem;
        }
        
        .features {
            background-color: white;
            padding: 3rem 1rem;
            margin: 2rem 0;
        }
        
        .features-container {
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .features h2 {
            text-align: center;
            margin-bottom: 2rem;
            color: var(--primary-color);
        }
        
        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
        }
        
        .feature-card {
            text-align: center;
            padding: 2rem;
            border-radius: 8px;
            background-color: var(--light-color);
            transition: all 0.3s;
        }
        
        .feature-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 16px rgba(0,0,0,0.1);
        }
        
        .feature-icon {
            font-size: 2.5rem;
            color: var(--primary-color);
            margin-bottom: 1rem;
        }
        
        footer {
            background-color: var(--dark-color);
            color: white;
            padding: 2rem 1rem;
            text-align: center;
        }
        
        .footer-content {
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .footer-content p {
            margin-bottom: 1rem;
        }
        
        .social-links {
            display: flex;
            justify-content: center;
            gap: 1rem;
            margin-top: 1rem;
        }
        
        .social-links a {
            color: white;
            font-size: 1.5rem;
            transition: color 0.3s;
        }
        
        .social-links a:hover {
            color: var(--accent-color);
        }
        
        @media (max-width: 768px) {
            .header-container {
                flex-direction: column;
            }
            
            nav ul {
                margin-top: 1rem;
                flex-wrap: wrap;
                justify-content: center;
            }
            
            nav ul li {
                margin: 0.5rem;
            }
            
            .hero h2 {
                font-size: 2rem;
            }
            
            .subject-grid {
                grid-template-columns: 1fr;
            }
            
            .features-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="header-container">
            <div class="logo">
                <h1>Vestibular UEA 2025</h1>
            </div>
            <nav>
                <ul>
                    <li><a href="#inicio">Início</a></li>
                    <li><a href="#materias">Matérias</a></li>
                    <li><a href="#recursos">Recursos</a></li>
                    <li><a href="#sobre">Sobre</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <section class="hero" id="inicio">
        <div class="hero-content">
            <h2>Prepare-se para o Vestibular UEA 2025</h2>
            <p>Conteúdo programático completo, organizado por disciplina, com recursos para seus estudos</p>
            <a href="#materias" class="btn">Começar a Estudar</a>
            
            <div class="concept-credit">
                <i class="fas fa-lightbulb"></i> Site concebido por Alissa Medeiros
            </div>
        </div>
    </section>

    <section class="subjects" id="materias">
        <h2>Disciplinas do Conteúdo Programático</h2>
        <div class="subject-grid">
            <!-- Língua Portuguesa -->
            <div class="subject-card">
                <div class="subject-card-header">
                    <h3>Língua Portuguesa e Literatura</h3>
                </div>
                <div class="subject-card-body">
                    <ul>
                        <li>Análise de diversos gêneros textuais</li>
                        <li>Recursos linguísticos e semióticos</li>
                        <li>Literatura brasileira e portuguesa</li>
                        <li>Norma culta e variantes linguísticas</li>
                        <li>Obras: Macunaíma, Triste Fim de Policarpo Quaresma, Caligrafia de Deus</li>
                    </ul>
                </div>
                <div class="subject-card-footer">
                    <a href="#" class="btn">Estudar Português</a>
                </div>
            </div>
            
            <!-- Redação -->
            <div class="subject-card">
                <div class="subject-card-header">
                    <h3>Redação</h3>
                </div>
                <div class="subject-card-body">
                    <ul>
                        <li>Texto dissertativo-argumentativo</li>
                        <li>Estruturação de ideias</li>
                        <li>Argumentação e coerência textual</li>
                        <li>Norma culta da língua portuguesa</li>
                        <li>Temas atuais e regionais</li>
                    </ul>
                </div>
                <div class="subject-card-footer">
                    <a href="#" class="btn">Estudar Redação</a>
                </div>
            </div>
            
            <!-- Matemática -->
            <div class="subject-card">
                <div class="subject-card-header">
                    <h3>Matemática</h3>
                </div>
                <div class="subject-card-body">
                    <ul>
                        <li>Números e álgebra</li>
                        <li>Geometria e medidas</li>
                        <li>Probabilidade e estatística</li>
                        <li>Funções e matemática financeira</li>
                        <li>Razão, proporção e porcentagem</li>
                    </ul>
                </div>
                <div class="subject-card-footer">
                    <a href="#" class="btn">Estudar Matemática</a>
                </div>
            </div>
            
            <!-- História -->
            <div class="subject-card">
                <div class="subject-card-header">
                    <h3>História</h3>
                </div>
                <div class="subject-card-body">
                    <ul>
                        <li>História geral e do Brasil</li>
                        <li>História do Amazonas</li>
                        <li>Movimentos sociais</li>
                        <li>Processos históricos regionais</li>
                        <li>Período áureo da borracha</li>
                    </ul>
                </div>
                <div class="subject-card-footer">
                    <a href="#" class="btn">Estudar História</a>
                </div>
            </div>
            
            <!-- Geografia -->
            <div class="subject-card">
                <div class="subject-card-header">
                    <h3>Geografia</h3>
                </div>
                <div class="subject-card-body">
                    <ul>
                        <li>Cartografia e representações</li>
                        <li>Geografia humana e física</li>
                        <li>Questões ambientais</li>
                        <li>Geografia do Amazonas</li>
                        <li>Biomas brasileiros</li>
                    </ul>
                </div>
                <div class="subject-card-footer">
                    <a href="#" class="btn">Estudar Geografia</a>
                </div>
            </div>
            
            <!-- Biologia, Física, Química -->
            <div class="subject-card">
                <div class="subject-card-header">
                    <h3>Ciências da Natureza</h3>
                </div>
                <div class="subject-card-body">
                    <ul>
                        <li>Biologia: ecologia, genética, evolução</li>
                        <li>Física: matéria, energia, universo</li>
                        <li>Química: elementos, reações, ambiente</li>
                        <li>Interdisciplinaridade</li>
                        <li>Questões ambientais da Amazônia</li>
                    </ul>
                </div>
                <div class="subject-card-footer">
                    <a href="#" class="btn">Estudar Ciências</a>
                </div>
            </div>
            
            <!-- Filosofia e Sociologia -->
            <div class="subject-card">
                <div class="subject-card-header">
                    <h3>Humanidades</h3>
                </div>
                <div class="subject-card-body">
                    <ul>
                        <li>Filosofia: ética, política, sociedade</li>
                        <li>Sociologia: movimentos, cultura, trabalho</li>
                        <li>Pensamento crítico</li>
                        <li>Realidade amazônica</li>
                        <li>Movimentos sociais contemporâneos</li>
                    </ul>
                </div>
                <div class="subject-card-footer">
                    <a href="#" class="btn">Estudar Humanidades</a>
                </div>
            </div>
            
            <!-- Arte e Língua Inglesa -->
            <div class="subject-card">
                <div class="subject-card-header">
                    <h3>Arte e Inglês</h3>
                </div>
                <div class="subject-card-body">
                    <ul>
                        <li>Arte: manifestações e linguagens artísticas</li>
                        <li>Inglês: compreensão e interpretação textual</li>
                        <li>Cultura global e local</li>
                        <li>Análise crítica</li>
                        <li>Manifestações culturais amazônicas</li>
                    </ul>
                </div>
                <div class="subject-card-footer">
                    <a href="#" class="btn">Estudar Arte e Inglês</a>
                </div>
            </div>
        </div>
    </section>

    <section class="features" id="recursos">
        <div class="features-container">
            <h2>Recursos de Estudo</h2>
            <div class="features-grid">
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-book"></i>
                    </div>
                    <h3>Resumos</h3>
                    <p>Resumos organizados por disciplina e tópico para estudo eficiente</p>
                </div>
                
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-question-circle"></i>
                    </div>
                    <h3>Exercícios</h3>
                    <p>Questões de vestibulares anteriores e simulados personalizados</p>
                </div>
                
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-chart-line"></i>
                    </div>
                    <h3>Simulados</h3>
                    <p>Testes cronometrados com correção e estatísticas de desempenho</p>
                </div>
                
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-video"></i>
                    </div>
                    <h3>Videoaulas</h3>
                    <p>Explicações em vídeo dos tópicos mais importantes do conteúdo</p>
                </div>
            </div>
        </div>
    </section>

    <footer id="sobre">
        <div class="footer-content">
            <p>Site de estudos para o Vestibular UEA 2025 - Conteúdo não oficial</p>
            <p>Concebido por Alissa Medeiros - Desenvolvido para auxiliar nos estudos</p>
            <p>Baseado no conteúdo programático oficial da Universidade do Estado do Amazonas</p>
            
            <div class="social-links">
                <a href="#"><i class="fab fa-instagram"></i></a>
                <a href="#"><i class="fab fa-twitter"></i></a>
                <a href="#"><i class="fab fa-youtube"></i></a>
                <a href="#"><i class="fab fa-tiktok"></i></a>
            </div>
        </div>
    </footer>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            // Adicionar smooth scrolling para os links de navegação
            document.querySelectorAll('a[href^="#"]').forEach(anchor => {
                anchor.addEventListener('click', function (e) {
                    e.preventDefault();
                    
                    const targetId = this.getAttribute('href');
                    if (targetId === '#') return;
                    
                    const targetElement = document.querySelector(targetId);
                    if (targetElement) {
                        targetElement.scrollIntoView({
                            behavior: 'smooth',
                            block: 'start'
                        });
                    }
                });
            });
            
            // Exemplo de interatividade básica para os cards
            const subjectCards = document.querySelectorAll('.subject-card');
            
            subjectCards.forEach(card => {
                card.addEventListener('click', function(e) {
                    if (!e.target.classList.contains('btn')) {
                        this.querySelector('.btn').click();
                    }
                });
            });
            
            // Animação simples para os elementos ao rolar a página
            const observerOptions = {
                root: null,
                rootMargin: '0px',
                threshold: 0.1
            };
            
            const observer = new IntersectionObserver((entries) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.style.opacity = 1;
                        entry.target.style.transform = 'translateY(0)';
                    }
                });
            }, observerOptions);
            
            // Aplicar animação aos cards de matérias e recursos
            document.querySelectorAll('.subject-card, .feature-card').forEach(card => {
                card.style.opacity = 0;
                card.style.transform = 'translateY(20px)';
                card.style.transition = 'opacity 0.5s ease, transform 0.5s ease';
                observer.observe(card);
            });
        });
    </script>
</body>
</html>
