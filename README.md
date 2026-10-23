# BiteVerse Café — Your Campus. Your Cravings. Your Café.

A responsive, motion-enhanced café website concept for the Web Lumina college website competition. This is a static, GitHub Pages-friendly frontend demo.

## Files
- `index.html` — structure, metadata, homepage, menu, offers and dialogs
- `styles.css` — responsive brand design, animations and reduced-motion support
- `app.js` — sample menu data, search and dietary filters, cart, promo validation, BiteBot, hours and feedback
- `README.md` — setup and deployment instructions

## Features
- Responsive café homepage with warm cream, charcoal, orange and green palette
- Searchable sample menu with 30 products across Indian snacks, South Indian, Chinese, burgers/pizza, beverages, desserts, non-veg snacks and value meals
- Search, category filters, and combined vegetarian/non-vegetarian filters
- Quick-view cards, cart quantity controls, localStorage cart persistence and INR totals
- Three illustrative combo cards and `CAMPUS10` (10% off eligible cart subtotal of ₹149 or more)
- BiteBot deterministic menu recommendations
- Open/closed status based on Asia/Kolkata and demo opening hours
- Campus Club visual, guest-profile preview, star rating and feedback form
- Responsive mobile navigation, image fallbacks, keyboard Escape handling and SEO metadata

## Run locally in VS Code
1. Open this folder in VS Code.
2. Open `index.html` in a browser or install the Live Server extension.
3. Right-click `index.html` and select **Open with Live Server**.
4. An internet connection is recommended for Google Fonts, Lucide icons and externally hosted food photography.

No build step is required.

## Demo boundaries — read before presenting
This is a frontend competition prototype, not a production ordering platform.
- Login is a guest-profile preview; there is no real registration, password reset, secure session or protected account.
- Cart and feedback are stored in this browser with localStorage, not a shared database.
- Checkout creates a demonstration reference only. No kitchen receives an order and no payment is collected.
- BiteBot uses deterministic menu filtering; no external AI API is connected.
- Membership and loyalty points are visual/demo features only.
- Combo cards show example prices only. Adding a combo currently adds its components at individual listed prices; the example combo price is not charged as a bundle.
- No secure admin dashboard, live inventory, real database, backend authorization or live order tracking is included.
- Menu, prices, hours and photos are illustrative. Confirm real availability, licensing, ingredients and allergen/cross-contact information before commercial use.

## Before production
Add a backend such as Node.js, Express, TypeScript and PostgreSQL/Prisma or a managed platform. Implement secure authentication and authorization, server-side price calculation, persistent orders, inventory and opening-hour checks, admin moderation, validated feedback storage, privacy/terms pages, and a payment provider test environment if required. Store secrets in environment variables and never commit keys or passwords.

## Publish with GitHub Pages
1. Commit `index.html`, `styles.css`, `app.js` and `README.md` to the `main` branch.
2. Open repository **Settings → Pages**.
3. Select **Deploy from a branch**, choose `main` and `/(root)`, then click **Save**.
4. Wait for GitHub Pages to publish. Expected URL: https://web-lumina-2026.github.io/Nighthawks/
5. If the Pages setting is restricted by the organization, ask a repository administrator to enable it.

## Edit the demo
Edit the `PRODUCTS` array in `app.js`. Each product has an ID, name, description, INR price, category, diet label, preparation estimate and image URL. The opening schedule is displayed in `index.html` and calculated by the `hours()` function in `app.js`. Update both if the real café schedule changes.
