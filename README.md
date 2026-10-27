# Ndila Auctioneers website

This is a static, mobile-friendly GitHub Pages site. The page is `index.html`; `thanks.html` is the Formspree return page.

## Editing
- Text, page sections, and proposed colors: edit `index.html` from GitHub.com using the pencil icon.
- Colors are in the `:root` block near the top of the `<style>` section. The palette remains proposed until Ndila confirms it.
- Auction listings are in the `AUCTIONS` array near the bottom of `index.html`. Add only owner-approved listings with SAST timestamps; status is calculated from the opening and closing dates.
- Photos can be added under `images/`; update each listing's image path and alt text. Use only approved images.

## Enquiry form
The form includes the Formspree placeholder `YOUR_FORM_ID` and will not submit until it is replaced with a form ID. Confirm the privacy wording and form recipient first. The `_next` field currently points to `https://thato1943.github.io/ndila-website/thanks.html`; update it if the site URL changes.

No Netlify configuration is needed for GitHub Pages. Auction terms, bidding platform, logo, contact channels, and office details remain subject to owner confirmation.

