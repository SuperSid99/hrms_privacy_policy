# HRMS privacy policy

The privacy policy page for the HRMS app (Dinnisha Solutions). It is a single
self-contained `index.html`, with no external scripts, fonts or trackers, for
GitHub Pages.

## Before publishing

Replace every highlighted placeholder in `index.html`:

- `[privacy email]` (appears twice): the address for privacy and deletion requests
- `[registered address]`: the company's registered address
- `[name]` and `[email]` for the grievance officer (India's DPDP Act)

Then search for `class="fill"`; there should be no matches left.

## Publish on GitHub Pages

    git init && git add . && git commit -m "Privacy policy"
    gh repo create <owner>/hrms-privacy-policy --public --source . --push
    gh api -X POST repos/<owner>/hrms-privacy-policy/pages -f "source[branch]=main" -f "source[path]=/"

The page is then served at `https://<owner>.github.io/hrms-privacy-policy/`.
Use that URL as the **Privacy Policy URL** in App Store Connect and Play
Console. For Play's **data deletion URL**, use the same URL with
`#data-deletion` on the end.

## Keep it true

Update this page whenever the app starts collecting something new. It must
match the App Privacy answers in App Store Connect and Play's Data safety form.
