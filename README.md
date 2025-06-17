<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>苏轼《江城子·密州出猎》教学资源</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Microsoft YaHei', 'STHeiti', sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #f5f7fa 0%, #e4edf5 100%);
            color: #333;
            line-height: 1.6;
            padding-bottom: 40px;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        header {
            background: linear-gradient(90deg, #1a3a5f 0%, #2c5a8a 100%);
            color: white;
            padding: 20px 0;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
            position: sticky;
            top: 0;
            z-index: 100;
        }
        
        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            font-size: 28px;
            font-weight: bold;
            display: flex;
            align-items: center;
        }
        
        .logo i {
            margin-right: 10px;
            color: #ffcc00;
        }
        
        nav ul {
            display: flex;
            list-style: none;
        }
        
        nav ul li {
            margin-left: 25px;
        }
        
        nav ul li a {
            color: white;
            text-decoration: none;
            font-size: 18px;
            padding: 8px 15px;
            border-radius: 5px;
            transition: all 0.3s ease;
        }
        
        nav ul li a:hover {
            background: rgba(255, 255, 255, 0.15);
        }
        
        .hero {
            background: url('https://images.unsplash.com/photo-1504813184591-01572f98c85f?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1200&q=80') no-repeat center center/cover;
            height: 450px;
            display: flex;
            align-items: center;
            justify-content: center;
            position: relative;
            margin-bottom: 50px;
            border-radius: 0 0 10px 10px;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
        }
        
        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.5);
            border-radius: 0 0 10px 10px;
        }
        
        .hero-content {
            text-align: center;
            color: white;
            z-index: 2;
            max-width: 800px;
            padding: 0 20px;
        }
        
        .hero-content h1 {
            font-size: 48px;
            margin-bottom: 20px;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
        }
        
        .hero-content p {
            font-size: 22px;
            margin-bottom: 30px;
            text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.5);
        }
        
        .btn {
            display: inline-block;
            background: #ff6b3d;
            color: white;
            padding: 12px 30px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: bold;
            font-size: 18px;
            transition: all 0.3s ease;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
        }
        
        .btn:hover {
            background: #ff4f1a;
            transform: translateY(-3px);
            box-shadow: 0 6px 15px rgba(0, 0, 0, 0.3);
        }
        
        .section-title {
            text-align: center;
            margin: 50px 0 40px;
            color: #1a3a5f;
            position: relative;
            font-size: 36px;
        }
        
        .section-title::after {
            content: '';
            display: block;
            width: 80px;
            height: 4px;
            background: #ff6b3d;
            margin: 15px auto;
            border-radius: 2px;
        }
        
        .author-section {
            display: flex;
            gap: 40px;
            margin-bottom: 60px;
            background: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
        }
        
        .author-image {
            flex: 1;
            min-width: 300px;
            background: url('https://images.unsplash.com/photo-1563291074-2bf8677ac0e5?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80') center center/cover;
        }
        
        .author-info {
            flex: 2;
            padding: 30px;
        }
        
        .author-info h2 {
            color: #1a3a5f;
            margin-bottom: 20px;
            font-size: 32px;
        }
        
        .author-info p {
            margin-bottom: 20px;
            font-size: 18px;
            line-height: 1.8;
        }
        
        .highlight {
            background: #f0f7ff;
            padding: 20px;
            border-left: 4px solid #2c5a8a;
            margin: 25px 0;
            font-style: italic;
        }
        
        .poem-content {
            background: white;
            padding: 40px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
            margin-bottom: 60px;
            line-height: 2;
            font-size: 20px;
            text-align: center;
        }
        
        .poem-title {
            font-size: 32px;
            color: #1a3a5f;
            margin-bottom: 10px;
        }
        
        .poem-author {
            font-size: 20px;
            color: #666;
            margin-bottom: 30px;
        }
        
        .poem-text {
            margin: 30px 0;
            font-size: 22px;
            line-height: 2.2;
            text-align: center;
        }
        
        .analysis-section {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin-bottom: 60px;
        }
        
        .analysis-card {
            background: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
            transition: all 0.3s ease;
        }
        
        .analysis-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.15);
        }
        
        .card-header {
            background: #2c5a8a;
            color: white;
            padding: 20px;
            text-align: center;
            font-size: 22px;
        }
        
        .card-content {
            padding: 25px;
            font-size: 17px;
        }
        
        .card-content h3 {
            color: #1a3a5f;
            margin-bottom: 15px;
            font-size: 20px;
        }
        
        .card-content p {
            margin-bottom: 15px;
            line-height: 1.7;
        }
        
        .resources-section {
            background: white;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
            padding: 40px;
            margin-bottom: 60px;
        }
        
        .resource-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin-top: 30px;
        }
        
        .resource-card {
            background: #f0f7ff;
            border-radius: 10px;
            padding: 30px;
            text-align: center;
            transition: all 0.3s ease;
        }
        
        .resource-card:hover {
            background: #e1edfa;
            transform: translateY(-5px);
        }
        
        .resource-card i {
            font-size: 48px;
            color: #2c5a8a;
            margin-bottom: 20px;
        }
        
        .resource-card h3 {
            color: #1a3a5f;
            margin-bottom: 15px;
            font-size: 22px;
        }
        
        .resource-card p {
            margin-bottom: 20px;
            color: #555;
        }
        
        .resource-link {
            display: inline-block;
            background: #2c5a8a;
            color: white;
            padding: 10px 25px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: bold;
            transition: all 0.3s ease;
        }
        
        .resource-link:hover {
            background: #1a3a5f;
        }
        
        footer {
            background: #1a3a5f;
            color: white;
            text-align: center;
            padding: 30px 0;
            margin-top: 50px;
            border-radius: 10px 10px 0 0;
        }
        
        .footer-content {
            display: flex;
            flex-direction: column;
            align-items: center;
        }
        
        .social-icons {
            margin: 20px 0;
        }
        
        .social-icons a {
            display: inline-block;
            color: white;
            background: rgba(255, 255, 255, 0.1);
            width: 40px;
            height: 40px;
            line-height: 40px;
            border-radius: 50%;
            margin: 0 8px;
            transition: all 0.3s ease;
        }
        
        .social-icons a:hover {
            background: #ff6b3d;
            transform: translateY(-5px);
        }
        
        @media (max-width: 768px) {
            .header-content {
                flex-direction: column;
            }
            
            nav ul {
                margin-top: 20px;
                flex-wrap: wrap;
                justify-content: center;
            }
            
            nav ul li {
                margin: 5px 10px;
            }
            
            .author-section {
                flex-direction: column;
            }
            
            .author-image {
                min-height: 300px;
            }
            
            .hero-content h1 {
                font-size: 36px;
            }
            
            .hero-content p {
                font-size: 18px;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="container header-content">
            <div class="logo">
                <i class="fas fa-book-open"></i>
                <span>宋词鉴赏</span>
            </div>
            <nav>
                <ul>
                    <li><a href="#author">作者介绍</a></li>
                    <li><a href="#poem">词作赏析</a></li>
                    <li><a href="#analysis">词中"狂"字</a></li>
                    <li><a href="#resources">教学资源</a></li>
                </ul>
            </nav>
        </div>
    </header>
    
    <div class="hero">
        <div class="hero-content">
            <h1>苏轼《江城子·密州出猎》</h1>
            <p>豪放词风的典范之作，感受词人壮志豪情</p>
            <a href="#poem" class="btn">开始赏析</a>
        </div>
    </div>
    
    <div class="container">
        <section id="author" class="author-section">
            <div class="author-image"></div>
            <div class="author-info">
                <h2>苏轼（1037-1101）</h2>
                <p>苏轼，字子瞻，号东坡居士，北宋著名文学家、书画家、政治家。作为"唐宋八大家"之一，苏轼在诗、词、散文、书法、绘画等各个领域都有极高成就。</p>
                <p>苏轼的词风开创了豪放一派，突破了晚唐五代以来词为"艳科"的传统，大大拓展了词的题材范围，提升了词的艺术境界。《江城子·密州出猎》正是其豪放词风的代表作之一。</p>
                
                <div class="highlight">
                    <p>《江城子·密州出猎》作于苏轼被贬密州期间，反映了他壮志未酬的心境。这首词通过描述出猎的盛大场面，表达了苏轼渴望得到朝廷重用，杀敌报国的壮志豪情。</p>
                </div>
                
                <p>苏轼一生仕途坎坷，多次被贬，但他始终保持着旷达乐观的人生态度。其文学创作既有豪放雄浑的一面，也有婉约细腻的一面，对后世影响深远。</p>
            </div>
        </section>
        
        <h2 class="section-title">词作原文</h2>
        
        <section id="poem" class="poem-content">
            <div class="poem-title">江城子·密州出猎</div>
            <div class="poem-author">【宋】苏轼</div>
            
            <div class="poem-text">
                <p>老夫聊发少年狂，左牵黄，右擎苍，</p>
                <p>锦帽貂裘，千骑卷平冈。</p>
                <p>为报倾城随太守，亲射虎，看孙郎。</p>
                <p>酒酣胸胆尚开张，鬓微霜，又何妨！</p>
                <p>持节云中，何日遣冯唐？</p>
                <p>会挽雕弓如满月，西北望，射天狼。</p>
            </div>
        </section>
        
        <h2 class="section-title">词中"狂"字赏析</h2>
        
        <section id="analysis" class="analysis-section">
            <div class="analysis-card">
                <div class="card-header">装束之狂</div>
                <div class="card-content">
                    <h3>雄姿英发的形象</h3>
                    <p>"左牵黄，右擎苍，锦帽貂裘"等描写，展现了苏轼出猎时的装束，勾画出一个雄姿英发、豪迈英武的太守形象。</p>
                    <p>下阙中的"鬓微霜"是对上阙三句的补充，为我们具体刻画出苏轼当时的外貌特征。</p>
                </div>
            </div>
            
            <div class="analysis-card">
                <div class="card-header">气概之狂</div>
                <div class="card-content">
                    <h3>豪迈英勇的气概</h3>
                    <p>通过"亲射虎，看孙郎"、"会挽雕弓如满月，西北望，射天狼"等句，苏轼将自己比作孙权，将辽夏军队比作天狼星。</p>
                    <p>运用典故表达词人渴望杀敌报国、建功立业的愿望，突显词人豪迈英勇的气概。</p>
                </div>
            </div>
            
            <div class="analysis-card">
                <div class="card-header">心境之狂</div>
                <div class="card-content">
                    <h3>旷达坦荡的心境</h3>
                    <p>"持节云中，何日遣冯唐"运用典故，苏轼自比魏尚，表达渴望被重用的愿望。</p>
                    <p>词人在贬谪期间，对朝廷的期望，对杀敌报国的渴望，远远大过于对被贬谪的失望，体现出词人旷然坦荡、心胸开阔的心境。</p>
                </div>
            </div>
        </section>
        
        <h2 class="section-title">教学资源</h2>
        
        <section id="resources" class="resources-section">
            <div class="resource-grid">
                <div class="resource-card">
                    <i class="fas fa-file-powerpoint"></i>
                    <h3>教学PPT</h3>
                    <p>完整教学课件，包含词作背景、赏析要点和教学指导</p>
                    <a href="https://pan.baidu.com/s/1pSvXxnhr7vqE4kY2VWeLFg" class="resource-link" target="_blank">下载PPT</a>
                </div>
                
                <div class="resource-card">
                    <i class="fas fa-edit"></i>
                    <h3>学情调查表</h3>
                    <p>了解学生对宋词学习的兴趣点和难点</p>
                    <a href="https://www.wenjuan.com/s/UZBZJvlCCh/" class="resource-link" target="_blank">填写调查表</a>
                </div>
                
                <div class="resource-card">
                    <i class="fas fa-book"></i>
                    <h3>课后练习题</h3>
                    <p>巩固学习成果，检验理解程度</p>
                    <a href="https://kaoshi.wjx.top/vm/w1EUP3b.aspx" class="resource-link" target="_blank">开始练习</a>
                </div>
            </div>
            
            <div class="highlight" style="margin-top: 40px;">
                <h3>教学总结</h3>
                <p>通过本课的学习，学生应掌握豪放词从内容、手法、情感三方面的赏析方法，提升古诗词鉴赏能力。重点理解词人的"狂"在装束、气概、心境三方面的表现，体会苏轼壮志难酬、渴望建功立业报效国家的思想感情和豪迈的英雄气概。</p>
            </div>
        </section>
    </div>
    
    <footer>
        <div class="container footer-content">
            <h3>宋词鉴赏教学平台</h3>
            <p>传承中华优秀传统文化 · 提升学生文学素养</p>
            <div class="social-icons">
                <a href="#"><i class="fab fa-weixin"></i></a>
                <a href="#"><i class="fab fa-qq"></i></a>
                <a href="#"><i class="fab fa-weibo"></i></a>
                <a href="#"><i class="fab fa-github"></i></a>
            </div>
            <p>© 2023 宋词鉴赏教学平台 | 设计：姚佳彤</p>
        </div>
    </footer>
    
    <script>
        // 平滑滚动效果
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });
        
        // 卡片悬停动画
        const cards = document.querySelectorAll('.analysis-card, .resource-card');
        cards.forEach(card => {
            card.addEventListener('mouseenter', () => {
                card.style.transform = card.classList.contains('analysis-card') ? 'translateY(-10px)' : 'translateY(-5px)';
            });
            card.addEventListener('mouseleave', () => {
                card.style.transform = 'translateY(0)';
            });
        });
        
        // 页面加载动画
        window.addEventListener('load', () => {
            document.body.style.opacity = 1;
        });
        
        document.body.style.opacity = 0;
        document.body.style.transition = 'opacity 0.8s ease-in';
    </script>
</body>
</html>
