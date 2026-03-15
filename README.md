# Dra. Lizzie Cárdenas - Dental Website

A professional dental clinic website for **Dra. Lizzie Cárdenas**, an orthodontist with over 30 years of experience based in La Paz, Bolivia.

## 🦷 About

This website showcases the dental services offered by Dra. Lizzie Cárdenas, including orthodontics, Invisalign® treatments, pediatric dentistry, and more. The site is designed to be responsive, modern, and user-friendly.

## 📄 Pages

| Page | Description |
|------|-------------|
| `home.html` | Main landing page with hero section, about preview, specialties, testimonials, and contact form |
| `about_me.html` | Detailed biography and credentials of Dra. Lizzie Cárdenas |
| `especialidades.html` | Complete list of dental specialties and services offered |
| `galeria.html` | Photo and video gallery with interactive lightbox |
| `contact.html` | Contact information, WhatsApp link, and Google Maps location |
| `thanks.html` | Confirmation page after successful form submission |

## 🎨 Features

- **Responsive Design** - Works on desktop, tablet, and mobile devices
- **Sticky Navigation** - Navigation bar stays visible while scrolling
- **Interactive Gallery** - Lightbox with keyboard navigation, captions, and video support
- **Contact Form** - Integrated with FormSubmit.co for email delivery
- **WhatsApp Integration** - Direct link to contact via WhatsApp
- **Google Maps** - Embedded map showing clinic location

## 🏥 Specialties

- **Odontología Integral** - Comprehensive dental care
- **Ortodoncia Correctiva Fija** - Fixed orthodontics with brackets (including Damon® system)
- **Ortodoncia Invisible – Invisalign®** - Clear aligner treatment
- **Odontopediatría** - Pediatric dentistry
- **Ortopedia Funcional** - Functional orthopedics for children
- **Estética Dental** - Cosmetic dentistry

## 📁 Project Structure

```
Dental-Site/
├── index.html              # Redirect to home page
├── .htaccess               # Apache server configuration
├── pages/
│   ├── home.html           # Main landing page
│   ├── about_me.html       # About the doctor
│   ├── especialidades.html # Services/specialties
│   ├── galeria.html        # Photo & video gallery
│   ├── contact.html        # Contact information
│   └── thanks.html         # Form submission confirmation
├── assets/
│   ├── css/
│   │   └── shared-styles.css  # Common styles (header, footer, navigation)
│   └── images/
│       ├── galery/            # Gallery images
│       └── ...                # Other images and icons
└── README.md
```

## 🛠️ Technologies

- **HTML5** - Semantic markup
- **CSS3** - Custom styles with responsive media queries
- **JavaScript** - Interactive features (gallery, form handling, navigation)
- **Google Fonts** - Molengo, Libre Franklin, Nunito Sans
- **FormSubmit.co** - Form submission handling

---

## 🚀 Deployment to cPanel

### Prerequisites

- cPanel hosting account with:
  - File Manager access or FTP credentials
  - Domain configured and pointing to the server
  - SSL certificate (recommended)

### Method 1: Upload via cPanel File Manager

1. **Login to cPanel**
   - Go to your hosting provider's cPanel login page
   - Enter your username and password

2. **Open File Manager**
   - In cPanel dashboard, click on **File Manager**
   - Navigate to `public_html` folder (this is your website root)

3. **Upload Files**
   - Click **Upload** button in the toolbar
   - Select all project files and folders:
     - `index.html`
     - `.htaccess`
     - `pages/` folder
     - `assets/` folder
   - Wait for upload to complete

4. **Verify Upload**
   - Ensure all files are in `public_html`:
     ```
     public_html/
     ├── index.html
     ├── .htaccess
     ├── pages/
     └── assets/
     ```

5. **Set Permissions** (if needed)
   - Right-click on files/folders → **Change Permissions**
   - Folders: `755`
   - Files: `644`

### Method 2: Upload via FTP

1. **Get FTP Credentials**
   - In cPanel, go to **FTP Accounts**
   - Note your FTP hostname, username, and password
   - Default port: `21` (or `22` for SFTP)

2. **Connect with FTP Client**
   - Download [FileZilla](https://filezilla-project.org/) or similar
   - Connect using your FTP credentials
   - Navigate to `public_html` on remote server

3. **Upload Files**
   - Drag and drop all project files to `public_html`
   - Ensure `.htaccess` file is included (enable "show hidden files")

### Method 3: Upload via Terminal (SSH)

```bash
# Connect to server via SSH
ssh username@your-domain.com

# Navigate to public_html
cd public_html

# Clone the repository (if git is available)
git clone https://github.com/miguelfradeflores/Dental-Site.git .

# Or use wget to download
wget https://github.com/miguelfradeflores/Dental-Site/archive/main.zip
unzip main.zip
mv Dental-Site-main/* .
rm -rf Dental-Site-main main.zip
```

### Post-Upload Configuration

#### 1. Enable HTTPS (Recommended)

If you have SSL installed, uncomment these lines in `.htaccess`:

```apache
RewriteCond %{HTTPS} off
RewriteRule ^(.*)$ https://%{HTTP_HOST}%{REQUEST_URI} [L,R=301]
```

#### 2. Update Form Redirect URL

In `pages/home.html`, update the form redirect to your actual domain:

```html
<input type="hidden" name="_next" value="https://yourdomain.com/pages/thanks.html">
```

#### 3. Verify FormSubmit.co

- The first form submission will require email verification
- Check the inbox of `contacto@lizziecardenas.com.bo`
- Click the verification link from FormSubmit.co

#### 4. Test the Website

- Visit your domain to verify the site loads
- Test all navigation links
- Test the contact form submission
- Test the gallery lightbox
- Check mobile responsiveness

### Troubleshooting

| Issue | Solution |
|-------|----------|
| 404 errors on pages | Ensure `.htaccess` is uploaded and `mod_rewrite` is enabled |
| Images not loading | Check file paths and permissions (644 for files) |
| Form not submitting | Verify FormSubmit.co email and check browser console |
| CSS not loading | Clear browser cache, check file paths |
| Videos not playing | Ensure MIME types are set in `.htaccess` |

### .htaccess Features

The included `.htaccess` file provides:

- ✅ URL rewriting (clean URLs without .html)
- ✅ HTTPS redirect (when uncommented)
- ✅ GZIP compression for faster loading
- ✅ Browser caching for static assets
- ✅ Security headers (XSS protection, clickjacking prevention)
- ✅ Custom 404 error page
- ✅ Proper MIME types for videos and images

---

## 📍 Contact Information

- **Phone**: (+591) 62547130 / (2) 2799061
- **Email**: contacto@lizziecardenas.com.bo
- **Address**: Calacoto calle 21 #8226 piso 2 oficina 7, La Paz, Bolivia
- **WhatsApp**: [Contact via WhatsApp](https://wa.me/59162547130)

## 📜 Trademarks

- Damon® is a registered trademark of Ormco Corporation.
- Invisalign, the Invisalign logo, and iTero are trademarks of Align Technology, Inc.

## 📝 License

This project is proprietary and belongs to Dra. Lizzie Cárdenas.
