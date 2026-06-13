# Maheswari Travels - Website

A modern, responsive, and fast static website built for **Maheswari Travels**, a premium cab and tour service provider based in Visakhapatnam (Vizag), Andhra Pradesh, India. 

The website showcases local cab booking, outstation trips, airport transfers, custom tour packages (like Araku and Lambasingi), and tempo/bus rentals.

---

## 🚀 Key Features

* **Responsive Design:** Optimized for all devices including mobile phones, tablets, and desktop screens using Bootstrap 5.
* **Modern UI/UX:** Clean typography, smooth page transitions, animations, and image galleries.
* **Service Booking Info:** Dedicated pages detailing tour packages, outstation trips, local cab bookings, and coach rentals.
* **Interactive Components:** Features dynamic owl carousels (sliders), time & date pickers, custom select fields, and a contact map.
* **Direct Communication Integration:** Floating action buttons for instant **WhatsApp** chat and **Direct Phone Calls** to improve customer conversion rates.
* **SEO Optimized:** Structured semantic HTML with custom Meta tags, descriptions, and keywords for local search engines.

---

## 📁 Project Structure

```text
├── assets/
│   ├── css/          # Stylesheets (Bootstrap, FontAwesome, custom style-1.css, etc.)
│   ├── js/           # Scripts (jQuery, Bootstrap, OWL Carousel, main-1.js animation logic)
│   ├── img/          # Images (Logo, banners, cars, tour destinations)
│   └── fonts/        # Custom icons and fonts
├── index.html        # Home Page
├── about.html        # About Us Page
├── cab-booking.html  # Local & Airport Cab Services Page
├── outstation.html   # Outstation Booking Page
├── tour-packages.html# Tour Packages (Araku, Lambasingi, etc.) Page
├── tempo-bus.html    # Tempo Traveller & Bus Rental Page
├── contact.html      # Contact Us Page with Interactive Map & Enquiry Form
└── README.md         # Project documentation (this file)
```

---

## 🛠️ Technology Stack

* **Structure:** HTML5 (Semantic elements)
* **Styling:** CSS3, Bootstrap 5.x, FontAwesome 6 (for icons), Animate.css (for transition animations)
* **Logic & Animation:** JavaScript, jQuery 3.6.0, OWL Carousel, Magnific Popup, jQuery UI

---

## 💻 How to Run Locally

Since this is a fully static website, running it locally is very easy:

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/YOUR_USERNAME/maheswari-travels.git
   cd maheswari-travels
   ```
2. **Open the Website:**
   * Double-click on `index.html` to open it in any web browser.
   * *Alternatively (Recommended)*, use the **Live Server** extension in Visual Studio Code to run a local development server.

---

## 🌐 Deployment Guide

### Deploying to Netlify (Free & Recommended)
Netlify is perfect for hosting this website because of its ease of use and free form-handling service.

1. Create a free account at [Netlify](https://www.netlify.com/).
2. Drag and drop the project root folder directly into the Netlify dashboard under **Deploys**.
3. Connect your custom domain (e.g., `maheswaritravels.in`) in the Netlify Domain settings.
4. Netlify will configure your DNS and automatically install a free SSL certificate.

### Making the Enquiry Forms Functional
Since this is a static website, the HTML form fields (in `contact.html` and `cab-booking.html`) do not submit by default. Here is how you can make them work easily:

#### Option 1: Netlify Forms (Easiest)
If hosted on Netlify, simply add the `data-netlify="true"` attribute to the `<form>` element. Netlify will capture all customer submissions automatically:
```html
<form method="POST" action="/success.html" data-netlify="true" id="contact-form">
  <!-- Form inputs here -->
</form>
```

#### Option 2: WhatsApp Form Submission
You can use simple JavaScript to parse form inputs and redirect the user directly to a WhatsApp message containing their booking inquiry:
```javascript
// Example JS snippet to attach to form submission:
const phone = "+919290762224";
const text = `Name: ${name}%0APhone: ${userPhone}%0ADetails: ${details}`;
window.open(`https://wa.me/${phone}?text=${text}`, '_blank');
```
