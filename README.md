# Ndila Auctioneers website

Public site: https://thato1943.github.io/ndila-website/

## Where the website lives

- **Website files and photos:** the public repository `thato1943/ndila-website`.
- **Website hosting:** GitHub Pages publishes the files from the `main` branch.
- **Domain name and DNS:** managed separately by the registrar or DNS provider where the company domain is held.
- **Enquiry submissions:** Formspree, once the form is configured.

Because this repository is public, put only material approved for public viewing here. Do not upload customer enquiries, identity documents, contracts, passwords, private auction records or other confidential files. Enquiry submissions belong in the configured form service, not in the repository.

## A short guide to safe edits on GitHub.com

1. Open the repository and select `index.html`.
2. Click the pencil icon to edit. Make one small change at a time.
3. Preview the change, then choose **Commit changes** on the `main` branch. GitHub Pages will publish it after the deployment finishes.
4. Open the public site and check the change on a phone-sized screen as well as a computer.

### Text and colours

- Page text and sections are in `index.html`. Keep the existing owner-confirmation notes until the company confirms those items.
- Proposed colours are near the top of `index.html`, in the `:root` block: deep slate-green `#17332e`, muted gold `#b8924a`, and off-white backgrounds. They remain proposed until Ndila confirms the brand colours.
- Leave the page's JavaScript and the closing `</script>` tag in place when editing ordinary text.

### Auctions

- Confirm every listing with the company before adding it to the `AUCTIONS` list near the bottom of `index.html`.
- A listing uses its title, asset category, province, location, opening date and closing date in South African Standard Time, a details link, and optional approved photos.
- The site calculates **Upcoming**, **Live** and **Closed** from those dates. It also shows a countdown only for upcoming and live listings.
- Remove or update a listing when the company confirms that its public information should change. Do not use an example or old campaign as a current listing.

### Adding approved photos

1. In the repository, choose **Add file → Upload files**.
2. Upload approved public photos into a folder named `images` (GitHub creates the folder when the uploaded file path starts with `images/`).
3. Use short file names such as `madibeng-truck-01.jpg`; avoid spaces.
4. Add the photo path and a useful description of the image to the confirmed listing's gallery.
5. Commit the upload and the listing change. The site shows a clearly marked placeholder until approved listing photos are supplied.

Use photos Ndila has permission to publish. Do not upload identity documents, private client files or images that reveal confidential information.

## Enquiry form

The site currently contains the Formspree placeholder `YOUR_FORM_ID` and a clearly marked privacy placeholder. The form remains blocked until the company has connected a Formspree form and approved the final privacy wording. After those are ready, replace the placeholder with the form ID from Formspree's **Integration** screen and ask for the site form to be activated.

This version sends the form with Formspree's JSON/AJAX method and redirects a successful enquiry to `thanks.html`. Formspree's current custom redirect control is listed for paid plans; the website handles the return page itself so a free endpoint can use the site's thanks page. See [Formspree HTML form setup](https://help.formspree.io/articles/building-your-form/building-an-html-form/) and [AJAX form guide](https://help.formspree.io/articles/building-your-form/submit-forms-with-javascript-ajax).

## Finding and recovering the company's .co.za domain

The exact purchased domain and registrar have not yet been confirmed. Do not guess or change DNS while the company is still recovering access.

1. Search company email inboxes, invoices, bank statements and old IT or website correspondence for terms such as **domain**, **.co.za**, **renewal**, **registrar**, **DNS**, **nameservers**, **hosting** and **ZARC**. Ask the person or supplier who previously handled the website.
2. Once you know the exact domain, search it in the official [ZARC .co.za WHOIS lookup](https://whois.registry.net.za/). Note the registrar, domain status, expiry date and nameservers. The registry can identify registration details, but the registrar normally handles account access, billing and renewals.
3. Contact the registrar shown in WHOIS using its official website or support channel. Ask for company account recovery and the process to verify that the company is authorised to manage the domain. If the login belongs to a former staff member or supplier, explain that and ask the registrar how to update the company contact email safely.
4. Ask the registrar to confirm the domain is still registered, its expiry/status, who controls DNS, and how to renew it. If WHOIS shows an expired, suspended or pending-deletion status, contact the registrar promptly; once a domain is fully deleted, it may become available to someone else.
5. After access is restored, move the account email to a company-controlled mailbox, turn on two-step sign-in, and store recovery details in the company's password manager. Never send passwords or one-time security codes in chat.

The company profile contains an old email address using `ndilaauctioneers.co.za`, but the public contact details in the supplied documents conflict. It has not been assumed to be the purchased domain.

## Connecting the recovered domain to GitHub Pages

Do this only after the company has recovered the correct domain and confirmed which service currently manages its DNS.

1. In GitHub account settings, use **Pages → Add a domain** to verify the domain. GitHub will give you a unique TXT record. Add it as a new record in the active DNS manager; do not replace existing TXT records.
2. In this repository, open **Settings → Pages**, enter the confirmed custom domain and save it.
3. In the active DNS manager, point the root domain to GitHub Pages with these four **A** records. The host/name is usually `@`:
   - `185.199.108.153`
   - `185.199.109.153`
   - `185.199.110.153`
   - `185.199.111.153`
4. If the company wants the `www` address too, add a **CNAME** record: host/name `www`, value `thato1943.github.io` (do not include the repository name).
5. Wait for DNS to update, then return to **Settings → Pages**. When GitHub shows HTTPS is available, turn on **Enforce HTTPS**.

**Protect company email:** do not delete or change existing **MX** or **TXT** records. MX records route company email; TXT records can support email security and domain verification. Do not change nameservers as a shortcut: that can disconnect email or other services. First record the existing DNS entries and ask the email provider or DNS administrator to review them. Add GitHub's verification TXT alongside existing TXT entries, never in place of them.

GitHub says DNS changes can take up to 24 hours to propagate. Its current guidance and record details are in [Managing a custom domain for GitHub Pages](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site).
