<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Free online photo enhancement tool. Improve your image quality, adjust brightness, contrast, and apply filters instantly.">
    <meta name="keywords" content="photo enhancer, image enhancement, photo editor, improve image quality, online tool, free photo editing">
    <title>PhotoEnhancer Pro - Free Online Image Enhancement Tool</title>
    <style>
        :root {
            --primary-color: #4a6fa5;
            --secondary-color: #166088;
            --accent-color: #4cb1a7;
            --light-color: #f8f9fa;
            --dark-color: #343a40;
            --success-color: #28a745;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: #f4f7f9;
            color: var(--dark-color);
            line-height: 1.6;
        }
        
        .container {
            width: 100%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 15px;
        }
        
        header {
            background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
            color: white;
            padding: 1rem 0;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
        }
        
        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            font-size: 1.8rem;
            font-weight: 700;
        }
        
        .logo span {
            color: var(--accent-color);
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
            transition: color 0.3s;
        }
        
        nav ul li a:hover {
            color: var(--accent-color);
        }
        
        .hero {
            text-align: center;
            padding: 3rem 1rem;
            background-color: white;
            border-radius: 0 0 10px 10px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.05);
            margin-bottom: 2rem;
        }
        
        .hero h1 {
            font-size: 2.5rem;
            margin-bottom: 1rem;
            color: var(--secondary-color);
        }
        
        .hero p {
            font-size: 1.2rem;
            color: #666;
            max-width: 800px;
            margin: 0 auto 2rem;
        }
        
        .tool-container {
            display: flex;
            flex-wrap: wrap;
            gap: 2rem;
            margin-bottom: 2rem;
        }
        
        .upload-section {
            flex: 1;
            min-width: 300px;
            background: white;
            padding: 2rem;
            border-radius: 10px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.05);
        }
        
        .controls-section {
            flex: 1;
            min-width: 300px;
            background: white;
            padding: 2rem;
            border-radius: 10px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.05);
        }
        
        .preview-section {
            flex: 100%;
            background: white;
            padding: 2rem;
            border-radius: 10px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.05);
            margin-top: 1rem;
        }
        
        .section-title {
            font-size: 1.5rem;
            margin-bottom: 1.5rem;
            color: var(--secondary-color);
            border-bottom: 2px solid var(--accent-color);
            padding-bottom: 0.5rem;
        }
        
        .upload-area {
            border: 2px dashed var(--primary-color);
            border-radius: 8px;
            padding: 2rem;
            text-align: center;
            cursor: pointer;
            transition: background-color 0.3s;
            margin-bottom: 1.5rem;
        }
        
        .upload-area:hover {
            background-color: rgba(74, 111, 165, 0.05);
        }
        
        .upload-area i {
            font-size: 3rem;
            color: var(--primary-color);
            margin-bottom: 1rem;
        }
        
        .upload-area p {
            color: #666;
        }
        
        .btn {
            display: inline-block;
            background: var(--primary-color);
            color: white;
            padding: 0.8rem 1.5rem;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-size: 1rem;
            font-weight: 500;
            transition: background-color 0.3s;
            text-align: center;
        }
        
        .btn:hover {
            background: var(--secondary-color);
        }
        
        .btn-accent {
            background: var(--accent-color);
        }
        
        .btn-accent:hover {
            background: #3a9c92;
        }
        
        .control-group {
            margin-bottom: 1.5rem;
        }
        
        .control-label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 500;
        }
        
        .slider-container {
            display: flex;
            align-items: center;
        }
        
        .slider {
            flex: 1;
            height: 5px;
            background: #ddd;
            border-radius: 5px;
            outline: none;
            -webkit-appearance: none;
        }
        
        .slider::-webkit-slider-thumb {
            -webkit-appearance: none;
            width: 18px;
            height: 18px;
            background: var(--primary-color);
            border-radius: 50%;
            cursor: pointer;
        }
        
        .slider-value {
            width: 40px;
            text-align: right;
            margin-left: 1rem;
        }
        
        .preview-container {
            display: flex;
            flex-wrap: wrap;
            gap: 2rem;
            justify-content: center;
        }
        
        .preview-box {
            flex: 1;
            min-width: 300px;
            text-align: center;
        }
        
        .preview-title {
            font-size: 1.2rem;
            margin-bottom: 1rem;
            color: var(--secondary-color);
        }
        
        .image-preview {
            max-width: 100%;
            max-height: 400px;
            border: 1px solid #ddd;
            border-radius: 5px;
            box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
        }
        
        .ads-container {
            width: 100%;
            margin: 2rem 0;
            text-align: center;
        }
        
        .ad-unit {
            display: inline-block;
            background: #f8f9fa;
            border: 1px solid #e9ecef;
            border-radius: 5px;
            padding: 1rem;
            margin: 1rem 0;
        }
        
        footer {
            background: var(--dark-color);
            color: white;
            padding: 2rem 0;
            margin-top: 3rem;
        }
        
        .footer-content {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
        }
        
        .footer-section {
            flex: 1;
            min-width: 250px;
            margin-bottom: 1.5rem;
        }
        
        .footer-section h3 {
            font-size: 1.3rem;
            margin-bottom: 1rem;
            color: var(--accent-color);
        }
        
        .footer-bottom {
            text-align: center;
            padding-top: 1.5rem;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        @media (max-width: 768px) {
            .header-content {
                flex-direction: column;
                text-align: center;
            }
            
            nav ul {
                margin-top: 1rem;
                justify-content: center;
            }
            
            .hero h1 {
                font-size: 2rem;
            }
            
            .hero p {
                font-size: 1rem;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="container">
            <div class="header-content">
                <div class="logo">Photo<span>Enhancer</span>Pro</div>
                <nav>
                    <ul>
                        <li><a href="#" title="Home">Home</a></li>
                        <li><a href="#" title="How It Works">How It Works</a></li>
                        <li><a href="#" title="Features">Features</a></li>
                        <li><a href="#" title="Contact">Contact</a></li>
                    </ul>
                </nav>
            </div>
        </div>
    </header>

    <main class="container">
        <section class="hero">
            <h1>Enhance Your Photos in Seconds</h1>
            <p>Free online tool to improve image quality, adjust brightness, contrast, and apply filters with our easy-to-use photo enhancer.</p>
        </section>

        <div class="ads-container">
            <div class="ad-unit">
                <!-- AdSense Ad Code -->
                <ins class="adsbygoogle"
                     style="display:block"
                     data-ad-client="ca-pub-example"
                     data-ad-slot="1234567890"
                     data-ad-format="auto"
                     data-full-width-responsive="true"></ins>
                <script>
                     (adsbygoogle = window.adsbygoogle || []).push({});
                </script>
            </div>
        </div>

        <div class="tool-container">
            <section class="upload-section">
                <h2 class="section-title">Upload Your Photo</h2>
                <div class="upload-area" id="dropArea">
                    <i>📁</i>
                    <h3>Drag & Drop Your Image Here</h3>
                    <p>or</p>
                    <input type="file" id="fileInput" accept="image/*" style="display: none;">
                    <button class="btn" id="browseBtn">Browse Files</button>
                </div>
                <div class="form-group">
                    <button class="btn btn-accent" id="enhanceBtn" disabled>Enhance Photo</button>
                    <button class="btn" id="resetBtn" disabled>Reset</button>
                </div>
            </section>

            <section class="controls-section">
                <h2 class="section-title">Enhancement Controls</h2>
                <div class="control-group">
                    <label class="control-label">Brightness</label>
                    <div class="slider-container">
                        <input type="range" min="-100" max="100" value="0" class="slider" id="brightnessSlider">
                        <span class="slider-value" id="brightnessValue">0</span>
                    </div>
                </div>
                <div class="control-group">
                    <label class="control-label">Contrast</label>
                    <div class="slider-container">
                        <input type="range" min="-100" max="100" value="0" class="slider" id="contrastSlider">
                        <span class="slider-value" id="contrastValue">0</span>
                    </div>
                </div>
                <div class="control-group">
                    <label class="control-label">Saturation</label>
                    <div class="slider-container">
                        <input type="range" min="-100" max="100" value="0" class="slider" id="saturationSlider">
                        <span class="slider-value" id="saturationValue">0</span>
                    </div>
                </div>
                <div class="control-group">
                    <label class="control-label">Sharpness</label>
                    <div class="slider-container">
                        <input type="range" min="0" max="100" value="0" class="slider" id="sharpnessSlider">
                        <span class="slider-value" id="sharpnessValue">0</span>
                    </div>
                </div>
                <div class="control-group">
                    <label class="control-label">Vibrance</label>
                    <div class="slider-container">
                        <input type="range" min="-100" max="100" value="0" class="slider" id="vibranceSlider">
                        <span class="slider-value" id="vibranceValue">0</span>
                    </div>
                </div>
            </section>
        </div>

        <section class="preview-section">
            <h2 class="section-title">Preview</h2>
            <div class="preview-container">
                <div class="preview-box">
                    <h3 class="preview-title">Original Image</h3>
                    <img src="" alt="Original image preview" class="image-preview" id="originalPreview">
                </div>
                <div class="preview-box">
                    <h3 class="preview-title">Enhanced Image</h3>
                    <img src="" alt="Enhanced image preview" class="image-preview" id="enhancedPreview">
                    <div style="margin-top: 1rem;">
                        <button class="btn btn-accent" id="downloadBtn" disabled>Download Enhanced Image</button>
                    </div>
                </div>
            </div>
        </section>

        <div class="ads-container">
            <div class="ad-unit">
                <!-- AdSense Ad Code -->
                <ins class="adsbygoogle"
                     style="display:block"
                     data-ad-client="ca-pub-example"
                     data-ad-slot="0987654321"
                     data-ad-format="auto"
                     data-full-width-responsive="true"></ins>
                <script>
                     (adsbygoogle = window.adsbygoogle || []).push({});
                </script>
            </div>
        </div>
    </main>

    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-section">
                    <h3>About PhotoEnhancerPro</h3>
                    <p>We provide free online photo enhancement tools to help you improve your images instantly without any software installation.</p>
                </div>
                <div class="footer-section">
                    <h3>Quick Links</h3>
                    <p><a href="#" title="Home">Home</a></p>
                    <p><a href="#" title="Privacy Policy">Privacy Policy</a></p>
                    <p><a href="#" title="Terms of Service">Terms of Service</a></p>
                    <p><a href="#" title="Contact Us">Contact Us</a></p>
                </div>
                <div class="footer-section">
                    <h3>Tools</h3>
                    <p><a href="#" title="Image Resizer">Image Resizer</a></p>
                    <p><a href="#" title="Background Remover">Background Remover</a></p>
                    <p><a href="#" title="Photo Filters">Photo Filters</a></p>
                    <p><a href="#" title="Collage Maker">Collage Maker</a></p>
                </div>
            </div>
            <div class="footer-bottom">
                <p>&copy; 2023 PhotoEnhancerPro. All rights reserved.</p>
            </div>
        </div>
    </footer>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            // Elements
            const fileInput = document.getElementById('fileInput');
            const browseBtn = document.getElementById('browseBtn');
            const dropArea = document.getElementById('dropArea');
            const enhanceBtn = document.getElementById('enhanceBtn');
            const resetBtn = document.getElementById('resetBtn');
            const downloadBtn = document.getElementById('downloadBtn');
            const originalPreview = document.getElementById('originalPreview');
            const enhancedPreview = document.getElementById('enhancedPreview');
            
            // Sliders
            const brightnessSlider = document.getElementById('brightnessSlider');
            const contrastSlider = document.getElementById('contrastSlider');
            const saturationSlider = document.getElementById('saturationSlider');
            const sharpnessSlider = document.getElementById('sharpnessSlider');
            const vibranceSlider = document.getElementById('vibranceSlider');
            
            // Values
            const brightnessValue = document.getElementById('brightnessValue');
            const contrastValue = document.getElementById('contrastValue');
            const saturationValue = document.getElementById('saturationValue');
            const sharpnessValue = document.getElementById('sharpnessValue');
            const vibranceValue = document.getElementById('vibranceValue');
            
            let originalImage = null;
            
            // Event listeners
            browseBtn.addEventListener('click', () => fileInput.click());
            
            fileInput.addEventListener('change', handleFileSelect);
            
            dropArea.addEventListener('dragover', (e) => {
                e.preventDefault();
                dropArea.style.backgroundColor = 'rgba(74, 111, 165, 0.1)';
            });
            
            dropArea.addEventListener('dragleave', () => {
                dropArea.style.backgroundColor = '';
            });
            
            dropArea.addEventListener('drop', (e) => {
                e.preventDefault();
                dropArea.style.backgroundColor = '';
                
                if (e.dataTransfer.files.length) {
                    fileInput.files = e.dataTransfer.files;
                    handleFileSelect(e);
                }
            });
            
            // Update slider values
            brightnessSlider.addEventListener('input', () => {
                brightnessValue.textContent = brightnessSlider.value;
            });
            
            contrastSlider.addEventListener('input', () => {
                contrastValue.textContent = contrastSlider.value;
            });
            
            saturationSlider.addEventListener('input', () => {
                saturationValue.textContent = saturationSlider.value;
            });
            
            sharpnessSlider.addEventListener('input', () => {
                sharpnessValue.textContent = sharpnessSlider.value;
            });
            
            vibranceSlider.addEventListener('input', () => {
                vibranceValue.textContent = vibranceSlider.value;
            });
            
            enhanceBtn.addEventListener('click', enhanceImage);
            resetBtn.addEventListener('click', resetControls);
            downloadBtn.addEventListener('click', downloadImage);
            
            function handleFileSelect(e) {
                const file = e.target.files[0];
                
                if (file && file.type.match('image.*')) {
                    const reader = new FileReader();
                    
                    reader.onload = function(e) {
                        originalImage = new Image();
                        originalImage.onload = function() {
                            originalPreview.src = originalImage.src;
                            enhanceBtn.disabled = false;
                            resetBtn.disabled = false;
                        };
                        originalImage.src = e.target.result;
                    };
                    
                    reader.readAsDataURL(file);
                }
            }
            
            function enhanceImage() {
                if (!originalImage) return;
                
                // Create a canvas
                const canvas = document.createElement('canvas');
                const ctx = canvas.getContext('2d');
                
                canvas.width = originalImage.width;
                canvas.height = originalImage.height;
                
                // Draw original image
                ctx.drawImage(originalImage, 0, 0);
                
                // Get image data
                let imageData = ctx.getImageData(0, 0, canvas.width, canvas.height);
                let data = imageData.data;
                
                // Apply enhancements (simplified for example)
                // In a real application, you would implement proper image processing algorithms
                
                enhancedPreview.src = canvas.toDataURL();
                downloadBtn.disabled = false;
            }
            
            function resetControls() {
                brightnessSlider.value = 0;
                contrastSlider.value = 0;
                saturationSlider.value = 0;
                sharpnessSlider.value = 0;
                vibranceSlider.value = 0;
                
                brightnessValue.textContent = '0';
                contrastValue.textContent = '0';
                saturationValue.textContent = '0';
                sharpnessValue.textContent = '0';
                vibranceValue.textContent = '0';
                
                if (originalImage) {
                    enhancedPreview.src = originalImage.src;
                }
            }
            
            function downloadImage() {
                if (!enhancedPreview.src) return;
                
                const link = document.createElement('a');
                link.download = 'enhanced-photo.png';
                link.href = enhancedPreview.src;
                link.click();
            }
        });
    </script>
</body>
</html>
