# INVINNYTY Reads — Static Storefront (Starter)

This is a lightweight storefront for selling ebooks. It doesn't process payments itself. Instead, each product's `checkout_url` sends customers to your checkout on **Gumroad**, **Payhip**, **Lemon Squeezy**, or **Shopify** (with a digital downloads app).

## How to use

1. **Upload your ebooks** to your platform of choice:
   - Gumroad: create a product and copy its **product URL or overlay button link**.
   - Payhip: create a product and copy the **product link**.
   - Lemon Squeezy: create a product and copy the **checkout link**.
   - Shopify: create a product + digital file (use Shopify's *Digital Downloads* app), copy the product link or a direct checkout link.

2. **Edit `products.json`** and replace the placeholder items with your real data:
   - `title`, `price` (number), `category`, `tags` (array of strings),
   - `image` (URL to your cover image hosted anywhere),
   - `checkout_url` (your platform's link for that item).

3. **Open `index.html`** in a browser to test. It’s a fully static site (no build step).

4. **Host it** anywhere that serves static files: Netlify, Vercel, GitHub Pages, Cloudflare Pages, or your own hosting. Point your domain (e.g., `read.invinnyty.com`) to it.

5. **Payouts** happen on the platform you linked in `checkout_url` (e.g., Gumroad pays to your bank if you’re in Canada; Payhip pays out via PayPal or bank depending on your setup; Lemon Squeezy supports bank/PayPal depending on country).

## Tips

- You can mix platforms in one store. Each product can point to a different checkout.
- Use compressed JPG/WEBP covers (1200×750 recommended).
- Add more categories by simply using a new `category` value in `products.json` (chips auto‑generate).
- For a custom checkout embedded on your site, use the provider’s embed code instead of `checkout_url` links.

