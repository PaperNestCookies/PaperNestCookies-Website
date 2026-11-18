# Paper Nest Cookies — Website

A custom, lightweight website for Paper Nest Cookies in Eugene, Oregon.

## Publishing

The site is a static HTML/CSS/JavaScript site, designed for the GitHub repository `PaperNestCookies/PaperNestCookies-Website` and the Netlify project `papernestcookies`.

1. Upload the **contents** of this folder to the **root** of your existing GitHub repository (not inside another folder).
2. Keep the Netlify build command blank, and the publish directory as `.`.
3. Netlify automatically deploys changes to GitHub's `main` branch.
4. Open `https://papernestcookies.netlify.app` to review the result.

## Editing through Pages CMS

This repository includes `.pages.yml`. Once the files are uploaded, sign in at https://app.pagescms.org with GitHub, authorize the website repository, and open the site editor. Editing these files updates the live site through GitHub and Netlify:

- `data/cookies.json` — cookie name, description, photo and visibility
- `data/events.json` — upcoming markets and events
- `data/site.json` — website wording and contact details
- `data/pricing.json` — order packages and minimum quantity per flavor

Photographs can be uploaded to `assets/uploads/` and selected for cookies in Pages CMS. The initial image placeholders deliberately show the brand icon, **not invented cookies**.

## Important: Netlify Forms setup (before accepting orders)

The website includes three distinct Netlify Forms in the static `order.html` and `contact.html` files:

- `cookie-order` — **orders@papernestcookies.com**
- `event-inquiry` — **events@papernestcookies.com**
- `general-inquiry` — **hello@papernestcookies.com**

After the first deployment:

1. In Netlify, open the site's **Forms** section and make sure **form detection is enabled**. If you enable it after the deployment, redeploy the site.
2. Verify that all three form names are listed. (They may only appear after a deployment that contains the HTML.)
3. Configure a **separate email notification per form**, using the three forwarding addresses above. Netlify may require verifying notification recipients.
4. Submit a realistic *test* order and one inquiry through the public Netlify site. Confirm that the submission appears in Netlify Forms, the email arrives, and the correct Gmail label is applied. Check Netlify's spam submissions if a test is missing.
5. Test the pickup date, package quantities, mixes, confirmation page, and mobile experience before publicizing orders.

**Important:** Order price and quantity checking currently runs in the browser. It is suitable for an *inquiry/request* workflow where you manually review and confirm every order, **not an automatic checkout or guaranteed price quote**. Customers cannot make a binding purchase or pay on this site. Do not rely on browser-supplied amounts without reviewing the order. No special server-side order validation is included.

## Other notes

- No online payments are collected. Customers pay at pickup.
- Pickup date is requested by the customer, not automatically confirmed.
- Order package options: 6 for $24, 10 for $36, 20 for $70. Minimum of 6 cookies for each chosen flavor.
- Bigger quantities require contacting the bakery.
- The intended official domain is `papernestcookies.com`, managed separately at Porkbun. Do not change domain DNS until ready.
- Netlify Forms submissions consume plan allowances; check the Netlify dashboard for current usage and costs.
- A public GitHub repository contains public website source and photos, **not** customer order submissions. Customer submissions are stored by Netlify Forms.


## Version 2: Separate pages

The homepage is `index.html`, linking to `cookies.html`, `order.html`, `events.html`, and `contact.html`. All content still comes from the same `/data/*.json` files. Website forms live on the order and contact pages. Commit and push all website files using GitHub Desktop.

## Version 3

Retains the existing hero/header design while moving Cookies, Orders, Events, and Contact to their own pages. Events wording now includes Eugene and Springfield. Removed decorative arrows from buttons and navigation tiles.
