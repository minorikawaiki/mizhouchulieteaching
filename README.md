<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>苏轼《江城子・密州出猎》教学网站</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary-color: #3a5a40;
            --secondary-color: #588157;
            --accent-color: #a3b18a;
            --light-color: #dad7cd;
            --text-color: #344e41;
        }
        
        body {
            font-family: 'Noto Serif SC', 'SimSun', serif;
            background-color: #f8f9fa;
            color: var(--text-color);
            background-image: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="100" height="100" viewBox="0 0 100 100"><rect width="100" height="100" fill="%23f8f9fa"/><path d="M0 50 L100 50 M50 0 L50 100" stroke="%23e9ecef" stroke-width="0.5"/></svg>');
        }
        
        .header-bg {
            background: linear-gradient(135deg, var(--primary-color) 0%, var(--secondary-color) 100%);
            color: white;
            padding: 3rem 0;
            margin-bottom: 2rem;
            box-shadow: 0 4px 12px rgba(0,0,0,0.1);
            position: relative;
            overflow: hidden;
        }
        
        .header-bg::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-image: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="100" height="100" viewBox="0 0 100 100"><path d="M0 0 L100 100 M100 0 L0 100" stroke="%23ffffff20" stroke-width="1"/></svg>');
            opacity: 0.3;
        }
        
        .poem-title {
            font-family: 'STKaiti', 'KaiTi', serif;
            font-size: 2.8rem;
            letter-spacing: 8px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
            margin-bottom: 1rem;
        }
        
        .author {
            font-size: 1.4rem;
            opacity: 0.9;
        }
        
        .poem-content {
            font-family: 'STKaiti', 'KaiTi', serif;
            font-size: 1.6rem;
            line-height: 2.8;
            text-align: center;
            margin: 3rem 0;
            padding: 2rem;
            background: rgba(255, 255, 255, 0.9);
            border-radius: 12px;
            box-shadow: 0 6px 20px rgba(0,0,0,0.08);
            border-left: 5px solid var(--accent-color);
        }
        
        .section-title {
            position: relative;
            padding-bottom: 15px;
            margin-bottom: 30px;
            border-bottom: 2px solid var(--accent-color);
            font-weight: 700;
            color: var(--primary-color);
        }
        
        .section-title::after {
            content: "";
            position: absolute;
            bottom: -2px;
            left: 0;
            width: 100px;
            height: 4px;
            background: var(--primary-color);
        }
        
        .card {
            border: none;
            border-radius: 12px;
            box-shadow: 0 6px 15px rgba(0,0,0,0.08);
            transition: transform 0.3s, box-shadow 0.3s;
            margin-bottom: 1.5rem;
            overflow: hidden;
        }
        
        .card:hover {
            transform: translateY(-5px);
            box-shadow: 0 12px 25px rgba(0,0,0,0.15);
        }
        
        .card-header {
            background: linear-gradient(to right, var(--primary-color), var(--secondary-color));
            color: white;
            font-weight: 600;
            padding: 1rem 1.5rem;
        }
        
        .teaching-point {
            background: white;
            padding: 1.5rem;
            border-radius: 8px;
            margin-bottom: 1.5rem;
            border-left: 4px solid var(--accent-color);
        }
        
        .btn-primary {
            background: var(--primary-color);
            border: none;
            padding: 0.6rem 1.5rem;
            border-radius: 30px;
            font-weight: 600;
            transition: all 0.3s;
        }
        
        .btn-primary:hover {
            background: var(--secondary-color);
            transform: translateY(-3px);
        }
        
        .exam-container {
            background: white;
            border-radius: 12px;
            padding: 2.5rem;
            box-shadow: 0 8px 25px rgba(0,0,0,0.1);
            margin-bottom: 3rem;
        }
        
        .question {
            margin-bottom: 2rem;
            padding-bottom: 1.5rem;
            border-bottom: 1px dashed #dee2e6;
        }
        
        .answer-highlight {
            background: #e8f5e9;
            padding: 0.2rem 0.5rem;
            border-radius: 4px;
            font-weight: 600;
            color: var(--primary-color);
        }
        
        .timeline {
            position: relative;
            padding-left: 30px;
            margin: 2rem 0;
        }
        
        .timeline::before {
            content: "";
            position: absolute;
            left: 6px;
            top: 0;
            height: 100%;
            width: 2px;
            background: var(--accent-color);
        }
        
        .timeline-item {
            position: relative;
            margin-bottom: 2rem;
            padding-left: 20px;
        }
        
        .timeline-item::before {
            content: "";
            position: absolute;
            left: -8px;
            top: 8px;
            width: 16px;
            height: 16px;
            border-radius: 50%;
            background: var(--primary-color);
            border: 3px solid white;
            box-shadow: 0 0 0 2px var(--primary-color);
        }
        
        .quote-box {
            background: rgba(163, 177, 138, 0.15);
            border-left: 4px solid var(--accent-color);
            padding: 1.5rem;
            margin: 1.5rem 0;
            border-radius: 0 8px 8px 0;
            font-style: italic;
        }
        
        .footer {
            background: var(--text-color);
            color: white;
            padding: 3rem 0;
            margin-top: 3rem;
        }
        
        @media (max-width: 768px) {
            .poem-title {
                font-size: 2.2rem;
            }
            .poem-content {
                font-size: 1.3rem;
                line-height: 2.2;
                padding: 1.5rem;
            }
            .exam-container {
                padding: 1.5rem;
            }
        }
    </style>
</head>
<body>
    <!-- 顶部标题区域 -->
    <div class="header-bg text-center">
        <div class="container">
            <h1 class="poem-title">江城子・密州出猎</h1>
            <p class="author">宋 · 苏轼</p>
        </div>
    </div>
    
    <div class="container">
        <!-- 诗词展示区 -->
        <section class="mb-5">
            <div class="poem-content">
                <p>老夫聊发少年狂，左牵黄，右擎苍，</p>
                <p>锦帽貂裘，千骑卷平冈。</p>
                <p>为报倾城随太守，亲射虎，看孙郎。</p>
                <p class="mt-4">酒酣胸胆尚开张，鬓微霜，又何妨！</p>
                <p>持节云中，何日遣冯唐？</p>
                <p>会挽雕弓如满月，西北望，射天狼。</p>
            </div>
        </section>
        
        <!-- 教学要点区 -->
        <section class="mb-5">
            <h2 class="section-title"><i class="fas fa-book-open me-2"></i>教学要点解析</h2>
            
            <div class="row">
                <div class="col-md-4 mb-4">
                    <div class="card h-100">
                        <div class="card-header">词人简介</div>
                        <div class="card-body">
                            <p><strong>苏轼</strong>（1037-1101），字子瞻，号东坡居士，北宋著名文学家、书画家。</p>
                            <p>此词作于宋神宗熙宁八年（1075）冬，苏轼任密州知州时。</p>
                            <p>豪放词派代表人物，与辛弃疾并称"苏辛"。</p>
                        </div>
                    </div>
                </div>
                
                <div class="col-md-4 mb-4">
                    <div class="card h-100">
                        <div class="card-header">教学目标</div>
                        <div class="card-body">
                            <ul>
                                <li>有感情地吟诵诗词，熟读成诵</li>
                                <li>品析词人之"狂"，赏析豪放派词风</li>
                                <li>理解词人豪迈的英雄气概和壮志难酬、渴望建功立业的思想感情</li>
                            </ul>
                        </div>
                    </div>
                </div>
                
                <div class="col-md-4 mb-4">
                    <div class="card h-100">
                        <div class="card-header">教学重难点</div>
                        <div class="card-body">
                            <ul>
                                <li>理解壮志难酬、渴望建功立业报效国家的思想感情</li>
                                <li>赏析豪迈的英雄气概</li>
                                <li>学习赏析豪放派诗词的方法</li>
                            </ul>
                        </div>
                    </div>
                </div>
            </div>
            
            <div class="teaching-point">
                <h4><i class="fas fa-feather-alt me-2"></i>核心词眼："狂"</h4>
                <div class="row mt-3">
                    <div class="col-md-4">
                        <h5>装束之狂</h5>
                        <p>"左牵黄，右擎苍，锦帽貂裘"勾画出太守形象雄姿英发</p>
                        <p>"鬓微霜"补充外貌特征</p>
                    </div>
                    <div class="col-md-4">
                        <h5>气概之狂</h5>
                        <p>"亲射虎，看孙郎" - 自比孙权</p>
                        <p>"会挽雕弓如满月，西北望，射天狼" - 以天狼星喻辽夏军队</p>
                        <p>表达杀敌报国、建功立业的愿望</p>
                    </div>
                    <div class="col-md-4">
                        <h5>心境之狂</h5>
                        <p>"持节云中，何日遣冯唐" - 自比魏尚</p>
                        <p>表达渴望被重用的愿望</p>
                        <p>体现旷然坦荡、心胸开阔的心境</p>
                    </div>
                </div>
            </div>
        </section>
        
        <!-- 艺术手法解析 -->
        <section class="mb-5">
            <h2 class="section-title"><i class="fas fa-paint-brush me-2"></i>艺术手法解析</h2>
            
            <div class="row">
                <div class="col-md-6 mb-4">
                    <div class="card h-100">
                        <div class="card-header">用典手法</div>
                        <div class="card-body">
                            <p><strong>1. 孙权射虎</strong> - "亲射虎，看孙郎"</p>
                            <p>表现作者的少年狂气和英雄气概</p>
                            
                            <p class="mt-3"><strong>2. 冯唐持节</strong> - "持节云中，何日遣冯唐"</p>
                            <p>以魏尚自许，表达渴望被朝廷重用的愿望</p>
                            
                            <p class="mt-3"><strong>3. 天狼星</strong> - "西北望，射天狼"</p>
                            <p>喻指辽和西夏的侵略，表达抵御外侮的决心</p>
                        </div>
                    </div>
                </div>
                
                <div class="col-md-6 mb-4">
                    <div class="card h-100">
                        <div class="card-header">豪放词风特点</div>
                        <div class="card-body">
                            <ul>
                                <li>场面宏大："千骑卷平冈"展现雄伟壮观的出猎场面</li>
                                <li>情感豪迈：贯穿全词的报国豪情</li>
                                <li>语言雄健：动词"卷"、"挽"、"射"等极具力度</li>
                                <li>意境开阔：从出猎场景到报国志向的升华</li>
                            </ul>
                            
                            <div class="quote-box mt-3">
                                <p>"词至东坡，倾荡磊落，如诗如文，如天地奇观。"</p>
                                <p class="text-end mb-0">——刘辰翁《辛稼轩词序》</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>
        
        <!-- 在线试卷 -->
        <section class="mb-5">
            <h2 class="section-title"><i class="fas fa-file-alt me-2"></i>在线测试卷</h2>
            
            <div class="exam-container">
                <div class="alert alert-primary">
                    <i class="fas fa-info-circle me-2"></i>本试卷共四部分，满分100分，答题时间45分钟
                </div>
                
                <h4 class="mt-4 mb-3">一、选择题（每题3分，共30分）</h4>
                
                <div class="question">
                    <p><strong>1. 《江城子・密州出猎》的作者是（ ）</strong></p>
                    <div class="form-check">
                        <input class="form-check-input" type="radio" name="q1" id="q1a">
                        <label class="form-check-label" for="q1a">A. 辛弃疾</label>
                    </div>
                    <div class="form-check">
                        <input class="form-check-input" type="radio" name="q1" id="q1b" checked>
                        <label class="form-check-label" for="q1b"><span class="answer-highlight">B. 苏轼</span></label>
                    </div>
                    <div class="form-check">
                        <input class="form-check-input" type="radio" name="q1" id="q1c">
                        <label class="form-check-label" for="q1c">C. 李清照</label>
                    </div>
                    <div class="form-check">
                        <input class="form-check-input" type="radio" name="q1" id="q1d">
                        <label class="form-check-label" for="q1d">D. 柳永</label>
                    </div>
                </div>
                
                <div class="question">
                    <p><strong>2. 下列对"老夫聊发少年狂"中"狂"字理解不正确的一项是（ ）</strong></p>
                    <div class="form-check">
                        <input class="form-check-input" type="radio" name="q2" id="q2a">
                        <label class="form-check-label" for="q2a">A. 表现作者要尽情一抒渴望立功报国豪情的心情</label>
                    </div>
                    <div class="form-check">
                        <input class="form-check-input" type="radio" name="q2" id="q2b" checked>
                        <label class="form-check-label" for="q2b"><span class="answer-highlight">B. 是狂妄自大的体现</span></label>
                    </div>
                    <div class="form-check">
                        <input class="form-check-input" type="radio" name="q2" id="q2c">
                        <label class="form-check-label" for="q2c">C. 奠定了全词粗犷豪迈的感情基调</label>
                    </div>
                    <div class="form-check">
                        <input class="form-check-input" type="radio" name="q2" id="q2d">
                        <label class="form-check-label" for="q2d">D. 统领全词，贯穿始终</label>
                    </div>
                </div>
                
                <div class="text-center mt-4">
                    <button class="btn btn-primary btn-lg"><i class="fas fa-paper-plane me-2"></i>提交试卷</button>
                </div>
            </div>
        </section>
        
        <!-- 拓展延伸 -->
        <section class="mb-5">
            <h2 class="section-title"><i class="fas fa-expand-arrows-alt me-2"></i>拓展延伸</h2>
            
            <div class="row">
                <div class="col-md-6">
                    <div class="card">
                        <div class="card-header">对比阅读：陆游《诉衷情》</div>
                        <div class="card-body">
                            <p class="text-center fst-italic">当年万里觅封侯，匹马戍梁州。<br>
                            关河梦断何处？尘暗旧貂裘。<br>
                            胡未灭，鬓先秋，泪空流。<br>
                            此生谁料，心在天山，身老沧洲。</p>
                            
                            <p><strong>对比分析：</strong></p>
                            <ul>
                                <li>相同点：豪放悲壮，用典手法，壮志难酬的感慨</li>
                                <li>不同点：苏轼对未来充满希望，陆游更多英雄迟暮的无奈</li>
                            </ul>
                        </div>
                    </div>
                </div>
                
                <div class="col-md-6">
                    <div class="card">
                        <div class="card-header">豪放派代表作品</div>
                        <div class="card-body">
                            <ul>
                                <li>苏轼《念奴娇·赤壁怀古》</li>
                                <li>辛弃疾《破阵子·为陈同甫赋壮词以寄之》</li>
                                <li>辛弃疾《永遇乐·京口北固亭怀古》</li>
                                <li>岳飞《满江红·写怀》</li>
                            </ul>
                            
                            <div class="mt-3">
                                <h5>课后作业：</h5>
                                <ol>
                                    <li>总结词中运用用典的词句及其作用</li>
                                    <li>选取一首豪放派词进行赏析</li>
                                </ol>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>
    </div>
    
    <!-- 页脚 -->
    <footer class="footer">
        <div class="container">
            <div class="row">
                <div class="col-md-6">
                    <h5>《江城子・密州出猎》教学资源</h5>
                    <p>本网站提供苏轼词作《江城子・密州出猎》的全面教学资源，包括诗词赏析、教学要点、在线测试及拓展阅读。</p>
                </div>
                <div class="col-md-6 text-end">
                    <p>教学设计：中学语文教研组</p>
                    <p>资料整理时间：2023年10月</p>
                </div>
            </div>
            <hr class="mt-4 mb-4" style="background-color: rgba(255,255,255,0.1);">
            <p class="text-center mb-0">© 2023 古典诗词教学网 | 弘扬传统文化，传承诗词经典</p>
        </div>
    </footer>
    
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html># mizhouchulieteaching
