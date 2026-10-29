File 1: index.html
HTML
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Assignment 6.5 - Product Card Mini-Project</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>

  <header class="page-header">
    <h1>E-Commerce Component Showcase</h1>
    <p>Product Card designed with box model properties, borders, and absolute positioning.</p>
  </header>

  <main class="container">

    <!-- Product Card Component -->
    <div class="product-card">
      
      <!-- Positioned Badge (Absolute) -->
      <span class="product-badge">20% OFF</span>

      <!-- Product Image Placeholder -->
      <div class="product-image-container">
        <img src="https://images.unsplash.com/photo-1505740420928-5e560c06d30e?w=500&auto=format&fit=crop&q=60" alt="Wireless Headphones" class="product-image">
      </div>

      <!-- Product Information -->
      <div class="product-content">
        <h2 class="product-name">Wireless Noise-Canceling Headphones</h2>
        <div class="product-price">
          <span class="current-price">$199.99</span>
          <span class="original-price">$249.99</span>
        </div>
        <p class="product-description">
          Experience premium acoustic sound, active noise cancellation, and 30-hour battery life in a sleek, lightweight design.
        </p>
        <button class="btn-buy">Add to Cart</button>
      </div>

    </div>

  </main>

  <footer>
    <p>&copy; 2026 Web Development Assignment — Product Card</p>
  </footer>

</body>
</html>
File 2: styles.css
CSS
/* ==========================================================================
   1. GLOBAL RESET & BASE STYLES
   ========================================================================== */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
  background-color: #f1f5f9;
  color: #1e293b;
  line-height: 1.6;
  padding: 30px;
}

.page-header {
  text-align: center;
  margin-bottom: 40px;
}

.page-header h1 {
  color: #1e3a8a;
  margin-bottom: 6px;
}

.page-header p {
  color: #64748b;
  font-size: 0.95rem;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  display: flex;
  justify-content: center;
  align-items: center;
}

/* ==========================================================================
   2. PRODUCT CARD COMPONENT
   ========================================================================== */
.product-card {
  position: relative; /* Anchors the absolute badge */
  background-color: #ffffff;
  border: 1px solid #cbd5e1;
  border-radius: 12px;
  width: 100%;
  max-width: 360px; /* Responsive limit */
  overflow: hidden; /* Clips image inside rounded corners */
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
  transition: transform 0.2s ease, box-shadow 0.2s ease;
}

.product-card:hover {
  transform: translateY(-4px);
  box-shadow: 0 8px 20px rgba(0, 0, 0, 0.12);
}

/* Absolute Positioned Badge */
.product-badge {
  position: absolute;
  top: 15px;
  right: 15px;
  background-color: #ef4444;
  color: #ffffff;
  font-size: 0.75rem;
  font-weight: 700;
  text-transform: uppercase;
  padding: 6px 12px;
  border-radius: 20px;
  z-index: 10;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.15);
}

/* Product Image */
.product-image-container {
  width: 100%;
  height: 220px;
  background-color: #e2e8f0;
}

.product-image {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

/* Product Content Area */
.product-content {
  padding: 24px;
}

.product-name {
  font-size: 1.25rem;
  font-weight: 700;
  color: #0f172a;
  margin-bottom: 10px;
}

.product-price {
  display: flex;
  align-items: center;
  gap: 12px;
  margin-bottom: 12px;
}

.current-price {
  font-size: 1.4rem;
  font-weight: 800;
  color: #2563eb;
}

.original-price {
  font-size: 0.95rem;
  color: #94a3b8;
  text-decoration: line-through;
}

.product-description {
  font-size: 0.9rem;
  color: #475569;
  margin-bottom: 20px;
  line-height: 1.5;
}

/* Buy Button */
.btn-buy {
  width: 100%;
  padding: 12px;
  background-color: #2563eb;
  color: #ffffff;
  border: none;
  border-radius: 8px;
  font-size: 1rem;
  font-weight: 600;
  cursor: pointer;
  transition: background-color 0.2s;
}

.btn-buy:hover {
  background-color: #1d4ed8;
}

/* Footer */
footer {
  text-align: center;
  margin-top: 50px;
  color: #64748b;
  font-size: 0.9rem;
}
Assignment Checklist & Requirements Met
Component Elements: Includes product image, product name, price details, short description, and an interactive "Add to Cart" button.

Box Model & Spacing: Uses tailored padding, vertical margins, and box-sizing: border-box.

Styling: Distinct borders (1px solid #cbd5e1), clean white surface background against a neutral page background, and smooth rounded corners (border-radius: 12px).

Positioning: The .product-card uses position: relative, successfully anchoring the .product-badge (position: absolute) neatly in the top-right corner.

Responsive Layout: Controlled using max-width: 360px and flexible unit scaling so it renders cleanly across mobile and desktop viewports.