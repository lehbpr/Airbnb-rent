<!-- Meta Tags --> <meta charset="UTF-8"> <meta content="width=device-width, initial-scale=1.0" name="viewport"><!-- PWA Meta Tags --> <meta content="#FF5A5F" name="theme-color"> <meta content="Enhance your stay with Vista Charm. Manage your check-in and check-out times, access amenities, and more." name="description"> <!-- SEO Meta Tags --> <meta content="Vista Charm, Hotel, Accommodation, Check-In, Check-Out, Amenities" name="keywords"> <meta content="Vista Charm Team" name="author"> <!-- Open Graph Meta Tags --> <meta content="Vista Charm - Enhance Your Stay" property="og:title"> <meta content="Manage your check-in and check-out times, access amenities, and more with Vista Charm." property="og:description"> <meta content="https://via.placeholder.com/1200x630.png?text=Vista+Charm" property="og:image"> <meta content="https://yourwebsite.com" property="og:url"> <meta content="website" property="og:type"> <!-- Twitter Card Meta Tags --> <meta content="summary_large_image" name="twitter:card"> <meta content="Vista Charm - Enhance Your Stay" name="twitter:title"> <meta content="Manage your check-in and check-out times, access amenities, and more with Vista Charm." name="twitter:description"> <meta content="https://via.placeholder.com/1200x630.png?text=Vista+Charm" name="twitter:image"> <!-- Font Awesome for Icons --> <link referrerpolicy="no-referrer" crossorigin="anonymous" integrity="sha512-p6VhT+e1h4KHmOjYAlL+5kGdnNq0k9jXh2gHl9c6VjU1BvO36a2plvqN5J6FnvCj1mnhSItK4U8H2X45yg5S1w==" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css" rel="stylesheet"> <!-- Google Fonts: Montserrat for headings and Lato for body --> <link href="https://fonts.googleapis.com/css2?family=Lato:wght@400;500;700&amp;family=Montserrat:wght@700&amp;display=swap" rel="stylesheet"> <!-- Flatpickr CSS --> <link href="https://cdn.jsdelivr.net/npm/flatpickr/dist/flatpickr.min.css" rel="stylesheet"> <!-- Custom CSS -->
<style><!--
/* CSS Reset */
           *, *::before, *::after {
               margin: 0;
               padding: 0;
               box-sizing: border-box;
           }
 
           /* Root Variables */
           :root {
               --primary-color: #FF5A5F; /* Airbnb Red */
               --secondary-color: #484848; /* Dark Gray */
               --background-color: #FFFFFF; /* White */
               --text-color: #484848; /* Dark Gray */
               --card-background: #F8F8F8; /* Light Gray */
               --button-background: #FF5A5F; /* Airbnb Red */
               --button-text: #FFFFFF; /* White */
               --button-hover: #E04850; /* Darker Red */
               --modal-overlay: rgba(0, 0, 0, 0.6);
               --transition-speed: 0.3s;
               --font-family: 'Lato', sans-serif;
               --header-font-family: 'Montserrat', sans-serif;
               --border-radius: 12px;
               --border-color: #CCCCCC; /* Light border */
               --scrollbar-track-color: #E0E0E0; /* Light scrollbar track */
               --toggle-background: rgba(255, 255, 255, 0.1);
               --toggle-hover-background: rgba(255, 90, 95, 0.2);
               --card-shadow: rgba(0, 0, 0, 0.1) 0px 4px 12px;
               --card-hover-shadow: rgba(0, 0, 0, 0.2) 0px 8px 24px;
               --card-transition: transform var(--transition-speed) ease, box-shadow var(--transition-speed) ease;
               --error-color: #e74c3c;
               --available-bg: #e0f7fa;
               --upgrade-bg: #ffe0b2;
               --button-selected-bg: #FFB3B3;
           }
 
           /* Dark Theme Variables */
           [data-theme="dark"] {
               --primary-color: #FF5A5F; /* Airbnb Red */
               --secondary-color: #E0E0E0; /* Light Gray */
               --background-color: #121212; /* Dark Gray */
               --text-color: #E0E0E0; /* Light Gray */
               --card-background: #1E1E1E; /* Slightly Lighter Dark */
               --button-background: #FF5A5F; /* Airbnb Red */
               --button-text: #121212; /* Dark Gray */
               --button-hover: #E04850; /* Darker Red */
               --border-color: #555555; /* Darker border */
               --scrollbar-track-color: #555555; /* Dark scrollbar track */
               --toggle-background: rgba(18, 18, 18, 0.1);
               --toggle-hover-background: rgba(255, 90, 95, 0.2);
               --card-shadow: rgba(0, 0, 0, 0.3) 0px 4px 12px;
               --card-hover-shadow: rgba(0, 0, 0, 0.4) 0px 8px 24px;
           }
 
           /* Body Styles */
           body {
               font-family: var(--font-family);
               background-color: var(--background-color);
               color: var(--text-color);
               line-height: 1.6;
               margin: 0;
               padding: 0;
               transition: background-color var(--transition-speed) ease, color var(--transition-speed) ease;
           }
 
           /* Header Font */
           h1, h2, h3 {
               font-family: var(--header-font-family);
           }
 
           /* Theme Toggle Button */
           #theme-toggle-scroll {
               position: fixed;
               top: 20px;
               left: 20px;
               background: var(--toggle-background);
               border: 2px solid var(--primary-color);
               border-radius: 50%;
               padding: 10px;
               cursor: grab;
               font-size: 1.8rem;
               color: var(--text-color);
               transition: color var(--transition-speed) ease, background var(--transition-speed) ease;
               z-index: 1000;
               user-select: none; /* Prevents text selection */
               touch-action: none; /* Prevents default touch actions */
           }
           #theme-toggle-scroll.grabbing {
               cursor: grabbing;
           }
           #theme-toggle-scroll:hover,
           #theme-toggle-scroll:focus {
               color: var(--button-text);
               background: var(--toggle-hover-background);
               outline: none;
           }
 
           /* Container */
           .container {
               max-width: 1200px;
               margin: 0 auto;
               padding: 20px;
           }
 
           /* Main Sections */
           main {
               padding: 20px 0;
           }
 
           /* Section Titles */
           .section-title {
               font-size: 2.2rem;
               margin-bottom: 10px;
               color: var(--primary-color);
               text-align: center;
               font-weight: 700;
           }
 
           /* Section Subtitles */
           .section-subtitle {
               font-size: 1.8rem;
               margin-bottom: 10px;
               color: var(--secondary-color);
               text-align: center;
           }
 
           /* Section Rich Text */
           .section-rich-text,
           .section-description {
               font-size: 1rem;
               color: var(--text-color);
               max-width: 800px;
               margin: 0 auto 20px auto;
               text-align: center;
           }
 
           /* Shared Grid */
           .shared-grid {
               display: flex;
               flex-wrap: nowrap;
               gap: 20px;
               margin-bottom: 40px;
               overflow-x: auto;
               padding-bottom: 10px;
               scroll-behavior: smooth;
               justify-content: flex-start;
               scroll-snap-type: x mandatory;
           }
           .shared-grid::-webkit-scrollbar {
               height: 8px;
           }
           .shared-grid::-webkit-scrollbar-track {
               background: var(--scrollbar-track-color);
               border-radius: 4px;
           }
           .shared-grid::-webkit-scrollbar-thumb {
               background: var(--primary-color);
               border-radius: 4px;
           }
           .shared-grid::-webkit-scrollbar-thumb:hover {
               background: var(--button-hover);
           }
 
           /* Cards */
           .card {
               background-color: var(--card-background);
               border-radius: var(--border-radius);
               box-shadow: var(--card-shadow);
               padding: 20px;
               text-align: center;
               transition: var(--card-transition);
               cursor: pointer;
               display: flex;
               flex-direction: column;
               align-items: center;
               min-width: 280px;
               flex-shrink: 0;
               scroll-snap-align: start;
               border: 1px solid var(--border-color);
               position: relative;
               overflow: hidden;
               background-clip: padding-box;
           }
           .card::before {
               content: '';
               position: absolute;
               top: 0;
               left: 0;
               width: 100%;
               height: 5px;
               background-color: var(--primary-color);
               border-top-left-radius: var(--border-radius);
               border-top-right-radius: var(--border-radius);
               opacity: 0.8;
           }
           .card:hover,
           .card:focus {
               transform: translateY(-10px);
               box-shadow: var(--card-hover-shadow);
               outline: none;
           }
           .card i {
               font-size: 3rem;
               color: var(--primary-color);
               margin-bottom: 20px;
           }
           .card h3 {
               font-size: 1.6rem;
               margin-bottom: 15px;
               color: var(--text-color);
               font-weight: 700;
           }
           .card p {
               font-size: 1rem;
               color: var(--text-color);
               margin-bottom: 10px;
               transition: color var(--transition-speed) ease;
           }
           /* Enhancements for engaging content */
           .card:hover p,
           .card:focus p {
               color: var(--primary-color);
           }
           .timer {
               font-size: 1.4rem;
               color: var(--primary-color);
               margin: 15px 0;
               font-weight: 600;
           }
 
           /* Check-In & Check-Out Card */
           .card-container {
               max-width: 800px;
               margin: 40px auto;
               padding: 30px;
               background-color: var(--card-background);
               border-radius: var(--border-radius);
               box-shadow: var(--card-shadow);
               text-align: center;
               transition: var(--card-transition);
               display: flex;
               flex-direction: column;
               border: 1px solid var(--border-color);
           }
           .card-container:hover,
           .card-container:focus {
               transform: translateY(-10px);
               box-shadow: var(--card-hover-shadow);
               outline: none;
           }
           .card-container h2 {
               font-size: 2rem;
               color: var(--primary-color);
               margin-bottom: 15px;
           }
           .checkin-checkout-wrapper {
               display: flex;
               justify-content: space-around;
               align-items: stretch;
               gap: 20px;
               flex-wrap: wrap;
           }
           .checkin-checkout-section {
               flex: 1;
               background-color: var(--background-color);
               border: 1px solid var(--primary-color);
               border-radius: var(--border-radius);
               padding: 20px;
               box-shadow: var(--card-shadow);
               display: flex;
               flex-direction: column;
               align-items: center;
               cursor: pointer;
               transition: background-color var(--transition-speed) ease, color var(--transition-speed) ease;
               min-width: 200px;
               position: relative;
               background-clip: padding-box;
           }
           .checkin-checkout-section:hover,
           .checkin-checkout-section:focus {
               background-color: var(--primary-color);
               color: var(--button-text);
               outline: none;
               box-shadow: var(--card-hover-shadow);
           }
           .checkin-checkout-section:hover .timer,
           .checkin-checkout-section:focus .timer {
               color: var(--button-text);
           }
           .checkin-checkout-section strong {
               font-size: 1.2rem;
               margin-bottom: 10px;
           }
           .date-display {
               font-size: 1rem;
               color: var(--secondary-color);
               margin-top: 5px;
           }
 
           /* Enhancement Widgets */
           .enhance-your-stay-wrapper {
               display: flex;
               flex-wrap: nowrap;
               overflow-x: auto;
               gap: 20px;
               padding-bottom: 10px;
               scroll-behavior: smooth;
               justify-content: flex-start;
               scroll-snap-type: x mandatory;
           }
           .enhance-your-stay-wrapper::-webkit-scrollbar {
               height: 8px;
           }
           .enhance-your-stay-wrapper::-webkit-scrollbar-track {
               background: var(--scrollbar-track-color);
               border-radius: 4px;
           }
           .enhance-your-stay-wrapper::-webkit-scrollbar-thumb {
               background: var(--primary-color);
               border-radius: 4px;
           }
           .enhance-your-stay-wrapper::-webkit-scrollbar-thumb:hover {
               background: var(--button-hover);
           }
           .enhancement-widget {
               width: 220px;
               height: 220px;
               background-color: var(--card-background);
               border-radius: var(--border-radius);
               padding: 20px;
               box-shadow: var(--card-shadow);
               transition: var(--card-transition);
               cursor: pointer;
               display: flex;
               flex-direction: column;
               align-items: center;
               justify-content: center;
               text-align: center;
               flex-shrink: 0;
               scroll-snap-align: start;
               border: 1px solid var(--border-color);
               position: relative;
               overflow: hidden;
               background-clip: padding-box;
           }
           .enhancement-widget::before {
               content: '';
               position: absolute;
               top: 0;
               left: 0;
               width: 100%;
               height: 5px;
               background-color: var(--primary-color);
               border-top-left-radius: var(--border-radius);
               border-top-right-radius: var(--border-radius);
               opacity: 0.8;
           }
           .enhancement-widget:hover,
           .enhancement-widget:focus {
               transform: translateY(-10px);
               box-shadow: var(--card-hover-shadow);
               outline: none;
           }
           .enhancement-widget i {
               font-size: 2.5rem;
               color: var(--primary-color);
               margin-bottom: 15px;
           }
           .enhancement-widget h3 {
               font-size: 1.2rem;
               margin-bottom: 8px;
               color: var(--text-color);
               font-weight: 600;
           }
           .enhancement-widget p {
               font-size: 1rem;
               color: var(--text-color);
           }
 
           /* FAQs */
           .faq-section {
               margin-bottom: 40px;
           }
           .faq-card {
               background-color: var(--card-background);
               border-radius: var(--border-radius);
               box-shadow: var(--card-shadow);
               padding: 25px;
               transition: var(--card-transition);
               border: 1px solid var(--border-color);
           }
           .faq-card:hover,
           .faq-card:focus-within {
               transform: translateY(-10px);
               box-shadow: var(--card-hover-shadow);
               outline: none;
           }
           .faq-item {
               margin-bottom: 15px;
               border-bottom: 1px solid var(--border-color);
               padding-bottom: 15px;
           }
           .faq-item:last-child {
               border-bottom: none;
           }
           .faq-item button {
               width: 100%;
               text-align: left;
               background: none;
               border: none;
               padding: 10px 0;
               font-size: 1.1rem;
               font-weight: 600;
               cursor: pointer;
               color: var(--text-color);
               display: flex;
               justify-content: space-between;
               align-items: center;
               transition: color var(--transition-speed) ease;
           }
           .faq-item button:focus {
               outline: none;
               color: var(--primary-color);
           }
           .faq-answer {
               max-height: 0;
               overflow: hidden;
               transition: max-height var(--transition-speed) ease;
           }
           .faq-answer p {
               padding: 10px 0;
               color: var(--text-color);
               font-size: 1rem;
           }
           .faq-item.active .faq-answer {
               max-height: 200px;
           }
           .faq-item.active button::after {
               transform: rotate(180deg);
           }
           .faq-item button::after {
               content: '\f078';
               font-family: 'Font Awesome 6 Free';
               font-weight: 900;
               transition: transform var(--transition-speed) ease;
           }
 
           /* Contact Section */
           .contact-section {
               margin-bottom: 40px;
           }
           .contact-card {
               background-color: var(--card-background);
               border-radius: var(--border-radius);
               box-shadow: var(--card-shadow);
               padding: 25px;
               transition: var(--card-transition);
               border: 1px solid var(--border-color);
           }
           .contact-card:hover,
           .contact-card:focus-within {
               transform: translateY(-10px);
               box-shadow: var(--card-hover-shadow);
               outline: none;
           }
           .contact-details {
               text-align: center;
               margin-bottom: 20px;
           }
           .contact-details p {
               font-size: 1.1rem;
               color: var(--text-color);
               margin-bottom: 10px;
           }
           .contact-details a {
               color: var(--primary-color);
               text-decoration: none;
               transition: color var(--transition-speed) ease;
           }
           .contact-details a:hover,
           .contact-details a:focus {
               color: var(--button-hover);
           }
           .quick-access-buttons {
               display: flex;
               gap: 15px;
               overflow-x: auto;
               padding-bottom: 10px;
               scroll-behavior: smooth;
               scroll-snap-type: x mandatory;
           }
           .quick-access-buttons::-webkit-scrollbar {
               height: 8px;
           }
           .quick-access-buttons::-webkit-scrollbar-track {
               background: var(--scrollbar-track-color);
               border-radius: 4px;
           }
           .quick-access-buttons::-webkit-scrollbar-thumb {
               background: var(--primary-color);
               border-radius: 4px;
           }
           .quick-access-buttons::-webkit-scrollbar-thumb:hover {
               background: var(--button-hover);
           }
           .cta-button {
               background-color: var(--button-background);
               color: var(--button-text);
               padding: 12px 25px;
               border: none;
               border-radius: 8px;
               text-decoration: none;
               font-size: 1.1rem;
               cursor: pointer;
               transition: background-color var(--transition-speed) ease, transform var(--transition-speed) ease, box-shadow var(--transition-speed) ease;
               font-weight: 600;
               display: inline-flex;
               align-items: center;
               gap: 8px;
               scroll-snap-align: start;
               white-space: nowrap;
           }
           .cta-button:hover,
           .cta-button:focus {
               background-color: var(--button-hover);
               transform: translateY(-2px);
               box-shadow: var(--card-hover-shadow);
               outline: none;
           }
 
           /* Reservation Details */
           .reservation-details {
               max-width: 600px;
               margin: 20px auto;
               padding: 25px;
               border: 1px solid var(--border-color);
               border-radius: var(--border-radius);
               background: var(--card-background);
               box-shadow: var(--card-shadow);
               text-align: center;
               display: block; /* Always visible */
           }
           .reservation-card {
               padding: 20px;
               background: linear-gradient(135deg, #f7f7f7 25%, #fff 25%, #fff 50%, #f7f7f7 50%, #f7f7f7 75%, #fff 75%, #fff 100%);
               border-radius: var(--border-radius);
               box-shadow: var(--card-shadow);
               position: relative;
           }
           .reservation-card-header {
               font-size: 1.8rem;
               font-weight: 700;
               color: var(--primary-color);
               margin-bottom: 15px;
           }
           .reservation-card-body {
               font-size: 1.1rem;
               margin-bottom: 15px;
               line-height: 1.6;
           }
           .reservation-barcode {
               width: 90%;
               height: 60px;
               background: url('https://via.placeholder.com/400x60?text=Barcode') center/cover no-repeat;
               margin: 0 auto;
               border-radius: 8px;
           }
 
           /* Modals */
           .modal {
               display: none;
               position: fixed;
               z-index: 1000;
               left: 0;
               top: 0;
               width: 100%;
               height: 100vh;
               background-color: var(--modal-overlay);
               justify-content: center;
               align-items: center;
               padding: 20px;
               opacity: 0;
               transition: opacity var(--transition-speed) ease;
           }
           .modal.active {
               display: flex;
               opacity: 1;
           }
           .modal-content {
               background-color: var(--card-background);
               padding: 30px;
               border-radius: var(--border-radius);
               max-width: 500px;
               width: 100%;
               position: relative;
               box-shadow: var(--card-hover-shadow);
               animation: slideDown 0.3s ease;
               overflow-y: auto;
               max-height: 90vh;
               border: 1px solid var(--border-color);
           }
           @keyframes slideDown {
               from {
                   transform: translateY(-50px);
                   opacity: 0;
               }
               to {
                   transform: translateY(0);
                   opacity: 1;
               }
           }
           .close-button {
               position: absolute;
               top: 15px;
               right: 20px;
               background: none;
               border: none;
               font-size: 1.5rem;
               color: var(--text-color);
               cursor: pointer;
               transition: color var(--transition-speed) ease;
           }
           .close-button:hover,
           .close-button:focus {
               color: var(--primary-color);
               outline: none;
           }
           .modal-content h2 {
               margin-bottom: 20px;
               color: var(--text-color);
               font-size: 1.8rem;
               font-weight: 700;
           }
           .modal-content p {
               font-size: 1rem;
               color: var(--text-color);
               margin-bottom: 15px;
           }
           .modal-content form div {
               margin-bottom: 20px;
           }
           .modal-content label {
               display: block;
               margin-bottom: 8px;
               color: var(--text-color);
               font-size: 1rem;
               font-weight: 500;
           }
           .modal-content input,
           .modal-content select {
               width: 100%;
               padding: 10px 12px;
               border: 1px solid var(--border-color);
               border-radius: 6px;
               font-size: 1rem;
               background-color: var(--background-color);
               color: var(--text-color);
               transition: border-color var(--transition-speed) ease;
           }
           .modal-content input:focus,
           .modal-content select:focus {
               border-color: var(--primary-color);
               outline: none;
           }
           .submit-button {
               background-color: var(--button-background);
               color: var(--button-text);
               padding: 12px 20px;
               border: none;
               border-radius: 6px;
               cursor: pointer;
               font-size: 1.1rem;
               transition: background-color var(--transition-speed) ease, transform var(--transition-speed) ease, box-shadow var(--transition-speed) ease;
               font-weight: 600;
               width: 100%;
               display: none; /* Hidden by default */
           }
           .submit-button.visible {
               display: block;
           }
           .submit-button:hover,
           .submit-button:focus {
               background-color: var(--button-hover);
               transform: translateY(-2px);
               box-shadow: var(--card-hover-shadow);
               outline: none;
           }
 
           .submit-button:disabled {
             background-color: var(--button-background, #ccc);
             cursor: not-allowed;
             opacity: 0.6;
             box-shadow: none;
             transform: none;
           }
 
           /* Error Messages */
           .error-message {
               color: var(--error-color);
               font-size: 0.9rem;
               display: none;
           }
           .error-message.visible {
               display: block;
           }
 
           /* Upgrade Options */
           .upgrade-options {
               margin-top: 30px;
               text-align: left;
           }
           .upgrade-option {
               background-color: var(--upgrade-bg);
               padding: 15px;
               border-radius: var(--border-radius);
               margin-bottom: 15px;
               box-shadow: var(--card-shadow);
               display: flex;
               align-items: center;
               justify-content: space-between;
               flex-wrap: wrap;
               position: relative;
           }
           .upgrade-option label {
               font-size: 1rem;
               color: var(--primary-color);
               flex: 1 1 70%;
               margin-bottom: 10px;
           }
           .upgrade-option button {
               background-color: var(--button-background);
               color: var(--button-text);
               border: none;
               padding: 8px 16px;
               border-radius: var(--border-radius);
               cursor: pointer;
               transition: background-color var(--transition-speed);
               font-size: 0.9rem;
               flex: 1 1 25%;
               min-width: 100px;
           }
           .upgrade-option button:hover {
               background-color: var(--button-hover);
           }
 
           /* Hidden Upgrade Details */
           .upgrade-details {
               display: none;
               margin-top: 10px;
               width: 100%;
               padding-left: 20px;
           }
           .upgrade-details button {
               width: 100%;
               margin-bottom: 10px;
               background-color: var(--button-background);
               color: var(--button-text);
               border: none;
               padding: 8px 12px;
               border-radius: var(--border-radius);
               cursor: pointer;
               transition: background-color var(--transition-speed);
               font-size: 0.9rem;
           }
           .upgrade-details button:hover {
               background-color: var(--button-hover);
           }
           .upgrade-button.selected {
               background-color: var(--button-selected-bg);
               color: var(--text-color);
           }
 
           /* Upgrade Confirmation Modal */
           #upgrade-confirmation-modal .submit-button {
               margin-top: 10px;
               display: block; /* Ensure buttons are visible */
           }
 
           /* Add to Home Screen Modal */
           #add-to-home-modal .submit-button {
               margin-top: 10px;
               display: block;
           }
 
           /* Download Guest Pass Button */
           #download-guest-pass-button {
               display: none; /* Hidden by default */
           }
 
           /* Responsive Adjustments */
           @media (max-width: 768px) {
               .checkin-checkout-wrapper {
                   flex-direction: column;
                   gap: 20px;
               }
               .upgrade-option {
                   flex-direction: column;
                   align-items: flex-start;
               }
               .upgrade-option button {
                   margin-top: 10px;
                   width: 100%;
               }
           }
           @media (max-width: 480px) {
               .section-title {
                   font-size: 1.8rem;
               }
               .section-subtitle {
                   font-size: 1.5rem;
               }
               .section-rich-text,
               .section-description {
                   font-size: 0.9rem;
               }
               .card h3,
               .enhancement-widget h3 {
                   font-size: 1.5rem;
               }
               .cta-button {
                   padding: 10px 20px;
                   font-size: 1rem;
               }
               #theme-toggle-scroll {
                   font-size: 1.5rem;
                   padding: 8px;
               }
           }
 
           /* Disabled Days Styling */
           .flatpickr-day.disabled {
               color: #ccc;
               pointer-events: none;
               background-color: #f0f0f0;
               border-radius: 50%;
           }
           /* Highlight Available Days */
           .flatpickr-day.available {
               background-color: var(--available-bg);
               color: var(--primary-color);
               border: 2px solid var(--primary-color);
           }
           /* Highlight Selected Days */
           .flatpickr-day.selected {
               background-color: var(--primary-color);
               color: #fff;
           }
           /* Modern Input Focus */
           input:focus, select:focus, button:focus {
               outline: 2px solid var(--primary-color);
               outline-offset: 2px;
           }
           .flatpickr-calendar {
               box-shadow: var(--card-shadow);
               border-radius: var(--border-radius);
           }
 
           /* Loading Spinner */
           .spinner {
               border: 4px solid rgba(0, 0, 0, 0.1);
               width: 36px;
               height: 36px;
               border-radius: 50%;
               border-left-color: var(--primary-color);
               animation: spin 1s linear infinite;
               margin: 20px auto;
           }
           @keyframes spin {
               to { transform: rotate(360deg); }
           }
 
           /* Overlay Styles */
           .overlay {
               position: absolute;
               top: 0;
               left: 0;
               width: 100%;
               height: 100%;
               background-color: rgba(255, 255, 255, 0.9); /* Semi-transparent white */
               display: flex;
               justify-content: center;
               align-items: center;
               z-index: 10;
               border-radius: var(--border-radius);
               transition: opacity var(--transition-speed) ease;
           }
 
           .overlay-content {
               text-align: center;
               font-size: 1.2rem;
               color: var(--primary-color);
           }
 
           .locked-overlay.hidden {
               opacity: 0;
               pointer-events: none;
           }
 
           /* Positioning Overlays Correctly */
           .card.locked {
               position: relative;
           }
 
           .form-group-container {
             display: flex;
             justify-content: space-around;
           }
           @media (max-width: 560px) {
             .form-group-container .form-group {
               max-width: 150px;
               padding-left: 5px;
               padding-right: 5px;
           }  
         }
         .display-none {
           display: none;
         }  
         .share-buttons {
           margin-top: 20px;
         }
         .share-buttons a {
           margin: 5px;
         }
--></style>
<!-- Inline Manifest --> <script>
 const manifest = {
   name: "Vista Charm",
   short_name: "VistaCharm",
   description:
     "Enhance your stay with Vista Charm. Manage your check-in and check-out times, access amenities, and more.",
   start_url: "/",
   display: "standalone",
   background_color: "#FFFFFF",
   theme_color: "#FF5A5F",
   icons: [
     {
       src: "https://via.placeholder.com/192x192.png?text=Icon+192",
       sizes: "192x192",
       type: "image/png",
     },
     {
       src: "https://via.placeholder.com/512x512.png?text=Icon+512",
       sizes: "512x512",
       type: "image/png",
     },
   ],
 };
 const blob = new Blob([JSON.stringify(manifest)], {
   type: "application/json",
 });
 const manifestURL = URL.createObjectURL(blob);
 const manifestLink = document.createElement("link");
 manifestLink.rel = "manifest";
 manifestLink.href = manifestURL;
 document.head.appendChild(manifestLink);
</script> <!-- Theme Toggle Button --> <button aria-label="Toggle Dark Mode" id="theme-toggle-scroll"> <i aria-hidden="true" class="fas fa-moon" id="theme-icon-scroll"></i> </button> <!-- Container -->
<div class="container"><main> <!-- Stay Overview Section -->
<section aria-labelledby="stay-overview-title">
<h1 class="section-title" id="stay-overview-title">Your Stay at Vista Charm</h1>
<!-- Image --> <img style="width: 100%; border-radius: var(--border-radius); margin: 20px 0;" alt="Vista Charm" src="https://via.placeholder.com/1200x600"> <!-- Section Description -->
<p class="section-description">Easily manage your check-in and check-out times according to your stay.</p>
<!-- Check-In & Check-Out Card -->
<div aria-labelledby="checkin-checkout-title" tabindex="0" class="card-container" id="checkin-checkout-card">
<h2 id="checkin-checkout-title">Check-In &amp; Check-Out Times</h2>
<div class="checkin-checkout-wrapper"><!-- Check-In Section -->
<div aria-label="Set Check-In Time" tabindex="0" class="checkin-checkout-section" id="checkin-section"><strong>Check-In Time</strong>
<p class="timer" id="checkin-display">--:--:--</p>
<p id="checkin-date" class="date-display">--/--/----</p>
<!-- Timer Display -->
<div aria-live="polite" class="timer" id="checkin-timer">--:--:--</div>
</div>
<!-- Check-Out Section -->
<div aria-label="Set Check-Out Time" tabindex="0" class="checkin-checkout-section" id="checkout-section"><strong>Check-Out Time</strong>
<p class="timer" id="checkout-display">--:--:--</p>
<p id="checkout-date" class="date-display">--/--/----</p>
<!-- Timer Display -->
<div aria-live="polite" class="timer" id="checkout-timer">--:--:--</div>
</div>
</div>
</div>
<!-- Pre-Check-In Information -->
<h2 class="section-subtitle">Pre-Check-In Information</h2>
<p class="section-rich-text">To ensure a smooth &amp; enjoyable experience, review our guidelines and policies.</p>
<!-- Horizontal Scrollable Cards -->
<div class="shared-grid"><!-- Before Check-In Card -->
<div aria-labelledby="information-title-1" tabindex="0" class="card"><i aria-hidden="true" class="fas fa-info-circle"></i>
<h3 id="information-title-1">Before Check-In</h3>
<p><strong>Max Guests:</strong> 2 | No Visitors</p>
<p><strong>No Smoking / No Pets</strong></p>
<p><strong>Parking:</strong> 1 spot available</p>
<p><strong>Respect Neighbors:</strong> Keep noise levels down.</p>
<p><strong>Security:</strong> Cameras active on premises.</p>
<p><strong>Door Code:</strong> Provided upon arrival.</p>
<p><strong>Cleanliness:</strong> Please maintain cleanliness for a refund.</p>
</div>
<!-- House Rules Card (Locked) -->
<div aria-labelledby="information-title-2" tabindex="0" class="card locked"><i aria-hidden="true" class="fas fa-balance-scale"></i>
<h3 id="information-title-2">House Rules</h3>
<p><strong>Check-In:</strong> After 3:00 PM</p>
<p><strong>Check-Out:</strong> Before 11:00 AM</p>
<p><strong>No Parties:</strong> Strictly no events or parties.</p>
<p><strong>Quiet Hours:</strong> 10:00 PM - 8:00 AM.</p>
<p><strong>Garbage Disposal:</strong> Please dispose of waste properly.</p>
<!-- Overlay -->
<div class="overlay locked-overlay" id="house-rules-overlay">
<div class="overlay-content">
<p>House Rules will be available in <span id="house-rules-timer">--:--:--</span></p>
</div>
</div>
</div>
<!-- Amenities Card (Locked) -->
<div aria-labelledby="amenities-title" tabindex="0" class="card locked"><i aria-hidden="true" class="fas fa-concierge-bell"></i>
<h3 id="amenities-title">Amenities</h3>
<p><strong>Wi-Fi:</strong> Complimentary high-speed internet.</p>
<p><strong>Breakfast:</strong> Free continental breakfast.</p>
<p><strong>Parking:</strong> Free parking available.</p>
<p><strong>Air Conditioning:</strong> Climate control in every room.</p>
<p><strong>24/7 Support:</strong> We're here to help anytime.</p>
<!-- Overlay -->
<div class="overlay locked-overlay" id="amenities-overlay">
<div class="overlay-content">
<p>Amenities will be available in <span id="amenities-timer">--:--:--</span></p>
</div>
</div>
</div>
</div>
</section>
<!-- Enhance Your Stay Section -->
<section aria-labelledby="enhancements-title">
<h2 class="section-title" id="enhancements-title">Enhance Your Stay</h2>
<p class="section-description">Add extra amenities or services for an even more comfortable &amp; enjoyable stay.</p>
<div class="enhance-your-stay-wrapper"><!-- Early Check-In -->
<div aria-label="Early Check-in" tabindex="0" class="enhancement-widget" data-modal="early-checkin-modal"><i class="fas fa-clock"></i>
<h3>Early Check-In</h3>
<p>Arrive earlier for added convenience.</p>
</div>
<!-- Late Check-Out -->
<div aria-label="Late Check-out" tabindex="0" class="enhancement-widget" data-modal="late-checkout-modal"><i class="fas fa-calendar-alt"></i>
<h3>Late Check-Out</h3>
<p>Extend your stay beyond standard time.</p>
</div>
<!-- Toiletries & Essentials -->
<div aria-label="Toiletries &amp; Essentials" tabindex="0" class="enhancement-widget" data-modal="toiletries-modal"><i class="fas fa-bath"></i>
<h3>Toiletries</h3>
<p>Complimentary essentials for your comfort.</p>
</div>
<!-- Detergents -->
<div aria-label="Detergents" tabindex="0" class="enhancement-widget" data-modal="detergents-modal"><i class="fas fa-tshirt"></i>
<h3>Detergents</h3>
<p>Keep your clothes fresh and clean.</p>
</div>
<!-- Food & Snacks -->
<div aria-label="Food &amp; Snacks" tabindex="0" class="enhancement-widget" data-modal="food-snacks-modal"><i class="fas fa-utensils"></i>
<h3>Food &amp; Snacks</h3>
<p>Enjoy complimentary treats 24/7.</p>
</div>
</div>
</section>
<!-- Check-Out Details Section -->
<section aria-labelledby="checkout-details-title">
<h2 class="section-title" id="checkout-details-title">Check-Out Details</h2>
<p class="section-description">Ensure a smooth check-out process by following these simple instructions.</p>
<div class="shared-grid"><!-- Check-Out Instructions (Locked until day before check-out) -->
<div aria-labelledby="checkout-instructions-title" tabindex="0" class="card locked" id="checkout-instructions-card"><i aria-hidden="true" class="fas fa-file-signature"></i>
<h3 id="checkout-instructions-title">Check-Out Instructions</h3>
<p><strong>Remove Waste:</strong> Use provided bins.</p>
<p><strong>Dry Towels:</strong> Hang towels to dry.</p>
<p><strong>Secure Premises:</strong> Ensure all doors and windows are locked.</p>
<p><strong>Laundry:</strong> Use laundry facilities responsibly.</p>
<p><strong>Cleanliness:</strong> Leave the space clean for a refund.</p>
<!-- Overlay -->
<div class="overlay locked-overlay" id="checkout-overlay">
<div class="overlay-content">
<p>Check-Out Instructions will be available in <span id="checkout-timer-overlay">--:--:--</span></p>
</div>
</div>
</div>
</div>
</section>
<!-- FAQs Section -->
<section aria-labelledby="faq-title" class="faq-section">
<h2 class="section-title" id="faq-title">Frequently Asked Questions</h2>
<p class="section-description">Find answers to common questions about your stay at Vista Charm.</p>
<div class="faq-card">
<div class="faq-item"><button aria-expanded="false">What is the check-in process?</button>
<div class="faq-answer">
<p>Check-in starts at 3:00 PM. Use our app to set your preferred time.</p>
</div>
</div>
<div class="faq-item"><button aria-expanded="false">Can I request a late check-out?</button>
<div class="faq-answer">
<p>Yes, you can request a late check-out through the "Enhance Your Stay" section.</p>
</div>
</div>
<div class="faq-item"><button aria-expanded="false">How do I use the door code?</button>
<div class="faq-answer">
<p>Enter the unique door code provided upon arrival to access your room.</p>
</div>
</div>
<div class="faq-item"><button aria-expanded="false">Where do I park?</button>
<div class="faq-answer">
<p>We provide one parking spot in the driveway. Additional spots may be available on the street.</p>
</div>
</div>
</div>
</section>
<!-- Contact Us Section -->
<section aria-labelledby="contact-title" class="contact-section">
<h2 class="section-title" id="contact-title">Contact Us</h2>
<p class="section-description">If you have any questions or need assistance, feel free to reach out!</p>
<div class="contact-card">
<div class="contact-details">
<p><strong>Email:</strong> <a href="mailto:support@yourhotel.com">support@yourhotel.com</a></p>
<p><strong>Phone:</strong> <a href="tel:+1234567890">+1 (234) 567-890</a></p>
</div>
<div class="quick-access-buttons"><a aria-label="Call Support" href="tel:+1234567890" class="cta-button"> <i class="fas fa-phone-alt"></i> Call Now </a> <a aria-label="Email Support" href="mailto:support@yourhotel.com" class="cta-button"> <i class="fas fa-envelope"></i> Email Us </a> <a aria-label="Chat with Support" href="https://yourchatservice.com" class="cta-button" target="_blank"> <i class="fas fa-comments"></i> Chat Now </a></div>
</div>
</section>
<!-- Reservation Details -->
<div aria-labelledby="reservation-title" role="region" id="reservation-details" class="reservation-details">
<div class="reservation-card">
<div id="reservation-title" class="reservation-card-header">Your Reservation Details</div>
<div class="reservation-card-body"><strong>Check-In:</strong> <span id="preview-checkin">--/--/---- --:--</span><br> <strong>Check-Out:</strong> <span id="preview-checkout">--/--/---- --:--</span></div>
<!-- Share and Download Buttons --></div>
<div class="share-buttons"><a aria-label="Share on Facebook" href="https://www.facebook.com/sharer/sharer.php?u=https://yourwebsite.com" class="cta-button" target="_blank"> <i class="fab fa-facebook-f"></i> Facebook </a> <a aria-label="Share on Twitter" href="https://twitter.com/intent/tweet?url=https://yourwebsite.com&amp;text=Check+out+my+Reservation!" class="cta-button" target="_blank"> <i class="fab fa-twitter"></i> Twitter </a> <a aria-label="Share via Email" href="mailto:?subject=Check%20out%20my%20Reservation!&amp;body=Here%20are%20my%20reservation%20details:%20https://yourwebsite.com" class="cta-button"> <i class="fas fa-envelope"></i> Email </a> <a aria-label="Download Your Guest Pass" download="GuestPass.pkpass" href="https://drive.usercontent.google.com/download?id=1OhFMzoZwH5CpZtE4CXwrqyVOclSBvIi-&amp;export=download&amp;authuser=0" class="cta-button" id="download-guest-pass-button"> <i class="fas fa-download"></i> Download Your Guest Pass </a></div>
</div>
</main></div>
<!-- Modals --> <!-- Generate Passbook Modal (Active on Page Load) -->
<div aria-modal="true" aria-labelledby="generate-passbook-title" role="dialog" class="modal active" id="generate-passbook-modal">
<div class="modal-content">
<h2 id="generate-passbook-title">Enter Your Reservation Details</h2>
<form class="passbook-form" id="passbook-form"><!-- Check-In Date -->
<div class="form-group-container">
<div class="form-group"><label for="checkin-datetime">Check-In Date</label> <input required="" aria-label="Check-In Date" readonly="readonly" class="flatpickr-input" id="checkin-datetime" type="text"> <span id="error-checkin-datetime" class="error-message"></span></div>
<!-- Check-Out Date -->
<div class="form-group"><label for="checkout-datetime">Check-Out Date</label> <input required="" aria-label="Check-Out Date" readonly="readonly" class="flatpickr-input" id="checkout-datetime" type="text"> <span id="error-checkout-datetime" class="error-message"></span></div>
</div>
<!-- Upgrade Options -->
<div class="upgrade-options"><!-- Early Check-In Upgrade -->
<div class="upgrade-option display-none" id="upgrade-early-option"><label for="early-checkin">Early Check-In (Before 3:00 PM)</label> <button id="upgrade-early" type="button">Select Time</button> <!-- Hidden Upgrade Details -->
<div class="upgrade-details" id="early-upgrade-details"><button data-time="12:00 PM" data-price="49" class="upgrade-button" type="button"> 12:00 PM - $49 </button> <button data-time="1:00 PM" data-price="39" class="upgrade-button" type="button"> 1:00 PM - $39 </button> <button data-time="2:00 PM" data-price="29" class="upgrade-button" type="button"> 2:00 PM - $29 </button> <button data-time="3:00 PM" data-price="0" class="upgrade-button" type="button"> 3:00 PM - No Charge </button></div>
</div>
<!-- Late Check-Out Upgrade -->
<div class="upgrade-option display-none" id="upgrade-late-option"><label for="late-checkout">Late Check-Out (After 11:00 AM)</label> <button id="upgrade-late" type="button">Select Time</button> <!-- Hidden Upgrade Details -->
<div class="upgrade-details" id="late-upgrade-details"><button data-time="12:00 PM" data-price="29" class="upgrade-button" type="button"> 12:00 PM - $29 </button> <button data-time="1:00 PM" data-price="39" class="upgrade-button" type="button"> 1:00 PM - $39 </button> <button data-time="2:00 PM" data-price="49" class="upgrade-button" type="button"> 2:00 PM - $49 </button> <button data-time="3:00 PM" data-price="59" class="upgrade-button" type="button"> 3:00 PM - $59 </button> <button data-time="11:00 AM" data-price="0" class="upgrade-button" type="button"> 11:00 AM - No Charge </button></div>
</div>
</div>
<!-- Generate Passbook Button --> <button id="generate-passbook-button" class="submit-button" type="submit"> Submit </button></form></div>
</div>
<!-- Upgrade Confirmation Modal -->
<div aria-modal="true" aria-labelledby="upgrade-confirmation-title" role="dialog" class="modal" id="upgrade-confirmation-modal">
<div class="modal-content"><button aria-label="Close Modal" class="close-button">×</button>
<h2 id="upgrade-confirmation-title">Confirm Upgrade</h2>
<p id="upgrade-confirmation-message">Are you sure you want to select this time?</p>
<button id="confirm-upgrade" class="submit-button">Confirm</button> <button style="background-color: var(--error-color);" id="cancel-upgrade" class="submit-button"> Cancel </button></div>
</div>
<!-- Add to Home Screen Modal -->
<div aria-modal="true" aria-labelledby="add-to-home-title" role="dialog" class="modal" id="add-to-home-modal">
<div class="modal-content">
<h2 id="add-to-home-title">Add to Home Screen</h2>
<p>To receive your security code, please add this app to your home screen.</p>
<p id="add-to-home-instructions">&nbsp;</p>
<button class="submit-button" id="add-to-home-button"> Add to Home Screen </button> <!-- "Your Guest Pass" Button --> <button class="submit-button" id="your-guest-pass-button"> Your Guest Pass </button> <!-- Download Guest Pass --> <a aria-label="Download Your Guest Pass" download="GuestPass.pkpass" href="https://drive.usercontent.google.com/download?id=1OhFMzoZwH5CpZtE4CXwrqyVOclSBvIi-&amp;export=download&amp;authuser=0" class="cta-button" id="download-guest-pass"> <i class="fas fa-download"></i> Download Your Guest Pass </a></div>
</div>
<!-- Enhancement Modals --> <!-- Early Check-In Modal -->
<div aria-modal="true" aria-labelledby="early-checkin-title" role="dialog" class="modal" id="early-checkin-modal">
<div class="modal-content"><button aria-label="Close Modal" class="close-button">×</button>
<h2 id="early-checkin-title">Early Check-In</h2>
<p>Need to check in early? Upgrade your arrival time for added convenience.</p>
<h3>Pricing</h3>
<p>Early check-in available for an additional fee.</p>
<a aria-label="Buy Early Check-In Option" href="https://yourshopifystore.com/early-checkin" class="cta-button" target="_blank">Buy Now</a></div>
</div>
<!-- Late Check-Out Modal -->
<div aria-modal="true" aria-labelledby="late-checkout-title" role="dialog" class="modal" id="late-checkout-modal">
<div class="modal-content"><button aria-label="Close Modal" class="close-button">×</button>
<h2 id="late-checkout-title">Late Check-Out</h2>
<p>Extend your stay beyond the standard checkout time for added comfort.</p>
<h3>Pricing</h3>
<p>Late check-out available for an additional fee.</p>
<a aria-label="Buy Late Check-Out Option" href="https://yourshopifystore.com/late-checkout" class="cta-button" target="_blank">Buy Now</a></div>
</div>
<!-- Toiletries & Essentials Modal -->
<div aria-modal="true" aria-labelledby="toiletries-title" role="dialog" class="modal" id="toiletries-modal">
<div class="modal-content"><button aria-label="Close Modal" class="close-button">×</button>
<h2 id="toiletries-title">Toiletries &amp; Essentials</h2>
<p>We provide complimentary toiletries and essential items to ensure your comfort.</p>
<a aria-label="Buy Toiletries Option" href="https://yourshopifystore.com/toiletries" class="cta-button" target="_blank">Buy Now</a></div>
</div>
<!-- Detergents Modal -->
<div aria-modal="true" aria-labelledby="detergents-title" role="dialog" class="modal" id="detergents-modal">
<div class="modal-content"><button aria-label="Close Modal" class="close-button">×</button>
<h2 id="detergents-title">Detergents</h2>
<p>We offer complimentary detergents to keep your clothes fresh and clean.</p>
<a aria-label="Buy Detergents Option" href="https://yourshopifystore.com/detergents" class="cta-button" target="_blank">Buy Now</a></div>
</div>
<!-- Food & Snacks Modal -->
<div aria-modal="true" aria-labelledby="food-snacks-title" role="dialog" class="modal" id="food-snacks-modal">
<div class="modal-content"><button aria-label="Close Modal" class="close-button">×</button>
<h2 id="food-snacks-title">Food &amp; Snacks</h2>
<p>Enjoy complimentary treats 24/7 to satisfy your hunger and cravings.</p>
<a aria-label="Buy Food &amp; Snacks Option" href="https://yourshopifystore.com/food-snacks" class="cta-button" target="_blank">Buy Now</a></div>
</div>
<!-- Inline Service Worker Registration --> <script>
 if ("serviceWorker" in navigator) {
   const swCode = `
           const CACHE_NAME = 'vista-charm-cache-v1';
           const urlsToCache = [
               '/',
               // Add other assets you want to cache
               'https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css',
               'https://fonts.googleapis.com/css2?family=Lato:wght@400;500;700&family=Montserrat:wght@700&display=swap',
               'https://cdn.jsdelivr.net/npm/flatpickr/dist/flatpickr.min.css',
               'https://cdn.jsdelivr.net/npm/flatpickr/dist/flatpickr.min.js',
               // Add images and other assets as needed
               'https://via.placeholder.com/1200x630.png?text=Vista+Charm',
               'https://via.placeholder.com/192x192.png?text=Icon+192',
               'https://via.placeholder.com/512x512.png?text=Icon+512',
               'https://via.placeholder.com/400x60.png?text=Barcode',
               // Add offline.html if you have a fallback page
           ];
           self.addEventListener('install', event => {
               event.waitUntil(
                   caches.open(CACHE_NAME)
                       .then(cache => {
                           console.log('Opened cache');
                           return cache.addAll(urlsToCache);
                       })
               );
               self.skipWaiting();
           });
           self.addEventListener('fetch', event => {
               event.respondWith(
                   caches.match(event.request)
                       .then(response => {
                           if (response) {
                               return response;
                           }
                           return fetch(event.request).catch(() => {
                               // Return a fallback page or image
                               if (event.request.destination === 'document') {
                                   return caches.match('/offline.html');
                               }
                           });
                       })
               );
           });
           self.addEventListener('activate', event => {
               const cacheWhitelist = [CACHE_NAME];
               event.waitUntil(
                   caches.keys().then(cacheNames => {
                       return Promise.all(
                           cacheNames.map(cacheName => {
                               if (!cacheWhitelist.includes(cacheName)) {
                                   return caches.delete(cacheName);
                               }
                           })
                       );
                   })
               );
               self.clients.claim();
           });
           // Push notification event listener (requires server-side setup)
           self.addEventListener('push', event => {
               const data = event.data ? event.data.text() : 'Default message';
               const options = {
                   body: data,
                   icon: 'https://via.placeholder.com/192x192.png?text=Icon+192',
                   badge: 'https://via.placeholder.com/192x192.png?text=Badge',
               };
               event.waitUntil(
                   self.registration.showNotification('Vista Charm', options)
               );
           });
           `;
   const swBlob = new Blob([swCode], { type: "application/javascript" });
   const swURL = URL.createObjectURL(swBlob);
   navigator.serviceWorker
     .register(swURL)
     .then((registration) => {
       console.log(
         "Service Worker registered with scope:",
         registration.scope
       );
     })
     .catch((error) => {
       console.log("Service Worker registration failed:", error);
     });
 }
</script> <!-- Continue Theme Toggle Script with Draggable Functionality --> <script>
 document.addEventListener("DOMContentLoaded", () => {
   const themeToggleButton = document.getElementById("theme-toggle-scroll");
   const themeIcon = document.getElementById("theme-icon-scroll");
   // Persist theme preference
   const currentTheme = localStorage.getItem("theme") || "light";
   if (currentTheme === "dark") {
     document.body.setAttribute("data-theme", "dark");
     themeIcon.classList.remove("fa-moon");
     themeIcon.classList.add("fa-sun");
   }
   // Toggle theme on button click
   themeToggleButton.addEventListener("click", () => {
     const isDark = document.body.getAttribute("data-theme") === "dark";
     if (isDark) {
       document.body.setAttribute("data-theme", "light");
       themeIcon.classList.remove("fa-sun");
       themeIcon.classList.add("fa-moon");
       localStorage.setItem("theme", "light");
     } else {
       document.body.setAttribute("data-theme", "dark");
       themeIcon.classList.remove("fa-moon");
       themeIcon.classList.add("fa-sun");
       localStorage.setItem("theme", "dark");
     }
   });
   // Make Theme Toggle Button Draggable
   let isDragging = false;
   let initialX, initialY;
   let offsetX = 20,
     offsetY = 20; // Starting position
   themeToggleButton.style.left = offsetX + "px";
   themeToggleButton.style.top = offsetY + "px";
 
   // Mouse Events
   themeToggleButton.addEventListener("mousedown", (e) => {
     isDragging = true;
     initialX = e.clientX - offsetX;
     initialY = e.clientY - offsetY;
     themeToggleButton.classList.add("grabbing");
     e.preventDefault();
   });
 
   document.addEventListener("mousemove", (e) => {
     if (isDragging) {
       offsetX = e.clientX - initialX;
       offsetY = e.clientY - initialY;
       themeToggleButton.style.left = `${offsetX}px`;
       themeToggleButton.style.top = `${offsetY}px`;
       keepButtonInView();
     }
   });
 
   document.addEventListener("mouseup", () => {
     if (isDragging) {
       isDragging = false;
       themeToggleButton.classList.remove("grabbing");
     }
   });
 
   // Touch Events for Mobile
   themeToggleButton.addEventListener("touchstart", (e) => {
     isDragging = true;
     const touch = e.touches[0];
     initialX = touch.clientX - offsetX;
     initialY = touch.clientY - offsetY;
     themeToggleButton.classList.add("grabbing");
     e.preventDefault();
   });
 
   document.addEventListener(
     "touchmove",
     (e) => {
       if (isDragging) {
         const touch = e.touches[0];
         offsetX = touch.clientX - initialX;
         offsetY = touch.clientY - initialY;
         themeToggleButton.style.left = `${offsetX}px`;
         themeToggleButton.style.top = `${offsetY}px`;
         keepButtonInView();
       }
     },
     { passive: false }
   );
 
   document.addEventListener("touchend", () => {
     if (isDragging) {
       isDragging = false;
       themeToggleButton.classList.remove("grabbing");
     }
   });
 
   // Ensure the theme toggle button stays within viewport bounds
   function keepButtonInView() {
     const button = themeToggleButton;
     const rect = button.getBoundingClientRect();
     const padding = 10; // Padding from edges
 
     if (rect.left < padding) {
       button.style.left = `${padding}px`;
     }
     if (rect.top < padding) {
       button.style.top = `${padding}px`;
     }
     if (rect.right > window.innerWidth - padding) {
       button.style.left = `${window.innerWidth - rect.width - padding}px`;
     }
     if (rect.bottom > window.innerHeight - padding) {
       button.style.top = `${window.innerHeight - rect.height - padding}px`;
     }
   }
 
   window.addEventListener("resize", keepButtonInView);
   keepButtonInView();
 });
</script> <!-- Flatpickr JS --> <script src="https://cdn.jsdelivr.net/npm/flatpickr"></script> <!-- Polyfills for Older Browsers --> <script src="https://cdn.jsdelivr.net/npm/promise-polyfill@8/dist/polyfill.min.js"></script> <script src="https://cdn.jsdelivr.net/npm/whatwg-fetch@3.6.2/dist/fetch.umd.min.js"></script> <script src="https://cdn.jsdelivr.net/npm/classlist-polyfill@1.2.0/classList.min.js"></script> <!-- Main Script --> <script>
 document.addEventListener("DOMContentLoaded", () => {
   // Variables to track selections
   let isCheckinDateSelected = false;
   let isCheckoutDateSelected = false;
   let isCheckinTimeSelected = false;
   let isCheckoutTimeSelected = false;
   let userSelectedCheckinTime = "3:00 PM"; // Default check-in time
   let userSelectedCheckoutTime = "11:00 AM"; // Default check-out time
   const generatePassbookButton = document.getElementById(
     "generate-passbook-button"
   );
   const checkinDateInput = document.getElementById("checkin-datetime");
   const checkoutDateInput = document.getElementById("checkout-datetime");
   const upgradeEarlyButton = document.getElementById("upgrade-early");
   const upgradeLateButton = document.getElementById("upgrade-late");
   const upgradeEarlyGroup = document.getElementById("upgrade-early-option");
 
   let timers = {};
 
   let selectedCheckinDate = null;
   let selectedCheckoutDate = null;
 
   // Initialize Flatpickr without time selection
   flatpickr("#checkin-datetime, #checkout-datetime", {
     enableTime: false,
     dateFormat: "m-d-Y",
     minDate: "today",
     locale: "auto",
     onChange: function (selectedDates, dateStr, instance) {
       if (instance.element.id === "checkin-datetime") {
         selectedCheckinDate = selectedDates[0]; // Store Date object
         isCheckinDateSelected = selectedDates.length > 0;
         isCheckinTimeSelected = true; // Default time confirmed
       } else if (instance.element.id === "checkout-datetime") {
         selectedCheckoutDate = selectedDates[0]; // Store Date object
         isCheckoutDateSelected = selectedDates.length > 0;
         isCheckoutTimeSelected = true; // Default time confirmed
         upgradeEarlyGroup.classList.remove("display-none");
       }
       /* checkAllSelections(); */
       updateReservationPreview();
       handleCheckoutInstructionsLock();
     },
   });
 
   // Helper function to format Date object to mm/dd/yyyy
   function formatDate(date) {
     const mm = String(date.getMonth() + 1).padStart(2, "0"); // Months start at 0!
     const dd = String(date.getDate()).padStart(2, "0");
     const yyyy = date.getFullYear();
     return `${mm}/${dd}/${yyyy}`;
   }
 
   // Update Reservation Preview
   function updateReservationPreview() {
     const checkin = selectedCheckinDate
       ? `${formatDate(selectedCheckinDate)} ${userSelectedCheckinTime}`
       : "--";
     const checkout = selectedCheckoutDate
       ? `${formatDate(selectedCheckoutDate)} ${userSelectedCheckoutTime}`
       : "--";
 
     document.getElementById("preview-checkin").textContent = checkin;
     document.getElementById("preview-checkout").textContent = checkout;
     document.getElementById("checkin-display").textContent =
       userSelectedCheckinTime;
     document.getElementById("checkout-display").textContent =
       userSelectedCheckoutTime;
 
     // Display Dates
     document.getElementById("checkin-date").textContent = selectedCheckinDate
       ? formatDate(selectedCheckinDate)
       : "--/--/----";
     document.getElementById("checkout-date").textContent =
       selectedCheckoutDate ? formatDate(selectedCheckoutDate) : "--/--/----";
 
       // Function to calculate the countdown time and update only if the values change
       /* function updateCountdown(targetDate, element) {
           const now = new Date().getTime();
           const timeRemaining = targetDate - now;
 
           if (timeRemaining > 0) {
               const days = Math.floor(timeRemaining / (1000 * 60 * 60 * 24));
               const hours = Math.floor((timeRemaining % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
               const minutes = Math.floor((timeRemaining % (1000 * 60 * 60)) / (1000 * 60));
               const seconds = Math.floor((timeRemaining % (1000 * 60)) / 1000);
 
               const newText = `${days}d ${hours}h ${minutes}m ${seconds}s`;
 
               // Only update the text if it's different from the current value
               if (element.innerHTML !== newText) {
                   element.innerHTML = newText;
               }
           } else {
               // When the countdown is over
               element.innerHTML = "Time's up!";
           }
       }
 
       // Set the target dates (replace these with your actual checkin and checkout times)
       const checkinDate = new Date(checkin).getTime(); // Example checkin date
       const checkoutDate = new Date(checkout).getTime(); // Example checkout date
 
       // Update the countdown every second
       setInterval(function () {
           updateCountdown(checkinDate, document.getElementById("checkin-timer"));
           updateCountdown(checkoutDate, document.getElementById("checkout-timer"));
       }, 1000); */
 
 
 
   }
 
   // Function to open modal
   function openModal(modalId) {
     document.getElementById(modalId).classList.add("active");
   }
 
   // Function to close modal
   function closeModal(modalId) {
     document.getElementById(modalId).classList.remove("active");
   }
 
   // Close modals when close button is clicked
   const closeButtons = document.querySelectorAll(".close-button");
   closeButtons.forEach((btn) => {
     btn.addEventListener("click", () => {
       btn.closest(".modal").classList.remove("active");
     });
   });
 
   // Open modals when enhancement widgets are clicked
   const enhancementWidgets = document.querySelectorAll(".enhancement-widget");
   enhancementWidgets.forEach((widget) => {
     widget.addEventListener("click", () => {
       const modalId = widget.getAttribute("data-modal");
       openModal(modalId);
     });
   });
 
   // Handle upgrade options toggling
   const upgradeOptions = document.querySelectorAll(".upgrade-option");
   upgradeOptions.forEach((option) => {
     const upgradeButton = option.querySelector("button");
     upgradeButton.addEventListener("click", () => {
       const details = option.querySelector(".upgrade-details");
       details.style.display =
         details.style.display === "block" ? "none" : "block";
     });
   });
 
   // Handle upgrade button selection and confirmation
   const upgradeOptionButtons = document.querySelectorAll(".upgrade-button");
   let selectedUpgrade = null;
   upgradeOptionButtons.forEach((button) => {
     button.addEventListener("click", () => {
       // Remove 'selected' class from all upgrade buttons
       upgradeOptionButtons.forEach((btn) => btn.classList.remove("selected"));
       // Add 'selected' class to the clicked button
       button.classList.add("selected");
       // Store selected upgrade details
       const price = button.getAttribute("data-price");
       const time = button.getAttribute("data-time");
       const isEarly =
         button.closest(".upgrade-option").id === "upgrade-early-option";
       selectedUpgrade = { price, time, isEarly };
       // Set confirmation message based on upgrade type
       const confirmationMessage = isEarly
         ? `Do you want to set your check-in time to ${time} for $${price}?`
         : `Do you want to set your check-out time to ${time} for $${price}?`;
       document.getElementById("upgrade-confirmation-message").textContent =
         confirmationMessage;
       // Close the dropdown
       button.closest(".upgrade-details").style.display = "none";
       // Open the confirmation modal
       openModal("upgrade-confirmation-modal");
     });
   });
 
   // Handle confirmation modal actions
   document.getElementById("confirm-upgrade").addEventListener("click", () => {
     if (selectedUpgrade) {
       const { price, time, isEarly } = selectedUpgrade;
       // Close the confirmation modal
       closeModal("upgrade-confirmation-modal");
       if (price > 0) {
         // Redirect to payment or handle payment logic
         const paymentUrl = isEarly
           ? "https://yourshopifystore.com/early-checkin"
           : "https://yourshopifystore.com/late-checkout";
         window.location.href = paymentUrl;
       } else {
         // Set the selected time without payment
         if (isEarly) {
           userSelectedCheckinTime = time;
           isCheckinTimeSelected = true;
           // Update the "Select Time" button text
           upgradeEarlyButton.textContent = `Selected: ${time} - $${price}`;
           document.getElementById("upgrade-late-option").classList.remove("display-none");
         } else {
           userSelectedCheckoutTime = time;
           isCheckoutTimeSelected = true;
           // Update the "Select Time" button text
           upgradeLateButton.textContent = `Selected: ${time} - $${price}`;
           checkAllSelections();
         }
         updateReservationPreview();
         /* checkAllSelections(); */
         // Show success message
         alert("Upgrade applied successfully!");
       }
       // Reset selectedUpgrade
       selectedUpgrade = null;
     }
   });
 
   document.getElementById("cancel-upgrade").addEventListener("click", () => {
     // Close the confirmation modal
     closeModal("upgrade-confirmation-modal");
     // Reset selectedUpgrade
     selectedUpgrade = null;
   });
 
   // Handle FAQ accordion functionality
   const faqButtons = document.querySelectorAll(".faq-item button");
   faqButtons.forEach((button) => {
     button.addEventListener("click", () => {
       const faqItem = button.parentElement;
       const isActive = faqItem.classList.contains("active");
       // Close all FAQs
       document.querySelectorAll(".faq-item").forEach((item) => {
         item.classList.remove("active");
         item.querySelector("button").setAttribute("aria-expanded", "false");
       });
       // Toggle the clicked FAQ
       if (!isActive) {
         faqItem.classList.add("active");
         button.setAttribute("aria-expanded", "true");
       }
     });
   });
 
   // Passbook Form Handling
   const passbookForm = document.getElementById("passbook-form");
   passbookForm.addEventListener("submit", (e) => {
     e.preventDefault();
     let isValid = true;
 
     // Validate Check-In Date
     const checkinError = document.getElementById("error-checkin-datetime");
     if (checkinDateInput.value.trim() === "") {
       checkinError.textContent = "Check-in date is required.";
       checkinError.classList.add("visible");
       isValid = false;
     } else {
       checkinError.textContent = "";
       checkinError.classList.remove("visible");
     }
 
     // Validate Check-Out Date
     const checkoutError = document.getElementById("error-checkout-datetime");
     if (checkoutDateInput.value.trim() === "") {
       checkoutError.textContent = "Check-out date is required.";
       checkoutError.classList.add("visible");
       isValid = false;
     } else {
       checkoutError.textContent = "";
       checkoutError.classList.remove("visible");
     }
 
     // Ensure Check-Out Date is after Check-In Date
     if (isCheckinDateSelected && isCheckoutDateSelected) {
       if (selectedCheckoutDate <= selectedCheckinDate) {
         checkoutError.textContent =
           "Check-out date must be after check-in date.";
         checkoutError.classList.add("visible");
         isValid = false;
       }
     }
 
     if (isValid) {
       // Start Download and Timers
       startDownload();
     }
   });
 
   // Function to handle passbook download and start timers
   function startDownload() {
     // Close the Generate Passbook Modal
     closeModal("generate-passbook-modal");
 
     // Open the pkpass URL in a new tab
     window.open(
       "https://drive.usercontent.google.com/download?id=1OhFMzoZwH5CpZtE4CXwrqyVOclSBvIi-&export=download&authuser=0",
       "_blank"
     );
 
     // Show the Download Guest Pass button
     document.getElementById("download-guest-pass-button").style.display =
       "inline-block";
 
     // Start the overlay timers based on selected dates and times
     startOverlayTimers();
   }
 
   // Timer Function
   function startTimer(element, unlockTime, callback) {
     function updateCountdown() {
       const now = Date.now();
       const remaining = unlockTime - now;
 
       if (remaining <= 0) {
         element.textContent = "00:00:00";
         clearInterval(interval);
         callback();
       } else {
         /* const hours = Math.floor(
           (remaining % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60)
         ); */
         const days = Math.floor(remaining / (1000 * 60 * 60 * 24));
         const hours = Math.floor((remaining % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
         const minutes = Math.floor(
           (remaining % (1000 * 60 * 60)) / (1000 * 60)
         );
         const seconds = Math.floor((remaining % (1000 * 60)) / 1000);
         element.textContent = `D:${pad(days)} H:${pad(hours)} S:${pad(minutes)}`;
       }
     }
 
     function pad(num) {
       return num.toString().padStart(2, "0");
     }
 
     // Initial call
     updateCountdown();
     // Update every second
     const interval = setInterval(updateCountdown, 1000);
   }
 
   // Function to start overlay timers based on selected dates and times
   function startOverlayTimers() {
     // Calculate unlock times based on selected dates and times
     // Assuming:
     // - House Rules unlock at check-in time
     // - Amenities unlock at check-in time
     // - Check-Out Instructions unlock 24 hours before check-out
 
     const now = new Date();
 
     // House Rules and Amenities unlock at check-in time
     const checkinDateTime = new Date(
       `${formatDate(selectedCheckinDate)} ${userSelectedCheckinTime}`
     );
     // Check-Out Instructions unlock 24 hours before check-out time
     const checkoutDateTime = new Date(
       `${formatDate(selectedCheckoutDate)} ${userSelectedCheckoutTime}`
     );
     const checkoutInstructionsUnlockTime = new Date(
       checkoutDateTime.getTime() - 24 * 60 * 60 * 1000
     );
 
     // Start House Rules Timer
     const houseRulesTimerElem = document.getElementById("house-rules-timer");
     if (checkinDateTime > now) {
       startTimer(houseRulesTimerElem, checkinDateTime.getTime(), () => {
         document
           .getElementById("house-rules-overlay")
           .classList.add("hidden");
         document
           .querySelector("#information-title-2")
           .parentElement.classList.remove("locked");
       });
     } else {
       // If check-in time has passed, unlock immediately
       houseRulesTimerElem.textContent = "00:00:00";
       document.getElementById("house-rules-overlay").classList.add("hidden");
       document
         .querySelector("#information-title-2")
         .parentElement.classList.remove("locked");
     }
 
     // Start Amenities Timer
     const amenitiesTimerElem = document.getElementById("amenities-timer");
     if (checkinDateTime > now) {
       startTimer(amenitiesTimerElem, checkinDateTime.getTime(), () => {
         document.getElementById("amenities-overlay").classList.add("hidden");
         document
           .getElementById("amenities-title")
           .parentElement.classList.remove("locked");
       });
     } else {
       // If check-in time has passed, unlock immediately
       amenitiesTimerElem.textContent = "00:00:00";
       document.getElementById("amenities-overlay").classList.add("hidden");
       document
         .getElementById("amenities-title")
         .parentElement.classList.remove("locked");
     }
 
     const checkInTimerElem = document.getElementById("checkin-timer");
     if (checkinDateTime > now) {
       startTimer(checkInTimerElem, checkinDateTime.getTime(), () => {});
     } else {
       // If check-in time has passed, unlock immediately
       checkInTimerElem.textContent = "00:00:00";
     }
 
     const checkooutTimerElem = document.getElementById("checkout-timer");
     if (checkoutDateTime > now) {
       startTimer(checkooutTimerElem, checkoutDateTime, () => {});
     } else {
       // If check-in time has passed, unlock immediately
       checkooutTimerElem.textContent = "00:00:00";
     }
 
     // Start Check-Out Instructions Timer
     const checkoutInstructionTimerElem = document.getElementById(
       "checkout-timer-overlay"
     );
     if (checkoutInstructionsUnlockTime > now) {
       startTimer(
         checkoutInstructionTimerElem,
         checkoutInstructionsUnlockTime.getTime(),
         () => {
           document.getElementById("checkout-overlay").classList.add("hidden");
           document
             .getElementById("checkout-instructions-title")
             .parentElement.classList.remove("locked");
         }
       );
     } else if (checkoutDateTime > now) {
       // If within 24 hours before checkout, start countdown
       startTimer(
         checkoutInstructionTimerElem,
         checkoutInstructionsUnlockTime.getTime(),
         () => {
           document.getElementById("checkout-overlay").classList.add("hidden");
           document
             .getElementById("checkout-instructions-title")
             .parentElement.classList.remove("locked");
         }
       );
     } else {
       // If checkout time has passed, unlock immediately
       checkoutInstructionTimerElem.textContent = "00:00:00";
       document.getElementById("checkout-overlay").classList.add("hidden");
       document
         .getElementById("checkout-instructions-title")
         .parentElement.classList.remove("locked");
     }
   }
 
   // Function to convert 12-hour to 24-hour format
   function convertTo24Hour(timeStr) {
     const [time, modifier] = timeStr.split(" ");
     let [hours, minutes] = time.split(":");
 
     if (modifier === "PM" && hours !== "12") {
       hours = parseInt(hours, 10) + 12;
     }
     if (modifier === "AM" && hours === "12") {
       hours = "00";
     }
 
     return `${hours}:${minutes}:00`;
   }
 
   // Automatically close enhancement modals after clicking "Buy Now"
   const ctaButtons = document.querySelectorAll(".cta-button");
   ctaButtons.forEach((button) => {
     button.addEventListener("click", () => {
       const modalContent = button.closest(".modal-content");
       if (modalContent) {
         const modal = modalContent.parentElement;
         closeModal(modal.id);
       }
     });
   });
 
   // Add to Home Screen Functionality
   let deferredPrompt;
   window.addEventListener("beforeinstallprompt", (e) => {
     // Prevent the default mini-infobar
     e.preventDefault();
     // Save the event for later use
     deferredPrompt = e;
     // Optionally, show the add to home screen button
     openModal("add-to-home-modal");
   });
 
   document
     .getElementById("add-to-home-button")
     .addEventListener("click", async () => {
       if (deferredPrompt) {
         deferredPrompt.prompt();
         const { outcome } = await deferredPrompt.userChoice;
         if (outcome === "accepted") {
           console.log("User accepted the A2HS prompt");
         } else {
           console.log("User dismissed the A2HS prompt");
         }
         deferredPrompt = null;
         closeModal("add-to-home-modal");
         // Proceed to display the security code
         displaySecurityCode();
       } else {
         // Provide instructions for manual installation
         alert("Please add this app to your home screen manually.");
       }
     });
 
   // Handle "Your Guest Pass" Button
   document
     .getElementById("your-guest-pass-button")
     .addEventListener("click", () => {
       // Close the modal
       closeModal("add-to-home-modal");
       // Let the user interact with the rest of the app
     });
 
   // Function to display security code
   function displaySecurityCode() {
     // Display the security code to the user
     alert("Your security code is: 1234");
   }
 
   // Provide instructions for unsupported browsers
   window.addEventListener("DOMContentLoaded", () => {
     const instructions = document.getElementById("add-to-home-instructions");
     if (navigator.userAgent.match(/iPhone|iPad|iPod/i)) {
       instructions.innerHTML =
         'Tap the share icon and select "Add to Home Screen".';
     } else if (navigator.userAgent.match(/Android/i)) {
       instructions.textContent = "";
       // Android handles the beforeinstallprompt event
     } else {
       instructions.textContent =
         "Please add this app to your home screen manually.";
     }
   });
 
   // Handle Check-Out Instructions Lock
   function handleCheckoutInstructionsLock() {
     if (!checkoutDateInput.value) {
       // If no checkout date selected, keep instructions locked
       const checkoutCard = document.getElementById(
         "checkout-instructions-card"
       );
       checkoutCard.classList.add("locked");
       document.getElementById("checkout-overlay").classList.remove("hidden");
       return;
     }
 
     const checkoutDateTimeStr = `${formatDate(
       selectedCheckoutDate
     )} ${userSelectedCheckoutTime}`;
     const checkoutDateTime = new Date(checkoutDateTimeStr);
     const now = new Date();
     const checkoutInstructionsUnlockTime = new Date(
       checkoutDateTime.getTime() - 24 * 60 * 60 * 1000
     );
 
     const checkoutCard = document.getElementById(
       "checkout-instructions-card"
     );
     const checkoutInstructionTimerElem = document.getElementById(
       "checkout-timer-overlay"
     );
 
     if (now >= checkoutInstructionsUnlockTime) {
       // Unlock immediately if within 24 hours of checkout
       checkoutInstructionTimerElem.textContent = "00:00:00";
       document.getElementById("checkout-overlay").classList.add("hidden");
       checkoutCard.classList.remove("locked");
     } else if (checkoutInstructionsUnlockTime > now) {
       // Start countdown to unlock
       startTimer(
         checkoutInstructionTimerElem,
         checkoutInstructionsUnlockTime.getTime(),
         () => {
           document.getElementById("checkout-overlay").classList.add("hidden");
           checkoutCard.classList.remove("locked");
         }
       );
     }
   }
 
   // Initially lock Check-Out Instructions if dates are not set
   handleCheckoutInstructionsLock();
 
   // Update lock status whenever checkout date or time changes
   checkoutDateInput.addEventListener(
     "change",
     handleCheckoutInstructionsLock
   );
 
   // Update lock status whenever checkout time changes (after selecting upgrade)
   document.addEventListener("change", () => {
     handleCheckoutInstructionsLock();
   });
 
   // Function to check all selections
   function checkAllSelections() {
     if (
       isCheckinDateSelected &&
       isCheckoutDateSelected &&
       isCheckinTimeSelected &&
       isCheckoutTimeSelected
     ) {
       generatePassbookButton.classList.add("visible");
     } else {
       generatePassbookButton.classList.remove("visible");
     }
   }
 });
</script>
