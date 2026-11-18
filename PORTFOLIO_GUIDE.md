# Portfolio Modification & Upload Guide
## Author: Neelakantha Sahu
## File: C:\Users\Neelakantha.Sahu\Portfolio\index.html

---

## PART 1: HOW TO MODIFY YOUR PORTFOLIO

### 1. Change Your Name / Title
**Line ~787** (Hero Section)
```html
<h1>Hi, I'm <span>Neelakantha</span><br>Sahu</h1>
<p class="hero-subtitle">Oracle Database Developer | Azure Data Engineer</p>
```

### 2. Change Typing Text (Rotating Roles)
**Line ~1270** (JavaScript Section)
```javascript
const texts = [
    'ETL/ELT Pipeline Developer',
    'Azure Data Engineer',
    'Oracle PL/SQL Expert',
    'Pro*C Developer',
    'Microsoft Fabric Developer'
];
```
- Add or remove roles from this array

### 3. Change Stats Counter (Years, Projects, Technologies)
**Line ~1300** (JavaScript Section)
```javascript
animateCounter('expCount', 4, 1500);   // 4+ Years
animateCounter('projCount', 5, 1500);  // 5+ Projects
animateCounter('techCount', 15, 1500); // 15+ Technologies
```
- Change the numbers (4, 5, 15) to your actual counts

### 4. Change About Me Section
**Line ~810** (About Section)
```html
<h3>Software Developer from Mumbai</h3>
<p>
    Software Developer with approximately 4 years of IT experience...
</p>
```
- Update your summary text here

### 5. Change Personal Info
**Line ~825** (About Info)
```html
<span><strong>Name:</strong> Neelakantha Sahu</span>
<span><strong>Location:</strong> Mumbai</span>
<span><strong>Email:</strong> neelsa99@gmail.com</span>
<span><strong>Notice:</strong> 30 Days</span>
<span><strong>Domain:</strong> Airlines</span>
<span><strong>Relocate:</strong> Yes</span>
```

### 6. Add/Remove Skills
**Line ~860** (Skills Section) - Each skill card looks like:
```html
<div class="skill-card reveal">
    <div class="skill-icon"><i class="fas fa-database"></i></div>
    <h3>Oracle & PL/SQL</h3>
    <div class="skill-tags">
        <span class="skill-tag">Oracle Database</span>
        <span class="skill-tag">SQL</span>
        <!-- Add more tags here -->
    </div>
</div>
```
- To add a new skill tag: `<span class="skill-tag">New Skill</span>`
- To remove: Delete the `<span class="skill-tag">...</span>` line

### 7. Add New Experience
**Line ~940** (Experience Section) - Copy this template:
```html
<div class="timeline-item reveal">
    <div class="timeline-dot"></div>
    <div class="timeline-content">
        <div class="timeline-date"><i class="fas fa-calendar-alt"></i> Start Date - End Date</div>
        <h3>Your Job Title</h3>
        <div class="timeline-company"><i class="fas fa-building"></i> Company Name</div>
        <div class="timeline-location"><i class="fas fa-map-marker-alt"></i> Location</div>
        <div class="timeline-stack">
            <span class="stack-tag">Skill 1</span>
            <span class="stack-tag">Skill 2</span>
        </div>
        <ul class="timeline-points">
            <li>Your achievement or responsibility 1</li>
            <li>Your achievement or responsibility 2</li>
        </ul>
    </div>
</div>
```
- Paste this ABOVE the first timeline-item to add as latest experience

### 8. Change Education
**Line ~1020** (Education Section)
```html
<h3>Bachelor of Computer Applications (BCA)</h3>
<p class="edu-university"><i class="fas fa-university"></i> Berhampur University</p>
<p class="edu-year"><i class="fas fa-calendar"></i> 2017 - 2020</p>
```

### 9. Change Contact Details
**Line ~1050** (Contact Section)
```html
<a href="mailto:neelsa99@gmail.com" class="contact-card">    <!-- Email -->
<a href="tel:+917788882863" class="contact-card">             <!-- Phone -->
<a href="https://linkedin.com/in/neelakantha-sahu-a77085299"  <!-- LinkedIn -->
```

### 10. Change Colors/Theme
**Line ~10** (CSS Root Variables)
```css
:root {
    --primary: #6c5ce7;        /* Main purple color */
    --primary-light: #a29bfe;  /* Light purple */
    --secondary: #00cec9;      /* Teal color */
    --accent: #fd79a8;         /* Pink accent */
    --dark: #0a0a1a;           /* Background dark */
    --dark-card: #12122a;      /* Card background */
    --text: #e0e0e0;           /* Main text color */
    --text-muted: #8a8a9a;     /* Muted text */
}
```
Popular color alternatives:
- Blue theme: `--primary: #0984e3; --primary-light: #74b9ff;`
- Green theme: `--primary: #00b894; --primary-light: #55efc4;`
- Orange theme: `--primary: #e17055; --primary-light: #fab1a0;`

### 11. Add Profile Photo
Replace the icon in About section with an image:
```html
<!-- Change this: -->
<div class="about-image-wrapper">
    <i class="fas fa-code"></i>
</div>

<!-- To this: -->
<div class="about-image-wrapper">
    <img src="photo.jpg" alt="Neelakantha Sahu"
         style="width:100%; height:100%; object-fit:cover; border-radius:30px;">
</div>
```
- Upload `photo.jpg` to same GitHub repository

### 12. Add New Section (e.g., Certifications)
Add this before the Contact section:
```html
<section class="education" id="certifications">
    <div class="section-header reveal">
        <div class="section-tag">Certifications</div>
        <h2 class="section-title">My <span>Certifications</span></h2>
    </div>
    <div class="edu-card reveal">
        <div class="edu-icon"><i class="fas fa-certificate"></i></div>
        <h3>Certification Name</h3>
        <p class="edu-university"><i class="fas fa-building"></i> Issuing Organization</p>
        <p class="edu-year"><i class="fas fa-calendar"></i> Year</p>
    </div>
</section>
```

---

## PART 2: HOW TO UPLOAD CHANGES TO GITHUB

### Method 1: Edit Directly on GitHub (Easiest)
1. Go to your GitHub repository: `https://github.com/<username>/portfolio`
2. Click on `index.html` file
3. Click pencil icon (Edit this file) - top right
4. Make your changes
5. Click **"Commit changes"** green button
6. Changes will be live in 1-2 minutes

### Method 2: Upload Modified File (Replace)
1. Go to your GitHub repository
2. Click on `index.html` file
3. Click **"..."** (three dots) → **"Delete file"** → Commit
4. Go back to repository main page
5. Click **"Add file"** → **"Upload files"**
6. Upload your modified `index.html` from your computer
7. Click **"Commit changes"**
8. Changes will be live in 1-2 minutes

### Method 3: Using Git Command Line
```bash
# Step 1: Clone repository (first time only)
git clone https://github.com/<username>/portfolio.git
cd portfolio

# Step 2: Make changes to index.html in your editor

# Step 3: Stage and commit
git add index.html
git commit -m "Updated portfolio"

# Step 4: Push to GitHub
git push origin main

# Changes will be live in 1-2 minutes
```

---

## PART 3: QUICK REFERENCE

### File Location on Your Computer
```
C:\Users\Neelakantha.Sahu\Portfolio\index.html
```

### Your Public Portfolio URL
```
https://<your-github-username>.github.io/portfolio/
```

### Icon Reference (Font Awesome)
- Database: `<i class="fas fa-database"></i>`
- Code: `<i class="fas fa-code"></i>`
- Cloud: `<i class="fas fa-cloud"></i>`
- Server: `<i class="fas fa-server"></i>`
- Chart: `<i class="fas fa-chart-line"></i>`
- Certificate: `<i class="fas fa-certificate"></i>`
- Star: `<i class="fas fa-star"></i>`
- Phone: `<i class="fas fa-phone"></i>`
- Email: `<i class="fas fa-envelope"></i>`
- LinkedIn: `<i class="fab fa-linkedin-in"></i>`
- GitHub: `<i class="fab fa-github"></i>`
- Full list: https://fontawesome.com/icons

### Tips
- Always test locally before uploading (open index.html in browser)
- Keep a backup of index.html before making changes
- Use Ctrl+F in editor to find specific text to change
- After uploading to GitHub, wait 1-2 minutes and hard refresh (Ctrl+F5)
