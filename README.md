<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Free YouTube video downloader - Extract and download videos from YouTube in HD quality. Supports MP4, WEBM, 3GP formats for both PC and mobile devices.">
    <meta name="keywords" content="youtube downloader, video extractor, youtube to mp4, download youtube videos, online video converter">
    <meta name="author" content="YouTube Video Extractor">
    <meta name="robots" content="index, follow">
    <title>YouTube Video Extractor & Downloader | Fast & Free</title>
    <link rel="canonical" href="https://yourwebsite.com" />
    
    <!-- Open Graph / Facebook -->
    <meta property="og:type" content="website">
    <meta property="og:url" content="https://yourwebsite.com/">
    <meta property="og:title" content="YouTube Video Extractor & Downloader">
    <meta property="og:description" content="Free YouTube video downloader - Extract and download videos from YouTube in HD quality.">
    <meta property="og:image" content="https://yourwebsite.com/images/preview.jpg">
    
    <!-- Twitter -->
    <meta property="twitter:card" content="summary_large_image">
    <meta property="twitter:url" content="https://yourwebsite.com/">
    <meta property="twitter:title" content="YouTube Video Extractor & Downloader">
    <meta property="twitter:description" content="Free YouTube video downloader - Extract and download videos from YouTube in HD quality.">
    <meta property="twitter:image" content="https://yourwebsite.com/images/preview.jpg">
    
    <!-- Favicon -->
    <link rel="icon" type="image/png" href="favicon.png">
    
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;500;700&display=swap" rel="stylesheet">
    
    <!-- Font Awesome -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    
    <style>
        :root {
            --primary-color: #ff0000;
            --secondary-color: #282828;
            --accent-color: #f1f1f1;
            --text-color: #333333;
            --light-text: #ffffff;
            --shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Roboto', sans-serif;
            line-height: 1.6;
            color: var(--text-color);
            background-color: #f9f9f9;
        }
        
        .container {
            width: 100%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 15px;
        }
        
        header {
            background-color: var(--light-text);
            box-shadow: var(--shadow);
            padding: 15px 0;
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
            display: flex;
            align-items: center;
        }
        
        .logo i {
            color: var(--primary-color);
            font-size: 2rem;
            margin-right: 10px;
        }
        
        .logo h1 {
            font-size: 1.5rem;
            font-weight: 700;
        }
        
        nav ul {
            display: flex;
            list-style: none;
        }
        
        nav ul li {
            margin-left: 20px;
        }
        
        nav ul li a {
            text-decoration: none;
            color: var(--text-color);
            font-weight: 500;
            transition: color 0.3s;
        }
        
        nav ul li a:hover {
            color: var(--primary-color);
        }
        
        .mobile-menu {
            display: none;
            font-size: 1.5rem;
            cursor: pointer;
        }
        
        .hero {
            background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
            color: var(--light-text);
            padding: 60px 0;
            text-align: center;
        }
        
        .hero h2 {
            font-size: 2.5rem;
            margin-bottom: 20px;
        }
        
        .hero p {
            font-size: 1.2rem;
            max-width: 800px;
            margin: 0 auto 30px;
        }
        
        .download-form {
            background-color: var(--light-text);
            padding: 30px;
            border-radius: 8px;
            box-shadow: var(--shadow);
            max-width: 800px;
            margin: -50px auto 0;
            position: relative;
            z-index: 10;
        }
        
        .form-group {
            margin-bottom: 20px;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: 500;
        }
        
        .input-group {
            display: flex;
        }
        
        .input-group input {
            flex: 1;
            padding: 12px 15px;
            border: 1px solid #ddd;
            border-radius: 4px 0 0 4px;
            font-size: 1rem;
        }
        
        .input-group button {
            background-color: var(--primary-color);
            color: var(--light-text);
            border: none;
            padding: 0 20px;
            border-radius: 0 4px 4px 0;
            cursor: pointer;
            font-weight: 500;
            transition: background-color 0.3s;
        }
        
        .input-group button:hover {
            background-color: #cc0000;
        }
        
        .options {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            margin-top: 20px;
        }
        
        .option {
            flex: 1;
            min-width: 150px;
        }
        
        .option select {
            width: 100%;
            padding: 10px;
            border: 1px solid #ddd;
            border-radius: 4px;
        }
        
        .results {
            display: none;
            margin-top: 40px;
            padding: 30px;
            background-color: var(--light-text);
            border-radius: 8px;
            box-shadow: var(--shadow);
        }
        
        .video-info {
            display: flex;
            flex-direction: column;
            align-items: center;
            margin-bottom: 30px;
        }
        
        @media (min-width: 768px) {
            .video-info {
                flex-direction: row;
                align-items: flex-start;
            }
        }
        
        .thumbnail {
            width: 100%;
            max-width: 320px;
            border-radius: 8px;
            margin-bottom: 20px;
        }
        
        @media (min-width: 768px) {
            .thumbnail {
                margin-right: 30px;
                margin-bottom: 0;
            }
        }
        
        .video-details {
            flex: 1;
        }
        
        .video-details h3 {
            font-size: 1.5rem;
            margin-bottom: 10px;
        }
        
        .video-details p {
            margin-bottom: 15px;
            color: #666;
        }
        
        .download-options {
            width: 100%;
        }
        
        .download-options h4 {
            margin-bottom: 20px;
            font-size: 1.2rem;
            border-bottom: 1px solid #eee;
            padding-bottom: 10px;
        }
        
        .quality-options {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 15px;
        }
        
        .quality-option {
            background-color: var(--accent-color);
            padding: 15px;
            border-radius: 6px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .quality-info {
            display: flex;
            align-items: center;
        }
        
        .quality-info i {
            margin-right: 10px;
            color: var(--primary-color);
        }
        
        .download-btn {
            background-color: var(--primary-color);
            color: var(--light-text);
            border: none;
            padding: 8px 15px;
            border-radius: 4px;
            cursor: pointer;
            font-weight: 500;
            transition: background-color 0.3s;
            text-decoration: none;
            font-size: 0.9rem;
        }
        
        .download-btn:hover {
            background-color: #cc0000;
        }
        
        .ad-container {
            margin: 30px 0;
            background-color: #f1f1f1;
            padding: 20px;
            border-radius: 8px;
            text-align: center;
        }
        
        .features {
            padding: 60px 0;
            background-color: var(--light-text);
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 40px;
        }
        
        .section-title h2 {
            font-size: 2rem;
            color: var(--secondary-color);
        }
        
        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .feature-card {
            background-color: var(--accent-color);
            padding: 25px;
            border-radius: 8px;
            text-align: center;
            transition: transform 0.3s;
        }
        
        .feature-card:hover {
            transform: translateY(-5px);
        }
        
        .feature-icon {
            font-size: 2.5rem;
            color: var(--primary-color);
            margin-bottom: 20px;
        }
        
        .feature-card h3 {
            margin-bottom: 15px;
            font-size: 1.3rem;
        }
        
        .how-to-use {
            padding: 60px 0;
            background-color: #f5f5f5;
        }
        
        .steps {
            max-width: 800px;
            margin: 0 auto;
        }
        
        .step {
            display: flex;
            margin-bottom: 30px;
        }
        
        .step-number {
            background-color: var(--primary-color);
            color: var(--light-text);
            width: 40px;
            height: 40px;
            border-radius: 50%;
            display: flex;
            justify-content: center;
            align-items: center;
            font-weight: bold;
            margin-right: 20px;
            flex-shrink: 0;
        }
        
        .step-content h3 {
            margin-bottom: 10px;
        }
        
        footer {
            background-color: var(--secondary-color);
            color: var(--light-text);
            padding: 40px 0 20px;
        }
        
        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 30px;
            margin-bottom: 30px;
        }
        
        .footer-column h3 {
            margin-bottom: 20px;
            font-size: 1.2rem;
        }
        
        .footer-column ul {
            list-style: none;
        }
        
        .footer-column ul li {
            margin-bottom: 10px;
        }
        
        .footer-column ul li a {
            color: #aaa;
            text-decoration: none;
            transition: color 0.3s;
        }
        
        .footer-column ul li a:hover {
            color: var(--light-text);
        }
        
        .social-links {
            display: flex;
            gap: 15px;
        }
        
        .social-links a {
            color: var(--light-text);
            font-size: 1.2rem;
        }
        
        .copyright {
            text-align: center;
            padding-top: 20px;
            border-top: 1px solid #444;
            color: #aaa;
            font-size: 0.9rem;
        }
        
        /* Responsive styles */
        @media (max-width: 768px) {
            .header-content {
                flex-direction: column;
                text-align: center;
            }
            
            nav ul {
                margin-top: 15px;
                justify-content: center;
            }
            
            nav ul li {
                margin: 0 10px;
            }
            
            .hero h2 {
                font-size: 2rem;
            }
            
            .hero p {
                font-size: 1rem;
            }
            
            .download-form {
                padding: 20px;
            }
            
            .input-group {
                flex-direction: column;
            }
            
            .input-group input {
                border-radius: 4px;
                margin-bottom: 10px;
            }
            
            .input-group button {
                border-radius: 4px;
                padding: 12px;
            }
            
            .video-info {
                flex-direction: column;
                align-items: center;
            }
            
            .thumbnail {
                margin-right: 0;
                margin-bottom: 20px;
            }
        }
        
        @media (max-width: 480px) {
            .mobile-menu {
                display: block;
            }
            
            nav {
                display: none;
                width: 100%;
                margin-top: 15px;
            }
            
            nav.active {
                display: block;
            }
            
            nav ul {
                flex-direction: column;
            }
            
            nav ul li {
                margin: 5px 0;
            }
            
            .hero h2 {
                font-size: 1.8rem;
            }
            
            .options {
                flex-direction: column;
            }
            
            .quality-options {
                grid-template-columns: 1fr;
            }
        }
        
        /* Loading spinner */
        .spinner {
            display: none;
            width: 40px;
            height: 40px;
            margin: 20px auto;
            border: 4px solid rgba(0, 0, 0, 0.1);
            border-radius: 50%;
            border-top: 4px solid var(--primary-color);
            animation: spin 1s linear infinite;
        }
        
        @keyframes spin {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }
    </style>
</head>
<body>
    <header>
        <div class="container header-content">
            <div class="logo">
                <i class="fab fa-youtube"></i>
                <h1>YouTube Extractor</h1>
            </div>
            <div class="mobile-menu" id="mobileMenu">
                <i class="fas fa-bars"></i>
            </div>
            <nav id="mainNav">
                <ul>
                    <li><a href="#">Home</a></li>
                    <li><a href="#features">Features</a></li>
                    <li><a href="#how-to-use">How to Use</a></li>
                    <li><a href="#faq">FAQ</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>
    
    <section class="hero">
        <div class="container">
            <h2>Download YouTube Videos in HD Quality</h2>
            <p>Extract and save videos from YouTube quickly and easily. No registration required. Works on all devices.</p>
        </div>
    </section>
    
    <div class="container">
        <div class="download-form">
            <div class="form-group">
                <label for="videoUrl">Enter YouTube Video URL:</label>
                <div class="input-group">
                    <input type="text" id="videoUrl" placeholder="https://www.youtube.com/watch?v=..." required>
                    <button id="extractBtn">Extract</button>
                </div>
            </div>
            
            <div class="options">
                <div class="option">
                    <label for="format">Format:</label>
                    <select id="format">
                        <option value="mp4">MP4</option>
                        <option value="webm">WEBM</option>
                        <option value="3gp">3GP</option>
                    </select>
                </div>
                <div class="option">
                    <label for="quality">Quality:</label>
                    <select id="quality">
                        <option value="highest">Highest Quality</option>
                        <option value="720p">720p HD</option>
                        <option value="480p">480p</option>
                        <option value="360p">360p</option>
                    </select>
                </div>
            </div>
            
            <div class="spinner" id="loadingSpinner"></div>
        </div>
        
        <!-- Ad Container - Top -->
        <div class="ad-container">
            <!-- Replace with your AdSense code -->
            <script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=<script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=ca-pub-7195227609473922"
     crossorigin="anonymous"></script>"
                crossorigin="anonymous"></script>
            <!-- Your Ad Unit -->
            <ins class="adsbygoogle"
                style="display:block"
                data-ad-client="ca-pub-YOUR_PUBLISHER_ID"
                data-ad-slot="YOUR_AD_SLOT_ID"
                data-ad-format="auto"
                data-full-width-responsive="true"></ins>
            <script>
                (adsbygoogle = window.adsbygoogle || []).push({});
            </script>
        </div>
        
        <div class="results" id="results">
            <div class="video-info">
                <img src="" alt="Video Thumbnail" class="thumbnail" id="videoThumbnail">
                <div class="video-details">
                    <h3 id="videoTitle"></h3>
                    <p id="videoDuration"></p>
                    <p id="videoViews"></p>
                    <p id="videoDescription"></p>
                </div>
            </div>
            
            <div class="download-options">
                <h4>Available Download Options:</h4>
                <div class="quality-options" id="qualityOptions">
                    <!-- Quality options will be dynamically inserted here -->
                </div>
            </div>
        </div>
        
        <!-- Ad Container - Middle -->
        <div class="ad-container">
            <!-- Replace with your AdSense code -->
            <script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js<script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=ca-pub-7195227609473922"
     crossorigin="anonymous"></script>?"
                crossorigin="anonymous"></script>
            <!-- Your Ad Unit -->
            <ins class="adsbygoogle"
                style="display:block"
                data-ad-client="ca-pub-YOUR_PUBLISHER_ID"
                data-ad-slot="YOUR_AD_SLOT_ID"
                data-ad-format="auto"
                data-full-width-responsive="true"></ins>
            <script>
                (adsbygoogle = window.adsbygoogle || []).push({});
            </script>
        </div>
    </div>
    
    <section class="features" id="features">
        <div class="container">
            <div class="section-title">
                <h2>Why Choose Our YouTube Downloader</h2>
            </div>
            <div class="features-grid">
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-bolt"></i>
                    </div>
                    <h3>Fast Downloads</h3>
                    <p>Download YouTube videos at high speed with our optimized servers and technology.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-mobile-alt"></i>
                    </div>
                    <h3>Mobile Friendly</h3>
                    <p>Works perfectly on all devices including smartphones and tablets.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-shield-alt"></i>
                    </div>
                    <h3>Safe & Secure</h3>
                    <p>No registration required. We don't store your videos or personal data.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-file-video"></i>
                    </div>
                    <h3>Multiple Formats</h3>
                    <p>Download in MP4, WEBM, 3GP and other popular video formats.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-hdd"></i>
                    </div>
                    <h3>High Quality</h3>
                    <p>Supports HD and 4K video downloads with original quality.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-comment-dollar"></i>
                    </div>
                    <h3>Free Forever</h3>
                    <p>Our service is completely free with no hidden charges.</p>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Ad Container - Middle -->
    <div class="container">
        <div class="ad-container">
            <!-- Replace with your AdSense code -->
            <script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=<script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=ca-pub-7195227609473922"
     crossorigin="anonymous"></script>"
                crossorigin="anonymous"></script>
            <!-- Your Ad Unit -->
            <ins class="adsbygoogle"
                style="display:block"
                data-ad-client="ca-pub-YOUR_PUBLISHER_ID"
                data-ad-slot="YOUR_AD_SLOT_ID"
                data-ad-format="auto"
                data-full-width-responsive="true"></ins>
            <script>
                (adsbygoogle = window.adsbygoogle || []).push({});
            </script>
        </div>
    </div>
    
    <section class="how-to-use" id="how-to-use">
        <div class="container">
            <div class="section-title">
                <h2>How to Download YouTube Videos</h2>
            </div>
            <div class="steps">
                <div class="step">
                    <div class="step-number">1</div>
                    <div class="step-content">
                        <h3>Copy YouTube Video URL</h3>
                        <p>Go to YouTube and copy the URL of the video you want to download from the address bar.</p>
                    </div>
                </div>
                <div class="step">
                    <div class="step-number">2</div>
                    <div class="step-content">
                        <h3>Paste the URL</h3>
                        <p>Paste the YouTube video URL in the input field above and click the "Extract" button.</p>
                    </div>
                </div>
                <div class="step">
                    <div class="step-number">3</div>
                    <div class="step-content">
                        <h3>Select Format & Quality</h3>
                        <p>Choose your preferred video format and quality from the available options.</p>
                    </div>
                </div>
                <div class="step">
                    <div class="step-number">4</div>
                    <div class="step-content">
                        <h3>Download Video</h3>
                        <p>Click the download button and save the video to your device. It's that simple!</p>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-column">
                    <h3>YouTube Extractor</h3>
                    <p>The fastest and easiest way to download YouTube videos in HD quality. No registration required.</p>
                    <div class="social-links">
                        <a href="#"><i class="fab fa-facebook-f"></i></a>
                        <a href="#"><i class="fab fa-twitter"></i></a>
                        <a href="#"><i class="fab fa-instagram"></i></a>
                        <a href="#"><i class="fab fa-youtube"></i></a>
                    </div>
                </div>
                <div class="footer-column">
                    <h3>Quick Links</h3>
                    <ul>
                        <li><a href="#">Home</a></li>
                        <li><a href="#features">Features</a></li>
                        <li><a href="#how-to-use">How to Use</a></li>
                        <li><a href="#faq">FAQ</a></li>
                        <li><a href="#contact">Contact</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Legal</h3>
                    <ul>
                        <li><a href="#">Terms of Service</a></li>
                        <li><a href="#">Privacy Policy</a></li>
                        <li><a href="#">Cookie Policy</a></li>
                        <li><a href="#">DMCA</a></li>
                    </ul>
                </div>
                <div class="footer-column" id="contact">
                    <h3>Contact Us</h3>
                    <ul>
                        <li><i class="fas fa-envelope"></i> support@youtubeextractor.com</li>
                        <li><i class="fas fa-map-marker-alt"></i> 123 Street, City, Country</li>
                    </ul>
                </div>
            </div>
            <div class="copyright">
                <p>&copy; <span id="currentYear"></span> YouTube Video Extractor. All rights reserved.</p>
                <p>Disclaimer: This tool is for educational purposes only. Download only videos you have rights to.</p>
            </div>
        </div>
    </footer>
    
    <script>
        // Mobile menu toggle
        document.getElementById('mobileMenu').addEventListener('click', function() {
            document.getElementById('mainNav').classList.toggle('active');
        });
        
        // Set current year in footer
        document.getElementById('currentYear').textContent = new Date().getFullYear();
        
        // Video extraction functionality
        document.getElementById('extractBtn').addEventListener('click', function() {
            const videoUrl = document.getElementById('videoUrl').value.trim();
            
            if (!videoUrl) {
                alert('Please enter a YouTube video URL');
                return;
            }
            
            // Validate YouTube URL
            if (!isValidYouTubeUrl(videoUrl)) {
                alert('Please enter a valid YouTube video URL');
                return;
            }
            
            // Show loading spinner
            document.getElementById('loadingSpinner').style.display = 'block';
            
            // In a real implementation, you would call your backend API here
            // For demo purposes, we'll simulate an API call with setTimeout
            setTimeout(function() {
                // Hide loading spinner
                document.getElementById('loadingSpinner').style.display = 'none';
                
                // Extract video ID from URL
                const videoId = extractVideoId(videoUrl);
                
                // Simulate video data (in a real app, this would come from your API)
                const videoData = {
                    id: videoId,
                    title: 'Sample YouTube Video Title',
                    duration: '10:30',
                    views: '1,234,567 views',
                    description: 'This is a sample description of the YouTube video. In a real implementation, this would be fetched from YouTube.',
                    thumbnail: `https://img.youtube.com/vi/${videoId}/maxresdefault.jpg`,
                    formats: [
                        { type: 'video', quality: '1080p', format: 'MP4', size: '45.2 MB', url: '#' },
                        { type: 'video', quality: '720p', format: 'MP4', size: '28.7 MB', url: '#' },
                        { type: 'video', quality: '480p', format: 'MP4', size: '15.3 MB', url: '#' },
                        { type: 'video', quality: '360p', format: 'MP4', size: '9.8 MB', url: '#' },
                        { type: 'video', quality: '240p', format: 'MP4', size: '5.2 MB', url: '#' },
                        { type: 'audio', quality: '128kbps', format: 'MP3', size: '3.7 MB', url: '#' }
                    ]
                };
                
                // Display video information
                displayVideoInfo(videoData);
                
                // Show results section
                document.getElementById('results').style.display = 'block';
                
                // Scroll to results
                document.getElementById('results').scrollIntoView({ behavior: 'smooth' });
            }, 1500);
        });
        
        function isValidYouTubeUrl(url) {
            const pattern = /^(https?:\/\/)?(www\.)?(youtube\.com|youtu\.?be)\/.+$/;
            return pattern.test(url);
        }
        
        function extractVideoId(url) {
            // This is a simplified version - in a real app you'd need more robust parsing
            const regExp = /^.*(youtu.be\/|v\/|u\/\w\/|embed\/|watch\?v=|&v=)([^#&?]*).*/;
            const match = url.match(regExp);
            return (match && match[2].length === 11) ? match[2] : 'dQw4w9WgXcQ'; // Default to Rick Astley if invalid
        }
        
        function displayVideoInfo(videoData) {
            // Set video information
            document.getElementById('videoTitle').textContent = videoData.title;
            document.getElementById('videoDuration').textContent = `Duration: ${videoData.duration}`;
            document.getElementById('videoViews').textContent = videoData.views;
            document.getElementById('videoDescription').textContent = videoData.description;
            document.getElementById('videoThumbnail').src = videoData.thumbnail;
            document.getElementById('videoThumbnail').alt = videoData.title;
            
            // Generate download options
            const qualityOptionsContainer = document.getElementById('qualityOptions');
            qualityOptionsContainer.innerHTML = '';
            
            videoData.formats.forEach(format => {
                const optionElement = document.createElement('div');
                optionElement.className = 'quality-option';
                
                const icon = format.type === 'video' ? 'fa-file-video' : 'fa-file-audio';
                
                optionElement.innerHTML = `
                    <div class="quality-info">
                        <i class="fas ${icon}"></i>
                        <div>
                            <strong>${format.quality}</strong>
                            <div>${format.format} • ${format.size}</div>
                        </div>
                    </div>
                    <a href="${format.url}" class="download-btn" download>
                        Download <i class="fas fa-download"></i>
                    </a>
                `;
                
                qualityOptionsContainer.appendChild(optionElement);
            });
        }
        
        // Function to handle actual download (would be implemented in backend)
        function downloadVideo(videoId, format, quality) {
            // In a real implementation, this would:
            // 1. Call your backend API with the video ID, format, and quality
            // 2. The backend would process the YouTube video
            // 3. Return a download URL or initiate the download
            
            console.log(`Downloading video ${videoId} in ${quality} quality as ${format}`);
            
            // For mobile devices, we might want to handle downloads differently
            if (/Android|webOS|iPhone|iPad|iPod|BlackBerry|IEMobile|Opera Mini/i.test(navigator.userAgent)) {
                // Mobile device - might want to open in new tab or use different handling
                window.open(`#download-mobile?videoId=${videoId}&format=${format}&quality=${quality}`, '_blank');
            } else {
                // Desktop - initiate download
                window.location.href = `#download?videoId=${videoId}&format=${format}&quality=${quality}`;
            }
        }
    </script>
</body>
</html>
