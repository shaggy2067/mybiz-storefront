# My Biz — Live Selling Storefront

A beautiful, deployable buyer-facing storefront for live sellers on TikTok, Instagram, Facebook and YouTube.

## 🌐 Live Site

**[View Storefront →](https://shaggy2067.github.io/mybiz-storefront/)**

---

## ✦ What This Is

My Biz gives live-streaming creators a single link to share with their audience during a live. Viewers tap the link, browse products, and check out — without leaving their app.

Built as a single `index.html` file with zero dependencies. No npm. No framework. No build step. Just open it in a browser or drop it on any host.

---

## 🚀 Features

- **Live drop banners** — products featured during a live are highlighted at the top with a pulsing LIVE badge
- **Real-time viewer count** — animated viewer number that updates every 3 seconds
- **Full checkout flow** — 2-step checkout (delivery → payment) with order confirmation
- **Product grid** — full catalogue with ratings, stock indicators, and qty controls
- **Reviews tab** — star breakdown and customer testimonials
- **About tab** — shipping, returns, contact, and live schedule info
- **Sticky live bar** — persistent CTA at the bottom while shopping
- **Black, white & gold design** — elegant, premium feel with shimmer animations
- **Mobile-first** — optimised for phone screens, works perfectly on desktop too

---

## 📁 File Structure

```
mybiz-storefront/
├── index.html        ← The entire storefront (one file)
└── README.md         ← This file
```

---

## ✏️ How to Personalise

Open `index.html` in any text editor (VS Code, Notepad, TextEdit) and update the following:

### Seller details
Search for `Lena Creates` and replace with the seller's name.
Search for `@lenacreates` and replace with their handle.
Search for `mybiz.io/lena` and replace with their storefront URL.
Update the bio, follower count, and social links near the top of the `<body>`.

### Products
Each product is clearly marked in the HTML. Update the name, price, emoji, stock count, description, and rating for each item.

### Live status
Change `isLive` behaviour by showing or hiding the live banner section.

---

## 💳 Connecting Real Payments

The checkout currently simulates a payment. To accept real money:

1. Create a free [Stripe](https://stripe.com) account
2. For each product, create a **Stripe Payment Link** in the Stripe dashboard
3. Replace the `confirmOrder()` JavaScript function with a redirect to your Stripe Payment Link:

```javascript
function confirmOrder() {
  window.location.href = 'https://buy.stripe.com/your_payment_link';
}
```

For a more integrated checkout (keeping buyers on your page), use **Stripe.js** with a Payment Intent. See: [stripe.com/docs/payments/accept-a-payment](https://stripe.com/docs/payments/accept-a-payment)

---

## 🌍 Custom Domain

To use your own domain (e.g. `mybiz.io/lenacreates`):

1. Buy a domain from [Namecheap](https://namecheap.com) or [Cloudflare](https://cloudflare.com) (~£10/year)
2. In your GitHub repository, go to **Settings → Pages**
3. Under "Custom domain", enter your domain
4. In your domain registrar, add a CNAME DNS record pointing to `yourusername.github.io`
5. Enable "Enforce HTTPS" in GitHub Pages settings

---

## 📈 Next Steps

- [ ] Personalise with real seller details
- [ ] Connect Stripe for real payments
- [ ] Add your custom domain
- [ ] Share the link in TikTok/Instagram bio
- [ ] Build the seller dashboard (My Biz seller app)

---

## 🏗 Built With

- Pure HTML5, CSS3, and vanilla JavaScript
- Google Fonts (Cormorant Garamond + DM Sans)
- Zero external dependencies

---

## 📄 Licence

© 2025 My Biz. All rights reserved.
