
1. Create `index.html`:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Village Empowerment Hub | Reuben Mwaura</title>
    <link rel="stylesheet" href="style.css">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
</head>
<body>
    <!-- Navigation -->
    <nav>
        <div class="logo">Empowerment Hub</div>
        <ul class="nav-links">
            <li><a href="index.html">Home</a></li>
            <li><a href="farmers.html">Farmers Portal</a></li>
            <li><a href="students.html">Students Portal</a></li>
            <li><a href="blogs.html">Blogs/Vlogs</a></li>
            <li><a href="testimonials.html">Testimonials</a></li>
            <li><a href="partners.html">Partners</a></li>
        </ul>
    </nav>

    <!-- Hero Section -->
    <header class="hero">
        <h1>Community Empowerment Platform</h1>
        <p>Connecting farmers, students, and partners for sustainable development</p>
    </header>

    <!-- Main Content -->
    <main>
        <section class="features">
            <div class="feature-card">
                <i class="fas fa-tractor"></i>
                <h3>Farmer Support</h3>
                <p>Access resources, training, and market links</p>
            </div>
            <div class="feature-card">
                <i class="fas fa-graduation-cap"></i>
                <h3>Student Sponsorships</h3>
                <p>Educational support and mentorship programs</p>
            </div>
            <div class="feature-card">
                <i class="fas fa-handshake"></i>
                <h3>Partnerships</h3>
                <p>Collaborate for community development</p>
            </div>
        </section>

        <!-- Social Media Integration -->
        <section class="social-media">
            <h2>Connect With Us</h2>
            <div class="social-icons">
                <a href="#"><i class="fab fa-facebook"></i></a>
                <a href="#"><i class="fab fa-twitter"></i></a>
                <a href="#"><i class="fab fa-linkedin"></i></a>
                <a href="#"><i class="fab fa-tiktok"></i></a>
            </div>
        </section>
    </main>

    <!-- Footer -->
    <footer>
        <p>&copy; 2023 Village Empowerment Hub. Created by Reuben Mwaura</p>
    </footer>

    <script src="script.js"></script>
</body>
</html>
```

2. Create `style.css`:
```css
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: 'Arial', sans-serif;
    line-height: 1.6;
}

nav {
    display: flex;
    justify-content: space-between;
    padding: 1rem 5%;
    background: #2c3e50;
    color: white;
}

.nav-links {
    display: flex;
    gap: 2rem;
    list-style: none;
}

.nav-links a {
    color: white;
    text-decoration: none;
}

.hero {
    text-align: center;
    padding: 4rem 2rem;
    background: #3498db;
    color: white;
}

.features {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 2rem;
    padding: 3rem 5%;
}

.feature-card {
    text-align: center;
    padding: 2rem;
    border-radius: 10px;
    box-shadow: 0 2px 5px rgba(0,0,0,0.1);
}

.social-media {
    text-align: center;
    padding: 3rem 5%;
    background: #f4f4f4;
}

.social-icons {
    font-size: 2rem;
    margin-top: 1rem;
}

.social-icons a {
    margin: 0 1rem;
    color: #2c3e50;
}

footer {
    text-align: center;
    padding: 2rem;
    background: #2c3e50;
    color: white;
}

/* Responsive Design */
@media (max-width: 768px) {
    .nav-links {
        display: none;
    }
    
    .features {
        grid-template-columns: 1fr;
    }
}
```

3. Create additional pages (farmers.html, students.html, etc.) with similar structure. Example for `farmers.html`:
```html
<!-- Similar header/nav as index.html -->
<section class="portal">
    <h2>Farmers Portal</h2>
    <div class="portal-content">
        <div class="resources">
            <h3>Resources</h3>
            <!-- Add resource links -->
        </div>
        <div class="accounting">
            <h3>Records</h3>
            <!-- Add accounting features -->
        </div>
    </div>
</section>
<!-- Similar footer as index.html -->
```

4. Create `script.js`:
```javascript
// Social Media Sharing Functionality
function shareContent(platform) {
    const message = encodeURIComponent("Check out this great initiative!");
    const url = encodeURIComponent(window.location.href);
    
    const platforms = {
        facebook: `https://www.facebook.com/sharer/sharer.php?u=${url}`,
        twitter: `https://twitter.com/intent/tweet?text=${message}&url=${url}`,
        linkedin: `https://www.linkedin.com/shareArticle?mini=true&url=${url}&title=${message}`,
        tiktok: '#' // TikTok requires different implementation
    };

    if (platforms[platform]) {
        window.open(platforms[platform], '_blank');
    }
}

// Form Handling
document.querySelectorAll('form').forEach(form => {
    form.addEventListener('submit', (e) => {
        e.preventDefault();
        // Add form submission logic
    });
});
```# vee-kenya
