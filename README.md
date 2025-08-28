<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Como Hospedar seu Site no GitHub Pages</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #24292e;
            --secondary: #0366d6;
            --accent: #28a745;
            --light: #f6f8fa;
            --dark: #1F1F1F;
            --text: #333;
            --bg: #ffffff;
            --card-bg: #ffffff;
            --shadow: 0 4px 12px rgba(0,0,0,0.1);
            --transition: all 0.3s ease;
        }

        .dark-mode {
            --primary: #c9d1d9;
            --secondary: #58a6ff;
            --accent: #3fb950;
            --light: #0d1117;
            --dark: #f0f6fc;
            --text: #c9d1d9;
            --bg: #0d1117;
            --card-bg: #161b22;
            --shadow: 0 4px 12px rgba(0,0,0,0.4);
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            transition: var(--transition);
        }
        
        body {
            background-color: var(--bg);
            color: var(--text);
            line-height: 1.6;
        }
        
        header {
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            color: white;
            padding: 2rem 1.5rem;
            text-align: center;
            box-shadow: var(--shadow);
            position: relative;
        }
        
        .header-content {
            max-width: 1000px;
            margin: 0 auto;
            display: flex;
            flex-direction: column;
            align-items: center;
        }
        
        .top-bar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            width: 100%;
            margin-bottom: 1rem;
        }
        
        .theme-switch {
            background: rgba(255, 255, 255, 0.2);
            border: none;
            color: white;
            padding: 0.5rem 1rem;
            border-radius: 20px;
            cursor: pointer;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }
        
        .logo-container {
            display: flex;
            align-items: center;
            justify-content: center;
            margin-bottom: 1rem;
        }
        
        .logo {
            font-size: 2.5rem;
            margin-right: 1rem;
        }
        
        h1 {
            font-size: 2.5rem;
            margin-bottom: 0.5rem;
        }
        
        .subtitle {
            font-size: 1.2rem;
            opacity: 0.9;
            max-width: 800px;
            margin: 0 auto;
        }
        
        .container {
            max-width: 1000px;
            margin: 0 auto;
            padding: 2rem;
        }
        
        .intro {
            text-align: center;
            margin-bottom: 3rem;
            padding: 2rem;
            background: var(--card-bg);
            border-radius: 10px;
            box-shadow: var(--shadow);
        }
        
        .intro p {
            margin-bottom: 1.5rem;
            font-size: 1.1rem;
        }
        
        .steps-container {
            display: flex;
            flex-direction: column;
            gap: 2rem;
            margin-bottom: 3rem;
        }
        
        .step-card {
            background: var(--card-bg);
            border-radius: 10px;
            overflow: hidden;
            box-shadow: var(--shadow);
        }
        
        .step-header {
            background: var(--primary);
            color: white;
            padding: 1.2rem;
            font-size: 1.3rem;
            font-weight: bold;
            display: flex;
            align-items: center;
            gap: 1rem;
        }
        
        .step-number {
            background: white;
            color: var(--primary);
            width: 32px;
            height: 32px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
        }
        
        .step-body {
            padding: 2rem;
        }
        
        .step-body p {
            margin-bottom: 1.5rem;
        }
        
        .code-block {
            background: var(--light);
            border-radius: 5px;
            padding: 1.5rem;
            margin: 1.5rem 0;
            overflow-x: auto;
            font-family: 'Courier New', monospace;
            border-left: 4px solid var(--accent);
        }
        
        .screenshot {
            width: 100%;
            border-radius: 8px;
            margin: 1.5rem 0;
            box-shadow: var(--shadow);
            border: 1px solid #ddd;
        }
        
        .tip-box {
            background: #e6f7ff;
            border-left: 4px solid #1890ff;
            padding: 1rem;
            margin: 1.5rem 0;
            border-radius: 4px;
        }
        
        .dark-mode .tip-box {
            background: #003a8c;
            border-left: 4px solid #096dd9;
        }
        
        .warning-box {
            background: #fff2e8;
            border-left: 4px solid #fa8c16;
            padding: 1rem;
            margin: 1.5rem 0;
            border-radius: 4px;
        }
        
        .dark-mode .warning-box {
            background: #612500;
            border-left: 4px solid #d46b08;
        }
        
        .faq-section {
            background: var(--card-bg);
            border-radius: 10px;
            padding: 2rem;
            margin-bottom: 2.5rem;
            box-shadow: var(--shadow);
        }
        
        .faq-header {
            color: var(--primary);
            margin-bottom: 1.5rem;
            padding-bottom: 0.5rem;
            border-bottom: 2px solid var(--accent);
        }
        
        .faq-item {
            margin-bottom: 1.5rem;
        }
        
        .faq-question {
            font-weight: bold;
            margin-bottom: 0.5rem;
            color: var(--secondary);
            cursor: pointer;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .faq-answer {
            padding: 1rem;
            background: var(--light);
            border-radius: 5px;
            margin-top: 0.5rem;
        }
        
        .dark-mode .faq-answer {
            background: #161b22;
        }
        
        .next-steps {
            background: var(--card-bg);
            border-radius: 10px;
            padding: 2rem;
            margin-bottom: 2.5rem;
            box-shadow: var(--shadow);
        }
        
        .next-steps-header {
            color: var(--primary);
            margin-bottom: 1.5rem;
            padding-bottom: 0.5rem;
            border-bottom: 2px solid var(--accent);
        }
        
        footer {
            background: var(--dark);
            color: white;
            text-align: center;
            padding: 2rem;
            margin-top: 2rem;
        }
        
        .footer-content {
            max-width: 1000px;
            margin: 0 auto;
            display: flex;
            flex-direction: column;
            gap: 1rem;
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
        }
        
        @media (max-width: 768px) {
            h1 {
                font-size: 2rem;
            }
            
            .container {
                padding: 1rem;
            }
            
            .step-body {
                padding: 1.5rem;
            }
            
            .code-block {
                padding: 1rem;
                font-size: 0.9rem;
            }
        }
        
        /* Animações */
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        .animate {
            animation: fadeIn 0.5s ease forwards;
        }
    </style>
</head>
<body>
    <header>
        <div class="header-content">
            <div class="top-bar">
                <button class="theme-switch" id="themeSwitch">
                    <i class="fas fa-moon"></i> Modo Escuro
                </button>
                <div class="logo-container">
                    <span class="logo"><i class="fab fa-github"></i></span>
                    <div>
                        <h1>Como Hospedar no GitHub Pages</h1>
                        <p class="subtitle">Guia completo para colocar seu site do Vestibular UEA 2025 no ar</p>
                    </div>
                </div>
                <div></div>
            </div>
        </div>
    </header>
    
    <div class="container">
        <section class="intro animate">
            <h2>Seu site está pronto, agora vamos colocá-lo online!</h2>
            <p>O GitHub Pages é um serviço gratuito de hospedagem oferecido pelo GitHub que permite publicar sites estáticos diretamente de um repositório. É perfeito para projetos como o seu site de estudos para o vestibular.</p>
            
            <div class="tip-box">
                <p><strong>Dica:</strong> Você não precisa saber programação para seguir este tutorial. Apenas siga os passos cuidadosamente.</p>
            </div>
        </section>
        
        <section class="steps-container">
            <div class="step-card animate">
                <div class="step-header">
                    <div class="step-number">1</div>
                    <span>Crie uma conta no GitHub</span>
                </div>
                <div class="step-body">
                    <p>Se você ainda não tem uma conta no GitHub, acesse <a href="https://github.com/" target="_blank">github.com</a> e clique em "Sign up". Preencha suas informações para criar uma conta gratuita.</p>
                    
                    <div class="tip-box">
                        <p><strong>Dica:</strong> Escolha um nome de usuário profissional, pois ele fará parte do URL do seu site (ex: seunome.github.io).</p>
                    </div>
                </div>
            </div>
            
            <div class="step-card animate">
                <div class="step-header">
                    <div class="step-number">2</div>
                    <span>Crie um novo repositório</span>
                </div>
                <div class="step-body">
                    <p>Após fazer login, clique no ícone "+" no canto superior direito e selecione "New repository".</p>
                    
                    <p><strong>Configurações importantes:</strong></p>
                    <ul>
                        <li><strong>Repository name:</strong> Digite: <code>seuusuario.github.io</code> (substitua "seuusuario" pelo seu nome de usuário)</li>
                        <li><strong>Description:</strong> Adicione uma descrição como "Site do Vestibular UEA 2025"</li>
                        <li><strong>Public:</strong> Deixe o repositório público (gratuito)</li>
                        <li><strong>Initialize this repository with a README:</strong> Marque esta opção</li>
                    </ul>
                    
                    <p>Clique em "Create repository".</p>
                    
                    <div class="warning-box">
                        <p><strong>Importante:</strong> O nome do repositório DEVE seguir o formato <code>seuusuario.github.io</code> para funcionar com o GitHub Pages.</p>
                    </div>
                </div>
            </div>
            
            <div class="step-card animate">
                <div class="step-header">
                    <div class="step-number">3</div>
                    <span>Faça upload dos arquivos do seu site</span>
                </div>
                <div class="step-body">
                    <p>Na página do seu repositório recém-criado, clique no botão "Add file" e selecione "Upload files".</p>
                    
                    <p>Arraste o arquivo HTML do seu site ou clique em "choose your files" para selecioná-lo. Você pode renomear o arquivo para <code>index.html</code> se ainda não tiver feito isso.</p>
                    
                    <div class="tip-box">
                        <p><strong>Dica:</strong> Se você tem múltiplos arquivos (CSS, JS, imagens), faça upload de todos eles. A estrutura de pastas será mantida.</p>
                    </div>
                    
                    <p>Role para baixo da página, adicione uma descrição do commit (ex: "Adicionar site do vestibular") e clique em "Commit changes".</p>
                </div>
            </div>
            
            <div class="step-card animate">
                <div class="step-header">
                    <div class="step-number">4</div>
                    <span>Ative o GitHub Pages</span>
                </div>
                <div class="step-body">
                    <p>No repositório, clique na aba "Settings" (no topo da página, ao lado de "Code").</p>
                    
                    <p>No menu lateral esquerdo, clique em "Pages".</p>
                    
                    <p>Na seção "Source", selecione a branch "main" e a pasta "/ (root)".</p>
                    
                    <p>Clique em "Save".</p>
                    
                    <div class="tip-box">
                        <p><strong>Dica:</strong> Pode levar alguns minutos para que seu site fique disponível. Uma mensagem verde aparecerá quando estiver pronto.</p>
                    </div>
                </div>
            </div>
            
            <div class="step-card animate">
                <div class="step-header">
                    <div class="step-number">5</div>
                    <span>Acesse seu site</span>
                </div>
                <div class="step-body">
                    <p>Após alguns minutos, seu site estará disponível em:</p>
                    
                    <div class="code-block">
                        https://seuusuario.github.io
                    </div>
                    
                    <p>Substitua "seuusuario" pelo seu nome de usuário do GitHub.</p>
                    
                    <div class="tip-box">
                        <p><strong>Dica:</strong> Você pode personalizar seu URL posteriormente com um domínio personalizado se desejar.</p>
                    </div>
                </div>
            </div>
        </section>
        
        <section class="faq-section">
            <h2 class="faq-header">Perguntas Frequentes</h2>
            
            <div class="faq-item">
                <div class="faq-question" onclick="toggleFAQ(this)">
                    Preciso pagar para usar o GitHub Pages?
                    <i class="fas fa-chevron-down"></i>
                </div>
                <div class="faq-answer" style="display: none;">
                    Não, o GitHub Pages é completamente gratuito para repositórios públicos. Existe uma versão paga apenas para repositórios privados, mas para sites pessoais e de projetos, o plano gratuito é mais que suficiente.
                </div>
            </div>
            
            <div class="faq-item">
                <div class="faq-question" onclick="toggleFAQ(this)">
                    Posso usar um domínio personalizado?
                    <i class="fas fa-chevron-down"></i>
                </div>
                <div class="faq-answer" style="display: none;">
                    Sim, você pode configurar um domínio personalizado (como meusite.com) no GitHub Pages. Nas configurações do seu repositório, na seção Pages, há uma opção para adicionar um domínio personalizado. Você também precisará configurar os registros DNS com seu registrador de domínio.
                </div>
            </div>
            
            <div class="faq-item">
                <div class="faq-question" onclick="toggleFAQ(this)">
                    Quais são as limitações do GitHub Pages?
                    <i class="fas fa-chevron-down"></i>
                </div>
                <div class="faq-answer" style="display: none;">
                    O GitHub Pages é ideal para sites estáticos (HTML, CSS, JavaScript). Não suporta tecnologias server-side como PHP ou bancos de dados. Há também limites de banda larga (100GB/mês) e tráfego (10 builds por hora), que são mais que suficientes para a maioria dos sites pessoais.
                </div>
            </div>
            
            <div class="faq-item">
                <div class="faq-question" onclick="toggleFAQ(this)">
                    Como atualizo meu site depois?
                    <i class="fas fa-chevron-down"></i>
                </div>
                <div class="faq-answer" style="display: none;">
                    Para atualizar seu site, basta fazer upload dos novos arquivos ou editar os arquivos existentes diretamente no GitHub através da interface web. Você também pode usar o Git no seu computador para gerenciar as atualizações de forma mais eficiente.
                </div>
            </div>
        </section>
        
        <section class="next-steps">
            <h2 class="next-steps-header">Próximos Passos</h2>
            <p>Agora que você sabe como hospedar seu site, aqui estão algumas sugestões para melhorá-lo ainda mais:</p>
            
            <ul>
                <li>Adicione mais conteúdo sobre o vestibular UEA</li>
                <li>Crie um sistema de simulados online</li>
                <li>Adicione um fórum para discussão entre estudantes</li>
                <li>Inclua videoaulas e materiais em PDF</li>
                <li>Implemente um sistema de comentários</li>
            </ul>
            
            <div class="tip-box">
                <p><strong>Dica Avançada:</strong> Aprenda a usar o Git para versionamento de código. Isso facilitará muito as atualizações do seu site no futuro.</p>
            </div>
        </section>
    </div>
    
    <footer>
        <div class="footer-content">
            <p>Guia criado para o Site do Vestibular UEA 2025</p>
            <p>© 2025 - Todos os direitos reservados</p>
            <div class="social-links">
                <a href="#"><i class="fab fa-github"></i></a>
                <a href="#"><i class="fab fa-instagram"></i></a>
                <a href="#"><i class="fab fa-twitter"></i></a>
            </div>
        </div>
    </footer>

    <script>
        // Alternar modo escuro/claro
        const themeSwitch = document.getElementById('themeSwitch');
        themeSwitch.addEventListener('click', () => {
            document.body.classList.toggle('dark-mode');
            if (document.body.classList.contains('dark-mode')) {
                themeSwitch.innerHTML = '<i class="fas fa-sun"></i> Modo Claro';
            } else {
                themeSwitch.innerHTML = '<i class="fas fa-moon"></i> Modo Escuro';
            }
        });

        // Alternar FAQ
        function toggleFAQ(element) {
            const answer = element.nextElementSibling;
            const icon = element.querySelector('i');
            
            if (answer.style.display === 'none') {
                answer.style.display = 'block';
                icon.classList.remove('fa-chevron-down');
                icon.classList.add('fa-chevron-up');
            } else {
                answer.style.display = 'none';
                icon.classList.remove('fa-chevron-up');
                icon.classList.add('fa-chevron-down');
            }
        }

        // Animação de entrada dos elementos
        document.addEventListener('DOMContentLoaded', () => {
            const animatedElements = document.querySelectorAll('.animate');
            animatedElements.forEach(element => {
                element.style.opacity = '0';
            });
            
            setTimeout(() => {
                animatedElements.forEach(element => {
                    element.style.opacity = '1';
                });
            }, 100);
        });
    </script>
</body>
</html>
