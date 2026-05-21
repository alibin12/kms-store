# 🏪 KMS Departmental Store Website

A complete, interactive, mobile-responsive website for KMS Departmental Store with WhatsApp + Email ordering.

## 📁 File Structure

```
kms-store/
├── index.html          # Homepage with hero, categories, featured products
├── products.html       # All products with filters and sorting
├── cart.html           # Shopping cart with order form
├── about.html          # About Us page
├── contact.html        # Contact & Store Locator page
├── thank-you.html      # Order confirmation page
├── css/
│   └── style.css       # Complete stylesheet
├── js/
│   └── main.js         # All JavaScript functionality
└── assets/
    ├── images/         # (Add your product images here)
    └── icons/          # (Add custom icons here)
```

## ✨ Features

### 🛍️ Shopping
- **30 Products** across 5 categories (Groceries, Snacks, Juices, Toys, Essentials)
- **Add to Cart** with quantity controls
- **localStorage** cart (persists across sessions, no login needed)
- **Search** products by name or category
- **Filter** by category
- **Sort** by relevance, price (low-high, high-low), name (A-Z)
- **Special offers** banner system

### 📱 Order Flow
1. Customer adds items to cart
2. Goes to cart page
3. Fills name, phone, address (optional)
4. Selects order type (Store Pickup / Home Delivery)
5. Clicks "Send Order via WhatsApp"
6. **WhatsApp** opens with pre-filled order summary
7. **Email** also opens with the same order details
8. Cart clears automatically
9. Redirects to Thank You page

### 📐 Design
- **Mobile-first** responsive design
- **Sticky navigation** with cart counter
- **Hamburger menu** for mobile
- **Smooth animations** and hover effects
- **Toast notifications** for user feedback
- **Custom scrollbar** styling
- **Emoji-based** product images (easily replaceable with real photos)

## 🚀 How to Use

### 1. Setup (No server required!)
Simply open `index.html` in any modern web browser. The site works entirely client-side.

### 2. Customize Store Details
Edit `js/main.js` and update the `STORE` object:

```javascript
const STORE = {
    name: "KMS Departmental Store",
    phone: "919876543210",     // <-- Replace with your WhatsApp number (with country code)
    email: "kmsstore@example.com",  // <-- Replace with your email
    address: "Main Road, Near Bus Stand",
    hours: "8:00 AM – 10:00 PM (Mon–Sun)",
    mapLink: "https://maps.google.com"  // <-- Add your Google Maps link
};
```

### 3. Add Real Product Images
Replace emoji placeholders with actual product images:

In `js/main.js`, update the `products` array:
```javascript
{ 
    id: 1, 
    name: "Basmati Rice", 
    category: "groceries", 
    price: 280, 
    unit: "5kg", 
    image: "assets/images/rice.jpg",  // <-- Replace emoji with image path
    badge: "Popular" 
}
```

Then update the product card rendering in the HTML/JS to use `<img>` tags instead of emoji spans.

### 4. Email Setup (Optional)
The current implementation uses `mailto:` links which open the user's default email client.

For automatic email sending without a backend, you can integrate:
- **EmailJS** (free tier available)
- **Formspree**
- **Getform**

### 5. Deploy
Upload all files to any static hosting:
- GitHub Pages
- Netlify
- Vercel
- Any web server

## 📱 Pages

| Page | Description |
|------|-------------|
| **Home** | Hero banner, search, category icons, featured products, store info |
| **Products** | Full product grid with category filter and sort |
| **Cart** | Cart items, quantity controls, order form, WhatsApp/Email submit |
| **About** | Store story, products list, why choose us |
| **Contact** | Store info, map placeholder, contact form, WhatsApp button |
| **Thank You** | Order confirmation, next steps |

## 🎨 Customization

### Colors
Edit CSS variables in `css/style.css`:
```css
:root {
    --primary: #1a5f2a;      /* Main green */
    --secondary: #f39c12;      /* Orange accent */
    --accent: #e74c3c;       /* Red for badges */
    /* ... */
}
```

### Products
Add, remove, or edit products in `js/main.js` `products` array.

### Offers
Update offers in `js/main.js` `offers` array.

## 📋 Browser Support
- Chrome/Edge (latest)
- Firefox (latest)
- Safari (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

## 💡 Tips
- The cart uses **localStorage**, so items persist even if the browser is closed
- WhatsApp links use `wa.me` format — make sure to include country code (e.g., `91` for India)
- For testing, use your own WhatsApp number to see the order format
- Add Google Analytics or similar for tracking (optional)

## 📝 License
Free to use for KMS Departmental Store.

---
Built with ❤️ for KMS Departmental Store
