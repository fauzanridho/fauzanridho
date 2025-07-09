<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Fauzan Ridho - Mobile Developer</title>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            color: #333;
            line-height: 1.6;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }
        
        .header {
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            padding: 40px;
            margin-bottom: 30px;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.1);
            text-align: center;
            border: 1px solid rgba(255, 255, 255, 0.3);
        }
        
        .profile-section {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 30px;
            margin-bottom: 30px;
            flex-wrap: wrap;
        }
        
        .profile-info h1 {
            font-size: 3rem;
            background: linear-gradient(45deg, #667eea, #764ba2);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            margin-bottom: 10px;
            font-weight: 700;
        }
        
        .profile-info .title {
            font-size: 1.3rem;
            color: #666;
            margin-bottom: 20px;
        }
        
        .github-stats {
            display: flex;
            gap: 20px;
            justify-content: center;
            flex-wrap: wrap;
        }
        
        .github-stats img {
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease;
        }
        
        .github-stats img:hover {
            transform: translateY(-5px);
        }
        
        .section {
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            padding: 40px;
            margin-bottom: 30px;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.1);
            border: 1px solid rgba(255, 255, 255, 0.3);
        }
        
        .section h2 {
            font-size: 2.2rem;
            color: #333;
            margin-bottom: 25px;
            position: relative;
            padding-left: 20px;
        }
        
        .section h2::before {
            content: '';
            position: absolute;
            left: 0;
            top: 50%;
            transform: translateY(-50%);
            width: 5px;
            height: 30px;
            background: linear-gradient(45deg, #667eea, #764ba2);
            border-radius: 3px;
        }
        
        .about-content {
            font-size: 1.1rem;
            color: #555;
            text-align: justify;
        }
        
        .experience-item {
            padding: 30px;
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
            border-radius: 15px;
            margin-bottom: 20px;
            transition: transform 0.3s ease;
        }
        
        .experience-item:hover {
            transform: translateY(-5px);
        }
        
        .experience-item h3 {
            font-size: 1.5rem;
            color: #333;
            margin-bottom: 10px;
        }
        
        .experience-item .company {
            font-size: 1.1rem;
            color: #667eea;
            font-weight: 600;
            margin-bottom: 5px;
        }
        
        .experience-item .duration {
            color: #666;
            font-style: italic;
            margin-bottom: 15px;
        }
        
        .experience-item ul {
            list-style: none;
            padding-left: 0;
        }
        
        .experience-item li {
            margin-bottom: 10px;
            padding-left: 25px;
            position: relative;
        }
        
        .experience-item li::before {
            content: '▶';
            position: absolute;
            left: 0;
            color: #667eea;
            font-size: 0.8rem;
        }
        
        .project-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .project-card {
            background: linear-gradient(135deg, #ffecd2 0%, #fcb69f 100%);
            border-radius: 15px;
            padding: 30px;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        
        .project-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 30px 60px rgba(0, 0, 0, 0.15);
        }
        
        .project-card h3 {
            font-size: 1.4rem;
            color: #333;
            margin-bottom: 15px;
        }
        
        .project-card .description {
            color: #555;
            margin-bottom: 15px;
        }
        
        .project-card .tech-stack {
            margin-bottom: 15px;
        }
        
        .project-card .tech-stack strong {
            color: #333;
        }
        
        .project-card .role {
            color: #666;
            font-weight: 600;
        }
        
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
        }
        
        .skill-category {
            background: linear-gradient(135deg, #a8edea 0%, #fed6e3 100%);
            border-radius: 15px;
            padding: 25px;
            text-align: center;
            transition: transform 0.3s ease;
        }
        
        .skill-category:hover {
            transform: translateY(-5px);
        }
        
        .skill-category h3 {
            font-size: 1.3rem;
            color: #333;
            margin-bottom: 15px;
        }
        
        .skill-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            justify-content: center;
        }
        
        .skill-tag {
            background: rgba(255, 255, 255, 0.7);
            padding: 8px 15px;
            border-radius: 20px;
            font-size: 0.9rem;
            color: #333;
            border: 1px solid rgba(255, 255, 255, 0.3);
        }
        
        .contact-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
        }
        
        .contact-item {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 25px;
            border-radius: 15px;
            text-align: center;
            text-decoration: none;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        
        .contact-item:hover {
            transform: translateY(-5px);
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.2);
            text-decoration: none;
            color: white;
        }
        
        .contact-item i {
            font-size: 2rem;
            margin-bottom: 10px;
        }
        
        .contact-item .contact-label {
            font-size: 0.9rem;
            opacity: 0.8;
            margin-bottom: 5px;
        }
        
        .contact-item .contact-value {
            font-size: 1rem;
            font-weight: 600;
        }
        
        .floating-elements {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: -1;
        }
        
        .floating-element {
            position: absolute;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            animation: float 6s ease-in-out infinite;
        }
        
        .floating-element:nth-child(1) {
            width: 80px;
            height: 80px;
            top: 20%;
            left: 10%;
            animation-delay: 0s;
        }
        
        .floating-element:nth-child(2) {
            width: 60px;
            height: 60px;
            top: 60%;
            right: 10%;
            animation-delay: 2s;
        }
        
        .floating-element:nth-child(3) {
            width: 100px;
            height: 100px;
            bottom: 20%;
            left: 20%;
            animation-delay: 4s;
        }
        
        @keyframes float {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-20px); }
        }
        
        @media (max-width: 768px) {
            .profile-info h1 {
                font-size: 2.5rem;
            }
            
            .github-stats {
                flex-direction: column;
                align-items: center;
            }
            
            .github-stats img {
                width: 100%;
                max-width: 400px;
            }
            
            .section {
                padding: 25px;
            }
            
            .section h2 {
                font-size: 1.8rem;
            }
        }
    </style>
</head>
<body>
    <div class="floating-elements">
        <div class="floating-element"></div>
        <div class="floating-element"></div>
        <div class="floating-element"></div>
    </div>
    
    <div class="container">
        <div class="header">
            <div class="profile-section">
                <div class="profile-info">
                    <h1>Fauzan Ridho</h1>
                    <div class="title">Mobile Developer @ Bangkit Academy</div>
                </div>
            </div>
            
            <div class="github-stats">
                <img src="https://github-readme-stats-eight-theta.vercel.app/api?username=fauzanridho&show_icons=true&theme=algolia&include_all_commits=true&count_private=true" alt="GitHub Stats" />
                <img src="https://github-readme-stats-eight-theta.vercel.app/api/top-langs/?username=fauzanridho&layout=compact&theme=algolia" alt="Top Languages" />
            </div>
        </div>
        
        <div class="section">
            <h2><i class="fas fa-user"></i> Tentang Saya</h2>
            <div class="about-content">
                Halo! Saya <strong>Fauzan Ridho</strong>, seorang Mobile Developer yang bersemangat di Bangkit Academy. Saya memiliki pengalaman dalam pengembangan aplikasi mobile dan selalu antusias untuk mempelajari teknologi terbaru serta menyelesaikan tantangan pengembangan perangkat lunak. Dengan dedikasi tinggi terhadap kualitas kode dan pengalaman pengguna, saya berkomitmen untuk menciptakan aplikasi mobile yang inovatif dan user-friendly.
            </div>
        </div>
        
        <div class="section">
            <h2><i class="fas fa-briefcase"></i> Pengalaman</h2>
            <div class="experience-item">
                <h3>Mobile Developer</h3>
                <div class="company">Bangkit Academy led by Google, Tokopedia, Gojek, & Traveloka</div>
                <div class="duration">Januari 2024 - Sekarang</div>
                <ul>
                    <li>Mengembangkan aplikasi mobile untuk platform iOS dan Android menggunakan teknologi seperti Flutter, React Native, atau Kotlin/Swift</li>
                    <li>Bekerja sama dengan tim desain dan backend untuk memastikan integrasi yang mulus</li>
                    <li>Memimpin proyek pengembangan aplikasi dari awal hingga peluncuran, termasuk fase perencanaan, pengembangan, dan pemeliharaan</li>
                    <li>Mengimplementasikan berbagai fitur baru berdasarkan umpan balik pengguna dan kebutuhan bisnis</li>
                </ul>
            </div>
        </div>
        
        <div class="section">
            <h2><i class="fas fa-code"></i> Proyek Utama</h2>
            <div class="project-grid">
                <div class="project-card">
                    <h3>🛒 Aplikasi E-Commerce</h3>
                    <div class="description">
                        Aplikasi e-commerce yang memungkinkan pengguna untuk membeli produk secara online dengan antarmuka yang intuitif dan fitur-fitur lengkap untuk pengalaman berbelanja yang optimal.
                    </div>
                    <div class="tech-stack">
                        <strong>Teknologi:</strong> Flutter, Firebase, Payment Gateway Integration
                    </div>
                    <div class="role">
                        <strong>Peran:</strong> Lead Developer
                    </div>
                </div>
                
                <div class="project-card">
                    <h3>📱 Aplikasi Pembelajaran</h3>
                    <div class="description">
                        Platform pembelajaran digital yang menyediakan berbagai kursus online dengan fitur interaktif dan sistem tracking progress yang komprehensif.
                    </div>
                    <div class="tech-stack">
                        <strong>Teknologi:</strong> React Native, Node.js, MongoDB
                    </div>
                    <div class="role">
                        <strong>Peran:</strong> Frontend Developer
                    </div>
                </div>
                
                <div class="project-card">
                    <h3>🎯 Aplikasi Produktivitas</h3>
                    <div class="description">
                        Aplikasi manajemen tugas dan produktivitas dengan fitur reminder, tracking habit, dan analisis performa harian.
                    </div>
                    <div class="tech-stack">
                        <strong>Teknologi:</strong> Kotlin, Room Database, Material Design
                    </div>
                    <div class="role">
                        <strong>Peran:</strong> Android Developer
                    </div>
                </div>
            </div>
        </div>
        
        <div class="section">
            <h2><i class="fas fa-cog"></i> Keterampilan</h2>
            <div class="skills-grid">
                <div class="skill-category">
                    <h3>💻 Bahasa Pemrograman</h3>
                    <div class="skill-tags">
                        <span class="skill-tag">Dart</span>
                        <span class="skill-tag">Kotlin</span>
                        <span class="skill-tag">Swift</span>
                        <span class="skill-tag">Java</span>
                        <span class="skill-tag">JavaScript</span>
                    </div>
                </div>
                
                <div class="skill-category">
                    <h3>🚀 Framework & Library</h3>
                    <div class="skill-tags">
                        <span class="skill-tag">Flutter</span>
                        <span class="skill-tag">React Native</span>
                        <span class="skill-tag">Firebase</span>
                        <span class="skill-tag">SQLite</span>
                    </div>
                </div>
                
                <div class="skill-category">
                    <h3>🛠️ Tools & Platform</h3>
                    <div class="skill-tags">
                        <span class="skill-tag">Git</span>
                        <span class="skill-tag">JIRA</span>
                        <span class="skill-tag">Android Studio</span>
                        <span class="skill-tag">Xcode</span>
                        <span class="skill-tag">Figma</span>
                    </div>
                </div>
            </div>
        </div>
        
        <div class="section">
            <h2><i class="fas fa-envelope"></i> Kontak</h2>
            <div class="contact-grid">
                <a href="mailto:fauzanridho123456@gmail.com" class="contact-item">
                    <i class="fas fa-envelope"></i>
                    <div class="contact-label">Email</div>
                    <div class="contact-value">fauzanridho123456@gmail.com</div>
                </a>
                
                <a href="https://linkedin.com/in/fauzanridho" class="contact-item" target="_blank">
                    <i class="fab fa-linkedin"></i>
                    <div class="contact-label">LinkedIn</div>
                    <div class="contact-value">linkedin.com/in/fauzanridho</div>
                </a>
                
                <a href="https://github.com/fauzanridho" class="contact-item" target="_blank">
                    <i class="fab fa-github"></i>
                    <div class="contact-label">GitHub</div>
                    <div class="contact-value">github.com/fauzanridho</div>
                </a>
                
                <a href="https://wa.me/6281234567890" class="contact-item" target="_blank">
                    <i class="fab fa-whatsapp"></i>
                    <div class="contact-label">WhatsApp</div>
                    <div class="contact-value">+62 812-3456-7890</div>
                </a>
            </div>
        </div>
    </div>
</body>
</html>
